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
$ docker pull docker@sha256:07d028d0de432dfc03cdfc7caab341cdb59268ab8a8713da0ff2b69e83d2e97a
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
$ docker pull docker@sha256:9d333da203474f904de8a9015a8aa7dd57cf7caf99892310ee3385cc48f6e4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70144617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ac5d6dbc4c3b4d8e7acb45904b5c3a2abeee357c4c3e5114dc22603a8aa4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f73afb542db790cbc3066287dfef5ffd00340d0549d744479b3058343d3f2a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d63173cdff131b1d1f53e1ffa4a2fc23346cc99c4602fb586b25274874eca6`

```dockerfile
```

-	Layers:
	-	`sha256:e45b4371451b821b6cfc011796e67639ad92ee2a2efb4d7b03f36a9772f6fd71`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:a6aaabac67589f5be29664e13c38aac72c9d1a87aa0b873b7dbc53eb78c98b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66231561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65093f721bb517b6e87fa6db985093f3b19dba0f8557c722a18bc6ba44579d66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:12:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:13:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:13:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:13:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:13:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:13:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:13:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4966beab2abd2caae000b60fb3d0863d4d913fec33762bd7364c9936e5074ac`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 8.3 MB (8300913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd78c68208e09e5959e27ad40e600ec4e26cbe9858f10bb1f51efcd9a21bbe`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd85db1cd939918d85622cb20bf2d99274189c792e726ffd2feb38a4d7d61cd`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8140c036de5f8f497aae90ca8eb15e94c990291c8bb2198251ec7c81c71bb`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 26.6 MB (26570477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886a65e68d8490537f4822ea27ea88746863ed1a5d2ace64d4faf693696d5b0`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 10.2 MB (10213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f078db0ab6ca76f12b6987d5d5026527d6a8b05d961747f3c5ecbb9d460e58`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73781cde181d81e0f54a33c09b2bf4f74dda73d0dce94453867028087157732`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37fcb587067940ea9615f71ea5c3933aaf7887e71145ee736b999e66fc0c9`  
		Last Modified: Mon, 26 Jan 2026 22:13:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8e5c2977bc934a3402e72c37d4da9ad9cc93282435325f6596a3dfc858d351ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889186a6411e34f41e497ec55989e167d604a786e5f078107b36f92be0f1f47`

```dockerfile
```

-	Layers:
	-	`sha256:00b2c351101d169f3825a7b9d06bb40848a53f0d38c280a03c406bf642822284`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:2906512e82e006c385a4c4035af6680723426b4890935df8edc2f70bfa51034e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65189107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b4ec537c5044c40ee13734527bee2e291f86df60d792f11a7efeef5e0de517`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:09 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94cbbc20fd91588dd30d74cfc754e7f05c5a36e108e1b125d70cec6a75a254`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 7.6 MB (7597838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127fef2fb317852c25ef2d8175bb51a59e940787773222711ed84e9189774ff`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69850ac721aa9551589a83d36a207ea1b058267df549623221bdaeeaada2564`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 17.6 MB (17566466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc35ae9e8007289b4e0223b822025b9dc54a014b2d48083430e30f9be22a85`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 26.5 MB (26544670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d42e35e578117d06f8467a552017c29ad760872c70202779822ad5b47cb75`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 10.2 MB (10198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3232c78866f7ae82c173bdc5453e7571947578407f3cc193b0c5ec0fcc5fd6d`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794570663f9815d417e299bfc17f4261e57cd03285bd7bda017f79762e415ec0`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2ca54c5fd06bbde148a55ffb3fa162c862964e506218b0ad8f15a90ec005b`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a6ba1f4f7ea9b7d929144e488e1a3523320cba01e87a88195e7c562ba63565d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a90f4218f89ea32f378f7b13cdf5021417832ca66bb0bdb04b203a8e8ab568`

```dockerfile
```

-	Layers:
	-	`sha256:1820363c8615c6f091892572afb4755d72bd05c6ceafa2601868532aa5f8f59c`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:cd79225fd3b3bf72f8a9a8d310c021ff7012a5b54507b5769b1472e36c4fe70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65495561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27d0bb175154e2843d9954373055aea0e2b8c3846e0ad78fdb93bb1aec1805a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:beb44f5ded469261e57af335e8a2969ea2bbe533cb5ec6f31249058b1ec75b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612c3e3dd1b3e38ac4c39b08acc9f7ddaa3272a044d17079d9d234b4d205c2b7`

```dockerfile
```

-	Layers:
	-	`sha256:a0da1a0a490a5427e3e9ba4fbc85eab9912e473371c2360f67fb55702a30ce8b`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 38.3 KB (38255 bytes)  
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
$ docker pull docker@sha256:4f709cae1db898fd1ad6745f38c5e6d8ffec6e83cb8cc00d76f82fbd247675a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
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
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d163e49cad2b2f09e09d69f17ef3d97ae1ebbec30211ab2f8874adaba30d6211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
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
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b85a08b05795eb199c7a7fcc2b26612f7151d883c3cf1390d624fbf330a1789b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.2-cli`

```console
$ docker pull docker@sha256:07d028d0de432dfc03cdfc7caab341cdb59268ab8a8713da0ff2b69e83d2e97a
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
$ docker pull docker@sha256:9d333da203474f904de8a9015a8aa7dd57cf7caf99892310ee3385cc48f6e4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70144617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ac5d6dbc4c3b4d8e7acb45904b5c3a2abeee357c4c3e5114dc22603a8aa4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f73afb542db790cbc3066287dfef5ffd00340d0549d744479b3058343d3f2a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d63173cdff131b1d1f53e1ffa4a2fc23346cc99c4602fb586b25274874eca6`

```dockerfile
```

-	Layers:
	-	`sha256:e45b4371451b821b6cfc011796e67639ad92ee2a2efb4d7b03f36a9772f6fd71`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:a6aaabac67589f5be29664e13c38aac72c9d1a87aa0b873b7dbc53eb78c98b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66231561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65093f721bb517b6e87fa6db985093f3b19dba0f8557c722a18bc6ba44579d66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:12:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:13:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:13:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:13:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:13:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:13:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:13:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4966beab2abd2caae000b60fb3d0863d4d913fec33762bd7364c9936e5074ac`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 8.3 MB (8300913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd78c68208e09e5959e27ad40e600ec4e26cbe9858f10bb1f51efcd9a21bbe`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd85db1cd939918d85622cb20bf2d99274189c792e726ffd2feb38a4d7d61cd`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8140c036de5f8f497aae90ca8eb15e94c990291c8bb2198251ec7c81c71bb`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 26.6 MB (26570477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886a65e68d8490537f4822ea27ea88746863ed1a5d2ace64d4faf693696d5b0`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 10.2 MB (10213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f078db0ab6ca76f12b6987d5d5026527d6a8b05d961747f3c5ecbb9d460e58`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73781cde181d81e0f54a33c09b2bf4f74dda73d0dce94453867028087157732`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37fcb587067940ea9615f71ea5c3933aaf7887e71145ee736b999e66fc0c9`  
		Last Modified: Mon, 26 Jan 2026 22:13:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8e5c2977bc934a3402e72c37d4da9ad9cc93282435325f6596a3dfc858d351ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889186a6411e34f41e497ec55989e167d604a786e5f078107b36f92be0f1f47`

```dockerfile
```

-	Layers:
	-	`sha256:00b2c351101d169f3825a7b9d06bb40848a53f0d38c280a03c406bf642822284`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:2906512e82e006c385a4c4035af6680723426b4890935df8edc2f70bfa51034e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65189107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b4ec537c5044c40ee13734527bee2e291f86df60d792f11a7efeef5e0de517`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:09 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94cbbc20fd91588dd30d74cfc754e7f05c5a36e108e1b125d70cec6a75a254`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 7.6 MB (7597838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127fef2fb317852c25ef2d8175bb51a59e940787773222711ed84e9189774ff`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69850ac721aa9551589a83d36a207ea1b058267df549623221bdaeeaada2564`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 17.6 MB (17566466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc35ae9e8007289b4e0223b822025b9dc54a014b2d48083430e30f9be22a85`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 26.5 MB (26544670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d42e35e578117d06f8467a552017c29ad760872c70202779822ad5b47cb75`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 10.2 MB (10198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3232c78866f7ae82c173bdc5453e7571947578407f3cc193b0c5ec0fcc5fd6d`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794570663f9815d417e299bfc17f4261e57cd03285bd7bda017f79762e415ec0`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2ca54c5fd06bbde148a55ffb3fa162c862964e506218b0ad8f15a90ec005b`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a6ba1f4f7ea9b7d929144e488e1a3523320cba01e87a88195e7c562ba63565d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a90f4218f89ea32f378f7b13cdf5021417832ca66bb0bdb04b203a8e8ab568`

```dockerfile
```

-	Layers:
	-	`sha256:1820363c8615c6f091892572afb4755d72bd05c6ceafa2601868532aa5f8f59c`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:cd79225fd3b3bf72f8a9a8d310c021ff7012a5b54507b5769b1472e36c4fe70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65495561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27d0bb175154e2843d9954373055aea0e2b8c3846e0ad78fdb93bb1aec1805a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:beb44f5ded469261e57af335e8a2969ea2bbe533cb5ec6f31249058b1ec75b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612c3e3dd1b3e38ac4c39b08acc9f7ddaa3272a044d17079d9d234b4d205c2b7`

```dockerfile
```

-	Layers:
	-	`sha256:a0da1a0a490a5427e3e9ba4fbc85eab9912e473371c2360f67fb55702a30ce8b`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 38.3 KB (38255 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2-dind`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.2-dind-rootless`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.2-windowsservercore`

```console
$ docker pull docker@sha256:4f709cae1db898fd1ad6745f38c5e6d8ffec6e83cb8cc00d76f82fbd247675a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:29.2-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.2-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
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
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d163e49cad2b2f09e09d69f17ef3d97ae1ebbec30211ab2f8874adaba30d6211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:29.2-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
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
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b85a08b05795eb199c7a7fcc2b26612f7151d883c3cf1390d624fbf330a1789b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:29.2-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2.0`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.2.0-alpine3.23`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.2.0-cli`

```console
$ docker pull docker@sha256:07d028d0de432dfc03cdfc7caab341cdb59268ab8a8713da0ff2b69e83d2e97a
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

### `docker:29.2.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:9d333da203474f904de8a9015a8aa7dd57cf7caf99892310ee3385cc48f6e4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70144617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ac5d6dbc4c3b4d8e7acb45904b5c3a2abeee357c4c3e5114dc22603a8aa4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f73afb542db790cbc3066287dfef5ffd00340d0549d744479b3058343d3f2a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d63173cdff131b1d1f53e1ffa4a2fc23346cc99c4602fb586b25274874eca6`

```dockerfile
```

-	Layers:
	-	`sha256:e45b4371451b821b6cfc011796e67639ad92ee2a2efb4d7b03f36a9772f6fd71`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:a6aaabac67589f5be29664e13c38aac72c9d1a87aa0b873b7dbc53eb78c98b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66231561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65093f721bb517b6e87fa6db985093f3b19dba0f8557c722a18bc6ba44579d66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:12:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:13:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:13:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:13:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:13:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:13:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:13:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4966beab2abd2caae000b60fb3d0863d4d913fec33762bd7364c9936e5074ac`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 8.3 MB (8300913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd78c68208e09e5959e27ad40e600ec4e26cbe9858f10bb1f51efcd9a21bbe`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd85db1cd939918d85622cb20bf2d99274189c792e726ffd2feb38a4d7d61cd`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8140c036de5f8f497aae90ca8eb15e94c990291c8bb2198251ec7c81c71bb`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 26.6 MB (26570477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886a65e68d8490537f4822ea27ea88746863ed1a5d2ace64d4faf693696d5b0`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 10.2 MB (10213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f078db0ab6ca76f12b6987d5d5026527d6a8b05d961747f3c5ecbb9d460e58`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73781cde181d81e0f54a33c09b2bf4f74dda73d0dce94453867028087157732`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37fcb587067940ea9615f71ea5c3933aaf7887e71145ee736b999e66fc0c9`  
		Last Modified: Mon, 26 Jan 2026 22:13:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8e5c2977bc934a3402e72c37d4da9ad9cc93282435325f6596a3dfc858d351ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889186a6411e34f41e497ec55989e167d604a786e5f078107b36f92be0f1f47`

```dockerfile
```

-	Layers:
	-	`sha256:00b2c351101d169f3825a7b9d06bb40848a53f0d38c280a03c406bf642822284`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:2906512e82e006c385a4c4035af6680723426b4890935df8edc2f70bfa51034e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65189107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b4ec537c5044c40ee13734527bee2e291f86df60d792f11a7efeef5e0de517`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:09 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94cbbc20fd91588dd30d74cfc754e7f05c5a36e108e1b125d70cec6a75a254`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 7.6 MB (7597838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127fef2fb317852c25ef2d8175bb51a59e940787773222711ed84e9189774ff`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69850ac721aa9551589a83d36a207ea1b058267df549623221bdaeeaada2564`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 17.6 MB (17566466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc35ae9e8007289b4e0223b822025b9dc54a014b2d48083430e30f9be22a85`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 26.5 MB (26544670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d42e35e578117d06f8467a552017c29ad760872c70202779822ad5b47cb75`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 10.2 MB (10198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3232c78866f7ae82c173bdc5453e7571947578407f3cc193b0c5ec0fcc5fd6d`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794570663f9815d417e299bfc17f4261e57cd03285bd7bda017f79762e415ec0`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2ca54c5fd06bbde148a55ffb3fa162c862964e506218b0ad8f15a90ec005b`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a6ba1f4f7ea9b7d929144e488e1a3523320cba01e87a88195e7c562ba63565d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a90f4218f89ea32f378f7b13cdf5021417832ca66bb0bdb04b203a8e8ab568`

```dockerfile
```

-	Layers:
	-	`sha256:1820363c8615c6f091892572afb4755d72bd05c6ceafa2601868532aa5f8f59c`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:cd79225fd3b3bf72f8a9a8d310c021ff7012a5b54507b5769b1472e36c4fe70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65495561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27d0bb175154e2843d9954373055aea0e2b8c3846e0ad78fdb93bb1aec1805a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:beb44f5ded469261e57af335e8a2969ea2bbe533cb5ec6f31249058b1ec75b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612c3e3dd1b3e38ac4c39b08acc9f7ddaa3272a044d17079d9d234b4d205c2b7`

```dockerfile
```

-	Layers:
	-	`sha256:a0da1a0a490a5427e3e9ba4fbc85eab9912e473371c2360f67fb55702a30ce8b`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 38.3 KB (38255 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.0-cli-alpine3.23`

```console
$ docker pull docker@sha256:07d028d0de432dfc03cdfc7caab341cdb59268ab8a8713da0ff2b69e83d2e97a
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

### `docker:29.2.0-cli-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:9d333da203474f904de8a9015a8aa7dd57cf7caf99892310ee3385cc48f6e4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70144617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ac5d6dbc4c3b4d8e7acb45904b5c3a2abeee357c4c3e5114dc22603a8aa4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:f73afb542db790cbc3066287dfef5ffd00340d0549d744479b3058343d3f2a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d63173cdff131b1d1f53e1ffa4a2fc23346cc99c4602fb586b25274874eca6`

```dockerfile
```

-	Layers:
	-	`sha256:e45b4371451b821b6cfc011796e67639ad92ee2a2efb4d7b03f36a9772f6fd71`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-cli-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:a6aaabac67589f5be29664e13c38aac72c9d1a87aa0b873b7dbc53eb78c98b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66231561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65093f721bb517b6e87fa6db985093f3b19dba0f8557c722a18bc6ba44579d66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:12:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:13:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:13:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:13:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:13:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:13:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:13:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4966beab2abd2caae000b60fb3d0863d4d913fec33762bd7364c9936e5074ac`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 8.3 MB (8300913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd78c68208e09e5959e27ad40e600ec4e26cbe9858f10bb1f51efcd9a21bbe`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd85db1cd939918d85622cb20bf2d99274189c792e726ffd2feb38a4d7d61cd`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8140c036de5f8f497aae90ca8eb15e94c990291c8bb2198251ec7c81c71bb`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 26.6 MB (26570477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886a65e68d8490537f4822ea27ea88746863ed1a5d2ace64d4faf693696d5b0`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 10.2 MB (10213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f078db0ab6ca76f12b6987d5d5026527d6a8b05d961747f3c5ecbb9d460e58`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73781cde181d81e0f54a33c09b2bf4f74dda73d0dce94453867028087157732`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37fcb587067940ea9615f71ea5c3933aaf7887e71145ee736b999e66fc0c9`  
		Last Modified: Mon, 26 Jan 2026 22:13:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:8e5c2977bc934a3402e72c37d4da9ad9cc93282435325f6596a3dfc858d351ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889186a6411e34f41e497ec55989e167d604a786e5f078107b36f92be0f1f47`

```dockerfile
```

-	Layers:
	-	`sha256:00b2c351101d169f3825a7b9d06bb40848a53f0d38c280a03c406bf642822284`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-cli-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:2906512e82e006c385a4c4035af6680723426b4890935df8edc2f70bfa51034e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65189107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b4ec537c5044c40ee13734527bee2e291f86df60d792f11a7efeef5e0de517`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:09 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94cbbc20fd91588dd30d74cfc754e7f05c5a36e108e1b125d70cec6a75a254`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 7.6 MB (7597838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127fef2fb317852c25ef2d8175bb51a59e940787773222711ed84e9189774ff`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69850ac721aa9551589a83d36a207ea1b058267df549623221bdaeeaada2564`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 17.6 MB (17566466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc35ae9e8007289b4e0223b822025b9dc54a014b2d48083430e30f9be22a85`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 26.5 MB (26544670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d42e35e578117d06f8467a552017c29ad760872c70202779822ad5b47cb75`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 10.2 MB (10198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3232c78866f7ae82c173bdc5453e7571947578407f3cc193b0c5ec0fcc5fd6d`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794570663f9815d417e299bfc17f4261e57cd03285bd7bda017f79762e415ec0`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2ca54c5fd06bbde148a55ffb3fa162c862964e506218b0ad8f15a90ec005b`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:a6ba1f4f7ea9b7d929144e488e1a3523320cba01e87a88195e7c562ba63565d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a90f4218f89ea32f378f7b13cdf5021417832ca66bb0bdb04b203a8e8ab568`

```dockerfile
```

-	Layers:
	-	`sha256:1820363c8615c6f091892572afb4755d72bd05c6ceafa2601868532aa5f8f59c`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.0-cli-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:cd79225fd3b3bf72f8a9a8d310c021ff7012a5b54507b5769b1472e36c4fe70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65495561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27d0bb175154e2843d9954373055aea0e2b8c3846e0ad78fdb93bb1aec1805a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.0-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:beb44f5ded469261e57af335e8a2969ea2bbe533cb5ec6f31249058b1ec75b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612c3e3dd1b3e38ac4c39b08acc9f7ddaa3272a044d17079d9d234b4d205c2b7`

```dockerfile
```

-	Layers:
	-	`sha256:a0da1a0a490a5427e3e9ba4fbc85eab9912e473371c2360f67fb55702a30ce8b`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 38.3 KB (38255 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.0-dind`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.2.0-dind-alpine3.23`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.2.0-dind-rootless`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.2.0-windowsservercore`

```console
$ docker pull docker@sha256:4f709cae1db898fd1ad6745f38c5e6d8ffec6e83cb8cc00d76f82fbd247675a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:29.2.0-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.2.0-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
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
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d163e49cad2b2f09e09d69f17ef3d97ae1ebbec30211ab2f8874adaba30d6211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:29.2.0-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
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
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b85a08b05795eb199c7a7fcc2b26612f7151d883c3cf1390d624fbf330a1789b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:29.2.0-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:07d028d0de432dfc03cdfc7caab341cdb59268ab8a8713da0ff2b69e83d2e97a
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
$ docker pull docker@sha256:9d333da203474f904de8a9015a8aa7dd57cf7caf99892310ee3385cc48f6e4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70144617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760ac5d6dbc4c3b4d8e7acb45904b5c3a2abeee357c4c3e5114dc22603a8aa4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:f73afb542db790cbc3066287dfef5ffd00340d0549d744479b3058343d3f2a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d63173cdff131b1d1f53e1ffa4a2fc23346cc99c4602fb586b25274874eca6`

```dockerfile
```

-	Layers:
	-	`sha256:e45b4371451b821b6cfc011796e67639ad92ee2a2efb4d7b03f36a9772f6fd71`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:a6aaabac67589f5be29664e13c38aac72c9d1a87aa0b873b7dbc53eb78c98b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66231561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65093f721bb517b6e87fa6db985093f3b19dba0f8557c722a18bc6ba44579d66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:12:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:12:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:13:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:13:00 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:13:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:13:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:13:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:13:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:13:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4966beab2abd2caae000b60fb3d0863d4d913fec33762bd7364c9936e5074ac`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 8.3 MB (8300913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd78c68208e09e5959e27ad40e600ec4e26cbe9858f10bb1f51efcd9a21bbe`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd85db1cd939918d85622cb20bf2d99274189c792e726ffd2feb38a4d7d61cd`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8140c036de5f8f497aae90ca8eb15e94c990291c8bb2198251ec7c81c71bb`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 26.6 MB (26570477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886a65e68d8490537f4822ea27ea88746863ed1a5d2ace64d4faf693696d5b0`  
		Last Modified: Mon, 26 Jan 2026 22:13:12 GMT  
		Size: 10.2 MB (10213045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f078db0ab6ca76f12b6987d5d5026527d6a8b05d961747f3c5ecbb9d460e58`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73781cde181d81e0f54a33c09b2bf4f74dda73d0dce94453867028087157732`  
		Last Modified: Mon, 26 Jan 2026 22:13:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37fcb587067940ea9615f71ea5c3933aaf7887e71145ee736b999e66fc0c9`  
		Last Modified: Mon, 26 Jan 2026 22:13:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:8e5c2977bc934a3402e72c37d4da9ad9cc93282435325f6596a3dfc858d351ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889186a6411e34f41e497ec55989e167d604a786e5f078107b36f92be0f1f47`

```dockerfile
```

-	Layers:
	-	`sha256:00b2c351101d169f3825a7b9d06bb40848a53f0d38c280a03c406bf642822284`  
		Last Modified: Mon, 26 Jan 2026 22:13:11 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:2906512e82e006c385a4c4035af6680723426b4890935df8edc2f70bfa51034e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65189107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b4ec537c5044c40ee13734527bee2e291f86df60d792f11a7efeef5e0de517`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:04 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:09 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94cbbc20fd91588dd30d74cfc754e7f05c5a36e108e1b125d70cec6a75a254`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 7.6 MB (7597838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127fef2fb317852c25ef2d8175bb51a59e940787773222711ed84e9189774ff`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69850ac721aa9551589a83d36a207ea1b058267df549623221bdaeeaada2564`  
		Last Modified: Mon, 26 Jan 2026 22:15:16 GMT  
		Size: 17.6 MB (17566466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc35ae9e8007289b4e0223b822025b9dc54a014b2d48083430e30f9be22a85`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 26.5 MB (26544670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d42e35e578117d06f8467a552017c29ad760872c70202779822ad5b47cb75`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 10.2 MB (10198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3232c78866f7ae82c173bdc5453e7571947578407f3cc193b0c5ec0fcc5fd6d`  
		Last Modified: Mon, 26 Jan 2026 22:15:17 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794570663f9815d417e299bfc17f4261e57cd03285bd7bda017f79762e415ec0`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2ca54c5fd06bbde148a55ffb3fa162c862964e506218b0ad8f15a90ec005b`  
		Last Modified: Mon, 26 Jan 2026 22:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:a6ba1f4f7ea9b7d929144e488e1a3523320cba01e87a88195e7c562ba63565d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a90f4218f89ea32f378f7b13cdf5021417832ca66bb0bdb04b203a8e8ab568`

```dockerfile
```

-	Layers:
	-	`sha256:1820363c8615c6f091892572afb4755d72bd05c6ceafa2601868532aa5f8f59c`  
		Last Modified: Mon, 26 Jan 2026 22:15:15 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:cd79225fd3b3bf72f8a9a8d310c021ff7012a5b54507b5769b1472e36c4fe70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65495561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27d0bb175154e2843d9954373055aea0e2b8c3846e0ad78fdb93bb1aec1805a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:beb44f5ded469261e57af335e8a2969ea2bbe533cb5ec6f31249058b1ec75b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612c3e3dd1b3e38ac4c39b08acc9f7ddaa3272a044d17079d9d234b4d205c2b7`

```dockerfile
```

-	Layers:
	-	`sha256:a0da1a0a490a5427e3e9ba4fbc85eab9912e473371c2360f67fb55702a30ce8b`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 38.3 KB (38255 bytes)  
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
$ docker pull docker@sha256:4f709cae1db898fd1ad6745f38c5e6d8ffec6e83cb8cc00d76f82fbd247675a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
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
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d163e49cad2b2f09e09d69f17ef3d97ae1ebbec30211ab2f8874adaba30d6211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:d9f67e7e5cd236a9dd358a82eb5e1d4a86c36c1127c5f662a397f750cc5a3991
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896470404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8cffde6f0ba12542877a301342f6a8ac781dcebbdaa1ad5fd855e29c942cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Mon, 26 Jan 2026 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:56 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:06 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:07 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:24 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:39 GMT
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
	-	`sha256:706868eff489519530c458854b9414f97d7a8f5e9b774b69feb22ba4c885cd22`  
		Last Modified: Mon, 26 Jan 2026 22:10:28 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d55c8c93a0d982adfcaaf14568d692fe78f0bb461c1d8ad5fa15ff6f002e4`  
		Last Modified: Mon, 26 Jan 2026 22:24:48 GMT  
		Size: 495.2 KB (495238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a604e5ee429b56a01a1a37082b04204cc7e962ffdcf44264af93684d77833f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707319ff752c0e27e78c11ed06f0a93650eb6a1129b722daa50696b4b14d364f`  
		Last Modified: Mon, 26 Jan 2026 22:24:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e7ff0c488e4ce506ec0629b4368d54f4e941ebc1079c923c1b3ef26606f29`  
		Last Modified: Mon, 26 Jan 2026 22:24:49 GMT  
		Size: 19.4 MB (19435389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c5dfbd4028e1c4326f5eef4a441e04e070858443ad1cdfcd88f08da6c5740`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140aeaec72dba11754bb05df58fd786bbdee26cef57fe9f4a20a633c869a27c9`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd88e91cf8993d8ce9c69d02075aae7876002f5cd0a7bfa1e72d7ed1a8bb51f`  
		Last Modified: Mon, 26 Jan 2026 22:24:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896ef4b01ac64a8672aa34e9a3527823638dc9cacab2505244be06f2677b18c`  
		Last Modified: Mon, 26 Jan 2026 22:24:53 GMT  
		Size: 29.4 MB (29417628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b2c614d8f1f7c837f917642a8969cfa3ce9d592986d2b53b629c76c59a5dce`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaac2d59ab8b20586d5742390ab93004e42f58e35baaa0c4ce16106b7164ee1`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283f0b1e6e8ca6ea61699785162534c6880740c92c6d913807dcc2b6f641eb86`  
		Last Modified: Mon, 26 Jan 2026 22:24:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8321caa5769068a876d874e103d7e6c9d677fd6a90f5f69fe88da97e744d52b3`  
		Last Modified: Mon, 26 Jan 2026 22:24:46 GMT  
		Size: 11.5 MB (11451087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b85a08b05795eb199c7a7fcc2b26612f7151d883c3cf1390d624fbf330a1789b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:0b318f6fc03c6c4758cf9a3593677f49bc27806829ec1e65e8dee4695d49ba4f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556585400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3a87dfd681ad20bf8dc920ab30df2258bd3561f68bae3c8ab0e2780e9eb26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 22:07:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 26 Jan 2026 22:23:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 26 Jan 2026 22:23:53 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:23:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.0.zip
# Mon, 26 Jan 2026 22:24:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:24:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.windows-amd64.exe
# Mon, 26 Jan 2026 22:24:04 GMT
ENV DOCKER_BUILDX_SHA256=4718e18d07e96b87c21ad7a025d21ac1b5d2caf91448c864623dbd2f778fd192
# Mon, 26 Jan 2026 22:24:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 26 Jan 2026 22:24:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Mon, 26 Jan 2026 22:24:16 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Mon, 26 Jan 2026 22:24:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7c13b860fb95a9e6b04f473cc620e339ddf344435efac5f981943dfcdb708`  
		Last Modified: Mon, 26 Jan 2026 22:09:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8ea446c36f3ed413f6186e57c762b8dabe380d982d5f0426896a088fe2083`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 427.0 KB (426991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73a1b685ec756031cc68b4115f951566358cd8c34293e94c48cd3bc6d52b8c6`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6cee5d48b635466bfff2d8e45d111a265500b165808230289b16fa5e37eb53`  
		Last Modified: Mon, 26 Jan 2026 22:24:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67932a54b27ad915455543dfcafec3ea65fc7b5ea74bcdbdea22d187c7215c1c`  
		Last Modified: Mon, 26 Jan 2026 22:24:32 GMT  
		Size: 19.5 MB (19464188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63623139ffd2c2fc15fee8ded8fb73e593e790839e6acc6d2c77f29390cc52a`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e57b3805eb4c9713f5e74b5e309326a127044efbc5ceeb8db1bf5d8f4a07612`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b07431e45bc52f09d2d4f89cef4842cce858aafe7a8a0b60041af67206cba5`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45915a3406e8473ac9311ff452bd390524d12707c1e16378222070a9da3e7412`  
		Last Modified: Mon, 26 Jan 2026 22:24:30 GMT  
		Size: 29.4 MB (29440300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe657ac3f7f882a8397b5b8fa234bd5735901f4eafa80082971015df5dd890`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6abe219ab650172bc70725366a9b6db9944f527b396255518aaa9e98e98b356`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd575efc855d764371e7c425811be63844916b0c9ad5694223b692bddac35f9`  
		Last Modified: Mon, 26 Jan 2026 22:24:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457e1d780445906abcfe2e0053bc50693133fdbfaf2213465b60a9617faaa5b`  
		Last Modified: Mon, 26 Jan 2026 22:24:28 GMT  
		Size: 11.5 MB (11481877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
