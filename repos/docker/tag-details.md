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
-	[`docker:29.2.0`](#docker2920)
-	[`docker:29.2.0-alpine3.23`](#docker2920-alpine323)
-	[`docker:29.2.0-cli`](#docker2920-cli)
-	[`docker:29.2.0-cli-alpine3.23`](#docker2920-cli-alpine323)
-	[`docker:29.2.0-dind`](#docker2920-dind)
-	[`docker:29.2.0-dind-alpine3.23`](#docker2920-dind-alpine323)
-	[`docker:29.2.0-dind-rootless`](#docker2920-dind-rootless)
-	[`docker:29.2.0-windowsservercore`](#docker2920-windowsservercore)
-	[`docker:29.2.0-windowsservercore-ltsc2022`](#docker2920-windowsservercore-ltsc2022)
-	[`docker:29.2.0-windowsservercore-ltsc2025`](#docker2920-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:29`

```console
$ docker pull docker@sha256:3a33fc81fa4d38360f490f5b900e9846f725db45bb1d9b1fe02d849bd42a5cf2
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
$ docker pull docker@sha256:0ff14e6a992f2fdb7bef46123cd7fe61a58df0494e8df8bb6f9a5dac7486e1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136104845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374a53c1df9dbce9a844321500ad0d38af686f026dc7113c20b5cf0f114a4bf4`
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
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d08bf8475bf9e689c0d705f9b2b740fdc6f57fc7ea8522fa321e0407d5542a`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 8.4 MB (8399670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e0a1bb1a714c3574763a4e79760a69a83b79cfeb1bed66e1183734cba512ea`  
		Last Modified: Fri, 16 Jan 2026 23:30:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f56b512895821ca11cd19fa0f3496f6b325efd5ad4006b5c4dec5828cfbb46`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 18.7 MB (18749967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193ef8aa785fdc807d36f7842f2550fde47924a84196a0e8cae74d61c7ce918f`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 22.9 MB (22905484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd266dff25ac5344bf8acdd83dd1d11a4d114b78e85830c712f55773276c565`  
		Last Modified: Fri, 16 Jan 2026 23:30:57 GMT  
		Size: 10.8 MB (10787419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c46e30e1e8ddc2abe93c818cbc340f93e0d470ba6d76e35a129274946a2191`  
		Last Modified: Fri, 16 Jan 2026 23:30:57 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd70625831c839f25752faf71a054de3bf972e39226d555c0c024a6bb1af04f`  
		Last Modified: Fri, 16 Jan 2026 23:30:58 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa84a26e75eabb10ad201c611a85dfeeda810506ca9d74cfcda13603e3667d5f`  
		Last Modified: Fri, 16 Jan 2026 23:30:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a227f237fe1cc495143034aa29d1f3bb34935624b3a1968387be3be9643afd`  
		Last Modified: Fri, 16 Jan 2026 23:44:01 GMT  
		Size: 6.9 MB (6934060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9e772224d42944940e5982b30cb03a21c31a9597a8266f2dd3b8ee81c921a4`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
		Size: 92.5 KB (92455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9840a05cb973e2d8b0c68b64a66746c6d190887c3dd23d828c49ce56fd762bb6`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96e9a4646741eb4c737b5a5be006e0597cc26cef2276a4886f5fe1e3ba2288f`  
		Last Modified: Fri, 16 Jan 2026 23:44:02 GMT  
		Size: 64.4 MB (64367539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf27a6cf55bb7deeafc395d22479b56698da0c32ef86ab9e517d8d4ca1f33b41`  
		Last Modified: Fri, 16 Jan 2026 23:44:01 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6b1067e7e749c94b29fbcac41bc9d5ec545fb31d5b5ddb1f3a0b52ea357d41`  
		Last Modified: Fri, 16 Jan 2026 23:44:02 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:690a3533a5552c5e90f13a10a4b59da86854bf9b60446440dcdd8c168022f128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd04989d4be905d33abc134ff9eed506f20d21947bd8fe9e7dd3cf9603373ed`

```dockerfile
```

-	Layers:
	-	`sha256:f075788042fd798a5b7835588a5d1a1e119d28cf5c6ab3b938bd8d819adefe23`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v6

```console
$ docker pull docker@sha256:57d6151f7fb71e8b9bfe234e3be9512f8851f7e6bc21ed956381c6d7dbb3dbb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128357962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc21a1c40fa51d364b2f1ea3eb041ca809dd3c1f9b2262ce52db835f4ccac91`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:39:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Jan 2026 23:39:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Jan 2026 23:39:33 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Jan 2026 23:39:36 GMT
ENV DOCKER_VERSION=29.1.5
# Fri, 16 Jan 2026 23:39:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Jan 2026 23:39:36 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 16 Jan 2026 23:39:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Jan 2026 23:39:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 16 Jan 2026 23:39:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Jan 2026 23:39:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:39:39 GMT
CMD ["sh"]
# Fri, 16 Jan 2026 23:43:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 16 Jan 2026 23:43:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 16 Jan 2026 23:43:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 16 Jan 2026 23:43:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 16 Jan 2026 23:43:22 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 16 Jan 2026 23:43:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 16 Jan 2026 23:43:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:43:22 GMT
VOLUME [/var/lib/docker]
# Fri, 16 Jan 2026 23:43:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 16 Jan 2026 23:43:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 16 Jan 2026 23:43:22 GMT
CMD []
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8425a4561e629aa414ce86e2154f0076ff9a45b80d061f6543a5764c3cc6f8cd`  
		Last Modified: Fri, 16 Jan 2026 23:39:45 GMT  
		Size: 8.3 MB (8300932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e1fc32be12625d1cb40a6c0bbdb826b3f1cd9617cb46b7d36309048210facb`  
		Last Modified: Fri, 16 Jan 2026 23:39:45 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1a6d78aac1d4b760ea6465b655b17cd29903520f342d5fd358be2db9e129c2`  
		Last Modified: Fri, 16 Jan 2026 23:39:46 GMT  
		Size: 17.6 MB (17555343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6dd9350394ad68195ebf54510ebdf82ae71d4e29733f1801db09877c7ec2c7`  
		Last Modified: Fri, 16 Jan 2026 23:39:46 GMT  
		Size: 21.5 MB (21476547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8014e7548b42b4a7550cc19ad611cce6802080e7e8c5283651fbbd3c5c724438`  
		Last Modified: Fri, 16 Jan 2026 23:39:46 GMT  
		Size: 10.2 MB (10196881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc44c36b674b2071e02951d236d2ce771670678bd7f7293e22e81c5323b0cf54`  
		Last Modified: Fri, 16 Jan 2026 23:39:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f28a7994bba57c7766ea526fe8ebc2659178ebb61a0c69756655fa67bb7c202`  
		Last Modified: Fri, 16 Jan 2026 23:39:47 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02788a3462f1a595a505af2e9d009420d0bfb06e2d337dea3674e8bf736e134b`  
		Last Modified: Fri, 16 Jan 2026 23:39:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99c270ea4672ae7031121d6c3eb7150821ca52f133152c395baf84fdeaef335`  
		Last Modified: Fri, 16 Jan 2026 23:43:31 GMT  
		Size: 7.3 MB (7271448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a5c0fdb8ce4ad9734e2e154d06098bc7d3b66c67009e0cb63e21513d115c73`  
		Last Modified: Fri, 16 Jan 2026 23:43:31 GMT  
		Size: 91.8 KB (91772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c956cd4f121d5305de4f3ef19946cc75795eebf1b1f2b54bf5f340fa98de68`  
		Last Modified: Fri, 16 Jan 2026 23:43:31 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7332978ccc2976b3b6f16863ce750cf67e78d133ad47a1b496e943a97639e178`  
		Last Modified: Fri, 16 Jan 2026 23:43:33 GMT  
		Size: 59.9 MB (59888458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5ab6343c168d5995fad57f8a71b332852d0d1a2a35747ab883c9059dbe843c`  
		Last Modified: Fri, 16 Jan 2026 23:43:32 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71f35537c4608ca161ccf8b26e5ba3a7a237177b30c410d0e54aa5e5ff0e25`  
		Last Modified: Fri, 16 Jan 2026 23:43:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:aa0a301d83a325df841314b7bd7dde3dda152fb9a75bebaac99ac88a1451910a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b4a36c4242c6ba5c596734fcaa60697ed99cae2c45333bb5acb5e2d101ebd8`

```dockerfile
```

-	Layers:
	-	`sha256:7f2cc6b7f4ba2244c96a5b422d3eb723b81373c24cbf8052a3e85ae8613015f5`  
		Last Modified: Fri, 16 Jan 2026 23:43:31 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v7

```console
$ docker pull docker@sha256:8236ceb58e17942c161b981f016e36bb296cdbb8f7a0340b1fe59d243a312cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126449081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae08a90d372f5e8a9d947d84aa3b21f215b6dc66a6ff3b29b69d2cd52f307b8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:45:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Jan 2026 23:45:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Jan 2026 23:45:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Jan 2026 23:45:31 GMT
ENV DOCKER_VERSION=29.1.5
# Fri, 16 Jan 2026 23:45:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Jan 2026 23:45:31 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 16 Jan 2026 23:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Jan 2026 23:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 16 Jan 2026 23:45:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Jan 2026 23:45:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:45:35 GMT
CMD ["sh"]
# Sat, 17 Jan 2026 00:17:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 17 Jan 2026 00:17:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 17 Jan 2026 00:17:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 17 Jan 2026 00:17:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 17 Jan 2026 00:17:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 17 Jan 2026 00:17:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 17 Jan 2026 00:17:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 00:17:17 GMT
VOLUME [/var/lib/docker]
# Sat, 17 Jan 2026 00:17:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 17 Jan 2026 00:17:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 17 Jan 2026 00:17:17 GMT
CMD []
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d6ac0ea7d3f4c86291dcfd7858bfc22909b1def944c16f7a61df781848d473`  
		Last Modified: Fri, 16 Jan 2026 23:45:41 GMT  
		Size: 7.6 MB (7597845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fb5218cd2ac0d992f7285c73154c070f9a8c3df766b94feb1973537f455beb`  
		Last Modified: Fri, 16 Jan 2026 23:45:40 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bceaff09615dcc4132e2c0d594f2e3d5a3a843779117809a19f321f15fe2ad9e`  
		Last Modified: Fri, 16 Jan 2026 23:45:41 GMT  
		Size: 17.5 MB (17545469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a348d6c818ddd2fd3b40b4f2d7d93a164c0a1b76723cf4a32bdee4c3f3f709`  
		Last Modified: Fri, 16 Jan 2026 23:45:42 GMT  
		Size: 21.5 MB (21454902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcab9811786db808a1b33b234832a8e9f0395bb71953215ecda47d4b702e33a1`  
		Last Modified: Fri, 16 Jan 2026 23:45:42 GMT  
		Size: 10.2 MB (10189500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfbdbf2e294f4efe5c8d3b3ae54a4339dc3696f32a1cbf0413a44a460e2d27d`  
		Last Modified: Fri, 16 Jan 2026 23:45:42 GMT  
		Size: 534.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee14fa5d481a4a922464ebeaae676f7853468a840d0c41714bec1260541cda8`  
		Last Modified: Fri, 16 Jan 2026 23:45:43 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acb2cea06670f9754971cabf1fc7cf230bc3b5fcbc11ebd75b638239455f5da`  
		Last Modified: Fri, 16 Jan 2026 23:45:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2453c0e4f4894b542c662dea67f6213701f4fc355c2d020fad490bc8914572`  
		Last Modified: Sat, 17 Jan 2026 00:17:27 GMT  
		Size: 6.6 MB (6572857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5bf8ef2c4008a2d3965314f4295808b1801bcea094c21addffdfb0e4969e27`  
		Last Modified: Sat, 17 Jan 2026 00:17:27 GMT  
		Size: 88.1 KB (88139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417d31beb5548151e490cf03161b9aa6bc3169d4fbadd9a614b00d88d99394ee`  
		Last Modified: Sat, 17 Jan 2026 00:17:27 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b96020d2757029849b8a5d7e2328d9dbcbede2c16832b792aea4cbe92df97d`  
		Last Modified: Sat, 17 Jan 2026 00:17:29 GMT  
		Size: 59.7 MB (59712841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55262ae149e208b2a2fd5827d141bb0d8092baa2c93c47a7ed474a1576710534`  
		Last Modified: Sat, 17 Jan 2026 00:17:28 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da08a763fccaf17ff2fdadc52714e03107a5cf573f4c25b5e7837e9425d653`  
		Last Modified: Sat, 17 Jan 2026 00:17:28 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:ca46d59e18eba52837126d2b02c42cc12b13814954b5037e04dc7bb84dce309e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfae3d58cc56c795eb029b1de3f6d92122a531264255e6d4499886b13bd825bc`

```dockerfile
```

-	Layers:
	-	`sha256:97affc86a76a9497fb0cc56a7fc9355d583b08d33928e751d96813d8d33411ec`  
		Last Modified: Sat, 17 Jan 2026 00:17:27 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:87ca5378e2aaf821e5c84c6b5420b0bdec3cbeaff9fada3f838d7ddb528ea65e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126294567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a399de96efb1fb33c64b8559091aff5ecdaa4c85e5a4ed78e623b3ff3d7db00f`
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
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20aa2d791b8266f9dfa17d7927ad7bb695c7563923625c1f1b6b63d3e8a000b8`  
		Last Modified: Fri, 16 Jan 2026 23:33:49 GMT  
		Size: 8.5 MB (8453607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99f01766c5623ec5c29704949d2f9e78727351173fec312a472dda75bfe0fbc`  
		Last Modified: Fri, 16 Jan 2026 23:33:49 GMT  
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
		Last Modified: Fri, 16 Jan 2026 23:33:50 GMT  
		Size: 9.9 MB (9942176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f459c129e2df20f5a0b9d2cef232a2dcc43c1a744d94e95858ab5898896faead`  
		Last Modified: Fri, 16 Jan 2026 23:33:50 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cb42b654a8b7f6386af70afcfb18943c2b6ddfac3d25ac7663ad506613f927`  
		Last Modified: Fri, 16 Jan 2026 23:33:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985d6fb9c70efed7fba20dcfd74096bc1b34a04d71408695041842c10709c246`  
		Last Modified: Fri, 16 Jan 2026 23:33:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba14d49cf482ad8767be9715f12c32540f21afe52f5eeea827d7889eef9f4e5`  
		Last Modified: Fri, 16 Jan 2026 23:43:58 GMT  
		Size: 7.2 MB (7212983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f869ecca31b7e4cb47dac3444670d9ac67935d4711faf1f4dc73c54448119f58`  
		Last Modified: Fri, 16 Jan 2026 23:43:57 GMT  
		Size: 101.3 KB (101282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07025eda5cadcd2aad50deee35f3f3e4ab0f3bd4d0bf30ede81de47cfdde90d6`  
		Last Modified: Fri, 16 Jan 2026 23:43:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a4cc2ba717f8eaa4d250fcc460585a66fa48d9b640e570c448565b2ff4224`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
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

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:80b38265128675e62f9a23f63712d831c9f6f6800134cc0ce50c9658c521a3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c40b7c657c6e3c82a0476a1643e1b0b16cd2e9fd25fab6b77fa01522a9e855`

```dockerfile
```

-	Layers:
	-	`sha256:864ff6c43af948c3507e027a248d1476e720357b5a03a24de18633b231004d39`  
		Last Modified: Fri, 16 Jan 2026 23:43:57 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:931f63d7100eb6734405d92d8bd9f4aa708c587510e5cc673bb9ac196a3d733f
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
$ docker pull docker@sha256:05dfa31f4afd64888ef4cc0cbb1ab4d07a4828ef01cd29baa891fecbe50faf49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64704799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a30dc55d416d2e33ad1f7df0d566efc7abaae030c265daaf694ad4629e5a12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d08bf8475bf9e689c0d705f9b2b740fdc6f57fc7ea8522fa321e0407d5542a`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 8.4 MB (8399670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e0a1bb1a714c3574763a4e79760a69a83b79cfeb1bed66e1183734cba512ea`  
		Last Modified: Fri, 16 Jan 2026 23:30:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f56b512895821ca11cd19fa0f3496f6b325efd5ad4006b5c4dec5828cfbb46`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 18.7 MB (18749967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193ef8aa785fdc807d36f7842f2550fde47924a84196a0e8cae74d61c7ce918f`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 22.9 MB (22905484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd266dff25ac5344bf8acdd83dd1d11a4d114b78e85830c712f55773276c565`  
		Last Modified: Fri, 16 Jan 2026 23:30:57 GMT  
		Size: 10.8 MB (10787419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c46e30e1e8ddc2abe93c818cbc340f93e0d470ba6d76e35a129274946a2191`  
		Last Modified: Fri, 16 Jan 2026 23:30:57 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd70625831c839f25752faf71a054de3bf972e39226d555c0c024a6bb1af04f`  
		Last Modified: Fri, 16 Jan 2026 23:30:58 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa84a26e75eabb10ad201c611a85dfeeda810506ca9d74cfcda13603e3667d5f`  
		Last Modified: Fri, 16 Jan 2026 23:30:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c0897d8acf674622f9579bb143df44fd1116afeccaf11104aa737db661b38fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722265bbd6439a9e021b7c277085fd6673eafac84c3ca4606ebf76cc2abe2ae6`

```dockerfile
```

-	Layers:
	-	`sha256:75431dcba1812725df60e19ec7c314d1e0d5af58f9df2ee80ba07453f274c907`  
		Last Modified: Fri, 16 Jan 2026 23:30:55 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:eac252823aeabca009b148df41f51495e2075215e5719db3dd2e5103c8e41d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61100286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22621710f5734f5e80b1435dc6b55b8ae0c42b90aa882ab75ae73ea86664868`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:39:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Jan 2026 23:39:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Jan 2026 23:39:33 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Jan 2026 23:39:36 GMT
ENV DOCKER_VERSION=29.1.5
# Fri, 16 Jan 2026 23:39:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Jan 2026 23:39:36 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 16 Jan 2026 23:39:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Jan 2026 23:39:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 16 Jan 2026 23:39:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Jan 2026 23:39:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:39:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8425a4561e629aa414ce86e2154f0076ff9a45b80d061f6543a5764c3cc6f8cd`  
		Last Modified: Fri, 16 Jan 2026 23:39:45 GMT  
		Size: 8.3 MB (8300932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e1fc32be12625d1cb40a6c0bbdb826b3f1cd9617cb46b7d36309048210facb`  
		Last Modified: Fri, 16 Jan 2026 23:39:45 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1a6d78aac1d4b760ea6465b655b17cd29903520f342d5fd358be2db9e129c2`  
		Last Modified: Fri, 16 Jan 2026 23:39:46 GMT  
		Size: 17.6 MB (17555343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6dd9350394ad68195ebf54510ebdf82ae71d4e29733f1801db09877c7ec2c7`  
		Last Modified: Fri, 16 Jan 2026 23:39:46 GMT  
		Size: 21.5 MB (21476547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8014e7548b42b4a7550cc19ad611cce6802080e7e8c5283651fbbd3c5c724438`  
		Last Modified: Fri, 16 Jan 2026 23:39:46 GMT  
		Size: 10.2 MB (10196881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc44c36b674b2071e02951d236d2ce771670678bd7f7293e22e81c5323b0cf54`  
		Last Modified: Fri, 16 Jan 2026 23:39:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f28a7994bba57c7766ea526fe8ebc2659178ebb61a0c69756655fa67bb7c202`  
		Last Modified: Fri, 16 Jan 2026 23:39:47 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02788a3462f1a595a505af2e9d009420d0bfb06e2d337dea3674e8bf736e134b`  
		Last Modified: Fri, 16 Jan 2026 23:39:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9cbf7a2de0b91f486a924d475390a9d48a99e429c34227fede037ea5c3ff55c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a396ae5c82b755921db2644de41e488cb95d1e426e5fee76536032c0b4367943`

```dockerfile
```

-	Layers:
	-	`sha256:70818a4518c56b0c3d2dab5a67b9d3bd964cbf38ed16dd7028512ae8cc216859`  
		Last Modified: Fri, 16 Jan 2026 23:39:45 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:3ebd30c1dc5192f94a8d0559d088e3a1ba1d52e1ce6a412fb7cc1a61ef793649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60069249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7d3b08056dbb48fbe7580a61a717065059b800b71239ecbb839ed83dcd6ca0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:45:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Jan 2026 23:45:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Jan 2026 23:45:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Jan 2026 23:45:31 GMT
ENV DOCKER_VERSION=29.1.5
# Fri, 16 Jan 2026 23:45:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Jan 2026 23:45:31 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 16 Jan 2026 23:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Jan 2026 23:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 16 Jan 2026 23:45:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Jan 2026 23:45:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:45:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d6ac0ea7d3f4c86291dcfd7858bfc22909b1def944c16f7a61df781848d473`  
		Last Modified: Fri, 16 Jan 2026 23:45:41 GMT  
		Size: 7.6 MB (7597845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fb5218cd2ac0d992f7285c73154c070f9a8c3df766b94feb1973537f455beb`  
		Last Modified: Fri, 16 Jan 2026 23:45:40 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bceaff09615dcc4132e2c0d594f2e3d5a3a843779117809a19f321f15fe2ad9e`  
		Last Modified: Fri, 16 Jan 2026 23:45:41 GMT  
		Size: 17.5 MB (17545469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a348d6c818ddd2fd3b40b4f2d7d93a164c0a1b76723cf4a32bdee4c3f3f709`  
		Last Modified: Fri, 16 Jan 2026 23:45:42 GMT  
		Size: 21.5 MB (21454902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcab9811786db808a1b33b234832a8e9f0395bb71953215ecda47d4b702e33a1`  
		Last Modified: Fri, 16 Jan 2026 23:45:42 GMT  
		Size: 10.2 MB (10189500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfbdbf2e294f4efe5c8d3b3ae54a4339dc3696f32a1cbf0413a44a460e2d27d`  
		Last Modified: Fri, 16 Jan 2026 23:45:42 GMT  
		Size: 534.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee14fa5d481a4a922464ebeaae676f7853468a840d0c41714bec1260541cda8`  
		Last Modified: Fri, 16 Jan 2026 23:45:43 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acb2cea06670f9754971cabf1fc7cf230bc3b5fcbc11ebd75b638239455f5da`  
		Last Modified: Fri, 16 Jan 2026 23:45:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a24250d752ac002ee2ad261c5a2a0ee85324c3760805ec1a12e20c408c11f04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aedac4f0a36ea54920d67db152805f1ec3414f6ed9be9659058da61c8bff3a07`

```dockerfile
```

-	Layers:
	-	`sha256:6a6873d72ecda31e1f24bbc65bc15765582381d99f215cd8d4adcd08b0b76e69`  
		Last Modified: Fri, 16 Jan 2026 23:45:41 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:16301c9c10717965d70f1651a641dd533a592016a90647ad66969fceda04a907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60568165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4d705451246e5bff54c8dca70a2099a093f07e744f1976b63d10c61b5fb0b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20aa2d791b8266f9dfa17d7927ad7bb695c7563923625c1f1b6b63d3e8a000b8`  
		Last Modified: Fri, 16 Jan 2026 23:33:49 GMT  
		Size: 8.5 MB (8453607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99f01766c5623ec5c29704949d2f9e78727351173fec312a472dda75bfe0fbc`  
		Last Modified: Fri, 16 Jan 2026 23:33:49 GMT  
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
		Last Modified: Fri, 16 Jan 2026 23:33:50 GMT  
		Size: 9.9 MB (9942176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f459c129e2df20f5a0b9d2cef232a2dcc43c1a744d94e95858ab5898896faead`  
		Last Modified: Fri, 16 Jan 2026 23:33:50 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cb42b654a8b7f6386af70afcfb18943c2b6ddfac3d25ac7663ad506613f927`  
		Last Modified: Fri, 16 Jan 2026 23:33:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985d6fb9c70efed7fba20dcfd74096bc1b34a04d71408695041842c10709c246`  
		Last Modified: Fri, 16 Jan 2026 23:33:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a73bb7b22189634a7f4135430f6caf9ec01e67883274b3950eb4088cdd2dba24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d139971a2dc86dc8a27dbf92c4978b25045b7f90411f6baabbe1a80d7f154c`

```dockerfile
```

-	Layers:
	-	`sha256:40134b323d2780d17cbaf43b8652eafbd904a31761a314b9d0d61efe6d2d0358`  
		Last Modified: Fri, 16 Jan 2026 23:33:49 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind`

```console
$ docker pull docker@sha256:3a33fc81fa4d38360f490f5b900e9846f725db45bb1d9b1fe02d849bd42a5cf2
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
$ docker pull docker@sha256:0ff14e6a992f2fdb7bef46123cd7fe61a58df0494e8df8bb6f9a5dac7486e1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136104845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374a53c1df9dbce9a844321500ad0d38af686f026dc7113c20b5cf0f114a4bf4`
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
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d08bf8475bf9e689c0d705f9b2b740fdc6f57fc7ea8522fa321e0407d5542a`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 8.4 MB (8399670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e0a1bb1a714c3574763a4e79760a69a83b79cfeb1bed66e1183734cba512ea`  
		Last Modified: Fri, 16 Jan 2026 23:30:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f56b512895821ca11cd19fa0f3496f6b325efd5ad4006b5c4dec5828cfbb46`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 18.7 MB (18749967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193ef8aa785fdc807d36f7842f2550fde47924a84196a0e8cae74d61c7ce918f`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 22.9 MB (22905484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd266dff25ac5344bf8acdd83dd1d11a4d114b78e85830c712f55773276c565`  
		Last Modified: Fri, 16 Jan 2026 23:30:57 GMT  
		Size: 10.8 MB (10787419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c46e30e1e8ddc2abe93c818cbc340f93e0d470ba6d76e35a129274946a2191`  
		Last Modified: Fri, 16 Jan 2026 23:30:57 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd70625831c839f25752faf71a054de3bf972e39226d555c0c024a6bb1af04f`  
		Last Modified: Fri, 16 Jan 2026 23:30:58 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa84a26e75eabb10ad201c611a85dfeeda810506ca9d74cfcda13603e3667d5f`  
		Last Modified: Fri, 16 Jan 2026 23:30:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a227f237fe1cc495143034aa29d1f3bb34935624b3a1968387be3be9643afd`  
		Last Modified: Fri, 16 Jan 2026 23:44:01 GMT  
		Size: 6.9 MB (6934060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9e772224d42944940e5982b30cb03a21c31a9597a8266f2dd3b8ee81c921a4`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
		Size: 92.5 KB (92455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9840a05cb973e2d8b0c68b64a66746c6d190887c3dd23d828c49ce56fd762bb6`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96e9a4646741eb4c737b5a5be006e0597cc26cef2276a4886f5fe1e3ba2288f`  
		Last Modified: Fri, 16 Jan 2026 23:44:02 GMT  
		Size: 64.4 MB (64367539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf27a6cf55bb7deeafc395d22479b56698da0c32ef86ab9e517d8d4ca1f33b41`  
		Last Modified: Fri, 16 Jan 2026 23:44:01 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6b1067e7e749c94b29fbcac41bc9d5ec545fb31d5b5ddb1f3a0b52ea357d41`  
		Last Modified: Fri, 16 Jan 2026 23:44:02 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:690a3533a5552c5e90f13a10a4b59da86854bf9b60446440dcdd8c168022f128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd04989d4be905d33abc134ff9eed506f20d21947bd8fe9e7dd3cf9603373ed`

```dockerfile
```

-	Layers:
	-	`sha256:f075788042fd798a5b7835588a5d1a1e119d28cf5c6ab3b938bd8d819adefe23`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:57d6151f7fb71e8b9bfe234e3be9512f8851f7e6bc21ed956381c6d7dbb3dbb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128357962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc21a1c40fa51d364b2f1ea3eb041ca809dd3c1f9b2262ce52db835f4ccac91`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:39:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Jan 2026 23:39:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Jan 2026 23:39:33 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Jan 2026 23:39:36 GMT
ENV DOCKER_VERSION=29.1.5
# Fri, 16 Jan 2026 23:39:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Jan 2026 23:39:36 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 16 Jan 2026 23:39:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Jan 2026 23:39:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 16 Jan 2026 23:39:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Jan 2026 23:39:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:39:39 GMT
CMD ["sh"]
# Fri, 16 Jan 2026 23:43:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 16 Jan 2026 23:43:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 16 Jan 2026 23:43:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 16 Jan 2026 23:43:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 16 Jan 2026 23:43:22 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 16 Jan 2026 23:43:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 16 Jan 2026 23:43:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:43:22 GMT
VOLUME [/var/lib/docker]
# Fri, 16 Jan 2026 23:43:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 16 Jan 2026 23:43:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 16 Jan 2026 23:43:22 GMT
CMD []
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8425a4561e629aa414ce86e2154f0076ff9a45b80d061f6543a5764c3cc6f8cd`  
		Last Modified: Fri, 16 Jan 2026 23:39:45 GMT  
		Size: 8.3 MB (8300932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e1fc32be12625d1cb40a6c0bbdb826b3f1cd9617cb46b7d36309048210facb`  
		Last Modified: Fri, 16 Jan 2026 23:39:45 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1a6d78aac1d4b760ea6465b655b17cd29903520f342d5fd358be2db9e129c2`  
		Last Modified: Fri, 16 Jan 2026 23:39:46 GMT  
		Size: 17.6 MB (17555343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6dd9350394ad68195ebf54510ebdf82ae71d4e29733f1801db09877c7ec2c7`  
		Last Modified: Fri, 16 Jan 2026 23:39:46 GMT  
		Size: 21.5 MB (21476547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8014e7548b42b4a7550cc19ad611cce6802080e7e8c5283651fbbd3c5c724438`  
		Last Modified: Fri, 16 Jan 2026 23:39:46 GMT  
		Size: 10.2 MB (10196881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc44c36b674b2071e02951d236d2ce771670678bd7f7293e22e81c5323b0cf54`  
		Last Modified: Fri, 16 Jan 2026 23:39:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f28a7994bba57c7766ea526fe8ebc2659178ebb61a0c69756655fa67bb7c202`  
		Last Modified: Fri, 16 Jan 2026 23:39:47 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02788a3462f1a595a505af2e9d009420d0bfb06e2d337dea3674e8bf736e134b`  
		Last Modified: Fri, 16 Jan 2026 23:39:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99c270ea4672ae7031121d6c3eb7150821ca52f133152c395baf84fdeaef335`  
		Last Modified: Fri, 16 Jan 2026 23:43:31 GMT  
		Size: 7.3 MB (7271448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a5c0fdb8ce4ad9734e2e154d06098bc7d3b66c67009e0cb63e21513d115c73`  
		Last Modified: Fri, 16 Jan 2026 23:43:31 GMT  
		Size: 91.8 KB (91772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c956cd4f121d5305de4f3ef19946cc75795eebf1b1f2b54bf5f340fa98de68`  
		Last Modified: Fri, 16 Jan 2026 23:43:31 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7332978ccc2976b3b6f16863ce750cf67e78d133ad47a1b496e943a97639e178`  
		Last Modified: Fri, 16 Jan 2026 23:43:33 GMT  
		Size: 59.9 MB (59888458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5ab6343c168d5995fad57f8a71b332852d0d1a2a35747ab883c9059dbe843c`  
		Last Modified: Fri, 16 Jan 2026 23:43:32 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71f35537c4608ca161ccf8b26e5ba3a7a237177b30c410d0e54aa5e5ff0e25`  
		Last Modified: Fri, 16 Jan 2026 23:43:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:aa0a301d83a325df841314b7bd7dde3dda152fb9a75bebaac99ac88a1451910a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b4a36c4242c6ba5c596734fcaa60697ed99cae2c45333bb5acb5e2d101ebd8`

```dockerfile
```

-	Layers:
	-	`sha256:7f2cc6b7f4ba2244c96a5b422d3eb723b81373c24cbf8052a3e85ae8613015f5`  
		Last Modified: Fri, 16 Jan 2026 23:43:31 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:8236ceb58e17942c161b981f016e36bb296cdbb8f7a0340b1fe59d243a312cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126449081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae08a90d372f5e8a9d947d84aa3b21f215b6dc66a6ff3b29b69d2cd52f307b8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:45:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Jan 2026 23:45:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Jan 2026 23:45:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Jan 2026 23:45:31 GMT
ENV DOCKER_VERSION=29.1.5
# Fri, 16 Jan 2026 23:45:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Jan 2026 23:45:31 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 16 Jan 2026 23:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Jan 2026 23:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 16 Jan 2026 23:45:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Jan 2026 23:45:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:45:35 GMT
CMD ["sh"]
# Sat, 17 Jan 2026 00:17:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 17 Jan 2026 00:17:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 17 Jan 2026 00:17:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 17 Jan 2026 00:17:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 17 Jan 2026 00:17:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 17 Jan 2026 00:17:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 17 Jan 2026 00:17:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 00:17:17 GMT
VOLUME [/var/lib/docker]
# Sat, 17 Jan 2026 00:17:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 17 Jan 2026 00:17:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 17 Jan 2026 00:17:17 GMT
CMD []
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d6ac0ea7d3f4c86291dcfd7858bfc22909b1def944c16f7a61df781848d473`  
		Last Modified: Fri, 16 Jan 2026 23:45:41 GMT  
		Size: 7.6 MB (7597845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fb5218cd2ac0d992f7285c73154c070f9a8c3df766b94feb1973537f455beb`  
		Last Modified: Fri, 16 Jan 2026 23:45:40 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bceaff09615dcc4132e2c0d594f2e3d5a3a843779117809a19f321f15fe2ad9e`  
		Last Modified: Fri, 16 Jan 2026 23:45:41 GMT  
		Size: 17.5 MB (17545469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a348d6c818ddd2fd3b40b4f2d7d93a164c0a1b76723cf4a32bdee4c3f3f709`  
		Last Modified: Fri, 16 Jan 2026 23:45:42 GMT  
		Size: 21.5 MB (21454902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcab9811786db808a1b33b234832a8e9f0395bb71953215ecda47d4b702e33a1`  
		Last Modified: Fri, 16 Jan 2026 23:45:42 GMT  
		Size: 10.2 MB (10189500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfbdbf2e294f4efe5c8d3b3ae54a4339dc3696f32a1cbf0413a44a460e2d27d`  
		Last Modified: Fri, 16 Jan 2026 23:45:42 GMT  
		Size: 534.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee14fa5d481a4a922464ebeaae676f7853468a840d0c41714bec1260541cda8`  
		Last Modified: Fri, 16 Jan 2026 23:45:43 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acb2cea06670f9754971cabf1fc7cf230bc3b5fcbc11ebd75b638239455f5da`  
		Last Modified: Fri, 16 Jan 2026 23:45:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2453c0e4f4894b542c662dea67f6213701f4fc355c2d020fad490bc8914572`  
		Last Modified: Sat, 17 Jan 2026 00:17:27 GMT  
		Size: 6.6 MB (6572857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5bf8ef2c4008a2d3965314f4295808b1801bcea094c21addffdfb0e4969e27`  
		Last Modified: Sat, 17 Jan 2026 00:17:27 GMT  
		Size: 88.1 KB (88139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417d31beb5548151e490cf03161b9aa6bc3169d4fbadd9a614b00d88d99394ee`  
		Last Modified: Sat, 17 Jan 2026 00:17:27 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b96020d2757029849b8a5d7e2328d9dbcbede2c16832b792aea4cbe92df97d`  
		Last Modified: Sat, 17 Jan 2026 00:17:29 GMT  
		Size: 59.7 MB (59712841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55262ae149e208b2a2fd5827d141bb0d8092baa2c93c47a7ed474a1576710534`  
		Last Modified: Sat, 17 Jan 2026 00:17:28 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da08a763fccaf17ff2fdadc52714e03107a5cf573f4c25b5e7837e9425d653`  
		Last Modified: Sat, 17 Jan 2026 00:17:28 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:ca46d59e18eba52837126d2b02c42cc12b13814954b5037e04dc7bb84dce309e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfae3d58cc56c795eb029b1de3f6d92122a531264255e6d4499886b13bd825bc`

```dockerfile
```

-	Layers:
	-	`sha256:97affc86a76a9497fb0cc56a7fc9355d583b08d33928e751d96813d8d33411ec`  
		Last Modified: Sat, 17 Jan 2026 00:17:27 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:87ca5378e2aaf821e5c84c6b5420b0bdec3cbeaff9fada3f838d7ddb528ea65e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126294567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a399de96efb1fb33c64b8559091aff5ecdaa4c85e5a4ed78e623b3ff3d7db00f`
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
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20aa2d791b8266f9dfa17d7927ad7bb695c7563923625c1f1b6b63d3e8a000b8`  
		Last Modified: Fri, 16 Jan 2026 23:33:49 GMT  
		Size: 8.5 MB (8453607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99f01766c5623ec5c29704949d2f9e78727351173fec312a472dda75bfe0fbc`  
		Last Modified: Fri, 16 Jan 2026 23:33:49 GMT  
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
		Last Modified: Fri, 16 Jan 2026 23:33:50 GMT  
		Size: 9.9 MB (9942176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f459c129e2df20f5a0b9d2cef232a2dcc43c1a744d94e95858ab5898896faead`  
		Last Modified: Fri, 16 Jan 2026 23:33:50 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cb42b654a8b7f6386af70afcfb18943c2b6ddfac3d25ac7663ad506613f927`  
		Last Modified: Fri, 16 Jan 2026 23:33:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985d6fb9c70efed7fba20dcfd74096bc1b34a04d71408695041842c10709c246`  
		Last Modified: Fri, 16 Jan 2026 23:33:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba14d49cf482ad8767be9715f12c32540f21afe52f5eeea827d7889eef9f4e5`  
		Last Modified: Fri, 16 Jan 2026 23:43:58 GMT  
		Size: 7.2 MB (7212983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f869ecca31b7e4cb47dac3444670d9ac67935d4711faf1f4dc73c54448119f58`  
		Last Modified: Fri, 16 Jan 2026 23:43:57 GMT  
		Size: 101.3 KB (101282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07025eda5cadcd2aad50deee35f3f3e4ab0f3bd4d0bf30ede81de47cfdde90d6`  
		Last Modified: Fri, 16 Jan 2026 23:43:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a4cc2ba717f8eaa4d250fcc460585a66fa48d9b640e570c448565b2ff4224`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
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

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:80b38265128675e62f9a23f63712d831c9f6f6800134cc0ce50c9658c521a3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c40b7c657c6e3c82a0476a1643e1b0b16cd2e9fd25fab6b77fa01522a9e855`

```dockerfile
```

-	Layers:
	-	`sha256:864ff6c43af948c3507e027a248d1476e720357b5a03a24de18633b231004d39`  
		Last Modified: Fri, 16 Jan 2026 23:43:57 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:3f2db3470a9c852cb3493b458358ec3a170a710b68f699db161b7ed87ec8583a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

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
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d08bf8475bf9e689c0d705f9b2b740fdc6f57fc7ea8522fa321e0407d5542a`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 8.4 MB (8399670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e0a1bb1a714c3574763a4e79760a69a83b79cfeb1bed66e1183734cba512ea`  
		Last Modified: Fri, 16 Jan 2026 23:30:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f56b512895821ca11cd19fa0f3496f6b325efd5ad4006b5c4dec5828cfbb46`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 18.7 MB (18749967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193ef8aa785fdc807d36f7842f2550fde47924a84196a0e8cae74d61c7ce918f`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 22.9 MB (22905484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd266dff25ac5344bf8acdd83dd1d11a4d114b78e85830c712f55773276c565`  
		Last Modified: Fri, 16 Jan 2026 23:30:57 GMT  
		Size: 10.8 MB (10787419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c46e30e1e8ddc2abe93c818cbc340f93e0d470ba6d76e35a129274946a2191`  
		Last Modified: Fri, 16 Jan 2026 23:30:57 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd70625831c839f25752faf71a054de3bf972e39226d555c0c024a6bb1af04f`  
		Last Modified: Fri, 16 Jan 2026 23:30:58 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa84a26e75eabb10ad201c611a85dfeeda810506ca9d74cfcda13603e3667d5f`  
		Last Modified: Fri, 16 Jan 2026 23:30:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a227f237fe1cc495143034aa29d1f3bb34935624b3a1968387be3be9643afd`  
		Last Modified: Fri, 16 Jan 2026 23:44:01 GMT  
		Size: 6.9 MB (6934060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9e772224d42944940e5982b30cb03a21c31a9597a8266f2dd3b8ee81c921a4`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
		Size: 92.5 KB (92455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9840a05cb973e2d8b0c68b64a66746c6d190887c3dd23d828c49ce56fd762bb6`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96e9a4646741eb4c737b5a5be006e0597cc26cef2276a4886f5fe1e3ba2288f`  
		Last Modified: Fri, 16 Jan 2026 23:44:02 GMT  
		Size: 64.4 MB (64367539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf27a6cf55bb7deeafc395d22479b56698da0c32ef86ab9e517d8d4ca1f33b41`  
		Last Modified: Fri, 16 Jan 2026 23:44:01 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6b1067e7e749c94b29fbcac41bc9d5ec545fb31d5b5ddb1f3a0b52ea357d41`  
		Last Modified: Fri, 16 Jan 2026 23:44:02 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1557b2a406cc6f243f0171436f503bdb8e8d1e3e77bdcf36bc1b684311ed72`  
		Last Modified: Sat, 17 Jan 2026 00:14:54 GMT  
		Size: 3.4 MB (3419929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d8849e55ddf8f1caa5eaf086451cea763b8e9545dd3c3e97fdcdb59ef201a5`  
		Last Modified: Sat, 17 Jan 2026 00:14:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a94cff53939cdff88071fbd8e0fa9d0603580457bd6118ab08d88cf2201942`  
		Last Modified: Sat, 17 Jan 2026 00:14:53 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47d0dfc54602c4b9b436657ddff22108d34d2abee74a876828b8012a4c8e868`  
		Last Modified: Sat, 17 Jan 2026 00:14:54 GMT  
		Size: 17.4 MB (17371697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b922a090e96a69d521d8afb6527fa2cb7242cbf56626b59321174c38d81e858a`  
		Last Modified: Sat, 17 Jan 2026 00:14:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

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
		Last Modified: Sat, 17 Jan 2026 00:14:53 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

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
		Last Modified: Fri, 16 Jan 2026 23:33:49 GMT  
		Size: 8.5 MB (8453607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99f01766c5623ec5c29704949d2f9e78727351173fec312a472dda75bfe0fbc`  
		Last Modified: Fri, 16 Jan 2026 23:33:49 GMT  
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
		Last Modified: Fri, 16 Jan 2026 23:33:50 GMT  
		Size: 9.9 MB (9942176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f459c129e2df20f5a0b9d2cef232a2dcc43c1a744d94e95858ab5898896faead`  
		Last Modified: Fri, 16 Jan 2026 23:33:50 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cb42b654a8b7f6386af70afcfb18943c2b6ddfac3d25ac7663ad506613f927`  
		Last Modified: Fri, 16 Jan 2026 23:33:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985d6fb9c70efed7fba20dcfd74096bc1b34a04d71408695041842c10709c246`  
		Last Modified: Fri, 16 Jan 2026 23:33:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba14d49cf482ad8767be9715f12c32540f21afe52f5eeea827d7889eef9f4e5`  
		Last Modified: Fri, 16 Jan 2026 23:43:58 GMT  
		Size: 7.2 MB (7212983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f869ecca31b7e4cb47dac3444670d9ac67935d4711faf1f4dc73c54448119f58`  
		Last Modified: Fri, 16 Jan 2026 23:43:57 GMT  
		Size: 101.3 KB (101282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07025eda5cadcd2aad50deee35f3f3e4ab0f3bd4d0bf30ede81de47cfdde90d6`  
		Last Modified: Fri, 16 Jan 2026 23:43:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a4cc2ba717f8eaa4d250fcc460585a66fa48d9b640e570c448565b2ff4224`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
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
		Last Modified: Sat, 17 Jan 2026 00:15:18 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12502433d4f521c091bf5f40e0a2f10c483376cd6cf491d5167d0d71255e93ae`  
		Last Modified: Sat, 17 Jan 2026 00:15:18 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028d45c1e6c47fa93138f7186507cc4c5173fce93755e0c753f472d31ca4449d`  
		Last Modified: Sat, 17 Jan 2026 00:15:18 GMT  
		Size: 17.7 MB (17709424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d784a5d534b102bd49b134cf1aa67620b01c91b045f85c4618fba5fa487ff05b`  
		Last Modified: Sat, 17 Jan 2026 00:15:19 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

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
		Last Modified: Sat, 17 Jan 2026 00:15:17 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:e5be8819c33c02450ae1cb0ffc732f43adce21efbf8bc516c2d83ad28ab7f609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:011b8de53ecb70fa60f226045aca2c69332bb6ee94d021bb9d3fcc085384a0d5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1550967984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6dccad077a318174c56c30ebe3c491c307ecc1db3239e2cd5c399177b281ef`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Fri, 16 Jan 2026 23:27:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Jan 2026 23:27:58 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Jan 2026 23:27:59 GMT
ENV DOCKER_VERSION=29.1.5
# Fri, 16 Jan 2026 23:28:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.5.zip
# Fri, 16 Jan 2026 23:28:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Jan 2026 23:28:10 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 16 Jan 2026 23:28:11 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 16 Jan 2026 23:28:11 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 16 Jan 2026 23:28:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Jan 2026 23:28:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 16 Jan 2026 23:28:20 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-windows-x86_64.exe
# Fri, 16 Jan 2026 23:28:21 GMT
ENV DOCKER_COMPOSE_SHA256=2ae341f9152b4d90f561f84b8f2e263d5b60e1613c6841c804447819290c4119
# Fri, 16 Jan 2026 23:28:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf85b52279cbf5f434afc4ab079f83bda3ef50d3486fc74a30c20f552694d85f`  
		Last Modified: Fri, 16 Jan 2026 23:28:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93445caeafc2bddea797a95857da92e939124df4d54c185f80f39445e80c0b94`  
		Last Modified: Fri, 16 Jan 2026 23:28:36 GMT  
		Size: 377.1 KB (377114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e299452bcfd7aca11225e6700bf13ba1fb4bcb19e176b8a1a14f554377c7dd2`  
		Last Modified: Fri, 16 Jan 2026 23:28:36 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4053285375a511f9c5e62aad814a3035f4e232806d8993ce9390e35ea7c757b1`  
		Last Modified: Fri, 16 Jan 2026 23:28:36 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dc97dec1a7c7fd01f0954f1b05bf600bd724c454ef5a252543bc69fd4fd00b`  
		Last Modified: Fri, 16 Jan 2026 23:28:38 GMT  
		Size: 19.4 MB (19432334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8f925ec92367d9f26dcaaf379beed54c2f51aa96dedc2c1426ee427cd71831`  
		Last Modified: Fri, 16 Jan 2026 23:28:34 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5376a23cd36fd59eb5251f2151e83a0e1a7a67013ba2b5899fba9a796e16092`  
		Last Modified: Fri, 16 Jan 2026 23:28:34 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c61331a4364799d750587d61e8cce8abf465f33de033951aefcaf07321e77d`  
		Last Modified: Fri, 16 Jan 2026 23:28:34 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b78cf75f88295cbd8090b41c814f0df5e0a6951e496caff112c42de8eac459`  
		Last Modified: Fri, 16 Jan 2026 23:28:36 GMT  
		Size: 23.9 MB (23929994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671ff8ed0c7f11b6caaf11da12b447a4a63e27b1711ecb4078f8007f675be90f`  
		Last Modified: Fri, 16 Jan 2026 23:28:32 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48250282c43183796eda8334f28230b90a9fac97a683cc4c7b9a49373dcf154e`  
		Last Modified: Fri, 16 Jan 2026 23:28:32 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07517cc4d488302c8930b5fac70a5e65f24ec3cf9a28ead9ab5dff5b3d276f0`  
		Last Modified: Fri, 16 Jan 2026 23:28:32 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4401644c9320335d7ccbf201067db845ccd52bb0dd1091a086309a20504d55`  
		Last Modified: Fri, 16 Jan 2026 23:28:34 GMT  
		Size: 11.5 MB (11456516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:27574c8077e47eae8b561adeac8e2136d1c27bb97bfb370868963f775372c3ac
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1890962783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fac75bb46939eff0674007ab202879fd5c512d38bc3477a4ce536005f69de5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Sat, 17 Jan 2026 00:31:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 17 Jan 2026 00:31:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 17 Jan 2026 00:31:37 GMT
ENV DOCKER_VERSION=29.1.5
# Sat, 17 Jan 2026 00:31:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.5.zip
# Sat, 17 Jan 2026 00:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 17 Jan 2026 00:31:55 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Sat, 17 Jan 2026 00:31:56 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Sat, 17 Jan 2026 00:31:57 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Sat, 17 Jan 2026 00:32:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 17 Jan 2026 00:32:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Sat, 17 Jan 2026 00:32:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-windows-x86_64.exe
# Sat, 17 Jan 2026 00:32:15 GMT
ENV DOCKER_COMPOSE_SHA256=2ae341f9152b4d90f561f84b8f2e263d5b60e1613c6841c804447819290c4119
# Sat, 17 Jan 2026 00:32:25 GMT
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
	-	`sha256:b7c78b49395f890e706d473e38c35368e19c6b35bb262c64ca03e023a301e2a6`  
		Last Modified: Sat, 17 Jan 2026 00:32:35 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78ca2adb184b097e41d61db1c4e93f50645315b61438a439b40c1900f125996`  
		Last Modified: Sat, 17 Jan 2026 00:32:34 GMT  
		Size: 501.7 KB (501717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24467fa2d0304efe337e545989ba3cd2e46d51af14ad0b64773f789d3afbeec7`  
		Last Modified: Sat, 17 Jan 2026 00:32:34 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c5802fad231b2fb1a2c83745d11231a54367bf5f857c22dd7e6435fad68712`  
		Last Modified: Sat, 17 Jan 2026 00:32:34 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e8f5908d5455b3264f322cb1a1cc727a24fd8b6f17df307574c2561b3e0f90`  
		Last Modified: Sat, 17 Jan 2026 00:32:36 GMT  
		Size: 19.4 MB (19418332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356fa589200fb90532adf9bf598defe12f34d1730f728a493cc1f47019d2dc46`  
		Last Modified: Sat, 17 Jan 2026 00:32:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bca3e0930ba28041675051a18961927142d24d6613f43643112d084fe2ea54`  
		Last Modified: Sat, 17 Jan 2026 00:32:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f85ec7305def0a28b34b0dc0d85d34383426f6ec7852bbb5f37a8505debe2c`  
		Last Modified: Sat, 17 Jan 2026 00:32:32 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860fb2aeaaed18a9b4d34daff9ddd454eecfc15f6c9788e79c3012cfc58e11a0`  
		Last Modified: Sat, 17 Jan 2026 00:32:37 GMT  
		Size: 23.9 MB (23926291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123dcce148cf36dc3fef9dcac9bc0744e708d97e50efaac5ce4d19cd88c4643a`  
		Last Modified: Sat, 17 Jan 2026 00:32:30 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac82bd7e1e254f2f86462290e0b6f665a884852c8aa1955b982a51ba89d28a65`  
		Last Modified: Sat, 17 Jan 2026 00:32:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac11280c48513ddcab1b722f8667f5032899f18af35a191af81071ac5cdb6914`  
		Last Modified: Sat, 17 Jan 2026 00:32:30 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3022a6d86f2499b629eedda0a7d2f272c52085b6ba6ea64307eb525200beeaa8`  
		Last Modified: Sat, 17 Jan 2026 00:32:32 GMT  
		Size: 11.4 MB (11445469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c02a7770053c43d314e65b709cd4998fa6a4e8f8adace2dd551564543ce94221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:27574c8077e47eae8b561adeac8e2136d1c27bb97bfb370868963f775372c3ac
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1890962783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fac75bb46939eff0674007ab202879fd5c512d38bc3477a4ce536005f69de5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Sat, 17 Jan 2026 00:31:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 17 Jan 2026 00:31:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 17 Jan 2026 00:31:37 GMT
ENV DOCKER_VERSION=29.1.5
# Sat, 17 Jan 2026 00:31:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.5.zip
# Sat, 17 Jan 2026 00:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 17 Jan 2026 00:31:55 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Sat, 17 Jan 2026 00:31:56 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Sat, 17 Jan 2026 00:31:57 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Sat, 17 Jan 2026 00:32:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 17 Jan 2026 00:32:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Sat, 17 Jan 2026 00:32:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-windows-x86_64.exe
# Sat, 17 Jan 2026 00:32:15 GMT
ENV DOCKER_COMPOSE_SHA256=2ae341f9152b4d90f561f84b8f2e263d5b60e1613c6841c804447819290c4119
# Sat, 17 Jan 2026 00:32:25 GMT
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
	-	`sha256:b7c78b49395f890e706d473e38c35368e19c6b35bb262c64ca03e023a301e2a6`  
		Last Modified: Sat, 17 Jan 2026 00:32:35 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78ca2adb184b097e41d61db1c4e93f50645315b61438a439b40c1900f125996`  
		Last Modified: Sat, 17 Jan 2026 00:32:34 GMT  
		Size: 501.7 KB (501717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24467fa2d0304efe337e545989ba3cd2e46d51af14ad0b64773f789d3afbeec7`  
		Last Modified: Sat, 17 Jan 2026 00:32:34 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c5802fad231b2fb1a2c83745d11231a54367bf5f857c22dd7e6435fad68712`  
		Last Modified: Sat, 17 Jan 2026 00:32:34 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e8f5908d5455b3264f322cb1a1cc727a24fd8b6f17df307574c2561b3e0f90`  
		Last Modified: Sat, 17 Jan 2026 00:32:36 GMT  
		Size: 19.4 MB (19418332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356fa589200fb90532adf9bf598defe12f34d1730f728a493cc1f47019d2dc46`  
		Last Modified: Sat, 17 Jan 2026 00:32:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bca3e0930ba28041675051a18961927142d24d6613f43643112d084fe2ea54`  
		Last Modified: Sat, 17 Jan 2026 00:32:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f85ec7305def0a28b34b0dc0d85d34383426f6ec7852bbb5f37a8505debe2c`  
		Last Modified: Sat, 17 Jan 2026 00:32:32 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860fb2aeaaed18a9b4d34daff9ddd454eecfc15f6c9788e79c3012cfc58e11a0`  
		Last Modified: Sat, 17 Jan 2026 00:32:37 GMT  
		Size: 23.9 MB (23926291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123dcce148cf36dc3fef9dcac9bc0744e708d97e50efaac5ce4d19cd88c4643a`  
		Last Modified: Sat, 17 Jan 2026 00:32:30 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac82bd7e1e254f2f86462290e0b6f665a884852c8aa1955b982a51ba89d28a65`  
		Last Modified: Sat, 17 Jan 2026 00:32:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac11280c48513ddcab1b722f8667f5032899f18af35a191af81071ac5cdb6914`  
		Last Modified: Sat, 17 Jan 2026 00:32:30 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3022a6d86f2499b629eedda0a7d2f272c52085b6ba6ea64307eb525200beeaa8`  
		Last Modified: Sat, 17 Jan 2026 00:32:32 GMT  
		Size: 11.4 MB (11445469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:0810dacd6ec19cb603ba71bd78b331efb51cffc6958820a4868ff1a67764849d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:011b8de53ecb70fa60f226045aca2c69332bb6ee94d021bb9d3fcc085384a0d5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1550967984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6dccad077a318174c56c30ebe3c491c307ecc1db3239e2cd5c399177b281ef`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Fri, 16 Jan 2026 23:27:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Jan 2026 23:27:58 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Jan 2026 23:27:59 GMT
ENV DOCKER_VERSION=29.1.5
# Fri, 16 Jan 2026 23:28:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.5.zip
# Fri, 16 Jan 2026 23:28:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Jan 2026 23:28:10 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 16 Jan 2026 23:28:11 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 16 Jan 2026 23:28:11 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 16 Jan 2026 23:28:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Jan 2026 23:28:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 16 Jan 2026 23:28:20 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-windows-x86_64.exe
# Fri, 16 Jan 2026 23:28:21 GMT
ENV DOCKER_COMPOSE_SHA256=2ae341f9152b4d90f561f84b8f2e263d5b60e1613c6841c804447819290c4119
# Fri, 16 Jan 2026 23:28:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf85b52279cbf5f434afc4ab079f83bda3ef50d3486fc74a30c20f552694d85f`  
		Last Modified: Fri, 16 Jan 2026 23:28:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93445caeafc2bddea797a95857da92e939124df4d54c185f80f39445e80c0b94`  
		Last Modified: Fri, 16 Jan 2026 23:28:36 GMT  
		Size: 377.1 KB (377114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e299452bcfd7aca11225e6700bf13ba1fb4bcb19e176b8a1a14f554377c7dd2`  
		Last Modified: Fri, 16 Jan 2026 23:28:36 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4053285375a511f9c5e62aad814a3035f4e232806d8993ce9390e35ea7c757b1`  
		Last Modified: Fri, 16 Jan 2026 23:28:36 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dc97dec1a7c7fd01f0954f1b05bf600bd724c454ef5a252543bc69fd4fd00b`  
		Last Modified: Fri, 16 Jan 2026 23:28:38 GMT  
		Size: 19.4 MB (19432334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8f925ec92367d9f26dcaaf379beed54c2f51aa96dedc2c1426ee427cd71831`  
		Last Modified: Fri, 16 Jan 2026 23:28:34 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5376a23cd36fd59eb5251f2151e83a0e1a7a67013ba2b5899fba9a796e16092`  
		Last Modified: Fri, 16 Jan 2026 23:28:34 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c61331a4364799d750587d61e8cce8abf465f33de033951aefcaf07321e77d`  
		Last Modified: Fri, 16 Jan 2026 23:28:34 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b78cf75f88295cbd8090b41c814f0df5e0a6951e496caff112c42de8eac459`  
		Last Modified: Fri, 16 Jan 2026 23:28:36 GMT  
		Size: 23.9 MB (23929994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671ff8ed0c7f11b6caaf11da12b447a4a63e27b1711ecb4078f8007f675be90f`  
		Last Modified: Fri, 16 Jan 2026 23:28:32 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48250282c43183796eda8334f28230b90a9fac97a683cc4c7b9a49373dcf154e`  
		Last Modified: Fri, 16 Jan 2026 23:28:32 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07517cc4d488302c8930b5fac70a5e65f24ec3cf9a28ead9ab5dff5b3d276f0`  
		Last Modified: Fri, 16 Jan 2026 23:28:32 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4401644c9320335d7ccbf201067db845ccd52bb0dd1091a086309a20504d55`  
		Last Modified: Fri, 16 Jan 2026 23:28:34 GMT  
		Size: 11.5 MB (11456516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2`

**does not exist** (yet?)

## `docker:29.2-cli`

**does not exist** (yet?)

## `docker:29.2-dind`

**does not exist** (yet?)

## `docker:29.2-dind-rootless`

**does not exist** (yet?)

## `docker:29.2-windowsservercore`

**does not exist** (yet?)

## `docker:29.2-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `docker:29.2-windowsservercore-ltsc2025`

**does not exist** (yet?)

## `docker:29.2.0`

**does not exist** (yet?)

## `docker:29.2.0-alpine3.23`

**does not exist** (yet?)

## `docker:29.2.0-cli`

**does not exist** (yet?)

## `docker:29.2.0-cli-alpine3.23`

**does not exist** (yet?)

## `docker:29.2.0-dind`

**does not exist** (yet?)

## `docker:29.2.0-dind-alpine3.23`

**does not exist** (yet?)

## `docker:29.2.0-dind-rootless`

**does not exist** (yet?)

## `docker:29.2.0-windowsservercore`

**does not exist** (yet?)

## `docker:29.2.0-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `docker:29.2.0-windowsservercore-ltsc2025`

**does not exist** (yet?)

## `docker:cli`

```console
$ docker pull docker@sha256:931f63d7100eb6734405d92d8bd9f4aa708c587510e5cc673bb9ac196a3d733f
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
$ docker pull docker@sha256:05dfa31f4afd64888ef4cc0cbb1ab4d07a4828ef01cd29baa891fecbe50faf49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64704799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a30dc55d416d2e33ad1f7df0d566efc7abaae030c265daaf694ad4629e5a12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d08bf8475bf9e689c0d705f9b2b740fdc6f57fc7ea8522fa321e0407d5542a`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 8.4 MB (8399670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e0a1bb1a714c3574763a4e79760a69a83b79cfeb1bed66e1183734cba512ea`  
		Last Modified: Fri, 16 Jan 2026 23:30:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f56b512895821ca11cd19fa0f3496f6b325efd5ad4006b5c4dec5828cfbb46`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 18.7 MB (18749967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193ef8aa785fdc807d36f7842f2550fde47924a84196a0e8cae74d61c7ce918f`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 22.9 MB (22905484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd266dff25ac5344bf8acdd83dd1d11a4d114b78e85830c712f55773276c565`  
		Last Modified: Fri, 16 Jan 2026 23:30:57 GMT  
		Size: 10.8 MB (10787419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c46e30e1e8ddc2abe93c818cbc340f93e0d470ba6d76e35a129274946a2191`  
		Last Modified: Fri, 16 Jan 2026 23:30:57 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd70625831c839f25752faf71a054de3bf972e39226d555c0c024a6bb1af04f`  
		Last Modified: Fri, 16 Jan 2026 23:30:58 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa84a26e75eabb10ad201c611a85dfeeda810506ca9d74cfcda13603e3667d5f`  
		Last Modified: Fri, 16 Jan 2026 23:30:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:c0897d8acf674622f9579bb143df44fd1116afeccaf11104aa737db661b38fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722265bbd6439a9e021b7c277085fd6673eafac84c3ca4606ebf76cc2abe2ae6`

```dockerfile
```

-	Layers:
	-	`sha256:75431dcba1812725df60e19ec7c314d1e0d5af58f9df2ee80ba07453f274c907`  
		Last Modified: Fri, 16 Jan 2026 23:30:55 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:eac252823aeabca009b148df41f51495e2075215e5719db3dd2e5103c8e41d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61100286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22621710f5734f5e80b1435dc6b55b8ae0c42b90aa882ab75ae73ea86664868`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:39:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Jan 2026 23:39:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Jan 2026 23:39:33 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Jan 2026 23:39:36 GMT
ENV DOCKER_VERSION=29.1.5
# Fri, 16 Jan 2026 23:39:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Jan 2026 23:39:36 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 16 Jan 2026 23:39:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Jan 2026 23:39:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 16 Jan 2026 23:39:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Jan 2026 23:39:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:39:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8425a4561e629aa414ce86e2154f0076ff9a45b80d061f6543a5764c3cc6f8cd`  
		Last Modified: Fri, 16 Jan 2026 23:39:45 GMT  
		Size: 8.3 MB (8300932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e1fc32be12625d1cb40a6c0bbdb826b3f1cd9617cb46b7d36309048210facb`  
		Last Modified: Fri, 16 Jan 2026 23:39:45 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1a6d78aac1d4b760ea6465b655b17cd29903520f342d5fd358be2db9e129c2`  
		Last Modified: Fri, 16 Jan 2026 23:39:46 GMT  
		Size: 17.6 MB (17555343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6dd9350394ad68195ebf54510ebdf82ae71d4e29733f1801db09877c7ec2c7`  
		Last Modified: Fri, 16 Jan 2026 23:39:46 GMT  
		Size: 21.5 MB (21476547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8014e7548b42b4a7550cc19ad611cce6802080e7e8c5283651fbbd3c5c724438`  
		Last Modified: Fri, 16 Jan 2026 23:39:46 GMT  
		Size: 10.2 MB (10196881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc44c36b674b2071e02951d236d2ce771670678bd7f7293e22e81c5323b0cf54`  
		Last Modified: Fri, 16 Jan 2026 23:39:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f28a7994bba57c7766ea526fe8ebc2659178ebb61a0c69756655fa67bb7c202`  
		Last Modified: Fri, 16 Jan 2026 23:39:47 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02788a3462f1a595a505af2e9d009420d0bfb06e2d337dea3674e8bf736e134b`  
		Last Modified: Fri, 16 Jan 2026 23:39:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:9cbf7a2de0b91f486a924d475390a9d48a99e429c34227fede037ea5c3ff55c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a396ae5c82b755921db2644de41e488cb95d1e426e5fee76536032c0b4367943`

```dockerfile
```

-	Layers:
	-	`sha256:70818a4518c56b0c3d2dab5a67b9d3bd964cbf38ed16dd7028512ae8cc216859`  
		Last Modified: Fri, 16 Jan 2026 23:39:45 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:3ebd30c1dc5192f94a8d0559d088e3a1ba1d52e1ce6a412fb7cc1a61ef793649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60069249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7d3b08056dbb48fbe7580a61a717065059b800b71239ecbb839ed83dcd6ca0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:45:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Jan 2026 23:45:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Jan 2026 23:45:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Jan 2026 23:45:31 GMT
ENV DOCKER_VERSION=29.1.5
# Fri, 16 Jan 2026 23:45:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Jan 2026 23:45:31 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 16 Jan 2026 23:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Jan 2026 23:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 16 Jan 2026 23:45:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Jan 2026 23:45:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:45:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d6ac0ea7d3f4c86291dcfd7858bfc22909b1def944c16f7a61df781848d473`  
		Last Modified: Fri, 16 Jan 2026 23:45:41 GMT  
		Size: 7.6 MB (7597845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fb5218cd2ac0d992f7285c73154c070f9a8c3df766b94feb1973537f455beb`  
		Last Modified: Fri, 16 Jan 2026 23:45:40 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bceaff09615dcc4132e2c0d594f2e3d5a3a843779117809a19f321f15fe2ad9e`  
		Last Modified: Fri, 16 Jan 2026 23:45:41 GMT  
		Size: 17.5 MB (17545469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a348d6c818ddd2fd3b40b4f2d7d93a164c0a1b76723cf4a32bdee4c3f3f709`  
		Last Modified: Fri, 16 Jan 2026 23:45:42 GMT  
		Size: 21.5 MB (21454902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcab9811786db808a1b33b234832a8e9f0395bb71953215ecda47d4b702e33a1`  
		Last Modified: Fri, 16 Jan 2026 23:45:42 GMT  
		Size: 10.2 MB (10189500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfbdbf2e294f4efe5c8d3b3ae54a4339dc3696f32a1cbf0413a44a460e2d27d`  
		Last Modified: Fri, 16 Jan 2026 23:45:42 GMT  
		Size: 534.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee14fa5d481a4a922464ebeaae676f7853468a840d0c41714bec1260541cda8`  
		Last Modified: Fri, 16 Jan 2026 23:45:43 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acb2cea06670f9754971cabf1fc7cf230bc3b5fcbc11ebd75b638239455f5da`  
		Last Modified: Fri, 16 Jan 2026 23:45:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:a24250d752ac002ee2ad261c5a2a0ee85324c3760805ec1a12e20c408c11f04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aedac4f0a36ea54920d67db152805f1ec3414f6ed9be9659058da61c8bff3a07`

```dockerfile
```

-	Layers:
	-	`sha256:6a6873d72ecda31e1f24bbc65bc15765582381d99f215cd8d4adcd08b0b76e69`  
		Last Modified: Fri, 16 Jan 2026 23:45:41 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:16301c9c10717965d70f1651a641dd533a592016a90647ad66969fceda04a907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60568165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4d705451246e5bff54c8dca70a2099a093f07e744f1976b63d10c61b5fb0b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20aa2d791b8266f9dfa17d7927ad7bb695c7563923625c1f1b6b63d3e8a000b8`  
		Last Modified: Fri, 16 Jan 2026 23:33:49 GMT  
		Size: 8.5 MB (8453607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99f01766c5623ec5c29704949d2f9e78727351173fec312a472dda75bfe0fbc`  
		Last Modified: Fri, 16 Jan 2026 23:33:49 GMT  
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
		Last Modified: Fri, 16 Jan 2026 23:33:50 GMT  
		Size: 9.9 MB (9942176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f459c129e2df20f5a0b9d2cef232a2dcc43c1a744d94e95858ab5898896faead`  
		Last Modified: Fri, 16 Jan 2026 23:33:50 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cb42b654a8b7f6386af70afcfb18943c2b6ddfac3d25ac7663ad506613f927`  
		Last Modified: Fri, 16 Jan 2026 23:33:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985d6fb9c70efed7fba20dcfd74096bc1b34a04d71408695041842c10709c246`  
		Last Modified: Fri, 16 Jan 2026 23:33:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:a73bb7b22189634a7f4135430f6caf9ec01e67883274b3950eb4088cdd2dba24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d139971a2dc86dc8a27dbf92c4978b25045b7f90411f6baabbe1a80d7f154c`

```dockerfile
```

-	Layers:
	-	`sha256:40134b323d2780d17cbaf43b8652eafbd904a31761a314b9d0d61efe6d2d0358`  
		Last Modified: Fri, 16 Jan 2026 23:33:49 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:3a33fc81fa4d38360f490f5b900e9846f725db45bb1d9b1fe02d849bd42a5cf2
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
$ docker pull docker@sha256:0ff14e6a992f2fdb7bef46123cd7fe61a58df0494e8df8bb6f9a5dac7486e1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136104845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374a53c1df9dbce9a844321500ad0d38af686f026dc7113c20b5cf0f114a4bf4`
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
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d08bf8475bf9e689c0d705f9b2b740fdc6f57fc7ea8522fa321e0407d5542a`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 8.4 MB (8399670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e0a1bb1a714c3574763a4e79760a69a83b79cfeb1bed66e1183734cba512ea`  
		Last Modified: Fri, 16 Jan 2026 23:30:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f56b512895821ca11cd19fa0f3496f6b325efd5ad4006b5c4dec5828cfbb46`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 18.7 MB (18749967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193ef8aa785fdc807d36f7842f2550fde47924a84196a0e8cae74d61c7ce918f`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 22.9 MB (22905484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd266dff25ac5344bf8acdd83dd1d11a4d114b78e85830c712f55773276c565`  
		Last Modified: Fri, 16 Jan 2026 23:30:57 GMT  
		Size: 10.8 MB (10787419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c46e30e1e8ddc2abe93c818cbc340f93e0d470ba6d76e35a129274946a2191`  
		Last Modified: Fri, 16 Jan 2026 23:30:57 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd70625831c839f25752faf71a054de3bf972e39226d555c0c024a6bb1af04f`  
		Last Modified: Fri, 16 Jan 2026 23:30:58 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa84a26e75eabb10ad201c611a85dfeeda810506ca9d74cfcda13603e3667d5f`  
		Last Modified: Fri, 16 Jan 2026 23:30:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a227f237fe1cc495143034aa29d1f3bb34935624b3a1968387be3be9643afd`  
		Last Modified: Fri, 16 Jan 2026 23:44:01 GMT  
		Size: 6.9 MB (6934060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9e772224d42944940e5982b30cb03a21c31a9597a8266f2dd3b8ee81c921a4`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
		Size: 92.5 KB (92455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9840a05cb973e2d8b0c68b64a66746c6d190887c3dd23d828c49ce56fd762bb6`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96e9a4646741eb4c737b5a5be006e0597cc26cef2276a4886f5fe1e3ba2288f`  
		Last Modified: Fri, 16 Jan 2026 23:44:02 GMT  
		Size: 64.4 MB (64367539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf27a6cf55bb7deeafc395d22479b56698da0c32ef86ab9e517d8d4ca1f33b41`  
		Last Modified: Fri, 16 Jan 2026 23:44:01 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6b1067e7e749c94b29fbcac41bc9d5ec545fb31d5b5ddb1f3a0b52ea357d41`  
		Last Modified: Fri, 16 Jan 2026 23:44:02 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:690a3533a5552c5e90f13a10a4b59da86854bf9b60446440dcdd8c168022f128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd04989d4be905d33abc134ff9eed506f20d21947bd8fe9e7dd3cf9603373ed`

```dockerfile
```

-	Layers:
	-	`sha256:f075788042fd798a5b7835588a5d1a1e119d28cf5c6ab3b938bd8d819adefe23`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:57d6151f7fb71e8b9bfe234e3be9512f8851f7e6bc21ed956381c6d7dbb3dbb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128357962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc21a1c40fa51d364b2f1ea3eb041ca809dd3c1f9b2262ce52db835f4ccac91`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:39:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Jan 2026 23:39:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Jan 2026 23:39:33 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Jan 2026 23:39:36 GMT
ENV DOCKER_VERSION=29.1.5
# Fri, 16 Jan 2026 23:39:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Jan 2026 23:39:36 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 16 Jan 2026 23:39:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Jan 2026 23:39:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 16 Jan 2026 23:39:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Jan 2026 23:39:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:39:39 GMT
CMD ["sh"]
# Fri, 16 Jan 2026 23:43:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 16 Jan 2026 23:43:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 16 Jan 2026 23:43:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 16 Jan 2026 23:43:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 16 Jan 2026 23:43:22 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 16 Jan 2026 23:43:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 16 Jan 2026 23:43:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:43:22 GMT
VOLUME [/var/lib/docker]
# Fri, 16 Jan 2026 23:43:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 16 Jan 2026 23:43:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 16 Jan 2026 23:43:22 GMT
CMD []
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8425a4561e629aa414ce86e2154f0076ff9a45b80d061f6543a5764c3cc6f8cd`  
		Last Modified: Fri, 16 Jan 2026 23:39:45 GMT  
		Size: 8.3 MB (8300932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e1fc32be12625d1cb40a6c0bbdb826b3f1cd9617cb46b7d36309048210facb`  
		Last Modified: Fri, 16 Jan 2026 23:39:45 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1a6d78aac1d4b760ea6465b655b17cd29903520f342d5fd358be2db9e129c2`  
		Last Modified: Fri, 16 Jan 2026 23:39:46 GMT  
		Size: 17.6 MB (17555343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6dd9350394ad68195ebf54510ebdf82ae71d4e29733f1801db09877c7ec2c7`  
		Last Modified: Fri, 16 Jan 2026 23:39:46 GMT  
		Size: 21.5 MB (21476547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8014e7548b42b4a7550cc19ad611cce6802080e7e8c5283651fbbd3c5c724438`  
		Last Modified: Fri, 16 Jan 2026 23:39:46 GMT  
		Size: 10.2 MB (10196881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc44c36b674b2071e02951d236d2ce771670678bd7f7293e22e81c5323b0cf54`  
		Last Modified: Fri, 16 Jan 2026 23:39:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f28a7994bba57c7766ea526fe8ebc2659178ebb61a0c69756655fa67bb7c202`  
		Last Modified: Fri, 16 Jan 2026 23:39:47 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02788a3462f1a595a505af2e9d009420d0bfb06e2d337dea3674e8bf736e134b`  
		Last Modified: Fri, 16 Jan 2026 23:39:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99c270ea4672ae7031121d6c3eb7150821ca52f133152c395baf84fdeaef335`  
		Last Modified: Fri, 16 Jan 2026 23:43:31 GMT  
		Size: 7.3 MB (7271448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a5c0fdb8ce4ad9734e2e154d06098bc7d3b66c67009e0cb63e21513d115c73`  
		Last Modified: Fri, 16 Jan 2026 23:43:31 GMT  
		Size: 91.8 KB (91772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c956cd4f121d5305de4f3ef19946cc75795eebf1b1f2b54bf5f340fa98de68`  
		Last Modified: Fri, 16 Jan 2026 23:43:31 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7332978ccc2976b3b6f16863ce750cf67e78d133ad47a1b496e943a97639e178`  
		Last Modified: Fri, 16 Jan 2026 23:43:33 GMT  
		Size: 59.9 MB (59888458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5ab6343c168d5995fad57f8a71b332852d0d1a2a35747ab883c9059dbe843c`  
		Last Modified: Fri, 16 Jan 2026 23:43:32 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71f35537c4608ca161ccf8b26e5ba3a7a237177b30c410d0e54aa5e5ff0e25`  
		Last Modified: Fri, 16 Jan 2026 23:43:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:aa0a301d83a325df841314b7bd7dde3dda152fb9a75bebaac99ac88a1451910a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b4a36c4242c6ba5c596734fcaa60697ed99cae2c45333bb5acb5e2d101ebd8`

```dockerfile
```

-	Layers:
	-	`sha256:7f2cc6b7f4ba2244c96a5b422d3eb723b81373c24cbf8052a3e85ae8613015f5`  
		Last Modified: Fri, 16 Jan 2026 23:43:31 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:8236ceb58e17942c161b981f016e36bb296cdbb8f7a0340b1fe59d243a312cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126449081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae08a90d372f5e8a9d947d84aa3b21f215b6dc66a6ff3b29b69d2cd52f307b8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:45:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Jan 2026 23:45:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Jan 2026 23:45:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Jan 2026 23:45:31 GMT
ENV DOCKER_VERSION=29.1.5
# Fri, 16 Jan 2026 23:45:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Jan 2026 23:45:31 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 16 Jan 2026 23:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Jan 2026 23:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 16 Jan 2026 23:45:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Jan 2026 23:45:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:45:35 GMT
CMD ["sh"]
# Sat, 17 Jan 2026 00:17:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 17 Jan 2026 00:17:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 17 Jan 2026 00:17:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 17 Jan 2026 00:17:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 17 Jan 2026 00:17:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 17 Jan 2026 00:17:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 17 Jan 2026 00:17:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 00:17:17 GMT
VOLUME [/var/lib/docker]
# Sat, 17 Jan 2026 00:17:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 17 Jan 2026 00:17:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 17 Jan 2026 00:17:17 GMT
CMD []
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d6ac0ea7d3f4c86291dcfd7858bfc22909b1def944c16f7a61df781848d473`  
		Last Modified: Fri, 16 Jan 2026 23:45:41 GMT  
		Size: 7.6 MB (7597845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fb5218cd2ac0d992f7285c73154c070f9a8c3df766b94feb1973537f455beb`  
		Last Modified: Fri, 16 Jan 2026 23:45:40 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bceaff09615dcc4132e2c0d594f2e3d5a3a843779117809a19f321f15fe2ad9e`  
		Last Modified: Fri, 16 Jan 2026 23:45:41 GMT  
		Size: 17.5 MB (17545469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a348d6c818ddd2fd3b40b4f2d7d93a164c0a1b76723cf4a32bdee4c3f3f709`  
		Last Modified: Fri, 16 Jan 2026 23:45:42 GMT  
		Size: 21.5 MB (21454902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcab9811786db808a1b33b234832a8e9f0395bb71953215ecda47d4b702e33a1`  
		Last Modified: Fri, 16 Jan 2026 23:45:42 GMT  
		Size: 10.2 MB (10189500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfbdbf2e294f4efe5c8d3b3ae54a4339dc3696f32a1cbf0413a44a460e2d27d`  
		Last Modified: Fri, 16 Jan 2026 23:45:42 GMT  
		Size: 534.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee14fa5d481a4a922464ebeaae676f7853468a840d0c41714bec1260541cda8`  
		Last Modified: Fri, 16 Jan 2026 23:45:43 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acb2cea06670f9754971cabf1fc7cf230bc3b5fcbc11ebd75b638239455f5da`  
		Last Modified: Fri, 16 Jan 2026 23:45:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2453c0e4f4894b542c662dea67f6213701f4fc355c2d020fad490bc8914572`  
		Last Modified: Sat, 17 Jan 2026 00:17:27 GMT  
		Size: 6.6 MB (6572857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5bf8ef2c4008a2d3965314f4295808b1801bcea094c21addffdfb0e4969e27`  
		Last Modified: Sat, 17 Jan 2026 00:17:27 GMT  
		Size: 88.1 KB (88139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417d31beb5548151e490cf03161b9aa6bc3169d4fbadd9a614b00d88d99394ee`  
		Last Modified: Sat, 17 Jan 2026 00:17:27 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b96020d2757029849b8a5d7e2328d9dbcbede2c16832b792aea4cbe92df97d`  
		Last Modified: Sat, 17 Jan 2026 00:17:29 GMT  
		Size: 59.7 MB (59712841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55262ae149e208b2a2fd5827d141bb0d8092baa2c93c47a7ed474a1576710534`  
		Last Modified: Sat, 17 Jan 2026 00:17:28 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da08a763fccaf17ff2fdadc52714e03107a5cf573f4c25b5e7837e9425d653`  
		Last Modified: Sat, 17 Jan 2026 00:17:28 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:ca46d59e18eba52837126d2b02c42cc12b13814954b5037e04dc7bb84dce309e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfae3d58cc56c795eb029b1de3f6d92122a531264255e6d4499886b13bd825bc`

```dockerfile
```

-	Layers:
	-	`sha256:97affc86a76a9497fb0cc56a7fc9355d583b08d33928e751d96813d8d33411ec`  
		Last Modified: Sat, 17 Jan 2026 00:17:27 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:87ca5378e2aaf821e5c84c6b5420b0bdec3cbeaff9fada3f838d7ddb528ea65e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126294567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a399de96efb1fb33c64b8559091aff5ecdaa4c85e5a4ed78e623b3ff3d7db00f`
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
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20aa2d791b8266f9dfa17d7927ad7bb695c7563923625c1f1b6b63d3e8a000b8`  
		Last Modified: Fri, 16 Jan 2026 23:33:49 GMT  
		Size: 8.5 MB (8453607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99f01766c5623ec5c29704949d2f9e78727351173fec312a472dda75bfe0fbc`  
		Last Modified: Fri, 16 Jan 2026 23:33:49 GMT  
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
		Last Modified: Fri, 16 Jan 2026 23:33:50 GMT  
		Size: 9.9 MB (9942176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f459c129e2df20f5a0b9d2cef232a2dcc43c1a744d94e95858ab5898896faead`  
		Last Modified: Fri, 16 Jan 2026 23:33:50 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cb42b654a8b7f6386af70afcfb18943c2b6ddfac3d25ac7663ad506613f927`  
		Last Modified: Fri, 16 Jan 2026 23:33:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985d6fb9c70efed7fba20dcfd74096bc1b34a04d71408695041842c10709c246`  
		Last Modified: Fri, 16 Jan 2026 23:33:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba14d49cf482ad8767be9715f12c32540f21afe52f5eeea827d7889eef9f4e5`  
		Last Modified: Fri, 16 Jan 2026 23:43:58 GMT  
		Size: 7.2 MB (7212983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f869ecca31b7e4cb47dac3444670d9ac67935d4711faf1f4dc73c54448119f58`  
		Last Modified: Fri, 16 Jan 2026 23:43:57 GMT  
		Size: 101.3 KB (101282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07025eda5cadcd2aad50deee35f3f3e4ab0f3bd4d0bf30ede81de47cfdde90d6`  
		Last Modified: Fri, 16 Jan 2026 23:43:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a4cc2ba717f8eaa4d250fcc460585a66fa48d9b640e570c448565b2ff4224`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
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

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:80b38265128675e62f9a23f63712d831c9f6f6800134cc0ce50c9658c521a3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c40b7c657c6e3c82a0476a1643e1b0b16cd2e9fd25fab6b77fa01522a9e855`

```dockerfile
```

-	Layers:
	-	`sha256:864ff6c43af948c3507e027a248d1476e720357b5a03a24de18633b231004d39`  
		Last Modified: Fri, 16 Jan 2026 23:43:57 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

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
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d08bf8475bf9e689c0d705f9b2b740fdc6f57fc7ea8522fa321e0407d5542a`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 8.4 MB (8399670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e0a1bb1a714c3574763a4e79760a69a83b79cfeb1bed66e1183734cba512ea`  
		Last Modified: Fri, 16 Jan 2026 23:30:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f56b512895821ca11cd19fa0f3496f6b325efd5ad4006b5c4dec5828cfbb46`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 18.7 MB (18749967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193ef8aa785fdc807d36f7842f2550fde47924a84196a0e8cae74d61c7ce918f`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 22.9 MB (22905484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd266dff25ac5344bf8acdd83dd1d11a4d114b78e85830c712f55773276c565`  
		Last Modified: Fri, 16 Jan 2026 23:30:57 GMT  
		Size: 10.8 MB (10787419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c46e30e1e8ddc2abe93c818cbc340f93e0d470ba6d76e35a129274946a2191`  
		Last Modified: Fri, 16 Jan 2026 23:30:57 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd70625831c839f25752faf71a054de3bf972e39226d555c0c024a6bb1af04f`  
		Last Modified: Fri, 16 Jan 2026 23:30:58 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa84a26e75eabb10ad201c611a85dfeeda810506ca9d74cfcda13603e3667d5f`  
		Last Modified: Fri, 16 Jan 2026 23:30:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a227f237fe1cc495143034aa29d1f3bb34935624b3a1968387be3be9643afd`  
		Last Modified: Fri, 16 Jan 2026 23:44:01 GMT  
		Size: 6.9 MB (6934060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9e772224d42944940e5982b30cb03a21c31a9597a8266f2dd3b8ee81c921a4`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
		Size: 92.5 KB (92455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9840a05cb973e2d8b0c68b64a66746c6d190887c3dd23d828c49ce56fd762bb6`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96e9a4646741eb4c737b5a5be006e0597cc26cef2276a4886f5fe1e3ba2288f`  
		Last Modified: Fri, 16 Jan 2026 23:44:02 GMT  
		Size: 64.4 MB (64367539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf27a6cf55bb7deeafc395d22479b56698da0c32ef86ab9e517d8d4ca1f33b41`  
		Last Modified: Fri, 16 Jan 2026 23:44:01 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6b1067e7e749c94b29fbcac41bc9d5ec545fb31d5b5ddb1f3a0b52ea357d41`  
		Last Modified: Fri, 16 Jan 2026 23:44:02 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1557b2a406cc6f243f0171436f503bdb8e8d1e3e77bdcf36bc1b684311ed72`  
		Last Modified: Sat, 17 Jan 2026 00:14:54 GMT  
		Size: 3.4 MB (3419929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d8849e55ddf8f1caa5eaf086451cea763b8e9545dd3c3e97fdcdb59ef201a5`  
		Last Modified: Sat, 17 Jan 2026 00:14:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a94cff53939cdff88071fbd8e0fa9d0603580457bd6118ab08d88cf2201942`  
		Last Modified: Sat, 17 Jan 2026 00:14:53 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47d0dfc54602c4b9b436657ddff22108d34d2abee74a876828b8012a4c8e868`  
		Last Modified: Sat, 17 Jan 2026 00:14:54 GMT  
		Size: 17.4 MB (17371697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b922a090e96a69d521d8afb6527fa2cb7242cbf56626b59321174c38d81e858a`  
		Last Modified: Sat, 17 Jan 2026 00:14:54 GMT  
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
		Last Modified: Sat, 17 Jan 2026 00:14:53 GMT  
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
		Last Modified: Fri, 16 Jan 2026 23:33:49 GMT  
		Size: 8.5 MB (8453607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99f01766c5623ec5c29704949d2f9e78727351173fec312a472dda75bfe0fbc`  
		Last Modified: Fri, 16 Jan 2026 23:33:49 GMT  
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
		Last Modified: Fri, 16 Jan 2026 23:33:50 GMT  
		Size: 9.9 MB (9942176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f459c129e2df20f5a0b9d2cef232a2dcc43c1a744d94e95858ab5898896faead`  
		Last Modified: Fri, 16 Jan 2026 23:33:50 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cb42b654a8b7f6386af70afcfb18943c2b6ddfac3d25ac7663ad506613f927`  
		Last Modified: Fri, 16 Jan 2026 23:33:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985d6fb9c70efed7fba20dcfd74096bc1b34a04d71408695041842c10709c246`  
		Last Modified: Fri, 16 Jan 2026 23:33:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba14d49cf482ad8767be9715f12c32540f21afe52f5eeea827d7889eef9f4e5`  
		Last Modified: Fri, 16 Jan 2026 23:43:58 GMT  
		Size: 7.2 MB (7212983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f869ecca31b7e4cb47dac3444670d9ac67935d4711faf1f4dc73c54448119f58`  
		Last Modified: Fri, 16 Jan 2026 23:43:57 GMT  
		Size: 101.3 KB (101282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07025eda5cadcd2aad50deee35f3f3e4ab0f3bd4d0bf30ede81de47cfdde90d6`  
		Last Modified: Fri, 16 Jan 2026 23:43:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a4cc2ba717f8eaa4d250fcc460585a66fa48d9b640e570c448565b2ff4224`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
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
		Last Modified: Sat, 17 Jan 2026 00:15:18 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12502433d4f521c091bf5f40e0a2f10c483376cd6cf491d5167d0d71255e93ae`  
		Last Modified: Sat, 17 Jan 2026 00:15:18 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028d45c1e6c47fa93138f7186507cc4c5173fce93755e0c753f472d31ca4449d`  
		Last Modified: Sat, 17 Jan 2026 00:15:18 GMT  
		Size: 17.7 MB (17709424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d784a5d534b102bd49b134cf1aa67620b01c91b045f85c4618fba5fa487ff05b`  
		Last Modified: Sat, 17 Jan 2026 00:15:19 GMT  
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
		Last Modified: Sat, 17 Jan 2026 00:15:17 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:3a33fc81fa4d38360f490f5b900e9846f725db45bb1d9b1fe02d849bd42a5cf2
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
$ docker pull docker@sha256:0ff14e6a992f2fdb7bef46123cd7fe61a58df0494e8df8bb6f9a5dac7486e1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136104845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374a53c1df9dbce9a844321500ad0d38af686f026dc7113c20b5cf0f114a4bf4`
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
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d08bf8475bf9e689c0d705f9b2b740fdc6f57fc7ea8522fa321e0407d5542a`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 8.4 MB (8399670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e0a1bb1a714c3574763a4e79760a69a83b79cfeb1bed66e1183734cba512ea`  
		Last Modified: Fri, 16 Jan 2026 23:30:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f56b512895821ca11cd19fa0f3496f6b325efd5ad4006b5c4dec5828cfbb46`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 18.7 MB (18749967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193ef8aa785fdc807d36f7842f2550fde47924a84196a0e8cae74d61c7ce918f`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 22.9 MB (22905484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd266dff25ac5344bf8acdd83dd1d11a4d114b78e85830c712f55773276c565`  
		Last Modified: Fri, 16 Jan 2026 23:30:57 GMT  
		Size: 10.8 MB (10787419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c46e30e1e8ddc2abe93c818cbc340f93e0d470ba6d76e35a129274946a2191`  
		Last Modified: Fri, 16 Jan 2026 23:30:57 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd70625831c839f25752faf71a054de3bf972e39226d555c0c024a6bb1af04f`  
		Last Modified: Fri, 16 Jan 2026 23:30:58 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa84a26e75eabb10ad201c611a85dfeeda810506ca9d74cfcda13603e3667d5f`  
		Last Modified: Fri, 16 Jan 2026 23:30:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a227f237fe1cc495143034aa29d1f3bb34935624b3a1968387be3be9643afd`  
		Last Modified: Fri, 16 Jan 2026 23:44:01 GMT  
		Size: 6.9 MB (6934060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9e772224d42944940e5982b30cb03a21c31a9597a8266f2dd3b8ee81c921a4`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
		Size: 92.5 KB (92455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9840a05cb973e2d8b0c68b64a66746c6d190887c3dd23d828c49ce56fd762bb6`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96e9a4646741eb4c737b5a5be006e0597cc26cef2276a4886f5fe1e3ba2288f`  
		Last Modified: Fri, 16 Jan 2026 23:44:02 GMT  
		Size: 64.4 MB (64367539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf27a6cf55bb7deeafc395d22479b56698da0c32ef86ab9e517d8d4ca1f33b41`  
		Last Modified: Fri, 16 Jan 2026 23:44:01 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6b1067e7e749c94b29fbcac41bc9d5ec545fb31d5b5ddb1f3a0b52ea357d41`  
		Last Modified: Fri, 16 Jan 2026 23:44:02 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:690a3533a5552c5e90f13a10a4b59da86854bf9b60446440dcdd8c168022f128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd04989d4be905d33abc134ff9eed506f20d21947bd8fe9e7dd3cf9603373ed`

```dockerfile
```

-	Layers:
	-	`sha256:f075788042fd798a5b7835588a5d1a1e119d28cf5c6ab3b938bd8d819adefe23`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:57d6151f7fb71e8b9bfe234e3be9512f8851f7e6bc21ed956381c6d7dbb3dbb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128357962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc21a1c40fa51d364b2f1ea3eb041ca809dd3c1f9b2262ce52db835f4ccac91`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:39:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Jan 2026 23:39:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Jan 2026 23:39:33 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Jan 2026 23:39:36 GMT
ENV DOCKER_VERSION=29.1.5
# Fri, 16 Jan 2026 23:39:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Jan 2026 23:39:36 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 16 Jan 2026 23:39:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Jan 2026 23:39:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 16 Jan 2026 23:39:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Jan 2026 23:39:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Jan 2026 23:39:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:39:39 GMT
CMD ["sh"]
# Fri, 16 Jan 2026 23:43:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 16 Jan 2026 23:43:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 16 Jan 2026 23:43:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 16 Jan 2026 23:43:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 16 Jan 2026 23:43:22 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 16 Jan 2026 23:43:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 16 Jan 2026 23:43:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:43:22 GMT
VOLUME [/var/lib/docker]
# Fri, 16 Jan 2026 23:43:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 16 Jan 2026 23:43:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 16 Jan 2026 23:43:22 GMT
CMD []
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8425a4561e629aa414ce86e2154f0076ff9a45b80d061f6543a5764c3cc6f8cd`  
		Last Modified: Fri, 16 Jan 2026 23:39:45 GMT  
		Size: 8.3 MB (8300932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e1fc32be12625d1cb40a6c0bbdb826b3f1cd9617cb46b7d36309048210facb`  
		Last Modified: Fri, 16 Jan 2026 23:39:45 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1a6d78aac1d4b760ea6465b655b17cd29903520f342d5fd358be2db9e129c2`  
		Last Modified: Fri, 16 Jan 2026 23:39:46 GMT  
		Size: 17.6 MB (17555343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6dd9350394ad68195ebf54510ebdf82ae71d4e29733f1801db09877c7ec2c7`  
		Last Modified: Fri, 16 Jan 2026 23:39:46 GMT  
		Size: 21.5 MB (21476547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8014e7548b42b4a7550cc19ad611cce6802080e7e8c5283651fbbd3c5c724438`  
		Last Modified: Fri, 16 Jan 2026 23:39:46 GMT  
		Size: 10.2 MB (10196881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc44c36b674b2071e02951d236d2ce771670678bd7f7293e22e81c5323b0cf54`  
		Last Modified: Fri, 16 Jan 2026 23:39:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f28a7994bba57c7766ea526fe8ebc2659178ebb61a0c69756655fa67bb7c202`  
		Last Modified: Fri, 16 Jan 2026 23:39:47 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02788a3462f1a595a505af2e9d009420d0bfb06e2d337dea3674e8bf736e134b`  
		Last Modified: Fri, 16 Jan 2026 23:39:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99c270ea4672ae7031121d6c3eb7150821ca52f133152c395baf84fdeaef335`  
		Last Modified: Fri, 16 Jan 2026 23:43:31 GMT  
		Size: 7.3 MB (7271448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a5c0fdb8ce4ad9734e2e154d06098bc7d3b66c67009e0cb63e21513d115c73`  
		Last Modified: Fri, 16 Jan 2026 23:43:31 GMT  
		Size: 91.8 KB (91772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c956cd4f121d5305de4f3ef19946cc75795eebf1b1f2b54bf5f340fa98de68`  
		Last Modified: Fri, 16 Jan 2026 23:43:31 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7332978ccc2976b3b6f16863ce750cf67e78d133ad47a1b496e943a97639e178`  
		Last Modified: Fri, 16 Jan 2026 23:43:33 GMT  
		Size: 59.9 MB (59888458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5ab6343c168d5995fad57f8a71b332852d0d1a2a35747ab883c9059dbe843c`  
		Last Modified: Fri, 16 Jan 2026 23:43:32 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71f35537c4608ca161ccf8b26e5ba3a7a237177b30c410d0e54aa5e5ff0e25`  
		Last Modified: Fri, 16 Jan 2026 23:43:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:aa0a301d83a325df841314b7bd7dde3dda152fb9a75bebaac99ac88a1451910a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b4a36c4242c6ba5c596734fcaa60697ed99cae2c45333bb5acb5e2d101ebd8`

```dockerfile
```

-	Layers:
	-	`sha256:7f2cc6b7f4ba2244c96a5b422d3eb723b81373c24cbf8052a3e85ae8613015f5`  
		Last Modified: Fri, 16 Jan 2026 23:43:31 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:8236ceb58e17942c161b981f016e36bb296cdbb8f7a0340b1fe59d243a312cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126449081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae08a90d372f5e8a9d947d84aa3b21f215b6dc66a6ff3b29b69d2cd52f307b8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:45:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Jan 2026 23:45:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Jan 2026 23:45:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Jan 2026 23:45:31 GMT
ENV DOCKER_VERSION=29.1.5
# Fri, 16 Jan 2026 23:45:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Jan 2026 23:45:31 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 16 Jan 2026 23:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Jan 2026 23:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 16 Jan 2026 23:45:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Jan 2026 23:45:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Jan 2026 23:45:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:45:35 GMT
CMD ["sh"]
# Sat, 17 Jan 2026 00:17:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 17 Jan 2026 00:17:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 17 Jan 2026 00:17:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 17 Jan 2026 00:17:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 17 Jan 2026 00:17:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 17 Jan 2026 00:17:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 17 Jan 2026 00:17:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 00:17:17 GMT
VOLUME [/var/lib/docker]
# Sat, 17 Jan 2026 00:17:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 17 Jan 2026 00:17:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 17 Jan 2026 00:17:17 GMT
CMD []
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d6ac0ea7d3f4c86291dcfd7858bfc22909b1def944c16f7a61df781848d473`  
		Last Modified: Fri, 16 Jan 2026 23:45:41 GMT  
		Size: 7.6 MB (7597845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fb5218cd2ac0d992f7285c73154c070f9a8c3df766b94feb1973537f455beb`  
		Last Modified: Fri, 16 Jan 2026 23:45:40 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bceaff09615dcc4132e2c0d594f2e3d5a3a843779117809a19f321f15fe2ad9e`  
		Last Modified: Fri, 16 Jan 2026 23:45:41 GMT  
		Size: 17.5 MB (17545469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a348d6c818ddd2fd3b40b4f2d7d93a164c0a1b76723cf4a32bdee4c3f3f709`  
		Last Modified: Fri, 16 Jan 2026 23:45:42 GMT  
		Size: 21.5 MB (21454902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcab9811786db808a1b33b234832a8e9f0395bb71953215ecda47d4b702e33a1`  
		Last Modified: Fri, 16 Jan 2026 23:45:42 GMT  
		Size: 10.2 MB (10189500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfbdbf2e294f4efe5c8d3b3ae54a4339dc3696f32a1cbf0413a44a460e2d27d`  
		Last Modified: Fri, 16 Jan 2026 23:45:42 GMT  
		Size: 534.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee14fa5d481a4a922464ebeaae676f7853468a840d0c41714bec1260541cda8`  
		Last Modified: Fri, 16 Jan 2026 23:45:43 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acb2cea06670f9754971cabf1fc7cf230bc3b5fcbc11ebd75b638239455f5da`  
		Last Modified: Fri, 16 Jan 2026 23:45:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2453c0e4f4894b542c662dea67f6213701f4fc355c2d020fad490bc8914572`  
		Last Modified: Sat, 17 Jan 2026 00:17:27 GMT  
		Size: 6.6 MB (6572857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5bf8ef2c4008a2d3965314f4295808b1801bcea094c21addffdfb0e4969e27`  
		Last Modified: Sat, 17 Jan 2026 00:17:27 GMT  
		Size: 88.1 KB (88139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417d31beb5548151e490cf03161b9aa6bc3169d4fbadd9a614b00d88d99394ee`  
		Last Modified: Sat, 17 Jan 2026 00:17:27 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b96020d2757029849b8a5d7e2328d9dbcbede2c16832b792aea4cbe92df97d`  
		Last Modified: Sat, 17 Jan 2026 00:17:29 GMT  
		Size: 59.7 MB (59712841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55262ae149e208b2a2fd5827d141bb0d8092baa2c93c47a7ed474a1576710534`  
		Last Modified: Sat, 17 Jan 2026 00:17:28 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da08a763fccaf17ff2fdadc52714e03107a5cf573f4c25b5e7837e9425d653`  
		Last Modified: Sat, 17 Jan 2026 00:17:28 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:ca46d59e18eba52837126d2b02c42cc12b13814954b5037e04dc7bb84dce309e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfae3d58cc56c795eb029b1de3f6d92122a531264255e6d4499886b13bd825bc`

```dockerfile
```

-	Layers:
	-	`sha256:97affc86a76a9497fb0cc56a7fc9355d583b08d33928e751d96813d8d33411ec`  
		Last Modified: Sat, 17 Jan 2026 00:17:27 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:87ca5378e2aaf821e5c84c6b5420b0bdec3cbeaff9fada3f838d7ddb528ea65e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126294567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a399de96efb1fb33c64b8559091aff5ecdaa4c85e5a4ed78e623b3ff3d7db00f`
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
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20aa2d791b8266f9dfa17d7927ad7bb695c7563923625c1f1b6b63d3e8a000b8`  
		Last Modified: Fri, 16 Jan 2026 23:33:49 GMT  
		Size: 8.5 MB (8453607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99f01766c5623ec5c29704949d2f9e78727351173fec312a472dda75bfe0fbc`  
		Last Modified: Fri, 16 Jan 2026 23:33:49 GMT  
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
		Last Modified: Fri, 16 Jan 2026 23:33:50 GMT  
		Size: 9.9 MB (9942176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f459c129e2df20f5a0b9d2cef232a2dcc43c1a744d94e95858ab5898896faead`  
		Last Modified: Fri, 16 Jan 2026 23:33:50 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cb42b654a8b7f6386af70afcfb18943c2b6ddfac3d25ac7663ad506613f927`  
		Last Modified: Fri, 16 Jan 2026 23:33:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985d6fb9c70efed7fba20dcfd74096bc1b34a04d71408695041842c10709c246`  
		Last Modified: Fri, 16 Jan 2026 23:33:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba14d49cf482ad8767be9715f12c32540f21afe52f5eeea827d7889eef9f4e5`  
		Last Modified: Fri, 16 Jan 2026 23:43:58 GMT  
		Size: 7.2 MB (7212983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f869ecca31b7e4cb47dac3444670d9ac67935d4711faf1f4dc73c54448119f58`  
		Last Modified: Fri, 16 Jan 2026 23:43:57 GMT  
		Size: 101.3 KB (101282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07025eda5cadcd2aad50deee35f3f3e4ab0f3bd4d0bf30ede81de47cfdde90d6`  
		Last Modified: Fri, 16 Jan 2026 23:43:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a4cc2ba717f8eaa4d250fcc460585a66fa48d9b640e570c448565b2ff4224`  
		Last Modified: Fri, 16 Jan 2026 23:44:00 GMT  
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

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:80b38265128675e62f9a23f63712d831c9f6f6800134cc0ce50c9658c521a3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c40b7c657c6e3c82a0476a1643e1b0b16cd2e9fd25fab6b77fa01522a9e855`

```dockerfile
```

-	Layers:
	-	`sha256:864ff6c43af948c3507e027a248d1476e720357b5a03a24de18633b231004d39`  
		Last Modified: Fri, 16 Jan 2026 23:43:57 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:e5be8819c33c02450ae1cb0ffc732f43adce21efbf8bc516c2d83ad28ab7f609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:011b8de53ecb70fa60f226045aca2c69332bb6ee94d021bb9d3fcc085384a0d5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1550967984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6dccad077a318174c56c30ebe3c491c307ecc1db3239e2cd5c399177b281ef`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Fri, 16 Jan 2026 23:27:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Jan 2026 23:27:58 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Jan 2026 23:27:59 GMT
ENV DOCKER_VERSION=29.1.5
# Fri, 16 Jan 2026 23:28:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.5.zip
# Fri, 16 Jan 2026 23:28:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Jan 2026 23:28:10 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 16 Jan 2026 23:28:11 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 16 Jan 2026 23:28:11 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 16 Jan 2026 23:28:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Jan 2026 23:28:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 16 Jan 2026 23:28:20 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-windows-x86_64.exe
# Fri, 16 Jan 2026 23:28:21 GMT
ENV DOCKER_COMPOSE_SHA256=2ae341f9152b4d90f561f84b8f2e263d5b60e1613c6841c804447819290c4119
# Fri, 16 Jan 2026 23:28:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf85b52279cbf5f434afc4ab079f83bda3ef50d3486fc74a30c20f552694d85f`  
		Last Modified: Fri, 16 Jan 2026 23:28:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93445caeafc2bddea797a95857da92e939124df4d54c185f80f39445e80c0b94`  
		Last Modified: Fri, 16 Jan 2026 23:28:36 GMT  
		Size: 377.1 KB (377114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e299452bcfd7aca11225e6700bf13ba1fb4bcb19e176b8a1a14f554377c7dd2`  
		Last Modified: Fri, 16 Jan 2026 23:28:36 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4053285375a511f9c5e62aad814a3035f4e232806d8993ce9390e35ea7c757b1`  
		Last Modified: Fri, 16 Jan 2026 23:28:36 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dc97dec1a7c7fd01f0954f1b05bf600bd724c454ef5a252543bc69fd4fd00b`  
		Last Modified: Fri, 16 Jan 2026 23:28:38 GMT  
		Size: 19.4 MB (19432334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8f925ec92367d9f26dcaaf379beed54c2f51aa96dedc2c1426ee427cd71831`  
		Last Modified: Fri, 16 Jan 2026 23:28:34 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5376a23cd36fd59eb5251f2151e83a0e1a7a67013ba2b5899fba9a796e16092`  
		Last Modified: Fri, 16 Jan 2026 23:28:34 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c61331a4364799d750587d61e8cce8abf465f33de033951aefcaf07321e77d`  
		Last Modified: Fri, 16 Jan 2026 23:28:34 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b78cf75f88295cbd8090b41c814f0df5e0a6951e496caff112c42de8eac459`  
		Last Modified: Fri, 16 Jan 2026 23:28:36 GMT  
		Size: 23.9 MB (23929994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671ff8ed0c7f11b6caaf11da12b447a4a63e27b1711ecb4078f8007f675be90f`  
		Last Modified: Fri, 16 Jan 2026 23:28:32 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48250282c43183796eda8334f28230b90a9fac97a683cc4c7b9a49373dcf154e`  
		Last Modified: Fri, 16 Jan 2026 23:28:32 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07517cc4d488302c8930b5fac70a5e65f24ec3cf9a28ead9ab5dff5b3d276f0`  
		Last Modified: Fri, 16 Jan 2026 23:28:32 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4401644c9320335d7ccbf201067db845ccd52bb0dd1091a086309a20504d55`  
		Last Modified: Fri, 16 Jan 2026 23:28:34 GMT  
		Size: 11.5 MB (11456516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:27574c8077e47eae8b561adeac8e2136d1c27bb97bfb370868963f775372c3ac
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1890962783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fac75bb46939eff0674007ab202879fd5c512d38bc3477a4ce536005f69de5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Sat, 17 Jan 2026 00:31:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 17 Jan 2026 00:31:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 17 Jan 2026 00:31:37 GMT
ENV DOCKER_VERSION=29.1.5
# Sat, 17 Jan 2026 00:31:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.5.zip
# Sat, 17 Jan 2026 00:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 17 Jan 2026 00:31:55 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Sat, 17 Jan 2026 00:31:56 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Sat, 17 Jan 2026 00:31:57 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Sat, 17 Jan 2026 00:32:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 17 Jan 2026 00:32:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Sat, 17 Jan 2026 00:32:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-windows-x86_64.exe
# Sat, 17 Jan 2026 00:32:15 GMT
ENV DOCKER_COMPOSE_SHA256=2ae341f9152b4d90f561f84b8f2e263d5b60e1613c6841c804447819290c4119
# Sat, 17 Jan 2026 00:32:25 GMT
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
	-	`sha256:b7c78b49395f890e706d473e38c35368e19c6b35bb262c64ca03e023a301e2a6`  
		Last Modified: Sat, 17 Jan 2026 00:32:35 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78ca2adb184b097e41d61db1c4e93f50645315b61438a439b40c1900f125996`  
		Last Modified: Sat, 17 Jan 2026 00:32:34 GMT  
		Size: 501.7 KB (501717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24467fa2d0304efe337e545989ba3cd2e46d51af14ad0b64773f789d3afbeec7`  
		Last Modified: Sat, 17 Jan 2026 00:32:34 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c5802fad231b2fb1a2c83745d11231a54367bf5f857c22dd7e6435fad68712`  
		Last Modified: Sat, 17 Jan 2026 00:32:34 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e8f5908d5455b3264f322cb1a1cc727a24fd8b6f17df307574c2561b3e0f90`  
		Last Modified: Sat, 17 Jan 2026 00:32:36 GMT  
		Size: 19.4 MB (19418332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356fa589200fb90532adf9bf598defe12f34d1730f728a493cc1f47019d2dc46`  
		Last Modified: Sat, 17 Jan 2026 00:32:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bca3e0930ba28041675051a18961927142d24d6613f43643112d084fe2ea54`  
		Last Modified: Sat, 17 Jan 2026 00:32:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f85ec7305def0a28b34b0dc0d85d34383426f6ec7852bbb5f37a8505debe2c`  
		Last Modified: Sat, 17 Jan 2026 00:32:32 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860fb2aeaaed18a9b4d34daff9ddd454eecfc15f6c9788e79c3012cfc58e11a0`  
		Last Modified: Sat, 17 Jan 2026 00:32:37 GMT  
		Size: 23.9 MB (23926291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123dcce148cf36dc3fef9dcac9bc0744e708d97e50efaac5ce4d19cd88c4643a`  
		Last Modified: Sat, 17 Jan 2026 00:32:30 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac82bd7e1e254f2f86462290e0b6f665a884852c8aa1955b982a51ba89d28a65`  
		Last Modified: Sat, 17 Jan 2026 00:32:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac11280c48513ddcab1b722f8667f5032899f18af35a191af81071ac5cdb6914`  
		Last Modified: Sat, 17 Jan 2026 00:32:30 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3022a6d86f2499b629eedda0a7d2f272c52085b6ba6ea64307eb525200beeaa8`  
		Last Modified: Sat, 17 Jan 2026 00:32:32 GMT  
		Size: 11.4 MB (11445469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c02a7770053c43d314e65b709cd4998fa6a4e8f8adace2dd551564543ce94221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:27574c8077e47eae8b561adeac8e2136d1c27bb97bfb370868963f775372c3ac
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1890962783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fac75bb46939eff0674007ab202879fd5c512d38bc3477a4ce536005f69de5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Sat, 17 Jan 2026 00:31:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 17 Jan 2026 00:31:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 17 Jan 2026 00:31:37 GMT
ENV DOCKER_VERSION=29.1.5
# Sat, 17 Jan 2026 00:31:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.5.zip
# Sat, 17 Jan 2026 00:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 17 Jan 2026 00:31:55 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Sat, 17 Jan 2026 00:31:56 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Sat, 17 Jan 2026 00:31:57 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Sat, 17 Jan 2026 00:32:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 17 Jan 2026 00:32:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Sat, 17 Jan 2026 00:32:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-windows-x86_64.exe
# Sat, 17 Jan 2026 00:32:15 GMT
ENV DOCKER_COMPOSE_SHA256=2ae341f9152b4d90f561f84b8f2e263d5b60e1613c6841c804447819290c4119
# Sat, 17 Jan 2026 00:32:25 GMT
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
	-	`sha256:b7c78b49395f890e706d473e38c35368e19c6b35bb262c64ca03e023a301e2a6`  
		Last Modified: Sat, 17 Jan 2026 00:32:35 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78ca2adb184b097e41d61db1c4e93f50645315b61438a439b40c1900f125996`  
		Last Modified: Sat, 17 Jan 2026 00:32:34 GMT  
		Size: 501.7 KB (501717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24467fa2d0304efe337e545989ba3cd2e46d51af14ad0b64773f789d3afbeec7`  
		Last Modified: Sat, 17 Jan 2026 00:32:34 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c5802fad231b2fb1a2c83745d11231a54367bf5f857c22dd7e6435fad68712`  
		Last Modified: Sat, 17 Jan 2026 00:32:34 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e8f5908d5455b3264f322cb1a1cc727a24fd8b6f17df307574c2561b3e0f90`  
		Last Modified: Sat, 17 Jan 2026 00:32:36 GMT  
		Size: 19.4 MB (19418332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356fa589200fb90532adf9bf598defe12f34d1730f728a493cc1f47019d2dc46`  
		Last Modified: Sat, 17 Jan 2026 00:32:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bca3e0930ba28041675051a18961927142d24d6613f43643112d084fe2ea54`  
		Last Modified: Sat, 17 Jan 2026 00:32:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f85ec7305def0a28b34b0dc0d85d34383426f6ec7852bbb5f37a8505debe2c`  
		Last Modified: Sat, 17 Jan 2026 00:32:32 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860fb2aeaaed18a9b4d34daff9ddd454eecfc15f6c9788e79c3012cfc58e11a0`  
		Last Modified: Sat, 17 Jan 2026 00:32:37 GMT  
		Size: 23.9 MB (23926291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123dcce148cf36dc3fef9dcac9bc0744e708d97e50efaac5ce4d19cd88c4643a`  
		Last Modified: Sat, 17 Jan 2026 00:32:30 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac82bd7e1e254f2f86462290e0b6f665a884852c8aa1955b982a51ba89d28a65`  
		Last Modified: Sat, 17 Jan 2026 00:32:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac11280c48513ddcab1b722f8667f5032899f18af35a191af81071ac5cdb6914`  
		Last Modified: Sat, 17 Jan 2026 00:32:30 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3022a6d86f2499b629eedda0a7d2f272c52085b6ba6ea64307eb525200beeaa8`  
		Last Modified: Sat, 17 Jan 2026 00:32:32 GMT  
		Size: 11.4 MB (11445469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:0810dacd6ec19cb603ba71bd78b331efb51cffc6958820a4868ff1a67764849d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:011b8de53ecb70fa60f226045aca2c69332bb6ee94d021bb9d3fcc085384a0d5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1550967984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6dccad077a318174c56c30ebe3c491c307ecc1db3239e2cd5c399177b281ef`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Fri, 16 Jan 2026 23:27:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Jan 2026 23:27:58 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Jan 2026 23:27:59 GMT
ENV DOCKER_VERSION=29.1.5
# Fri, 16 Jan 2026 23:28:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.5.zip
# Fri, 16 Jan 2026 23:28:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Jan 2026 23:28:10 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 16 Jan 2026 23:28:11 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 16 Jan 2026 23:28:11 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 16 Jan 2026 23:28:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Jan 2026 23:28:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 16 Jan 2026 23:28:20 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-windows-x86_64.exe
# Fri, 16 Jan 2026 23:28:21 GMT
ENV DOCKER_COMPOSE_SHA256=2ae341f9152b4d90f561f84b8f2e263d5b60e1613c6841c804447819290c4119
# Fri, 16 Jan 2026 23:28:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf85b52279cbf5f434afc4ab079f83bda3ef50d3486fc74a30c20f552694d85f`  
		Last Modified: Fri, 16 Jan 2026 23:28:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93445caeafc2bddea797a95857da92e939124df4d54c185f80f39445e80c0b94`  
		Last Modified: Fri, 16 Jan 2026 23:28:36 GMT  
		Size: 377.1 KB (377114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e299452bcfd7aca11225e6700bf13ba1fb4bcb19e176b8a1a14f554377c7dd2`  
		Last Modified: Fri, 16 Jan 2026 23:28:36 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4053285375a511f9c5e62aad814a3035f4e232806d8993ce9390e35ea7c757b1`  
		Last Modified: Fri, 16 Jan 2026 23:28:36 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dc97dec1a7c7fd01f0954f1b05bf600bd724c454ef5a252543bc69fd4fd00b`  
		Last Modified: Fri, 16 Jan 2026 23:28:38 GMT  
		Size: 19.4 MB (19432334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8f925ec92367d9f26dcaaf379beed54c2f51aa96dedc2c1426ee427cd71831`  
		Last Modified: Fri, 16 Jan 2026 23:28:34 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5376a23cd36fd59eb5251f2151e83a0e1a7a67013ba2b5899fba9a796e16092`  
		Last Modified: Fri, 16 Jan 2026 23:28:34 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c61331a4364799d750587d61e8cce8abf465f33de033951aefcaf07321e77d`  
		Last Modified: Fri, 16 Jan 2026 23:28:34 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b78cf75f88295cbd8090b41c814f0df5e0a6951e496caff112c42de8eac459`  
		Last Modified: Fri, 16 Jan 2026 23:28:36 GMT  
		Size: 23.9 MB (23929994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671ff8ed0c7f11b6caaf11da12b447a4a63e27b1711ecb4078f8007f675be90f`  
		Last Modified: Fri, 16 Jan 2026 23:28:32 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48250282c43183796eda8334f28230b90a9fac97a683cc4c7b9a49373dcf154e`  
		Last Modified: Fri, 16 Jan 2026 23:28:32 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07517cc4d488302c8930b5fac70a5e65f24ec3cf9a28ead9ab5dff5b3d276f0`  
		Last Modified: Fri, 16 Jan 2026 23:28:32 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4401644c9320335d7ccbf201067db845ccd52bb0dd1091a086309a20504d55`  
		Last Modified: Fri, 16 Jan 2026 23:28:34 GMT  
		Size: 11.5 MB (11456516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
