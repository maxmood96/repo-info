<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:23`](#docker23)
-	[`docker:23-cli`](#docker23-cli)
-	[`docker:23-dind`](#docker23-dind)
-	[`docker:23-dind-rootless`](#docker23-dind-rootless)
-	[`docker:23-git`](#docker23-git)
-	[`docker:23-windowsservercore`](#docker23-windowsservercore)
-	[`docker:23-windowsservercore-1809`](#docker23-windowsservercore-1809)
-	[`docker:23-windowsservercore-ltsc2022`](#docker23-windowsservercore-ltsc2022)
-	[`docker:23.0`](#docker230)
-	[`docker:23.0-cli`](#docker230-cli)
-	[`docker:23.0-dind`](#docker230-dind)
-	[`docker:23.0-dind-rootless`](#docker230-dind-rootless)
-	[`docker:23.0-git`](#docker230-git)
-	[`docker:23.0-windowsservercore`](#docker230-windowsservercore)
-	[`docker:23.0-windowsservercore-1809`](#docker230-windowsservercore-1809)
-	[`docker:23.0-windowsservercore-ltsc2022`](#docker230-windowsservercore-ltsc2022)
-	[`docker:23.0.6`](#docker2306)
-	[`docker:23.0.6-alpine3.18`](#docker2306-alpine318)
-	[`docker:23.0.6-cli`](#docker2306-cli)
-	[`docker:23.0.6-cli-alpine3.18`](#docker2306-cli-alpine318)
-	[`docker:23.0.6-dind`](#docker2306-dind)
-	[`docker:23.0.6-dind-alpine3.18`](#docker2306-dind-alpine318)
-	[`docker:23.0.6-dind-rootless`](#docker2306-dind-rootless)
-	[`docker:23.0.6-git`](#docker2306-git)
-	[`docker:23.0.6-windowsservercore`](#docker2306-windowsservercore)
-	[`docker:23.0.6-windowsservercore-1809`](#docker2306-windowsservercore-1809)
-	[`docker:23.0.6-windowsservercore-ltsc2022`](#docker2306-windowsservercore-ltsc2022)
-	[`docker:24`](#docker24)
-	[`docker:24-cli`](#docker24-cli)
-	[`docker:24-dind`](#docker24-dind)
-	[`docker:24-dind-rootless`](#docker24-dind-rootless)
-	[`docker:24-git`](#docker24-git)
-	[`docker:24-windowsservercore`](#docker24-windowsservercore)
-	[`docker:24-windowsservercore-1809`](#docker24-windowsservercore-1809)
-	[`docker:24-windowsservercore-ltsc2022`](#docker24-windowsservercore-ltsc2022)
-	[`docker:24.0`](#docker240)
-	[`docker:24.0-cli`](#docker240-cli)
-	[`docker:24.0-dind`](#docker240-dind)
-	[`docker:24.0-dind-rootless`](#docker240-dind-rootless)
-	[`docker:24.0-git`](#docker240-git)
-	[`docker:24.0-windowsservercore`](#docker240-windowsservercore)
-	[`docker:24.0-windowsservercore-1809`](#docker240-windowsservercore-1809)
-	[`docker:24.0-windowsservercore-ltsc2022`](#docker240-windowsservercore-ltsc2022)
-	[`docker:24.0.4`](#docker2404)
-	[`docker:24.0.4-alpine3.18`](#docker2404-alpine318)
-	[`docker:24.0.4-cli`](#docker2404-cli)
-	[`docker:24.0.4-cli-alpine3.18`](#docker2404-cli-alpine318)
-	[`docker:24.0.4-dind`](#docker2404-dind)
-	[`docker:24.0.4-dind-alpine3.18`](#docker2404-dind-alpine318)
-	[`docker:24.0.4-dind-rootless`](#docker2404-dind-rootless)
-	[`docker:24.0.4-git`](#docker2404-git)
-	[`docker:24.0.4-windowsservercore`](#docker2404-windowsservercore)
-	[`docker:24.0.4-windowsservercore-1809`](#docker2404-windowsservercore-1809)
-	[`docker:24.0.4-windowsservercore-ltsc2022`](#docker2404-windowsservercore-ltsc2022)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:git`](#dockergit)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)

## `docker:23`

```console
$ docker pull docker@sha256:744ae25d20431b9eccf9832fae189e43e06054b666df039b5552a46433cbe499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23` - linux; amd64

```console
$ docker pull docker@sha256:2d036f72fa2728ddd599238453528ad1e9f4a0609ab3371f69b90fcce188b6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115841865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810c2eb4df26b8c6cb07ee900ebd168d0142553f630d7088036fc7a9cfa4d227`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbbfe9c78c82698902d2f699f3a866996d040be1686dd10f629e37d89ea33ee`  
		Last Modified: Thu, 15 Jun 2023 05:28:31 GMT  
		Size: 16.3 MB (16250874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5708dec9aea531c023a63cb6d674e4e42d94d8d84f51fcb66e9ced1c260f9e8e`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65b66e2e2892b010a1e320cecb6edff9ba98ee75b8f29eef076c7283e7a304a`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 18.0 MB (17980092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb3e3c468fa108bf2f2fec6fe9280189753b2b7ee37469941e8a688e93d499`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436c2e539760ae39be8e540fcaa7b1d1bd2fb877e8d36435eda4696d8671cea3`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed4165006f30d0eaeedeff7a3519a447de7a7f04408360003f349d6eac00de`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0c3925a01970b8b6f4b30c4ae0394f4200f55cdf177c877ae2168802ac1af1`  
		Last Modified: Thu, 06 Jul 2023 20:22:44 GMT  
		Size: 7.1 MB (7080604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd90aaca53b9d97ecf639fdb1778a1b1916e3147ff0a2ac84d6b147d1716d9ea`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce803b02ed3e4ed43bd7c6ab9ba5562ccecbe574b1d6e06252d1475cd28b9e8`  
		Last Modified: Thu, 06 Jul 2023 20:22:50 GMT  
		Size: 51.7 MB (51657476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe710e1a3eab28e7bc6596ef135bba1ed104de7cd599ed563fcbee8eee777f9`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8189afb935336899691d8ca85748fd24ec7045a0f1d9ccad361e14df8e84f61b`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 2.8 KB (2790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7a17e1adde579f7913a1d5dd4411094f9becfb0320db66d280a26a09b7eb9c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107103059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e2bc332c22f7586e25665430021c48e8bf8f10c1e9ec574a05034a99fb50b8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51d2d067e69a1f5a948d2d1133441f75a192e5bcc4154ca7be51943ff4a24d5`  
		Last Modified: Wed, 14 Jun 2023 22:42:12 GMT  
		Size: 15.3 MB (15325099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f28a2d02144ee951238b5623115d8fe18645df105f9e258b004975a591788`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 15.8 MB (15759517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc821c9da813150074e2cdd9b1099f1ea4305b04232851161a942a0cff4ab7`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 16.3 MB (16312968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b312f8beda3531c97f8edbf8ba090359914ca1508325250ff3262cd64f386635`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212d8b0184b5e16c4fd2f221bbdac88bbec8f94f632ff8ae1997332cf161ef37`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa6cbfc4ca5d773f84f56574cc994db7b86481df32126e0f0b9bcc8e7a33f87`  
		Last Modified: Thu, 06 Jul 2023 19:43:50 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b5774c046c118941ffdd7940de95e7371426fed92f8f27cb2587d4dddcc2c2`  
		Last Modified: Thu, 06 Jul 2023 19:44:05 GMT  
		Size: 7.3 MB (7291362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accf38e0a7857aa4882234dae62ba6cc1ecf9a987234b2eb10476cbc56cd701b`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fe37bb22c274be66fca87ae65085ab0a4b07ec499f6c8da99e0687d8dea17e`  
		Last Modified: Thu, 06 Jul 2023 19:44:09 GMT  
		Size: 47.1 MB (47053345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acd2d702cadc0b2a4f3272301e99216dbbfca7534826bf448015df6463954df`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53635b71f6ec66afb091ea2ae377ba957cfa8e4b8c0e4ff8d41bb157cc33d5b5`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-cli`

```console
$ docker pull docker@sha256:f233d64cf3968d36c794b0354dde961256cccca2e3e4ebd51eaff3b15caf8fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23-cli` - linux; amd64

```console
$ docker pull docker@sha256:3ead83ab52c1d056fd65655d97797494b34383a6e062b80976f80f1691db62e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57098627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af26fe8bcb5b1a2b8e6b185d9a8fd75d932b97c1faa729bca3a932af8b1271f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbbfe9c78c82698902d2f699f3a866996d040be1686dd10f629e37d89ea33ee`  
		Last Modified: Thu, 15 Jun 2023 05:28:31 GMT  
		Size: 16.3 MB (16250874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5708dec9aea531c023a63cb6d674e4e42d94d8d84f51fcb66e9ced1c260f9e8e`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65b66e2e2892b010a1e320cecb6edff9ba98ee75b8f29eef076c7283e7a304a`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 18.0 MB (17980092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb3e3c468fa108bf2f2fec6fe9280189753b2b7ee37469941e8a688e93d499`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436c2e539760ae39be8e540fcaa7b1d1bd2fb877e8d36435eda4696d8671cea3`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed4165006f30d0eaeedeff7a3519a447de7a7f04408360003f349d6eac00de`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d39267d642857eadb6106a70304967b2e7b9c71e31bf722e55ca2d107aa84bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52753194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0660417e68d2e9295da7a725dcde7983a789e8dca5dd992d3c4bdc52b19d908`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51d2d067e69a1f5a948d2d1133441f75a192e5bcc4154ca7be51943ff4a24d5`  
		Last Modified: Wed, 14 Jun 2023 22:42:12 GMT  
		Size: 15.3 MB (15325099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f28a2d02144ee951238b5623115d8fe18645df105f9e258b004975a591788`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 15.8 MB (15759517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc821c9da813150074e2cdd9b1099f1ea4305b04232851161a942a0cff4ab7`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 16.3 MB (16312968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b312f8beda3531c97f8edbf8ba090359914ca1508325250ff3262cd64f386635`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212d8b0184b5e16c4fd2f221bbdac88bbec8f94f632ff8ae1997332cf161ef37`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa6cbfc4ca5d773f84f56574cc994db7b86481df32126e0f0b9bcc8e7a33f87`  
		Last Modified: Thu, 06 Jul 2023 19:43:50 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-dind`

```console
$ docker pull docker@sha256:744ae25d20431b9eccf9832fae189e43e06054b666df039b5552a46433cbe499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23-dind` - linux; amd64

```console
$ docker pull docker@sha256:2d036f72fa2728ddd599238453528ad1e9f4a0609ab3371f69b90fcce188b6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115841865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810c2eb4df26b8c6cb07ee900ebd168d0142553f630d7088036fc7a9cfa4d227`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbbfe9c78c82698902d2f699f3a866996d040be1686dd10f629e37d89ea33ee`  
		Last Modified: Thu, 15 Jun 2023 05:28:31 GMT  
		Size: 16.3 MB (16250874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5708dec9aea531c023a63cb6d674e4e42d94d8d84f51fcb66e9ced1c260f9e8e`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65b66e2e2892b010a1e320cecb6edff9ba98ee75b8f29eef076c7283e7a304a`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 18.0 MB (17980092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb3e3c468fa108bf2f2fec6fe9280189753b2b7ee37469941e8a688e93d499`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436c2e539760ae39be8e540fcaa7b1d1bd2fb877e8d36435eda4696d8671cea3`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed4165006f30d0eaeedeff7a3519a447de7a7f04408360003f349d6eac00de`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0c3925a01970b8b6f4b30c4ae0394f4200f55cdf177c877ae2168802ac1af1`  
		Last Modified: Thu, 06 Jul 2023 20:22:44 GMT  
		Size: 7.1 MB (7080604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd90aaca53b9d97ecf639fdb1778a1b1916e3147ff0a2ac84d6b147d1716d9ea`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce803b02ed3e4ed43bd7c6ab9ba5562ccecbe574b1d6e06252d1475cd28b9e8`  
		Last Modified: Thu, 06 Jul 2023 20:22:50 GMT  
		Size: 51.7 MB (51657476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe710e1a3eab28e7bc6596ef135bba1ed104de7cd599ed563fcbee8eee777f9`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8189afb935336899691d8ca85748fd24ec7045a0f1d9ccad361e14df8e84f61b`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 2.8 KB (2790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7a17e1adde579f7913a1d5dd4411094f9becfb0320db66d280a26a09b7eb9c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107103059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e2bc332c22f7586e25665430021c48e8bf8f10c1e9ec574a05034a99fb50b8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51d2d067e69a1f5a948d2d1133441f75a192e5bcc4154ca7be51943ff4a24d5`  
		Last Modified: Wed, 14 Jun 2023 22:42:12 GMT  
		Size: 15.3 MB (15325099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f28a2d02144ee951238b5623115d8fe18645df105f9e258b004975a591788`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 15.8 MB (15759517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc821c9da813150074e2cdd9b1099f1ea4305b04232851161a942a0cff4ab7`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 16.3 MB (16312968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b312f8beda3531c97f8edbf8ba090359914ca1508325250ff3262cd64f386635`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212d8b0184b5e16c4fd2f221bbdac88bbec8f94f632ff8ae1997332cf161ef37`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa6cbfc4ca5d773f84f56574cc994db7b86481df32126e0f0b9bcc8e7a33f87`  
		Last Modified: Thu, 06 Jul 2023 19:43:50 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b5774c046c118941ffdd7940de95e7371426fed92f8f27cb2587d4dddcc2c2`  
		Last Modified: Thu, 06 Jul 2023 19:44:05 GMT  
		Size: 7.3 MB (7291362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accf38e0a7857aa4882234dae62ba6cc1ecf9a987234b2eb10476cbc56cd701b`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fe37bb22c274be66fca87ae65085ab0a4b07ec499f6c8da99e0687d8dea17e`  
		Last Modified: Thu, 06 Jul 2023 19:44:09 GMT  
		Size: 47.1 MB (47053345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acd2d702cadc0b2a4f3272301e99216dbbfca7534826bf448015df6463954df`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53635b71f6ec66afb091ea2ae377ba957cfa8e4b8c0e4ff8d41bb157cc33d5b5`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-dind-rootless`

```console
$ docker pull docker@sha256:d72b65560351d3f141e9c5347d3f7e0289e1406d092d2571f1990ef48a67ad22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ab0ea6c0db98c62f962965d7de25509ddd8b7e9b48425901d61be736771a9bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137553077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38074c9fc8d6dfc4989a320e785d10807ec73758d1f9ece9c6f010263bfc56f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 16 May 2023 17:59:38 GMT
USER rootless
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbbfe9c78c82698902d2f699f3a866996d040be1686dd10f629e37d89ea33ee`  
		Last Modified: Thu, 15 Jun 2023 05:28:31 GMT  
		Size: 16.3 MB (16250874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5708dec9aea531c023a63cb6d674e4e42d94d8d84f51fcb66e9ced1c260f9e8e`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65b66e2e2892b010a1e320cecb6edff9ba98ee75b8f29eef076c7283e7a304a`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 18.0 MB (17980092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb3e3c468fa108bf2f2fec6fe9280189753b2b7ee37469941e8a688e93d499`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436c2e539760ae39be8e540fcaa7b1d1bd2fb877e8d36435eda4696d8671cea3`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed4165006f30d0eaeedeff7a3519a447de7a7f04408360003f349d6eac00de`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0c3925a01970b8b6f4b30c4ae0394f4200f55cdf177c877ae2168802ac1af1`  
		Last Modified: Thu, 06 Jul 2023 20:22:44 GMT  
		Size: 7.1 MB (7080604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd90aaca53b9d97ecf639fdb1778a1b1916e3147ff0a2ac84d6b147d1716d9ea`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce803b02ed3e4ed43bd7c6ab9ba5562ccecbe574b1d6e06252d1475cd28b9e8`  
		Last Modified: Thu, 06 Jul 2023 20:22:50 GMT  
		Size: 51.7 MB (51657476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe710e1a3eab28e7bc6596ef135bba1ed104de7cd599ed563fcbee8eee777f9`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8189afb935336899691d8ca85748fd24ec7045a0f1d9ccad361e14df8e84f61b`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 2.8 KB (2790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6230ff53f18c93c4a624bc8b1bd4e9b37917858576bb6bf7b2517e8234f13cf9`  
		Last Modified: Thu, 06 Jul 2023 20:23:15 GMT  
		Size: 1.4 MB (1362367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408ece9af5d25bd78a674ed3ef3f80cff66c0a767623748ccfd459561b834851`  
		Last Modified: Thu, 06 Jul 2023 20:23:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117f4f867ffe3f026946370181fcfe14820945807abe76b348243742c06e3672`  
		Last Modified: Thu, 06 Jul 2023 20:23:15 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edc62e51203e88508a6917f502d99673a58a8c375186a5445823c5e3b302e23`  
		Last Modified: Thu, 06 Jul 2023 20:23:18 GMT  
		Size: 20.3 MB (20347105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ff9f47195acd13e38adddd06b93bc5aae41f1626456905ebc5994bedc60f65`  
		Last Modified: Thu, 06 Jul 2023 20:23:15 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:501d9df4431674be20300e0a971aa665820b43564ad84ea14c18fbb5f21c8aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130759048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8aa08b3f258d7c85e3cca459f450f6fe424d614a34ee27035739b02c1c7fc8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 16 May 2023 17:59:38 GMT
USER rootless
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51d2d067e69a1f5a948d2d1133441f75a192e5bcc4154ca7be51943ff4a24d5`  
		Last Modified: Wed, 14 Jun 2023 22:42:12 GMT  
		Size: 15.3 MB (15325099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f28a2d02144ee951238b5623115d8fe18645df105f9e258b004975a591788`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 15.8 MB (15759517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc821c9da813150074e2cdd9b1099f1ea4305b04232851161a942a0cff4ab7`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 16.3 MB (16312968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b312f8beda3531c97f8edbf8ba090359914ca1508325250ff3262cd64f386635`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212d8b0184b5e16c4fd2f221bbdac88bbec8f94f632ff8ae1997332cf161ef37`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa6cbfc4ca5d773f84f56574cc994db7b86481df32126e0f0b9bcc8e7a33f87`  
		Last Modified: Thu, 06 Jul 2023 19:43:50 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b5774c046c118941ffdd7940de95e7371426fed92f8f27cb2587d4dddcc2c2`  
		Last Modified: Thu, 06 Jul 2023 19:44:05 GMT  
		Size: 7.3 MB (7291362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accf38e0a7857aa4882234dae62ba6cc1ecf9a987234b2eb10476cbc56cd701b`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fe37bb22c274be66fca87ae65085ab0a4b07ec499f6c8da99e0687d8dea17e`  
		Last Modified: Thu, 06 Jul 2023 19:44:09 GMT  
		Size: 47.1 MB (47053345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acd2d702cadc0b2a4f3272301e99216dbbfca7534826bf448015df6463954df`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53635b71f6ec66afb091ea2ae377ba957cfa8e4b8c0e4ff8d41bb157cc33d5b5`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c844a7243a0e537041a413b83b62a9ac6b95bf62b82c214edd944b0aa1d6016`  
		Last Modified: Thu, 06 Jul 2023 19:44:33 GMT  
		Size: 1.4 MB (1413250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39050000c34c799394809969e7bec9f3ae5307b0bf314f20b8aa6f43d6de3059`  
		Last Modified: Thu, 06 Jul 2023 19:44:32 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3548b5070aef57c8d9b4a8036d68869d662f3cfe4f60b1fdc2f3b004f504ac96`  
		Last Modified: Thu, 06 Jul 2023 19:44:32 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186d8f9b8f46c83c9aae60b5e8cd43468f600fedacbb82390a8aa41d4b340a04`  
		Last Modified: Thu, 06 Jul 2023 19:44:35 GMT  
		Size: 22.2 MB (22240999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff355f3f3ab86a69f7607c4556b4bc4bb7f70efc1a817f3696858af9bca2db20`  
		Last Modified: Thu, 06 Jul 2023 19:44:32 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-git`

```console
$ docker pull docker@sha256:937e04616ae1907a4ccbbec58d09314ed3341dfbbc298798565d4348f2000b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23-git` - linux; amd64

```console
$ docker pull docker@sha256:799dc31980d9fba48ccfdf94a6c2629bfbc781863cadc3cd49648a7ee5e50596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120776607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74c22e0f162a0f25996dd4f7660930512ef8234f92a4e569d08d5a5b5193d06`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbbfe9c78c82698902d2f699f3a866996d040be1686dd10f629e37d89ea33ee`  
		Last Modified: Thu, 15 Jun 2023 05:28:31 GMT  
		Size: 16.3 MB (16250874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5708dec9aea531c023a63cb6d674e4e42d94d8d84f51fcb66e9ced1c260f9e8e`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65b66e2e2892b010a1e320cecb6edff9ba98ee75b8f29eef076c7283e7a304a`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 18.0 MB (17980092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb3e3c468fa108bf2f2fec6fe9280189753b2b7ee37469941e8a688e93d499`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436c2e539760ae39be8e540fcaa7b1d1bd2fb877e8d36435eda4696d8671cea3`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed4165006f30d0eaeedeff7a3519a447de7a7f04408360003f349d6eac00de`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0c3925a01970b8b6f4b30c4ae0394f4200f55cdf177c877ae2168802ac1af1`  
		Last Modified: Thu, 06 Jul 2023 20:22:44 GMT  
		Size: 7.1 MB (7080604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd90aaca53b9d97ecf639fdb1778a1b1916e3147ff0a2ac84d6b147d1716d9ea`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce803b02ed3e4ed43bd7c6ab9ba5562ccecbe574b1d6e06252d1475cd28b9e8`  
		Last Modified: Thu, 06 Jul 2023 20:22:50 GMT  
		Size: 51.7 MB (51657476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe710e1a3eab28e7bc6596ef135bba1ed104de7cd599ed563fcbee8eee777f9`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8189afb935336899691d8ca85748fd24ec7045a0f1d9ccad361e14df8e84f61b`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 2.8 KB (2790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47db942abd1a5e7aaa96943c00a80dd34d9b8ad048680f169c7ad995d0004b7`  
		Last Modified: Thu, 06 Jul 2023 20:23:32 GMT  
		Size: 4.9 MB (4934742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f386ae6dd346abeb7f481719b53c3c7f2adb150c62b75c3b3ed3d070b8e1d9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112124141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a206b4fb14701c8db4057df2435babcf9e3f3ac4799c04f7b7c0b2215271ea92`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51d2d067e69a1f5a948d2d1133441f75a192e5bcc4154ca7be51943ff4a24d5`  
		Last Modified: Wed, 14 Jun 2023 22:42:12 GMT  
		Size: 15.3 MB (15325099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f28a2d02144ee951238b5623115d8fe18645df105f9e258b004975a591788`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 15.8 MB (15759517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc821c9da813150074e2cdd9b1099f1ea4305b04232851161a942a0cff4ab7`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 16.3 MB (16312968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b312f8beda3531c97f8edbf8ba090359914ca1508325250ff3262cd64f386635`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212d8b0184b5e16c4fd2f221bbdac88bbec8f94f632ff8ae1997332cf161ef37`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa6cbfc4ca5d773f84f56574cc994db7b86481df32126e0f0b9bcc8e7a33f87`  
		Last Modified: Thu, 06 Jul 2023 19:43:50 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b5774c046c118941ffdd7940de95e7371426fed92f8f27cb2587d4dddcc2c2`  
		Last Modified: Thu, 06 Jul 2023 19:44:05 GMT  
		Size: 7.3 MB (7291362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accf38e0a7857aa4882234dae62ba6cc1ecf9a987234b2eb10476cbc56cd701b`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fe37bb22c274be66fca87ae65085ab0a4b07ec499f6c8da99e0687d8dea17e`  
		Last Modified: Thu, 06 Jul 2023 19:44:09 GMT  
		Size: 47.1 MB (47053345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acd2d702cadc0b2a4f3272301e99216dbbfca7534826bf448015df6463954df`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53635b71f6ec66afb091ea2ae377ba957cfa8e4b8c0e4ff8d41bb157cc33d5b5`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3397c031c86d20662e77466a69635249b12fdfa5544cc8b292e65fedb2f70f`  
		Last Modified: Thu, 06 Jul 2023 19:44:47 GMT  
		Size: 5.0 MB (5021082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-windowsservercore`

```console
$ docker pull docker@sha256:796d95a96cb9faea174f2b482e2886b3d9d082621b814ecb064ba559d8431e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1787; amd64
	-	windows version 10.0.17763.4499; amd64

### `docker:23-windowsservercore` - windows version 10.0.20348.1787; amd64

```console
$ docker pull docker@sha256:4b08c7610e6e77ecaa1a902f4b45ebd9fe846cd8fc7dc4328188ffe2e206f96d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1480297932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea8c05f68944e9c20b7c71cedb22cc24c88b4e9420984a72f54a9404d4dd9c0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:33:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 24 Jun 2023 03:37:22 GMT
ENV DOCKER_VERSION=23.0.6
# Sat, 24 Jun 2023 03:37:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Sat, 24 Jun 2023 03:37:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:18:35 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:18:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:18:37 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:19:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:19:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:19:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:19:04 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:19:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27db350c833f7fe0378bc977cd819c1ffe4133ff02ff69f1531f8ddc552c2366`  
		Last Modified: Sat, 24 Jun 2023 01:15:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c818796445a77806e10e6c159d076d6b0f5105edd8e7f27848042efb890970dd`  
		Last Modified: Sat, 24 Jun 2023 03:41:36 GMT  
		Size: 326.7 KB (326673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e4d934aedb3408d39924086e00ca7aaad6ba9093494927ec3193aafd92a20f`  
		Last Modified: Sat, 24 Jun 2023 03:42:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d47816062ca7fccecb96be7bf6468c4f36ffddd3115cf4d9bf244c0379bf7c`  
		Last Modified: Sat, 24 Jun 2023 03:42:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0520b4152b36536d9d6e0fbb761f4d738b989c5b9bc20fdcb54002f3531479b5`  
		Last Modified: Sat, 24 Jun 2023 03:42:18 GMT  
		Size: 17.3 MB (17325743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdef24df9e2be75799ec275160025462aef6bfb95360fc2907a2083128ae16b7`  
		Last Modified: Thu, 06 Jul 2023 20:22:01 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc79a9ea08518357ee22844e397fc700662ad99e4301177931c051357c2b2ec1`  
		Last Modified: Thu, 06 Jul 2023 20:22:02 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22356ed2aac9af5f5f301124bc544866e9164e843b1953a756c1339b561d671`  
		Last Modified: Thu, 06 Jul 2023 20:22:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e8c3432dbb82df56e2f5401d6af16998e13e3c34c99e49bf8c4bcd962359c8`  
		Last Modified: Thu, 06 Jul 2023 20:22:04 GMT  
		Size: 17.9 MB (17887283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466ab729826a1f27a4da2bbdf7ca5b645dc751c2f402fb5430c4db779b23360f`  
		Last Modified: Thu, 06 Jul 2023 20:22:00 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b58ed4b305ad3e911a088a311609a4eea626236698ec9a473e0f7ebafa56f3`  
		Last Modified: Thu, 06 Jul 2023 20:21:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b74996437d952638b6792afde202c442b5c8edcaf2df2272c0462cd3a2e728f`  
		Last Modified: Thu, 06 Jul 2023 20:21:59 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb948d323920d86405286636657cfe2ab8b9bc59b04009e8b75829a97ec4991`  
		Last Modified: Thu, 06 Jul 2023 20:22:04 GMT  
		Size: 18.4 MB (18447582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23-windowsservercore` - windows version 10.0.17763.4499; amd64

```console
$ docker pull docker@sha256:f4abd94c28bd796305168cc5169ab6b53d0a3b3a6acbcb9358fef201b9df737c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1704713998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce3edf2c8c754fd78053708b617c25ecbf40dc11501ea6c0c46daf809b630d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:40:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:35:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 24 Jun 2023 03:39:11 GMT
ENV DOCKER_VERSION=23.0.6
# Sat, 24 Jun 2023 03:39:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Sat, 24 Jun 2023 03:39:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:19:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:19:39 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:20:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:20:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:20:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:20:09 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:20:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58717a727cd3a756d7c1180dfb74e95d49735ed12628bd25d2058bc90fa96991`  
		Last Modified: Sat, 24 Jun 2023 01:20:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb210483c7a5877c9d4e754a46a0085ff94bc31d9e32e64c37e1ed4d6e30162e`  
		Last Modified: Sat, 24 Jun 2023 03:41:56 GMT  
		Size: 306.0 KB (305975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabd176de44496cc60e08f954b7d47c99eb8d47e8a4338216815756e4e9659db`  
		Last Modified: Sat, 24 Jun 2023 03:42:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b649bbc9bc70f0249f614bd545fd46c7cae1690a92cc79ea5befcd92cdcbdaa`  
		Last Modified: Sat, 24 Jun 2023 03:42:33 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16f0093a3b9ea484ba6ea7db9214d3bc0d379d6ecdd7ee3a7fdecb30b09cde0`  
		Last Modified: Sat, 24 Jun 2023 03:42:36 GMT  
		Size: 17.3 MB (17317987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389161e994c15c3e9bb0d59b881f2e66c346741b5db56f1894dcf154ffd8e59e`  
		Last Modified: Thu, 06 Jul 2023 20:22:17 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b974715fdc8e49748b7df92467cf04b846153578451a263d09f3c06ac90f5b`  
		Last Modified: Thu, 06 Jul 2023 20:22:17 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319e27cb500eb4e95dee60ceaa99ff30aeb51e0135a38bdbab4f481df68c830f`  
		Last Modified: Thu, 06 Jul 2023 20:22:17 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e96a6b06fe957b7b5ef17e1e16befe81f9c587df9834a0d8ca0ead68d0473d`  
		Last Modified: Thu, 06 Jul 2023 20:22:19 GMT  
		Size: 17.9 MB (17893316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4d4160f106ae94c6259174699128c75a96e63bbc3b5174afa88ffad72c98ba`  
		Last Modified: Thu, 06 Jul 2023 20:22:15 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92eca18e3583f1e85682cd7ecc745d64ee25a7e8fc60f7a0f4e4eedca0f19bf4`  
		Last Modified: Thu, 06 Jul 2023 20:22:15 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e41015e9e122c67f575369bb6d2953b50e0d130796923de057ee61f5466f0a90`  
		Last Modified: Thu, 06 Jul 2023 20:22:15 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3871795cc5c72b3e7a4565d36516149ce596a94b90cb00fc8b82b26d9c26e5`  
		Last Modified: Thu, 06 Jul 2023 20:22:20 GMT  
		Size: 18.4 MB (18447545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-windowsservercore-1809`

```console
$ docker pull docker@sha256:eb129c605ee7370d5cdc683bd3faca768161d36fd0186e695110dd8296ba121d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `docker:23-windowsservercore-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull docker@sha256:f4abd94c28bd796305168cc5169ab6b53d0a3b3a6acbcb9358fef201b9df737c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1704713998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce3edf2c8c754fd78053708b617c25ecbf40dc11501ea6c0c46daf809b630d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:40:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:35:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 24 Jun 2023 03:39:11 GMT
ENV DOCKER_VERSION=23.0.6
# Sat, 24 Jun 2023 03:39:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Sat, 24 Jun 2023 03:39:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:19:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:19:39 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:20:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:20:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:20:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:20:09 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:20:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58717a727cd3a756d7c1180dfb74e95d49735ed12628bd25d2058bc90fa96991`  
		Last Modified: Sat, 24 Jun 2023 01:20:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb210483c7a5877c9d4e754a46a0085ff94bc31d9e32e64c37e1ed4d6e30162e`  
		Last Modified: Sat, 24 Jun 2023 03:41:56 GMT  
		Size: 306.0 KB (305975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabd176de44496cc60e08f954b7d47c99eb8d47e8a4338216815756e4e9659db`  
		Last Modified: Sat, 24 Jun 2023 03:42:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b649bbc9bc70f0249f614bd545fd46c7cae1690a92cc79ea5befcd92cdcbdaa`  
		Last Modified: Sat, 24 Jun 2023 03:42:33 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16f0093a3b9ea484ba6ea7db9214d3bc0d379d6ecdd7ee3a7fdecb30b09cde0`  
		Last Modified: Sat, 24 Jun 2023 03:42:36 GMT  
		Size: 17.3 MB (17317987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389161e994c15c3e9bb0d59b881f2e66c346741b5db56f1894dcf154ffd8e59e`  
		Last Modified: Thu, 06 Jul 2023 20:22:17 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b974715fdc8e49748b7df92467cf04b846153578451a263d09f3c06ac90f5b`  
		Last Modified: Thu, 06 Jul 2023 20:22:17 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319e27cb500eb4e95dee60ceaa99ff30aeb51e0135a38bdbab4f481df68c830f`  
		Last Modified: Thu, 06 Jul 2023 20:22:17 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e96a6b06fe957b7b5ef17e1e16befe81f9c587df9834a0d8ca0ead68d0473d`  
		Last Modified: Thu, 06 Jul 2023 20:22:19 GMT  
		Size: 17.9 MB (17893316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4d4160f106ae94c6259174699128c75a96e63bbc3b5174afa88ffad72c98ba`  
		Last Modified: Thu, 06 Jul 2023 20:22:15 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92eca18e3583f1e85682cd7ecc745d64ee25a7e8fc60f7a0f4e4eedca0f19bf4`  
		Last Modified: Thu, 06 Jul 2023 20:22:15 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e41015e9e122c67f575369bb6d2953b50e0d130796923de057ee61f5466f0a90`  
		Last Modified: Thu, 06 Jul 2023 20:22:15 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3871795cc5c72b3e7a4565d36516149ce596a94b90cb00fc8b82b26d9c26e5`  
		Last Modified: Thu, 06 Jul 2023 20:22:20 GMT  
		Size: 18.4 MB (18447545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:46e697d13a25a200fd12630190cae49387192ca89c7f96111a1bf8411053ad6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1787; amd64

### `docker:23-windowsservercore-ltsc2022` - windows version 10.0.20348.1787; amd64

```console
$ docker pull docker@sha256:4b08c7610e6e77ecaa1a902f4b45ebd9fe846cd8fc7dc4328188ffe2e206f96d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1480297932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea8c05f68944e9c20b7c71cedb22cc24c88b4e9420984a72f54a9404d4dd9c0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:33:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 24 Jun 2023 03:37:22 GMT
ENV DOCKER_VERSION=23.0.6
# Sat, 24 Jun 2023 03:37:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Sat, 24 Jun 2023 03:37:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:18:35 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:18:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:18:37 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:19:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:19:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:19:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:19:04 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:19:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27db350c833f7fe0378bc977cd819c1ffe4133ff02ff69f1531f8ddc552c2366`  
		Last Modified: Sat, 24 Jun 2023 01:15:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c818796445a77806e10e6c159d076d6b0f5105edd8e7f27848042efb890970dd`  
		Last Modified: Sat, 24 Jun 2023 03:41:36 GMT  
		Size: 326.7 KB (326673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e4d934aedb3408d39924086e00ca7aaad6ba9093494927ec3193aafd92a20f`  
		Last Modified: Sat, 24 Jun 2023 03:42:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d47816062ca7fccecb96be7bf6468c4f36ffddd3115cf4d9bf244c0379bf7c`  
		Last Modified: Sat, 24 Jun 2023 03:42:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0520b4152b36536d9d6e0fbb761f4d738b989c5b9bc20fdcb54002f3531479b5`  
		Last Modified: Sat, 24 Jun 2023 03:42:18 GMT  
		Size: 17.3 MB (17325743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdef24df9e2be75799ec275160025462aef6bfb95360fc2907a2083128ae16b7`  
		Last Modified: Thu, 06 Jul 2023 20:22:01 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc79a9ea08518357ee22844e397fc700662ad99e4301177931c051357c2b2ec1`  
		Last Modified: Thu, 06 Jul 2023 20:22:02 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22356ed2aac9af5f5f301124bc544866e9164e843b1953a756c1339b561d671`  
		Last Modified: Thu, 06 Jul 2023 20:22:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e8c3432dbb82df56e2f5401d6af16998e13e3c34c99e49bf8c4bcd962359c8`  
		Last Modified: Thu, 06 Jul 2023 20:22:04 GMT  
		Size: 17.9 MB (17887283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466ab729826a1f27a4da2bbdf7ca5b645dc751c2f402fb5430c4db779b23360f`  
		Last Modified: Thu, 06 Jul 2023 20:22:00 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b58ed4b305ad3e911a088a311609a4eea626236698ec9a473e0f7ebafa56f3`  
		Last Modified: Thu, 06 Jul 2023 20:21:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b74996437d952638b6792afde202c442b5c8edcaf2df2272c0462cd3a2e728f`  
		Last Modified: Thu, 06 Jul 2023 20:21:59 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb948d323920d86405286636657cfe2ab8b9bc59b04009e8b75829a97ec4991`  
		Last Modified: Thu, 06 Jul 2023 20:22:04 GMT  
		Size: 18.4 MB (18447582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0`

```console
$ docker pull docker@sha256:744ae25d20431b9eccf9832fae189e43e06054b666df039b5552a46433cbe499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0` - linux; amd64

```console
$ docker pull docker@sha256:2d036f72fa2728ddd599238453528ad1e9f4a0609ab3371f69b90fcce188b6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115841865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810c2eb4df26b8c6cb07ee900ebd168d0142553f630d7088036fc7a9cfa4d227`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbbfe9c78c82698902d2f699f3a866996d040be1686dd10f629e37d89ea33ee`  
		Last Modified: Thu, 15 Jun 2023 05:28:31 GMT  
		Size: 16.3 MB (16250874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5708dec9aea531c023a63cb6d674e4e42d94d8d84f51fcb66e9ced1c260f9e8e`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65b66e2e2892b010a1e320cecb6edff9ba98ee75b8f29eef076c7283e7a304a`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 18.0 MB (17980092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb3e3c468fa108bf2f2fec6fe9280189753b2b7ee37469941e8a688e93d499`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436c2e539760ae39be8e540fcaa7b1d1bd2fb877e8d36435eda4696d8671cea3`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed4165006f30d0eaeedeff7a3519a447de7a7f04408360003f349d6eac00de`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0c3925a01970b8b6f4b30c4ae0394f4200f55cdf177c877ae2168802ac1af1`  
		Last Modified: Thu, 06 Jul 2023 20:22:44 GMT  
		Size: 7.1 MB (7080604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd90aaca53b9d97ecf639fdb1778a1b1916e3147ff0a2ac84d6b147d1716d9ea`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce803b02ed3e4ed43bd7c6ab9ba5562ccecbe574b1d6e06252d1475cd28b9e8`  
		Last Modified: Thu, 06 Jul 2023 20:22:50 GMT  
		Size: 51.7 MB (51657476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe710e1a3eab28e7bc6596ef135bba1ed104de7cd599ed563fcbee8eee777f9`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8189afb935336899691d8ca85748fd24ec7045a0f1d9ccad361e14df8e84f61b`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 2.8 KB (2790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7a17e1adde579f7913a1d5dd4411094f9becfb0320db66d280a26a09b7eb9c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107103059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e2bc332c22f7586e25665430021c48e8bf8f10c1e9ec574a05034a99fb50b8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51d2d067e69a1f5a948d2d1133441f75a192e5bcc4154ca7be51943ff4a24d5`  
		Last Modified: Wed, 14 Jun 2023 22:42:12 GMT  
		Size: 15.3 MB (15325099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f28a2d02144ee951238b5623115d8fe18645df105f9e258b004975a591788`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 15.8 MB (15759517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc821c9da813150074e2cdd9b1099f1ea4305b04232851161a942a0cff4ab7`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 16.3 MB (16312968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b312f8beda3531c97f8edbf8ba090359914ca1508325250ff3262cd64f386635`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212d8b0184b5e16c4fd2f221bbdac88bbec8f94f632ff8ae1997332cf161ef37`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa6cbfc4ca5d773f84f56574cc994db7b86481df32126e0f0b9bcc8e7a33f87`  
		Last Modified: Thu, 06 Jul 2023 19:43:50 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b5774c046c118941ffdd7940de95e7371426fed92f8f27cb2587d4dddcc2c2`  
		Last Modified: Thu, 06 Jul 2023 19:44:05 GMT  
		Size: 7.3 MB (7291362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accf38e0a7857aa4882234dae62ba6cc1ecf9a987234b2eb10476cbc56cd701b`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fe37bb22c274be66fca87ae65085ab0a4b07ec499f6c8da99e0687d8dea17e`  
		Last Modified: Thu, 06 Jul 2023 19:44:09 GMT  
		Size: 47.1 MB (47053345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acd2d702cadc0b2a4f3272301e99216dbbfca7534826bf448015df6463954df`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53635b71f6ec66afb091ea2ae377ba957cfa8e4b8c0e4ff8d41bb157cc33d5b5`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-cli`

```console
$ docker pull docker@sha256:f233d64cf3968d36c794b0354dde961256cccca2e3e4ebd51eaff3b15caf8fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:3ead83ab52c1d056fd65655d97797494b34383a6e062b80976f80f1691db62e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57098627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af26fe8bcb5b1a2b8e6b185d9a8fd75d932b97c1faa729bca3a932af8b1271f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbbfe9c78c82698902d2f699f3a866996d040be1686dd10f629e37d89ea33ee`  
		Last Modified: Thu, 15 Jun 2023 05:28:31 GMT  
		Size: 16.3 MB (16250874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5708dec9aea531c023a63cb6d674e4e42d94d8d84f51fcb66e9ced1c260f9e8e`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65b66e2e2892b010a1e320cecb6edff9ba98ee75b8f29eef076c7283e7a304a`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 18.0 MB (17980092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb3e3c468fa108bf2f2fec6fe9280189753b2b7ee37469941e8a688e93d499`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436c2e539760ae39be8e540fcaa7b1d1bd2fb877e8d36435eda4696d8671cea3`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed4165006f30d0eaeedeff7a3519a447de7a7f04408360003f349d6eac00de`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d39267d642857eadb6106a70304967b2e7b9c71e31bf722e55ca2d107aa84bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52753194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0660417e68d2e9295da7a725dcde7983a789e8dca5dd992d3c4bdc52b19d908`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51d2d067e69a1f5a948d2d1133441f75a192e5bcc4154ca7be51943ff4a24d5`  
		Last Modified: Wed, 14 Jun 2023 22:42:12 GMT  
		Size: 15.3 MB (15325099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f28a2d02144ee951238b5623115d8fe18645df105f9e258b004975a591788`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 15.8 MB (15759517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc821c9da813150074e2cdd9b1099f1ea4305b04232851161a942a0cff4ab7`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 16.3 MB (16312968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b312f8beda3531c97f8edbf8ba090359914ca1508325250ff3262cd64f386635`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212d8b0184b5e16c4fd2f221bbdac88bbec8f94f632ff8ae1997332cf161ef37`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa6cbfc4ca5d773f84f56574cc994db7b86481df32126e0f0b9bcc8e7a33f87`  
		Last Modified: Thu, 06 Jul 2023 19:43:50 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-dind`

```console
$ docker pull docker@sha256:744ae25d20431b9eccf9832fae189e43e06054b666df039b5552a46433cbe499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:2d036f72fa2728ddd599238453528ad1e9f4a0609ab3371f69b90fcce188b6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115841865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810c2eb4df26b8c6cb07ee900ebd168d0142553f630d7088036fc7a9cfa4d227`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbbfe9c78c82698902d2f699f3a866996d040be1686dd10f629e37d89ea33ee`  
		Last Modified: Thu, 15 Jun 2023 05:28:31 GMT  
		Size: 16.3 MB (16250874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5708dec9aea531c023a63cb6d674e4e42d94d8d84f51fcb66e9ced1c260f9e8e`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65b66e2e2892b010a1e320cecb6edff9ba98ee75b8f29eef076c7283e7a304a`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 18.0 MB (17980092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb3e3c468fa108bf2f2fec6fe9280189753b2b7ee37469941e8a688e93d499`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436c2e539760ae39be8e540fcaa7b1d1bd2fb877e8d36435eda4696d8671cea3`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed4165006f30d0eaeedeff7a3519a447de7a7f04408360003f349d6eac00de`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0c3925a01970b8b6f4b30c4ae0394f4200f55cdf177c877ae2168802ac1af1`  
		Last Modified: Thu, 06 Jul 2023 20:22:44 GMT  
		Size: 7.1 MB (7080604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd90aaca53b9d97ecf639fdb1778a1b1916e3147ff0a2ac84d6b147d1716d9ea`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce803b02ed3e4ed43bd7c6ab9ba5562ccecbe574b1d6e06252d1475cd28b9e8`  
		Last Modified: Thu, 06 Jul 2023 20:22:50 GMT  
		Size: 51.7 MB (51657476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe710e1a3eab28e7bc6596ef135bba1ed104de7cd599ed563fcbee8eee777f9`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8189afb935336899691d8ca85748fd24ec7045a0f1d9ccad361e14df8e84f61b`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 2.8 KB (2790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7a17e1adde579f7913a1d5dd4411094f9becfb0320db66d280a26a09b7eb9c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107103059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e2bc332c22f7586e25665430021c48e8bf8f10c1e9ec574a05034a99fb50b8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51d2d067e69a1f5a948d2d1133441f75a192e5bcc4154ca7be51943ff4a24d5`  
		Last Modified: Wed, 14 Jun 2023 22:42:12 GMT  
		Size: 15.3 MB (15325099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f28a2d02144ee951238b5623115d8fe18645df105f9e258b004975a591788`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 15.8 MB (15759517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc821c9da813150074e2cdd9b1099f1ea4305b04232851161a942a0cff4ab7`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 16.3 MB (16312968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b312f8beda3531c97f8edbf8ba090359914ca1508325250ff3262cd64f386635`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212d8b0184b5e16c4fd2f221bbdac88bbec8f94f632ff8ae1997332cf161ef37`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa6cbfc4ca5d773f84f56574cc994db7b86481df32126e0f0b9bcc8e7a33f87`  
		Last Modified: Thu, 06 Jul 2023 19:43:50 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b5774c046c118941ffdd7940de95e7371426fed92f8f27cb2587d4dddcc2c2`  
		Last Modified: Thu, 06 Jul 2023 19:44:05 GMT  
		Size: 7.3 MB (7291362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accf38e0a7857aa4882234dae62ba6cc1ecf9a987234b2eb10476cbc56cd701b`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fe37bb22c274be66fca87ae65085ab0a4b07ec499f6c8da99e0687d8dea17e`  
		Last Modified: Thu, 06 Jul 2023 19:44:09 GMT  
		Size: 47.1 MB (47053345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acd2d702cadc0b2a4f3272301e99216dbbfca7534826bf448015df6463954df`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53635b71f6ec66afb091ea2ae377ba957cfa8e4b8c0e4ff8d41bb157cc33d5b5`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-dind-rootless`

```console
$ docker pull docker@sha256:d72b65560351d3f141e9c5347d3f7e0289e1406d092d2571f1990ef48a67ad22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ab0ea6c0db98c62f962965d7de25509ddd8b7e9b48425901d61be736771a9bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137553077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38074c9fc8d6dfc4989a320e785d10807ec73758d1f9ece9c6f010263bfc56f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 16 May 2023 17:59:38 GMT
USER rootless
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbbfe9c78c82698902d2f699f3a866996d040be1686dd10f629e37d89ea33ee`  
		Last Modified: Thu, 15 Jun 2023 05:28:31 GMT  
		Size: 16.3 MB (16250874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5708dec9aea531c023a63cb6d674e4e42d94d8d84f51fcb66e9ced1c260f9e8e`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65b66e2e2892b010a1e320cecb6edff9ba98ee75b8f29eef076c7283e7a304a`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 18.0 MB (17980092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb3e3c468fa108bf2f2fec6fe9280189753b2b7ee37469941e8a688e93d499`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436c2e539760ae39be8e540fcaa7b1d1bd2fb877e8d36435eda4696d8671cea3`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed4165006f30d0eaeedeff7a3519a447de7a7f04408360003f349d6eac00de`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0c3925a01970b8b6f4b30c4ae0394f4200f55cdf177c877ae2168802ac1af1`  
		Last Modified: Thu, 06 Jul 2023 20:22:44 GMT  
		Size: 7.1 MB (7080604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd90aaca53b9d97ecf639fdb1778a1b1916e3147ff0a2ac84d6b147d1716d9ea`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce803b02ed3e4ed43bd7c6ab9ba5562ccecbe574b1d6e06252d1475cd28b9e8`  
		Last Modified: Thu, 06 Jul 2023 20:22:50 GMT  
		Size: 51.7 MB (51657476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe710e1a3eab28e7bc6596ef135bba1ed104de7cd599ed563fcbee8eee777f9`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8189afb935336899691d8ca85748fd24ec7045a0f1d9ccad361e14df8e84f61b`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 2.8 KB (2790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6230ff53f18c93c4a624bc8b1bd4e9b37917858576bb6bf7b2517e8234f13cf9`  
		Last Modified: Thu, 06 Jul 2023 20:23:15 GMT  
		Size: 1.4 MB (1362367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408ece9af5d25bd78a674ed3ef3f80cff66c0a767623748ccfd459561b834851`  
		Last Modified: Thu, 06 Jul 2023 20:23:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117f4f867ffe3f026946370181fcfe14820945807abe76b348243742c06e3672`  
		Last Modified: Thu, 06 Jul 2023 20:23:15 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edc62e51203e88508a6917f502d99673a58a8c375186a5445823c5e3b302e23`  
		Last Modified: Thu, 06 Jul 2023 20:23:18 GMT  
		Size: 20.3 MB (20347105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ff9f47195acd13e38adddd06b93bc5aae41f1626456905ebc5994bedc60f65`  
		Last Modified: Thu, 06 Jul 2023 20:23:15 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:501d9df4431674be20300e0a971aa665820b43564ad84ea14c18fbb5f21c8aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130759048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8aa08b3f258d7c85e3cca459f450f6fe424d614a34ee27035739b02c1c7fc8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 16 May 2023 17:59:38 GMT
USER rootless
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51d2d067e69a1f5a948d2d1133441f75a192e5bcc4154ca7be51943ff4a24d5`  
		Last Modified: Wed, 14 Jun 2023 22:42:12 GMT  
		Size: 15.3 MB (15325099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f28a2d02144ee951238b5623115d8fe18645df105f9e258b004975a591788`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 15.8 MB (15759517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc821c9da813150074e2cdd9b1099f1ea4305b04232851161a942a0cff4ab7`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 16.3 MB (16312968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b312f8beda3531c97f8edbf8ba090359914ca1508325250ff3262cd64f386635`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212d8b0184b5e16c4fd2f221bbdac88bbec8f94f632ff8ae1997332cf161ef37`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa6cbfc4ca5d773f84f56574cc994db7b86481df32126e0f0b9bcc8e7a33f87`  
		Last Modified: Thu, 06 Jul 2023 19:43:50 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b5774c046c118941ffdd7940de95e7371426fed92f8f27cb2587d4dddcc2c2`  
		Last Modified: Thu, 06 Jul 2023 19:44:05 GMT  
		Size: 7.3 MB (7291362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accf38e0a7857aa4882234dae62ba6cc1ecf9a987234b2eb10476cbc56cd701b`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fe37bb22c274be66fca87ae65085ab0a4b07ec499f6c8da99e0687d8dea17e`  
		Last Modified: Thu, 06 Jul 2023 19:44:09 GMT  
		Size: 47.1 MB (47053345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acd2d702cadc0b2a4f3272301e99216dbbfca7534826bf448015df6463954df`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53635b71f6ec66afb091ea2ae377ba957cfa8e4b8c0e4ff8d41bb157cc33d5b5`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c844a7243a0e537041a413b83b62a9ac6b95bf62b82c214edd944b0aa1d6016`  
		Last Modified: Thu, 06 Jul 2023 19:44:33 GMT  
		Size: 1.4 MB (1413250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39050000c34c799394809969e7bec9f3ae5307b0bf314f20b8aa6f43d6de3059`  
		Last Modified: Thu, 06 Jul 2023 19:44:32 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3548b5070aef57c8d9b4a8036d68869d662f3cfe4f60b1fdc2f3b004f504ac96`  
		Last Modified: Thu, 06 Jul 2023 19:44:32 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186d8f9b8f46c83c9aae60b5e8cd43468f600fedacbb82390a8aa41d4b340a04`  
		Last Modified: Thu, 06 Jul 2023 19:44:35 GMT  
		Size: 22.2 MB (22240999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff355f3f3ab86a69f7607c4556b4bc4bb7f70efc1a817f3696858af9bca2db20`  
		Last Modified: Thu, 06 Jul 2023 19:44:32 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-git`

```console
$ docker pull docker@sha256:937e04616ae1907a4ccbbec58d09314ed3341dfbbc298798565d4348f2000b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0-git` - linux; amd64

```console
$ docker pull docker@sha256:799dc31980d9fba48ccfdf94a6c2629bfbc781863cadc3cd49648a7ee5e50596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120776607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74c22e0f162a0f25996dd4f7660930512ef8234f92a4e569d08d5a5b5193d06`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbbfe9c78c82698902d2f699f3a866996d040be1686dd10f629e37d89ea33ee`  
		Last Modified: Thu, 15 Jun 2023 05:28:31 GMT  
		Size: 16.3 MB (16250874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5708dec9aea531c023a63cb6d674e4e42d94d8d84f51fcb66e9ced1c260f9e8e`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65b66e2e2892b010a1e320cecb6edff9ba98ee75b8f29eef076c7283e7a304a`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 18.0 MB (17980092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb3e3c468fa108bf2f2fec6fe9280189753b2b7ee37469941e8a688e93d499`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436c2e539760ae39be8e540fcaa7b1d1bd2fb877e8d36435eda4696d8671cea3`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed4165006f30d0eaeedeff7a3519a447de7a7f04408360003f349d6eac00de`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0c3925a01970b8b6f4b30c4ae0394f4200f55cdf177c877ae2168802ac1af1`  
		Last Modified: Thu, 06 Jul 2023 20:22:44 GMT  
		Size: 7.1 MB (7080604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd90aaca53b9d97ecf639fdb1778a1b1916e3147ff0a2ac84d6b147d1716d9ea`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce803b02ed3e4ed43bd7c6ab9ba5562ccecbe574b1d6e06252d1475cd28b9e8`  
		Last Modified: Thu, 06 Jul 2023 20:22:50 GMT  
		Size: 51.7 MB (51657476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe710e1a3eab28e7bc6596ef135bba1ed104de7cd599ed563fcbee8eee777f9`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8189afb935336899691d8ca85748fd24ec7045a0f1d9ccad361e14df8e84f61b`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 2.8 KB (2790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47db942abd1a5e7aaa96943c00a80dd34d9b8ad048680f169c7ad995d0004b7`  
		Last Modified: Thu, 06 Jul 2023 20:23:32 GMT  
		Size: 4.9 MB (4934742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f386ae6dd346abeb7f481719b53c3c7f2adb150c62b75c3b3ed3d070b8e1d9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112124141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a206b4fb14701c8db4057df2435babcf9e3f3ac4799c04f7b7c0b2215271ea92`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51d2d067e69a1f5a948d2d1133441f75a192e5bcc4154ca7be51943ff4a24d5`  
		Last Modified: Wed, 14 Jun 2023 22:42:12 GMT  
		Size: 15.3 MB (15325099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f28a2d02144ee951238b5623115d8fe18645df105f9e258b004975a591788`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 15.8 MB (15759517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc821c9da813150074e2cdd9b1099f1ea4305b04232851161a942a0cff4ab7`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 16.3 MB (16312968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b312f8beda3531c97f8edbf8ba090359914ca1508325250ff3262cd64f386635`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212d8b0184b5e16c4fd2f221bbdac88bbec8f94f632ff8ae1997332cf161ef37`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa6cbfc4ca5d773f84f56574cc994db7b86481df32126e0f0b9bcc8e7a33f87`  
		Last Modified: Thu, 06 Jul 2023 19:43:50 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b5774c046c118941ffdd7940de95e7371426fed92f8f27cb2587d4dddcc2c2`  
		Last Modified: Thu, 06 Jul 2023 19:44:05 GMT  
		Size: 7.3 MB (7291362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accf38e0a7857aa4882234dae62ba6cc1ecf9a987234b2eb10476cbc56cd701b`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fe37bb22c274be66fca87ae65085ab0a4b07ec499f6c8da99e0687d8dea17e`  
		Last Modified: Thu, 06 Jul 2023 19:44:09 GMT  
		Size: 47.1 MB (47053345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acd2d702cadc0b2a4f3272301e99216dbbfca7534826bf448015df6463954df`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53635b71f6ec66afb091ea2ae377ba957cfa8e4b8c0e4ff8d41bb157cc33d5b5`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3397c031c86d20662e77466a69635249b12fdfa5544cc8b292e65fedb2f70f`  
		Last Modified: Thu, 06 Jul 2023 19:44:47 GMT  
		Size: 5.0 MB (5021082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-windowsservercore`

```console
$ docker pull docker@sha256:796d95a96cb9faea174f2b482e2886b3d9d082621b814ecb064ba559d8431e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1787; amd64
	-	windows version 10.0.17763.4499; amd64

### `docker:23.0-windowsservercore` - windows version 10.0.20348.1787; amd64

```console
$ docker pull docker@sha256:4b08c7610e6e77ecaa1a902f4b45ebd9fe846cd8fc7dc4328188ffe2e206f96d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1480297932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea8c05f68944e9c20b7c71cedb22cc24c88b4e9420984a72f54a9404d4dd9c0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:33:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 24 Jun 2023 03:37:22 GMT
ENV DOCKER_VERSION=23.0.6
# Sat, 24 Jun 2023 03:37:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Sat, 24 Jun 2023 03:37:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:18:35 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:18:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:18:37 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:19:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:19:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:19:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:19:04 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:19:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27db350c833f7fe0378bc977cd819c1ffe4133ff02ff69f1531f8ddc552c2366`  
		Last Modified: Sat, 24 Jun 2023 01:15:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c818796445a77806e10e6c159d076d6b0f5105edd8e7f27848042efb890970dd`  
		Last Modified: Sat, 24 Jun 2023 03:41:36 GMT  
		Size: 326.7 KB (326673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e4d934aedb3408d39924086e00ca7aaad6ba9093494927ec3193aafd92a20f`  
		Last Modified: Sat, 24 Jun 2023 03:42:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d47816062ca7fccecb96be7bf6468c4f36ffddd3115cf4d9bf244c0379bf7c`  
		Last Modified: Sat, 24 Jun 2023 03:42:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0520b4152b36536d9d6e0fbb761f4d738b989c5b9bc20fdcb54002f3531479b5`  
		Last Modified: Sat, 24 Jun 2023 03:42:18 GMT  
		Size: 17.3 MB (17325743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdef24df9e2be75799ec275160025462aef6bfb95360fc2907a2083128ae16b7`  
		Last Modified: Thu, 06 Jul 2023 20:22:01 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc79a9ea08518357ee22844e397fc700662ad99e4301177931c051357c2b2ec1`  
		Last Modified: Thu, 06 Jul 2023 20:22:02 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22356ed2aac9af5f5f301124bc544866e9164e843b1953a756c1339b561d671`  
		Last Modified: Thu, 06 Jul 2023 20:22:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e8c3432dbb82df56e2f5401d6af16998e13e3c34c99e49bf8c4bcd962359c8`  
		Last Modified: Thu, 06 Jul 2023 20:22:04 GMT  
		Size: 17.9 MB (17887283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466ab729826a1f27a4da2bbdf7ca5b645dc751c2f402fb5430c4db779b23360f`  
		Last Modified: Thu, 06 Jul 2023 20:22:00 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b58ed4b305ad3e911a088a311609a4eea626236698ec9a473e0f7ebafa56f3`  
		Last Modified: Thu, 06 Jul 2023 20:21:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b74996437d952638b6792afde202c442b5c8edcaf2df2272c0462cd3a2e728f`  
		Last Modified: Thu, 06 Jul 2023 20:21:59 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb948d323920d86405286636657cfe2ab8b9bc59b04009e8b75829a97ec4991`  
		Last Modified: Thu, 06 Jul 2023 20:22:04 GMT  
		Size: 18.4 MB (18447582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0-windowsservercore` - windows version 10.0.17763.4499; amd64

```console
$ docker pull docker@sha256:f4abd94c28bd796305168cc5169ab6b53d0a3b3a6acbcb9358fef201b9df737c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1704713998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce3edf2c8c754fd78053708b617c25ecbf40dc11501ea6c0c46daf809b630d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:40:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:35:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 24 Jun 2023 03:39:11 GMT
ENV DOCKER_VERSION=23.0.6
# Sat, 24 Jun 2023 03:39:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Sat, 24 Jun 2023 03:39:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:19:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:19:39 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:20:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:20:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:20:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:20:09 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:20:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58717a727cd3a756d7c1180dfb74e95d49735ed12628bd25d2058bc90fa96991`  
		Last Modified: Sat, 24 Jun 2023 01:20:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb210483c7a5877c9d4e754a46a0085ff94bc31d9e32e64c37e1ed4d6e30162e`  
		Last Modified: Sat, 24 Jun 2023 03:41:56 GMT  
		Size: 306.0 KB (305975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabd176de44496cc60e08f954b7d47c99eb8d47e8a4338216815756e4e9659db`  
		Last Modified: Sat, 24 Jun 2023 03:42:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b649bbc9bc70f0249f614bd545fd46c7cae1690a92cc79ea5befcd92cdcbdaa`  
		Last Modified: Sat, 24 Jun 2023 03:42:33 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16f0093a3b9ea484ba6ea7db9214d3bc0d379d6ecdd7ee3a7fdecb30b09cde0`  
		Last Modified: Sat, 24 Jun 2023 03:42:36 GMT  
		Size: 17.3 MB (17317987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389161e994c15c3e9bb0d59b881f2e66c346741b5db56f1894dcf154ffd8e59e`  
		Last Modified: Thu, 06 Jul 2023 20:22:17 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b974715fdc8e49748b7df92467cf04b846153578451a263d09f3c06ac90f5b`  
		Last Modified: Thu, 06 Jul 2023 20:22:17 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319e27cb500eb4e95dee60ceaa99ff30aeb51e0135a38bdbab4f481df68c830f`  
		Last Modified: Thu, 06 Jul 2023 20:22:17 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e96a6b06fe957b7b5ef17e1e16befe81f9c587df9834a0d8ca0ead68d0473d`  
		Last Modified: Thu, 06 Jul 2023 20:22:19 GMT  
		Size: 17.9 MB (17893316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4d4160f106ae94c6259174699128c75a96e63bbc3b5174afa88ffad72c98ba`  
		Last Modified: Thu, 06 Jul 2023 20:22:15 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92eca18e3583f1e85682cd7ecc745d64ee25a7e8fc60f7a0f4e4eedca0f19bf4`  
		Last Modified: Thu, 06 Jul 2023 20:22:15 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e41015e9e122c67f575369bb6d2953b50e0d130796923de057ee61f5466f0a90`  
		Last Modified: Thu, 06 Jul 2023 20:22:15 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3871795cc5c72b3e7a4565d36516149ce596a94b90cb00fc8b82b26d9c26e5`  
		Last Modified: Thu, 06 Jul 2023 20:22:20 GMT  
		Size: 18.4 MB (18447545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:eb129c605ee7370d5cdc683bd3faca768161d36fd0186e695110dd8296ba121d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `docker:23.0-windowsservercore-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull docker@sha256:f4abd94c28bd796305168cc5169ab6b53d0a3b3a6acbcb9358fef201b9df737c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1704713998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce3edf2c8c754fd78053708b617c25ecbf40dc11501ea6c0c46daf809b630d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:40:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:35:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 24 Jun 2023 03:39:11 GMT
ENV DOCKER_VERSION=23.0.6
# Sat, 24 Jun 2023 03:39:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Sat, 24 Jun 2023 03:39:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:19:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:19:39 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:20:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:20:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:20:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:20:09 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:20:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58717a727cd3a756d7c1180dfb74e95d49735ed12628bd25d2058bc90fa96991`  
		Last Modified: Sat, 24 Jun 2023 01:20:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb210483c7a5877c9d4e754a46a0085ff94bc31d9e32e64c37e1ed4d6e30162e`  
		Last Modified: Sat, 24 Jun 2023 03:41:56 GMT  
		Size: 306.0 KB (305975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabd176de44496cc60e08f954b7d47c99eb8d47e8a4338216815756e4e9659db`  
		Last Modified: Sat, 24 Jun 2023 03:42:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b649bbc9bc70f0249f614bd545fd46c7cae1690a92cc79ea5befcd92cdcbdaa`  
		Last Modified: Sat, 24 Jun 2023 03:42:33 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16f0093a3b9ea484ba6ea7db9214d3bc0d379d6ecdd7ee3a7fdecb30b09cde0`  
		Last Modified: Sat, 24 Jun 2023 03:42:36 GMT  
		Size: 17.3 MB (17317987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389161e994c15c3e9bb0d59b881f2e66c346741b5db56f1894dcf154ffd8e59e`  
		Last Modified: Thu, 06 Jul 2023 20:22:17 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b974715fdc8e49748b7df92467cf04b846153578451a263d09f3c06ac90f5b`  
		Last Modified: Thu, 06 Jul 2023 20:22:17 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319e27cb500eb4e95dee60ceaa99ff30aeb51e0135a38bdbab4f481df68c830f`  
		Last Modified: Thu, 06 Jul 2023 20:22:17 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e96a6b06fe957b7b5ef17e1e16befe81f9c587df9834a0d8ca0ead68d0473d`  
		Last Modified: Thu, 06 Jul 2023 20:22:19 GMT  
		Size: 17.9 MB (17893316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4d4160f106ae94c6259174699128c75a96e63bbc3b5174afa88ffad72c98ba`  
		Last Modified: Thu, 06 Jul 2023 20:22:15 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92eca18e3583f1e85682cd7ecc745d64ee25a7e8fc60f7a0f4e4eedca0f19bf4`  
		Last Modified: Thu, 06 Jul 2023 20:22:15 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e41015e9e122c67f575369bb6d2953b50e0d130796923de057ee61f5466f0a90`  
		Last Modified: Thu, 06 Jul 2023 20:22:15 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3871795cc5c72b3e7a4565d36516149ce596a94b90cb00fc8b82b26d9c26e5`  
		Last Modified: Thu, 06 Jul 2023 20:22:20 GMT  
		Size: 18.4 MB (18447545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:46e697d13a25a200fd12630190cae49387192ca89c7f96111a1bf8411053ad6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1787; amd64

### `docker:23.0-windowsservercore-ltsc2022` - windows version 10.0.20348.1787; amd64

```console
$ docker pull docker@sha256:4b08c7610e6e77ecaa1a902f4b45ebd9fe846cd8fc7dc4328188ffe2e206f96d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1480297932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea8c05f68944e9c20b7c71cedb22cc24c88b4e9420984a72f54a9404d4dd9c0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:33:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 24 Jun 2023 03:37:22 GMT
ENV DOCKER_VERSION=23.0.6
# Sat, 24 Jun 2023 03:37:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Sat, 24 Jun 2023 03:37:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:18:35 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:18:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:18:37 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:19:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:19:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:19:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:19:04 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:19:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27db350c833f7fe0378bc977cd819c1ffe4133ff02ff69f1531f8ddc552c2366`  
		Last Modified: Sat, 24 Jun 2023 01:15:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c818796445a77806e10e6c159d076d6b0f5105edd8e7f27848042efb890970dd`  
		Last Modified: Sat, 24 Jun 2023 03:41:36 GMT  
		Size: 326.7 KB (326673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e4d934aedb3408d39924086e00ca7aaad6ba9093494927ec3193aafd92a20f`  
		Last Modified: Sat, 24 Jun 2023 03:42:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d47816062ca7fccecb96be7bf6468c4f36ffddd3115cf4d9bf244c0379bf7c`  
		Last Modified: Sat, 24 Jun 2023 03:42:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0520b4152b36536d9d6e0fbb761f4d738b989c5b9bc20fdcb54002f3531479b5`  
		Last Modified: Sat, 24 Jun 2023 03:42:18 GMT  
		Size: 17.3 MB (17325743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdef24df9e2be75799ec275160025462aef6bfb95360fc2907a2083128ae16b7`  
		Last Modified: Thu, 06 Jul 2023 20:22:01 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc79a9ea08518357ee22844e397fc700662ad99e4301177931c051357c2b2ec1`  
		Last Modified: Thu, 06 Jul 2023 20:22:02 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22356ed2aac9af5f5f301124bc544866e9164e843b1953a756c1339b561d671`  
		Last Modified: Thu, 06 Jul 2023 20:22:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e8c3432dbb82df56e2f5401d6af16998e13e3c34c99e49bf8c4bcd962359c8`  
		Last Modified: Thu, 06 Jul 2023 20:22:04 GMT  
		Size: 17.9 MB (17887283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466ab729826a1f27a4da2bbdf7ca5b645dc751c2f402fb5430c4db779b23360f`  
		Last Modified: Thu, 06 Jul 2023 20:22:00 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b58ed4b305ad3e911a088a311609a4eea626236698ec9a473e0f7ebafa56f3`  
		Last Modified: Thu, 06 Jul 2023 20:21:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b74996437d952638b6792afde202c442b5c8edcaf2df2272c0462cd3a2e728f`  
		Last Modified: Thu, 06 Jul 2023 20:21:59 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb948d323920d86405286636657cfe2ab8b9bc59b04009e8b75829a97ec4991`  
		Last Modified: Thu, 06 Jul 2023 20:22:04 GMT  
		Size: 18.4 MB (18447582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6`

```console
$ docker pull docker@sha256:744ae25d20431b9eccf9832fae189e43e06054b666df039b5552a46433cbe499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.6` - linux; amd64

```console
$ docker pull docker@sha256:2d036f72fa2728ddd599238453528ad1e9f4a0609ab3371f69b90fcce188b6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115841865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810c2eb4df26b8c6cb07ee900ebd168d0142553f630d7088036fc7a9cfa4d227`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbbfe9c78c82698902d2f699f3a866996d040be1686dd10f629e37d89ea33ee`  
		Last Modified: Thu, 15 Jun 2023 05:28:31 GMT  
		Size: 16.3 MB (16250874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5708dec9aea531c023a63cb6d674e4e42d94d8d84f51fcb66e9ced1c260f9e8e`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65b66e2e2892b010a1e320cecb6edff9ba98ee75b8f29eef076c7283e7a304a`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 18.0 MB (17980092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb3e3c468fa108bf2f2fec6fe9280189753b2b7ee37469941e8a688e93d499`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436c2e539760ae39be8e540fcaa7b1d1bd2fb877e8d36435eda4696d8671cea3`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed4165006f30d0eaeedeff7a3519a447de7a7f04408360003f349d6eac00de`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0c3925a01970b8b6f4b30c4ae0394f4200f55cdf177c877ae2168802ac1af1`  
		Last Modified: Thu, 06 Jul 2023 20:22:44 GMT  
		Size: 7.1 MB (7080604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd90aaca53b9d97ecf639fdb1778a1b1916e3147ff0a2ac84d6b147d1716d9ea`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce803b02ed3e4ed43bd7c6ab9ba5562ccecbe574b1d6e06252d1475cd28b9e8`  
		Last Modified: Thu, 06 Jul 2023 20:22:50 GMT  
		Size: 51.7 MB (51657476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe710e1a3eab28e7bc6596ef135bba1ed104de7cd599ed563fcbee8eee777f9`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8189afb935336899691d8ca85748fd24ec7045a0f1d9ccad361e14df8e84f61b`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 2.8 KB (2790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.6` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7a17e1adde579f7913a1d5dd4411094f9becfb0320db66d280a26a09b7eb9c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107103059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e2bc332c22f7586e25665430021c48e8bf8f10c1e9ec574a05034a99fb50b8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51d2d067e69a1f5a948d2d1133441f75a192e5bcc4154ca7be51943ff4a24d5`  
		Last Modified: Wed, 14 Jun 2023 22:42:12 GMT  
		Size: 15.3 MB (15325099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f28a2d02144ee951238b5623115d8fe18645df105f9e258b004975a591788`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 15.8 MB (15759517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc821c9da813150074e2cdd9b1099f1ea4305b04232851161a942a0cff4ab7`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 16.3 MB (16312968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b312f8beda3531c97f8edbf8ba090359914ca1508325250ff3262cd64f386635`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212d8b0184b5e16c4fd2f221bbdac88bbec8f94f632ff8ae1997332cf161ef37`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa6cbfc4ca5d773f84f56574cc994db7b86481df32126e0f0b9bcc8e7a33f87`  
		Last Modified: Thu, 06 Jul 2023 19:43:50 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b5774c046c118941ffdd7940de95e7371426fed92f8f27cb2587d4dddcc2c2`  
		Last Modified: Thu, 06 Jul 2023 19:44:05 GMT  
		Size: 7.3 MB (7291362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accf38e0a7857aa4882234dae62ba6cc1ecf9a987234b2eb10476cbc56cd701b`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fe37bb22c274be66fca87ae65085ab0a4b07ec499f6c8da99e0687d8dea17e`  
		Last Modified: Thu, 06 Jul 2023 19:44:09 GMT  
		Size: 47.1 MB (47053345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acd2d702cadc0b2a4f3272301e99216dbbfca7534826bf448015df6463954df`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53635b71f6ec66afb091ea2ae377ba957cfa8e4b8c0e4ff8d41bb157cc33d5b5`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6-alpine3.18`

```console
$ docker pull docker@sha256:744ae25d20431b9eccf9832fae189e43e06054b666df039b5552a46433cbe499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.6-alpine3.18` - linux; amd64

```console
$ docker pull docker@sha256:2d036f72fa2728ddd599238453528ad1e9f4a0609ab3371f69b90fcce188b6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115841865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810c2eb4df26b8c6cb07ee900ebd168d0142553f630d7088036fc7a9cfa4d227`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbbfe9c78c82698902d2f699f3a866996d040be1686dd10f629e37d89ea33ee`  
		Last Modified: Thu, 15 Jun 2023 05:28:31 GMT  
		Size: 16.3 MB (16250874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5708dec9aea531c023a63cb6d674e4e42d94d8d84f51fcb66e9ced1c260f9e8e`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65b66e2e2892b010a1e320cecb6edff9ba98ee75b8f29eef076c7283e7a304a`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 18.0 MB (17980092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb3e3c468fa108bf2f2fec6fe9280189753b2b7ee37469941e8a688e93d499`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436c2e539760ae39be8e540fcaa7b1d1bd2fb877e8d36435eda4696d8671cea3`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed4165006f30d0eaeedeff7a3519a447de7a7f04408360003f349d6eac00de`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0c3925a01970b8b6f4b30c4ae0394f4200f55cdf177c877ae2168802ac1af1`  
		Last Modified: Thu, 06 Jul 2023 20:22:44 GMT  
		Size: 7.1 MB (7080604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd90aaca53b9d97ecf639fdb1778a1b1916e3147ff0a2ac84d6b147d1716d9ea`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce803b02ed3e4ed43bd7c6ab9ba5562ccecbe574b1d6e06252d1475cd28b9e8`  
		Last Modified: Thu, 06 Jul 2023 20:22:50 GMT  
		Size: 51.7 MB (51657476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe710e1a3eab28e7bc6596ef135bba1ed104de7cd599ed563fcbee8eee777f9`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8189afb935336899691d8ca85748fd24ec7045a0f1d9ccad361e14df8e84f61b`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 2.8 KB (2790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.6-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7a17e1adde579f7913a1d5dd4411094f9becfb0320db66d280a26a09b7eb9c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107103059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e2bc332c22f7586e25665430021c48e8bf8f10c1e9ec574a05034a99fb50b8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51d2d067e69a1f5a948d2d1133441f75a192e5bcc4154ca7be51943ff4a24d5`  
		Last Modified: Wed, 14 Jun 2023 22:42:12 GMT  
		Size: 15.3 MB (15325099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f28a2d02144ee951238b5623115d8fe18645df105f9e258b004975a591788`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 15.8 MB (15759517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc821c9da813150074e2cdd9b1099f1ea4305b04232851161a942a0cff4ab7`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 16.3 MB (16312968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b312f8beda3531c97f8edbf8ba090359914ca1508325250ff3262cd64f386635`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212d8b0184b5e16c4fd2f221bbdac88bbec8f94f632ff8ae1997332cf161ef37`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa6cbfc4ca5d773f84f56574cc994db7b86481df32126e0f0b9bcc8e7a33f87`  
		Last Modified: Thu, 06 Jul 2023 19:43:50 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b5774c046c118941ffdd7940de95e7371426fed92f8f27cb2587d4dddcc2c2`  
		Last Modified: Thu, 06 Jul 2023 19:44:05 GMT  
		Size: 7.3 MB (7291362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accf38e0a7857aa4882234dae62ba6cc1ecf9a987234b2eb10476cbc56cd701b`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fe37bb22c274be66fca87ae65085ab0a4b07ec499f6c8da99e0687d8dea17e`  
		Last Modified: Thu, 06 Jul 2023 19:44:09 GMT  
		Size: 47.1 MB (47053345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acd2d702cadc0b2a4f3272301e99216dbbfca7534826bf448015df6463954df`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53635b71f6ec66afb091ea2ae377ba957cfa8e4b8c0e4ff8d41bb157cc33d5b5`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6-cli`

```console
$ docker pull docker@sha256:f233d64cf3968d36c794b0354dde961256cccca2e3e4ebd51eaff3b15caf8fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.6-cli` - linux; amd64

```console
$ docker pull docker@sha256:3ead83ab52c1d056fd65655d97797494b34383a6e062b80976f80f1691db62e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57098627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af26fe8bcb5b1a2b8e6b185d9a8fd75d932b97c1faa729bca3a932af8b1271f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbbfe9c78c82698902d2f699f3a866996d040be1686dd10f629e37d89ea33ee`  
		Last Modified: Thu, 15 Jun 2023 05:28:31 GMT  
		Size: 16.3 MB (16250874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5708dec9aea531c023a63cb6d674e4e42d94d8d84f51fcb66e9ced1c260f9e8e`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65b66e2e2892b010a1e320cecb6edff9ba98ee75b8f29eef076c7283e7a304a`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 18.0 MB (17980092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb3e3c468fa108bf2f2fec6fe9280189753b2b7ee37469941e8a688e93d499`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436c2e539760ae39be8e540fcaa7b1d1bd2fb877e8d36435eda4696d8671cea3`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed4165006f30d0eaeedeff7a3519a447de7a7f04408360003f349d6eac00de`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.6-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d39267d642857eadb6106a70304967b2e7b9c71e31bf722e55ca2d107aa84bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52753194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0660417e68d2e9295da7a725dcde7983a789e8dca5dd992d3c4bdc52b19d908`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51d2d067e69a1f5a948d2d1133441f75a192e5bcc4154ca7be51943ff4a24d5`  
		Last Modified: Wed, 14 Jun 2023 22:42:12 GMT  
		Size: 15.3 MB (15325099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f28a2d02144ee951238b5623115d8fe18645df105f9e258b004975a591788`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 15.8 MB (15759517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc821c9da813150074e2cdd9b1099f1ea4305b04232851161a942a0cff4ab7`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 16.3 MB (16312968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b312f8beda3531c97f8edbf8ba090359914ca1508325250ff3262cd64f386635`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212d8b0184b5e16c4fd2f221bbdac88bbec8f94f632ff8ae1997332cf161ef37`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa6cbfc4ca5d773f84f56574cc994db7b86481df32126e0f0b9bcc8e7a33f87`  
		Last Modified: Thu, 06 Jul 2023 19:43:50 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6-cli-alpine3.18`

```console
$ docker pull docker@sha256:f233d64cf3968d36c794b0354dde961256cccca2e3e4ebd51eaff3b15caf8fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.6-cli-alpine3.18` - linux; amd64

```console
$ docker pull docker@sha256:3ead83ab52c1d056fd65655d97797494b34383a6e062b80976f80f1691db62e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57098627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af26fe8bcb5b1a2b8e6b185d9a8fd75d932b97c1faa729bca3a932af8b1271f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbbfe9c78c82698902d2f699f3a866996d040be1686dd10f629e37d89ea33ee`  
		Last Modified: Thu, 15 Jun 2023 05:28:31 GMT  
		Size: 16.3 MB (16250874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5708dec9aea531c023a63cb6d674e4e42d94d8d84f51fcb66e9ced1c260f9e8e`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65b66e2e2892b010a1e320cecb6edff9ba98ee75b8f29eef076c7283e7a304a`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 18.0 MB (17980092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb3e3c468fa108bf2f2fec6fe9280189753b2b7ee37469941e8a688e93d499`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436c2e539760ae39be8e540fcaa7b1d1bd2fb877e8d36435eda4696d8671cea3`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed4165006f30d0eaeedeff7a3519a447de7a7f04408360003f349d6eac00de`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.6-cli-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d39267d642857eadb6106a70304967b2e7b9c71e31bf722e55ca2d107aa84bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52753194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0660417e68d2e9295da7a725dcde7983a789e8dca5dd992d3c4bdc52b19d908`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51d2d067e69a1f5a948d2d1133441f75a192e5bcc4154ca7be51943ff4a24d5`  
		Last Modified: Wed, 14 Jun 2023 22:42:12 GMT  
		Size: 15.3 MB (15325099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f28a2d02144ee951238b5623115d8fe18645df105f9e258b004975a591788`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 15.8 MB (15759517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc821c9da813150074e2cdd9b1099f1ea4305b04232851161a942a0cff4ab7`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 16.3 MB (16312968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b312f8beda3531c97f8edbf8ba090359914ca1508325250ff3262cd64f386635`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212d8b0184b5e16c4fd2f221bbdac88bbec8f94f632ff8ae1997332cf161ef37`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa6cbfc4ca5d773f84f56574cc994db7b86481df32126e0f0b9bcc8e7a33f87`  
		Last Modified: Thu, 06 Jul 2023 19:43:50 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6-dind`

```console
$ docker pull docker@sha256:744ae25d20431b9eccf9832fae189e43e06054b666df039b5552a46433cbe499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.6-dind` - linux; amd64

```console
$ docker pull docker@sha256:2d036f72fa2728ddd599238453528ad1e9f4a0609ab3371f69b90fcce188b6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115841865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810c2eb4df26b8c6cb07ee900ebd168d0142553f630d7088036fc7a9cfa4d227`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbbfe9c78c82698902d2f699f3a866996d040be1686dd10f629e37d89ea33ee`  
		Last Modified: Thu, 15 Jun 2023 05:28:31 GMT  
		Size: 16.3 MB (16250874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5708dec9aea531c023a63cb6d674e4e42d94d8d84f51fcb66e9ced1c260f9e8e`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65b66e2e2892b010a1e320cecb6edff9ba98ee75b8f29eef076c7283e7a304a`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 18.0 MB (17980092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb3e3c468fa108bf2f2fec6fe9280189753b2b7ee37469941e8a688e93d499`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436c2e539760ae39be8e540fcaa7b1d1bd2fb877e8d36435eda4696d8671cea3`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed4165006f30d0eaeedeff7a3519a447de7a7f04408360003f349d6eac00de`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0c3925a01970b8b6f4b30c4ae0394f4200f55cdf177c877ae2168802ac1af1`  
		Last Modified: Thu, 06 Jul 2023 20:22:44 GMT  
		Size: 7.1 MB (7080604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd90aaca53b9d97ecf639fdb1778a1b1916e3147ff0a2ac84d6b147d1716d9ea`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce803b02ed3e4ed43bd7c6ab9ba5562ccecbe574b1d6e06252d1475cd28b9e8`  
		Last Modified: Thu, 06 Jul 2023 20:22:50 GMT  
		Size: 51.7 MB (51657476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe710e1a3eab28e7bc6596ef135bba1ed104de7cd599ed563fcbee8eee777f9`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8189afb935336899691d8ca85748fd24ec7045a0f1d9ccad361e14df8e84f61b`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 2.8 KB (2790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.6-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7a17e1adde579f7913a1d5dd4411094f9becfb0320db66d280a26a09b7eb9c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107103059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e2bc332c22f7586e25665430021c48e8bf8f10c1e9ec574a05034a99fb50b8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51d2d067e69a1f5a948d2d1133441f75a192e5bcc4154ca7be51943ff4a24d5`  
		Last Modified: Wed, 14 Jun 2023 22:42:12 GMT  
		Size: 15.3 MB (15325099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f28a2d02144ee951238b5623115d8fe18645df105f9e258b004975a591788`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 15.8 MB (15759517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc821c9da813150074e2cdd9b1099f1ea4305b04232851161a942a0cff4ab7`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 16.3 MB (16312968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b312f8beda3531c97f8edbf8ba090359914ca1508325250ff3262cd64f386635`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212d8b0184b5e16c4fd2f221bbdac88bbec8f94f632ff8ae1997332cf161ef37`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa6cbfc4ca5d773f84f56574cc994db7b86481df32126e0f0b9bcc8e7a33f87`  
		Last Modified: Thu, 06 Jul 2023 19:43:50 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b5774c046c118941ffdd7940de95e7371426fed92f8f27cb2587d4dddcc2c2`  
		Last Modified: Thu, 06 Jul 2023 19:44:05 GMT  
		Size: 7.3 MB (7291362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accf38e0a7857aa4882234dae62ba6cc1ecf9a987234b2eb10476cbc56cd701b`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fe37bb22c274be66fca87ae65085ab0a4b07ec499f6c8da99e0687d8dea17e`  
		Last Modified: Thu, 06 Jul 2023 19:44:09 GMT  
		Size: 47.1 MB (47053345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acd2d702cadc0b2a4f3272301e99216dbbfca7534826bf448015df6463954df`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53635b71f6ec66afb091ea2ae377ba957cfa8e4b8c0e4ff8d41bb157cc33d5b5`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6-dind-alpine3.18`

```console
$ docker pull docker@sha256:744ae25d20431b9eccf9832fae189e43e06054b666df039b5552a46433cbe499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.6-dind-alpine3.18` - linux; amd64

```console
$ docker pull docker@sha256:2d036f72fa2728ddd599238453528ad1e9f4a0609ab3371f69b90fcce188b6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115841865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810c2eb4df26b8c6cb07ee900ebd168d0142553f630d7088036fc7a9cfa4d227`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbbfe9c78c82698902d2f699f3a866996d040be1686dd10f629e37d89ea33ee`  
		Last Modified: Thu, 15 Jun 2023 05:28:31 GMT  
		Size: 16.3 MB (16250874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5708dec9aea531c023a63cb6d674e4e42d94d8d84f51fcb66e9ced1c260f9e8e`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65b66e2e2892b010a1e320cecb6edff9ba98ee75b8f29eef076c7283e7a304a`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 18.0 MB (17980092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb3e3c468fa108bf2f2fec6fe9280189753b2b7ee37469941e8a688e93d499`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436c2e539760ae39be8e540fcaa7b1d1bd2fb877e8d36435eda4696d8671cea3`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed4165006f30d0eaeedeff7a3519a447de7a7f04408360003f349d6eac00de`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0c3925a01970b8b6f4b30c4ae0394f4200f55cdf177c877ae2168802ac1af1`  
		Last Modified: Thu, 06 Jul 2023 20:22:44 GMT  
		Size: 7.1 MB (7080604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd90aaca53b9d97ecf639fdb1778a1b1916e3147ff0a2ac84d6b147d1716d9ea`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce803b02ed3e4ed43bd7c6ab9ba5562ccecbe574b1d6e06252d1475cd28b9e8`  
		Last Modified: Thu, 06 Jul 2023 20:22:50 GMT  
		Size: 51.7 MB (51657476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe710e1a3eab28e7bc6596ef135bba1ed104de7cd599ed563fcbee8eee777f9`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8189afb935336899691d8ca85748fd24ec7045a0f1d9ccad361e14df8e84f61b`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 2.8 KB (2790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.6-dind-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7a17e1adde579f7913a1d5dd4411094f9becfb0320db66d280a26a09b7eb9c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107103059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e2bc332c22f7586e25665430021c48e8bf8f10c1e9ec574a05034a99fb50b8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51d2d067e69a1f5a948d2d1133441f75a192e5bcc4154ca7be51943ff4a24d5`  
		Last Modified: Wed, 14 Jun 2023 22:42:12 GMT  
		Size: 15.3 MB (15325099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f28a2d02144ee951238b5623115d8fe18645df105f9e258b004975a591788`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 15.8 MB (15759517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc821c9da813150074e2cdd9b1099f1ea4305b04232851161a942a0cff4ab7`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 16.3 MB (16312968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b312f8beda3531c97f8edbf8ba090359914ca1508325250ff3262cd64f386635`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212d8b0184b5e16c4fd2f221bbdac88bbec8f94f632ff8ae1997332cf161ef37`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa6cbfc4ca5d773f84f56574cc994db7b86481df32126e0f0b9bcc8e7a33f87`  
		Last Modified: Thu, 06 Jul 2023 19:43:50 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b5774c046c118941ffdd7940de95e7371426fed92f8f27cb2587d4dddcc2c2`  
		Last Modified: Thu, 06 Jul 2023 19:44:05 GMT  
		Size: 7.3 MB (7291362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accf38e0a7857aa4882234dae62ba6cc1ecf9a987234b2eb10476cbc56cd701b`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fe37bb22c274be66fca87ae65085ab0a4b07ec499f6c8da99e0687d8dea17e`  
		Last Modified: Thu, 06 Jul 2023 19:44:09 GMT  
		Size: 47.1 MB (47053345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acd2d702cadc0b2a4f3272301e99216dbbfca7534826bf448015df6463954df`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53635b71f6ec66afb091ea2ae377ba957cfa8e4b8c0e4ff8d41bb157cc33d5b5`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6-dind-rootless`

```console
$ docker pull docker@sha256:d72b65560351d3f141e9c5347d3f7e0289e1406d092d2571f1990ef48a67ad22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.6-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ab0ea6c0db98c62f962965d7de25509ddd8b7e9b48425901d61be736771a9bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137553077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38074c9fc8d6dfc4989a320e785d10807ec73758d1f9ece9c6f010263bfc56f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 16 May 2023 17:59:38 GMT
USER rootless
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbbfe9c78c82698902d2f699f3a866996d040be1686dd10f629e37d89ea33ee`  
		Last Modified: Thu, 15 Jun 2023 05:28:31 GMT  
		Size: 16.3 MB (16250874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5708dec9aea531c023a63cb6d674e4e42d94d8d84f51fcb66e9ced1c260f9e8e`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65b66e2e2892b010a1e320cecb6edff9ba98ee75b8f29eef076c7283e7a304a`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 18.0 MB (17980092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb3e3c468fa108bf2f2fec6fe9280189753b2b7ee37469941e8a688e93d499`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436c2e539760ae39be8e540fcaa7b1d1bd2fb877e8d36435eda4696d8671cea3`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed4165006f30d0eaeedeff7a3519a447de7a7f04408360003f349d6eac00de`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0c3925a01970b8b6f4b30c4ae0394f4200f55cdf177c877ae2168802ac1af1`  
		Last Modified: Thu, 06 Jul 2023 20:22:44 GMT  
		Size: 7.1 MB (7080604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd90aaca53b9d97ecf639fdb1778a1b1916e3147ff0a2ac84d6b147d1716d9ea`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce803b02ed3e4ed43bd7c6ab9ba5562ccecbe574b1d6e06252d1475cd28b9e8`  
		Last Modified: Thu, 06 Jul 2023 20:22:50 GMT  
		Size: 51.7 MB (51657476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe710e1a3eab28e7bc6596ef135bba1ed104de7cd599ed563fcbee8eee777f9`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8189afb935336899691d8ca85748fd24ec7045a0f1d9ccad361e14df8e84f61b`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 2.8 KB (2790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6230ff53f18c93c4a624bc8b1bd4e9b37917858576bb6bf7b2517e8234f13cf9`  
		Last Modified: Thu, 06 Jul 2023 20:23:15 GMT  
		Size: 1.4 MB (1362367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408ece9af5d25bd78a674ed3ef3f80cff66c0a767623748ccfd459561b834851`  
		Last Modified: Thu, 06 Jul 2023 20:23:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117f4f867ffe3f026946370181fcfe14820945807abe76b348243742c06e3672`  
		Last Modified: Thu, 06 Jul 2023 20:23:15 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edc62e51203e88508a6917f502d99673a58a8c375186a5445823c5e3b302e23`  
		Last Modified: Thu, 06 Jul 2023 20:23:18 GMT  
		Size: 20.3 MB (20347105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ff9f47195acd13e38adddd06b93bc5aae41f1626456905ebc5994bedc60f65`  
		Last Modified: Thu, 06 Jul 2023 20:23:15 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.6-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:501d9df4431674be20300e0a971aa665820b43564ad84ea14c18fbb5f21c8aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130759048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8aa08b3f258d7c85e3cca459f450f6fe424d614a34ee27035739b02c1c7fc8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 16 May 2023 17:59:38 GMT
USER rootless
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51d2d067e69a1f5a948d2d1133441f75a192e5bcc4154ca7be51943ff4a24d5`  
		Last Modified: Wed, 14 Jun 2023 22:42:12 GMT  
		Size: 15.3 MB (15325099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f28a2d02144ee951238b5623115d8fe18645df105f9e258b004975a591788`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 15.8 MB (15759517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc821c9da813150074e2cdd9b1099f1ea4305b04232851161a942a0cff4ab7`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 16.3 MB (16312968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b312f8beda3531c97f8edbf8ba090359914ca1508325250ff3262cd64f386635`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212d8b0184b5e16c4fd2f221bbdac88bbec8f94f632ff8ae1997332cf161ef37`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa6cbfc4ca5d773f84f56574cc994db7b86481df32126e0f0b9bcc8e7a33f87`  
		Last Modified: Thu, 06 Jul 2023 19:43:50 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b5774c046c118941ffdd7940de95e7371426fed92f8f27cb2587d4dddcc2c2`  
		Last Modified: Thu, 06 Jul 2023 19:44:05 GMT  
		Size: 7.3 MB (7291362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accf38e0a7857aa4882234dae62ba6cc1ecf9a987234b2eb10476cbc56cd701b`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fe37bb22c274be66fca87ae65085ab0a4b07ec499f6c8da99e0687d8dea17e`  
		Last Modified: Thu, 06 Jul 2023 19:44:09 GMT  
		Size: 47.1 MB (47053345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acd2d702cadc0b2a4f3272301e99216dbbfca7534826bf448015df6463954df`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53635b71f6ec66afb091ea2ae377ba957cfa8e4b8c0e4ff8d41bb157cc33d5b5`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c844a7243a0e537041a413b83b62a9ac6b95bf62b82c214edd944b0aa1d6016`  
		Last Modified: Thu, 06 Jul 2023 19:44:33 GMT  
		Size: 1.4 MB (1413250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39050000c34c799394809969e7bec9f3ae5307b0bf314f20b8aa6f43d6de3059`  
		Last Modified: Thu, 06 Jul 2023 19:44:32 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3548b5070aef57c8d9b4a8036d68869d662f3cfe4f60b1fdc2f3b004f504ac96`  
		Last Modified: Thu, 06 Jul 2023 19:44:32 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186d8f9b8f46c83c9aae60b5e8cd43468f600fedacbb82390a8aa41d4b340a04`  
		Last Modified: Thu, 06 Jul 2023 19:44:35 GMT  
		Size: 22.2 MB (22240999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff355f3f3ab86a69f7607c4556b4bc4bb7f70efc1a817f3696858af9bca2db20`  
		Last Modified: Thu, 06 Jul 2023 19:44:32 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6-git`

```console
$ docker pull docker@sha256:937e04616ae1907a4ccbbec58d09314ed3341dfbbc298798565d4348f2000b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.6-git` - linux; amd64

```console
$ docker pull docker@sha256:799dc31980d9fba48ccfdf94a6c2629bfbc781863cadc3cd49648a7ee5e50596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120776607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74c22e0f162a0f25996dd4f7660930512ef8234f92a4e569d08d5a5b5193d06`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbbfe9c78c82698902d2f699f3a866996d040be1686dd10f629e37d89ea33ee`  
		Last Modified: Thu, 15 Jun 2023 05:28:31 GMT  
		Size: 16.3 MB (16250874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5708dec9aea531c023a63cb6d674e4e42d94d8d84f51fcb66e9ced1c260f9e8e`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65b66e2e2892b010a1e320cecb6edff9ba98ee75b8f29eef076c7283e7a304a`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 18.0 MB (17980092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdb3e3c468fa108bf2f2fec6fe9280189753b2b7ee37469941e8a688e93d499`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436c2e539760ae39be8e540fcaa7b1d1bd2fb877e8d36435eda4696d8671cea3`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed4165006f30d0eaeedeff7a3519a447de7a7f04408360003f349d6eac00de`  
		Last Modified: Thu, 06 Jul 2023 20:22:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0c3925a01970b8b6f4b30c4ae0394f4200f55cdf177c877ae2168802ac1af1`  
		Last Modified: Thu, 06 Jul 2023 20:22:44 GMT  
		Size: 7.1 MB (7080604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd90aaca53b9d97ecf639fdb1778a1b1916e3147ff0a2ac84d6b147d1716d9ea`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce803b02ed3e4ed43bd7c6ab9ba5562ccecbe574b1d6e06252d1475cd28b9e8`  
		Last Modified: Thu, 06 Jul 2023 20:22:50 GMT  
		Size: 51.7 MB (51657476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe710e1a3eab28e7bc6596ef135bba1ed104de7cd599ed563fcbee8eee777f9`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8189afb935336899691d8ca85748fd24ec7045a0f1d9ccad361e14df8e84f61b`  
		Last Modified: Thu, 06 Jul 2023 20:22:43 GMT  
		Size: 2.8 KB (2790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47db942abd1a5e7aaa96943c00a80dd34d9b8ad048680f169c7ad995d0004b7`  
		Last Modified: Thu, 06 Jul 2023 20:23:32 GMT  
		Size: 4.9 MB (4934742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.6-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f386ae6dd346abeb7f481719b53c3c7f2adb150c62b75c3b3ed3d070b8e1d9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112124141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a206b4fb14701c8db4057df2435babcf9e3f3ac4799c04f7b7c0b2215271ea92`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Wed, 05 Jul 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jul 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jul 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jul 2023 23:04:13 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:04:12 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:04:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:04:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:04:12 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:04:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:04:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:04:12 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51d2d067e69a1f5a948d2d1133441f75a192e5bcc4154ca7be51943ff4a24d5`  
		Last Modified: Wed, 14 Jun 2023 22:42:12 GMT  
		Size: 15.3 MB (15325099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f28a2d02144ee951238b5623115d8fe18645df105f9e258b004975a591788`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 15.8 MB (15759517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc821c9da813150074e2cdd9b1099f1ea4305b04232851161a942a0cff4ab7`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 16.3 MB (16312968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b312f8beda3531c97f8edbf8ba090359914ca1508325250ff3262cd64f386635`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212d8b0184b5e16c4fd2f221bbdac88bbec8f94f632ff8ae1997332cf161ef37`  
		Last Modified: Thu, 06 Jul 2023 19:43:49 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa6cbfc4ca5d773f84f56574cc994db7b86481df32126e0f0b9bcc8e7a33f87`  
		Last Modified: Thu, 06 Jul 2023 19:43:50 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b5774c046c118941ffdd7940de95e7371426fed92f8f27cb2587d4dddcc2c2`  
		Last Modified: Thu, 06 Jul 2023 19:44:05 GMT  
		Size: 7.3 MB (7291362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accf38e0a7857aa4882234dae62ba6cc1ecf9a987234b2eb10476cbc56cd701b`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fe37bb22c274be66fca87ae65085ab0a4b07ec499f6c8da99e0687d8dea17e`  
		Last Modified: Thu, 06 Jul 2023 19:44:09 GMT  
		Size: 47.1 MB (47053345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acd2d702cadc0b2a4f3272301e99216dbbfca7534826bf448015df6463954df`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53635b71f6ec66afb091ea2ae377ba957cfa8e4b8c0e4ff8d41bb157cc33d5b5`  
		Last Modified: Thu, 06 Jul 2023 19:44:04 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3397c031c86d20662e77466a69635249b12fdfa5544cc8b292e65fedb2f70f`  
		Last Modified: Thu, 06 Jul 2023 19:44:47 GMT  
		Size: 5.0 MB (5021082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6-windowsservercore`

```console
$ docker pull docker@sha256:796d95a96cb9faea174f2b482e2886b3d9d082621b814ecb064ba559d8431e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1787; amd64
	-	windows version 10.0.17763.4499; amd64

### `docker:23.0.6-windowsservercore` - windows version 10.0.20348.1787; amd64

```console
$ docker pull docker@sha256:4b08c7610e6e77ecaa1a902f4b45ebd9fe846cd8fc7dc4328188ffe2e206f96d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1480297932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea8c05f68944e9c20b7c71cedb22cc24c88b4e9420984a72f54a9404d4dd9c0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:33:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 24 Jun 2023 03:37:22 GMT
ENV DOCKER_VERSION=23.0.6
# Sat, 24 Jun 2023 03:37:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Sat, 24 Jun 2023 03:37:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:18:35 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:18:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:18:37 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:19:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:19:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:19:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:19:04 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:19:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27db350c833f7fe0378bc977cd819c1ffe4133ff02ff69f1531f8ddc552c2366`  
		Last Modified: Sat, 24 Jun 2023 01:15:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c818796445a77806e10e6c159d076d6b0f5105edd8e7f27848042efb890970dd`  
		Last Modified: Sat, 24 Jun 2023 03:41:36 GMT  
		Size: 326.7 KB (326673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e4d934aedb3408d39924086e00ca7aaad6ba9093494927ec3193aafd92a20f`  
		Last Modified: Sat, 24 Jun 2023 03:42:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d47816062ca7fccecb96be7bf6468c4f36ffddd3115cf4d9bf244c0379bf7c`  
		Last Modified: Sat, 24 Jun 2023 03:42:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0520b4152b36536d9d6e0fbb761f4d738b989c5b9bc20fdcb54002f3531479b5`  
		Last Modified: Sat, 24 Jun 2023 03:42:18 GMT  
		Size: 17.3 MB (17325743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdef24df9e2be75799ec275160025462aef6bfb95360fc2907a2083128ae16b7`  
		Last Modified: Thu, 06 Jul 2023 20:22:01 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc79a9ea08518357ee22844e397fc700662ad99e4301177931c051357c2b2ec1`  
		Last Modified: Thu, 06 Jul 2023 20:22:02 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22356ed2aac9af5f5f301124bc544866e9164e843b1953a756c1339b561d671`  
		Last Modified: Thu, 06 Jul 2023 20:22:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e8c3432dbb82df56e2f5401d6af16998e13e3c34c99e49bf8c4bcd962359c8`  
		Last Modified: Thu, 06 Jul 2023 20:22:04 GMT  
		Size: 17.9 MB (17887283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466ab729826a1f27a4da2bbdf7ca5b645dc751c2f402fb5430c4db779b23360f`  
		Last Modified: Thu, 06 Jul 2023 20:22:00 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b58ed4b305ad3e911a088a311609a4eea626236698ec9a473e0f7ebafa56f3`  
		Last Modified: Thu, 06 Jul 2023 20:21:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b74996437d952638b6792afde202c442b5c8edcaf2df2272c0462cd3a2e728f`  
		Last Modified: Thu, 06 Jul 2023 20:21:59 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb948d323920d86405286636657cfe2ab8b9bc59b04009e8b75829a97ec4991`  
		Last Modified: Thu, 06 Jul 2023 20:22:04 GMT  
		Size: 18.4 MB (18447582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.6-windowsservercore` - windows version 10.0.17763.4499; amd64

```console
$ docker pull docker@sha256:f4abd94c28bd796305168cc5169ab6b53d0a3b3a6acbcb9358fef201b9df737c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1704713998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce3edf2c8c754fd78053708b617c25ecbf40dc11501ea6c0c46daf809b630d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:40:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:35:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 24 Jun 2023 03:39:11 GMT
ENV DOCKER_VERSION=23.0.6
# Sat, 24 Jun 2023 03:39:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Sat, 24 Jun 2023 03:39:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:19:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:19:39 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:20:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:20:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:20:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:20:09 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:20:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58717a727cd3a756d7c1180dfb74e95d49735ed12628bd25d2058bc90fa96991`  
		Last Modified: Sat, 24 Jun 2023 01:20:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb210483c7a5877c9d4e754a46a0085ff94bc31d9e32e64c37e1ed4d6e30162e`  
		Last Modified: Sat, 24 Jun 2023 03:41:56 GMT  
		Size: 306.0 KB (305975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabd176de44496cc60e08f954b7d47c99eb8d47e8a4338216815756e4e9659db`  
		Last Modified: Sat, 24 Jun 2023 03:42:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b649bbc9bc70f0249f614bd545fd46c7cae1690a92cc79ea5befcd92cdcbdaa`  
		Last Modified: Sat, 24 Jun 2023 03:42:33 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16f0093a3b9ea484ba6ea7db9214d3bc0d379d6ecdd7ee3a7fdecb30b09cde0`  
		Last Modified: Sat, 24 Jun 2023 03:42:36 GMT  
		Size: 17.3 MB (17317987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389161e994c15c3e9bb0d59b881f2e66c346741b5db56f1894dcf154ffd8e59e`  
		Last Modified: Thu, 06 Jul 2023 20:22:17 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b974715fdc8e49748b7df92467cf04b846153578451a263d09f3c06ac90f5b`  
		Last Modified: Thu, 06 Jul 2023 20:22:17 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319e27cb500eb4e95dee60ceaa99ff30aeb51e0135a38bdbab4f481df68c830f`  
		Last Modified: Thu, 06 Jul 2023 20:22:17 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e96a6b06fe957b7b5ef17e1e16befe81f9c587df9834a0d8ca0ead68d0473d`  
		Last Modified: Thu, 06 Jul 2023 20:22:19 GMT  
		Size: 17.9 MB (17893316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4d4160f106ae94c6259174699128c75a96e63bbc3b5174afa88ffad72c98ba`  
		Last Modified: Thu, 06 Jul 2023 20:22:15 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92eca18e3583f1e85682cd7ecc745d64ee25a7e8fc60f7a0f4e4eedca0f19bf4`  
		Last Modified: Thu, 06 Jul 2023 20:22:15 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e41015e9e122c67f575369bb6d2953b50e0d130796923de057ee61f5466f0a90`  
		Last Modified: Thu, 06 Jul 2023 20:22:15 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3871795cc5c72b3e7a4565d36516149ce596a94b90cb00fc8b82b26d9c26e5`  
		Last Modified: Thu, 06 Jul 2023 20:22:20 GMT  
		Size: 18.4 MB (18447545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6-windowsservercore-1809`

```console
$ docker pull docker@sha256:eb129c605ee7370d5cdc683bd3faca768161d36fd0186e695110dd8296ba121d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `docker:23.0.6-windowsservercore-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull docker@sha256:f4abd94c28bd796305168cc5169ab6b53d0a3b3a6acbcb9358fef201b9df737c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1704713998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce3edf2c8c754fd78053708b617c25ecbf40dc11501ea6c0c46daf809b630d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:40:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:35:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 24 Jun 2023 03:39:11 GMT
ENV DOCKER_VERSION=23.0.6
# Sat, 24 Jun 2023 03:39:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Sat, 24 Jun 2023 03:39:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:19:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:19:39 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:20:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:20:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:20:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:20:09 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:20:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58717a727cd3a756d7c1180dfb74e95d49735ed12628bd25d2058bc90fa96991`  
		Last Modified: Sat, 24 Jun 2023 01:20:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb210483c7a5877c9d4e754a46a0085ff94bc31d9e32e64c37e1ed4d6e30162e`  
		Last Modified: Sat, 24 Jun 2023 03:41:56 GMT  
		Size: 306.0 KB (305975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabd176de44496cc60e08f954b7d47c99eb8d47e8a4338216815756e4e9659db`  
		Last Modified: Sat, 24 Jun 2023 03:42:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b649bbc9bc70f0249f614bd545fd46c7cae1690a92cc79ea5befcd92cdcbdaa`  
		Last Modified: Sat, 24 Jun 2023 03:42:33 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16f0093a3b9ea484ba6ea7db9214d3bc0d379d6ecdd7ee3a7fdecb30b09cde0`  
		Last Modified: Sat, 24 Jun 2023 03:42:36 GMT  
		Size: 17.3 MB (17317987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389161e994c15c3e9bb0d59b881f2e66c346741b5db56f1894dcf154ffd8e59e`  
		Last Modified: Thu, 06 Jul 2023 20:22:17 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b974715fdc8e49748b7df92467cf04b846153578451a263d09f3c06ac90f5b`  
		Last Modified: Thu, 06 Jul 2023 20:22:17 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319e27cb500eb4e95dee60ceaa99ff30aeb51e0135a38bdbab4f481df68c830f`  
		Last Modified: Thu, 06 Jul 2023 20:22:17 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e96a6b06fe957b7b5ef17e1e16befe81f9c587df9834a0d8ca0ead68d0473d`  
		Last Modified: Thu, 06 Jul 2023 20:22:19 GMT  
		Size: 17.9 MB (17893316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4d4160f106ae94c6259174699128c75a96e63bbc3b5174afa88ffad72c98ba`  
		Last Modified: Thu, 06 Jul 2023 20:22:15 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92eca18e3583f1e85682cd7ecc745d64ee25a7e8fc60f7a0f4e4eedca0f19bf4`  
		Last Modified: Thu, 06 Jul 2023 20:22:15 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e41015e9e122c67f575369bb6d2953b50e0d130796923de057ee61f5466f0a90`  
		Last Modified: Thu, 06 Jul 2023 20:22:15 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3871795cc5c72b3e7a4565d36516149ce596a94b90cb00fc8b82b26d9c26e5`  
		Last Modified: Thu, 06 Jul 2023 20:22:20 GMT  
		Size: 18.4 MB (18447545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:46e697d13a25a200fd12630190cae49387192ca89c7f96111a1bf8411053ad6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1787; amd64

### `docker:23.0.6-windowsservercore-ltsc2022` - windows version 10.0.20348.1787; amd64

```console
$ docker pull docker@sha256:4b08c7610e6e77ecaa1a902f4b45ebd9fe846cd8fc7dc4328188ffe2e206f96d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1480297932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea8c05f68944e9c20b7c71cedb22cc24c88b4e9420984a72f54a9404d4dd9c0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:33:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 24 Jun 2023 03:37:22 GMT
ENV DOCKER_VERSION=23.0.6
# Sat, 24 Jun 2023 03:37:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Sat, 24 Jun 2023 03:37:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:18:35 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:18:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:18:37 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:19:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:19:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:19:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:19:04 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:19:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27db350c833f7fe0378bc977cd819c1ffe4133ff02ff69f1531f8ddc552c2366`  
		Last Modified: Sat, 24 Jun 2023 01:15:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c818796445a77806e10e6c159d076d6b0f5105edd8e7f27848042efb890970dd`  
		Last Modified: Sat, 24 Jun 2023 03:41:36 GMT  
		Size: 326.7 KB (326673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e4d934aedb3408d39924086e00ca7aaad6ba9093494927ec3193aafd92a20f`  
		Last Modified: Sat, 24 Jun 2023 03:42:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d47816062ca7fccecb96be7bf6468c4f36ffddd3115cf4d9bf244c0379bf7c`  
		Last Modified: Sat, 24 Jun 2023 03:42:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0520b4152b36536d9d6e0fbb761f4d738b989c5b9bc20fdcb54002f3531479b5`  
		Last Modified: Sat, 24 Jun 2023 03:42:18 GMT  
		Size: 17.3 MB (17325743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdef24df9e2be75799ec275160025462aef6bfb95360fc2907a2083128ae16b7`  
		Last Modified: Thu, 06 Jul 2023 20:22:01 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc79a9ea08518357ee22844e397fc700662ad99e4301177931c051357c2b2ec1`  
		Last Modified: Thu, 06 Jul 2023 20:22:02 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22356ed2aac9af5f5f301124bc544866e9164e843b1953a756c1339b561d671`  
		Last Modified: Thu, 06 Jul 2023 20:22:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e8c3432dbb82df56e2f5401d6af16998e13e3c34c99e49bf8c4bcd962359c8`  
		Last Modified: Thu, 06 Jul 2023 20:22:04 GMT  
		Size: 17.9 MB (17887283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466ab729826a1f27a4da2bbdf7ca5b645dc751c2f402fb5430c4db779b23360f`  
		Last Modified: Thu, 06 Jul 2023 20:22:00 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b58ed4b305ad3e911a088a311609a4eea626236698ec9a473e0f7ebafa56f3`  
		Last Modified: Thu, 06 Jul 2023 20:21:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b74996437d952638b6792afde202c442b5c8edcaf2df2272c0462cd3a2e728f`  
		Last Modified: Thu, 06 Jul 2023 20:21:59 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb948d323920d86405286636657cfe2ab8b9bc59b04009e8b75829a97ec4991`  
		Last Modified: Thu, 06 Jul 2023 20:22:04 GMT  
		Size: 18.4 MB (18447582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24`

```console
$ docker pull docker@sha256:8c39dc84d3a2cf61545c50689140f0cb29a672b8bccac1a5ebce12b402c9b32f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:24` - linux; amd64

```console
$ docker pull docker@sha256:cd573a0e55aa7ef9f2b767816baabd96f1b7e0edb4e3409ed14b2247a75e978d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118505918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b102eb731a4a7323f0ec6d928a5c68a7ab09b0a0230fe2416692f0080f8cd24b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417625960f4eb232ff8f3c3c3c7466465957015bcb89ef3c065eeef1c297c63`  
		Last Modified: Thu, 06 Jul 2023 20:20:59 GMT  
		Size: 16.4 MB (16389605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897e976d1bc25ad87bf3bc0fc2fccea2dfd64a17b84c8ca84ac706cb06a01c32`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea3511797c57c128bbc7f13cde057bc2342792e1a74505110f5bbaf1a46252`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 18.0 MB (17980095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb167a9f2ed16642a240002a0084af086982ae9ea25df89e058ed0909630afd2`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26505e5ff7f014a740ba6d568c3a66941216e9075d788676625c608f68fdedad`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5959ab5c26b6b799bbf2edfcccda947cc9a991935504a736575796ef6cfbc7cd`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dee904fe330cea37e269897fc7d4f60071040bee3c9c62c840e2addf3ae80d`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 7.1 MB (7080821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4605fd7c180c48c0119af314b08c7f44cea60c2e158df2ee92620374d18b3`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e4046b12ba084fcd4bc6186263c4c8582665222f81806277e5ec9348c2abce`  
		Last Modified: Thu, 06 Jul 2023 20:21:23 GMT  
		Size: 54.2 MB (54182575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593971f39a74770044342d937af0589b370e628d67268791e6fc0a21da05761c`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab1fe34bfb27e76f04d40ee77c6b9a7ef89bd1382eed94c960e54e21dd04cb8`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 2.8 KB (2791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7a0abbf5e8f6711b11680ac63e811b2cb9021178f9f33274b1e19e8863fa2c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109645476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8d6284fedab4472799ada0958c4f8933b7ad583ce1ce8d4a9cbdda36ec2022`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138a1bfb0f6b169ee65e5a20efb7efbefe0586b88be7de24f6af78f14b32998a`  
		Last Modified: Thu, 06 Jul 2023 19:42:28 GMT  
		Size: 15.4 MB (15435069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fb6fd88347451934d0082d9c9a9bd060cc6956ad81f4383fbe5fafea69d676`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 15.8 MB (15759501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181ea99d9b3a3ea4ef43717a4dfa3e9aa03ea6ba3486302dc50e4f0305c9461`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 16.3 MB (16312956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee7977acecd2644fba3d007147c5e3b04abf32fa82d0ef6980e2addd6be948d`  
		Last Modified: Thu, 06 Jul 2023 19:42:24 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909d160bcaa21899b740ecf14d6ee51bbe9f839d0d85f908bbbaad8b9fa3b7c1`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1c4d47beb50032ea66762ccdfc20f6152b72a07f9e80b83eca2f0e4bc0918a`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeb0ef44ad7debf4180e87a10ea2002be4e01aeda327970ff29c5bfbd65c2e7`  
		Last Modified: Thu, 06 Jul 2023 19:42:44 GMT  
		Size: 7.3 MB (7291386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0d48658bc22db36bb84a46d5df20bc9752ff5b07fe125e4a13a9b3d0bd5cdb`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23815654a9b80c2e5d021f7949089b57fa11b0c1d0142ade7db5e2fb2ce416f8`  
		Last Modified: Thu, 06 Jul 2023 19:42:48 GMT  
		Size: 49.5 MB (49485797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffaff52c24235510cee867d28793f9f3d2c3e61d6f12d3584cff8a96b2882f0`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a95386d6a8f394c0ecd1f77ab00fab627db31ea9ead9caba667e87671d8bb51`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 2.8 KB (2792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24-cli`

```console
$ docker pull docker@sha256:03560e8a49bed0fcf4c95faa6d6bfcbabaec9a9fddb0d4021e2529911a3ecee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:24-cli` - linux; amd64

```console
$ docker pull docker@sha256:c5eb2895781a0f4dbd69e06592a83e06d0bcae82738ec6222947f6d097ee9c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57237362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d3c497c4020c189c0451838f1350661dcab40a016ca3834fb26ec7589f288d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417625960f4eb232ff8f3c3c3c7466465957015bcb89ef3c065eeef1c297c63`  
		Last Modified: Thu, 06 Jul 2023 20:20:59 GMT  
		Size: 16.4 MB (16389605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897e976d1bc25ad87bf3bc0fc2fccea2dfd64a17b84c8ca84ac706cb06a01c32`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea3511797c57c128bbc7f13cde057bc2342792e1a74505110f5bbaf1a46252`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 18.0 MB (17980095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb167a9f2ed16642a240002a0084af086982ae9ea25df89e058ed0909630afd2`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26505e5ff7f014a740ba6d568c3a66941216e9075d788676625c608f68fdedad`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5959ab5c26b6b799bbf2edfcccda947cc9a991935504a736575796ef6cfbc7cd`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2486e25cc930eb7262299c21cbb0e30fc0f33adb3e3eb90ea12b8a0cb9f1a20b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52863134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930466f01330adb4e89d3a391447368f0b41bd54f01dbf5ef428af5438cf90e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138a1bfb0f6b169ee65e5a20efb7efbefe0586b88be7de24f6af78f14b32998a`  
		Last Modified: Thu, 06 Jul 2023 19:42:28 GMT  
		Size: 15.4 MB (15435069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fb6fd88347451934d0082d9c9a9bd060cc6956ad81f4383fbe5fafea69d676`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 15.8 MB (15759501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181ea99d9b3a3ea4ef43717a4dfa3e9aa03ea6ba3486302dc50e4f0305c9461`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 16.3 MB (16312956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee7977acecd2644fba3d007147c5e3b04abf32fa82d0ef6980e2addd6be948d`  
		Last Modified: Thu, 06 Jul 2023 19:42:24 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909d160bcaa21899b740ecf14d6ee51bbe9f839d0d85f908bbbaad8b9fa3b7c1`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1c4d47beb50032ea66762ccdfc20f6152b72a07f9e80b83eca2f0e4bc0918a`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24-dind`

```console
$ docker pull docker@sha256:8c39dc84d3a2cf61545c50689140f0cb29a672b8bccac1a5ebce12b402c9b32f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:24-dind` - linux; amd64

```console
$ docker pull docker@sha256:cd573a0e55aa7ef9f2b767816baabd96f1b7e0edb4e3409ed14b2247a75e978d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118505918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b102eb731a4a7323f0ec6d928a5c68a7ab09b0a0230fe2416692f0080f8cd24b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417625960f4eb232ff8f3c3c3c7466465957015bcb89ef3c065eeef1c297c63`  
		Last Modified: Thu, 06 Jul 2023 20:20:59 GMT  
		Size: 16.4 MB (16389605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897e976d1bc25ad87bf3bc0fc2fccea2dfd64a17b84c8ca84ac706cb06a01c32`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea3511797c57c128bbc7f13cde057bc2342792e1a74505110f5bbaf1a46252`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 18.0 MB (17980095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb167a9f2ed16642a240002a0084af086982ae9ea25df89e058ed0909630afd2`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26505e5ff7f014a740ba6d568c3a66941216e9075d788676625c608f68fdedad`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5959ab5c26b6b799bbf2edfcccda947cc9a991935504a736575796ef6cfbc7cd`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dee904fe330cea37e269897fc7d4f60071040bee3c9c62c840e2addf3ae80d`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 7.1 MB (7080821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4605fd7c180c48c0119af314b08c7f44cea60c2e158df2ee92620374d18b3`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e4046b12ba084fcd4bc6186263c4c8582665222f81806277e5ec9348c2abce`  
		Last Modified: Thu, 06 Jul 2023 20:21:23 GMT  
		Size: 54.2 MB (54182575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593971f39a74770044342d937af0589b370e628d67268791e6fc0a21da05761c`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab1fe34bfb27e76f04d40ee77c6b9a7ef89bd1382eed94c960e54e21dd04cb8`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 2.8 KB (2791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7a0abbf5e8f6711b11680ac63e811b2cb9021178f9f33274b1e19e8863fa2c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109645476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8d6284fedab4472799ada0958c4f8933b7ad583ce1ce8d4a9cbdda36ec2022`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138a1bfb0f6b169ee65e5a20efb7efbefe0586b88be7de24f6af78f14b32998a`  
		Last Modified: Thu, 06 Jul 2023 19:42:28 GMT  
		Size: 15.4 MB (15435069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fb6fd88347451934d0082d9c9a9bd060cc6956ad81f4383fbe5fafea69d676`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 15.8 MB (15759501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181ea99d9b3a3ea4ef43717a4dfa3e9aa03ea6ba3486302dc50e4f0305c9461`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 16.3 MB (16312956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee7977acecd2644fba3d007147c5e3b04abf32fa82d0ef6980e2addd6be948d`  
		Last Modified: Thu, 06 Jul 2023 19:42:24 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909d160bcaa21899b740ecf14d6ee51bbe9f839d0d85f908bbbaad8b9fa3b7c1`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1c4d47beb50032ea66762ccdfc20f6152b72a07f9e80b83eca2f0e4bc0918a`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeb0ef44ad7debf4180e87a10ea2002be4e01aeda327970ff29c5bfbd65c2e7`  
		Last Modified: Thu, 06 Jul 2023 19:42:44 GMT  
		Size: 7.3 MB (7291386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0d48658bc22db36bb84a46d5df20bc9752ff5b07fe125e4a13a9b3d0bd5cdb`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23815654a9b80c2e5d021f7949089b57fa11b0c1d0142ade7db5e2fb2ce416f8`  
		Last Modified: Thu, 06 Jul 2023 19:42:48 GMT  
		Size: 49.5 MB (49485797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffaff52c24235510cee867d28793f9f3d2c3e61d6f12d3584cff8a96b2882f0`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a95386d6a8f394c0ecd1f77ab00fab627db31ea9ead9caba667e87671d8bb51`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 2.8 KB (2792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24-dind-rootless`

```console
$ docker pull docker@sha256:eb5cee8eeecc5b5a2f7757200b903fb48ff6decf135068367425edbc8c7dd7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:24-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:f092337b953d62b8d64b97f7eb44290811cbecc77b44fd9b2ed2b01eab39862c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140520384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313742b11beb8009157dbc242bae085f12de358e14f7b130b353cbc7d471706c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
USER rootless
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417625960f4eb232ff8f3c3c3c7466465957015bcb89ef3c065eeef1c297c63`  
		Last Modified: Thu, 06 Jul 2023 20:20:59 GMT  
		Size: 16.4 MB (16389605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897e976d1bc25ad87bf3bc0fc2fccea2dfd64a17b84c8ca84ac706cb06a01c32`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea3511797c57c128bbc7f13cde057bc2342792e1a74505110f5bbaf1a46252`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 18.0 MB (17980095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb167a9f2ed16642a240002a0084af086982ae9ea25df89e058ed0909630afd2`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26505e5ff7f014a740ba6d568c3a66941216e9075d788676625c608f68fdedad`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5959ab5c26b6b799bbf2edfcccda947cc9a991935504a736575796ef6cfbc7cd`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dee904fe330cea37e269897fc7d4f60071040bee3c9c62c840e2addf3ae80d`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 7.1 MB (7080821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4605fd7c180c48c0119af314b08c7f44cea60c2e158df2ee92620374d18b3`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e4046b12ba084fcd4bc6186263c4c8582665222f81806277e5ec9348c2abce`  
		Last Modified: Thu, 06 Jul 2023 20:21:23 GMT  
		Size: 54.2 MB (54182575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593971f39a74770044342d937af0589b370e628d67268791e6fc0a21da05761c`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab1fe34bfb27e76f04d40ee77c6b9a7ef89bd1382eed94c960e54e21dd04cb8`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 2.8 KB (2791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bc35a0dc3eb3e494e9bc68c57a01b07b4bef93e143a639d5973c394dca71b4`  
		Last Modified: Thu, 06 Jul 2023 20:21:54 GMT  
		Size: 1.4 MB (1362372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcb6ace6229c8a616b83b359ea04d5e2f95cb702d531da29bca3185b13f1ce0`  
		Last Modified: Thu, 06 Jul 2023 20:21:53 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c7035e55b9c75d1406886fc8f9cf808e88ed8cd02e3b489f30bfdffd6661b8`  
		Last Modified: Thu, 06 Jul 2023 20:21:53 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc9cc3e18eff8c744b78fb60f9b01d0b397433309d1fa90b72ce939bad40288`  
		Last Modified: Thu, 06 Jul 2023 20:21:57 GMT  
		Size: 20.7 MB (20650355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db87cb1cd3c112f8657f04b1ea20ccf06d330bd4d80196966f4eb8fa23205ee0`  
		Last Modified: Thu, 06 Jul 2023 20:21:53 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:49d71ba16a6e4899bad3069608b61d7117ae6cd1e48f813f8314a4d42d01011b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133511196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f605f34be1d9f7c3a910078506e30058c387d191f60900e8543a1a58f55e7a7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
USER rootless
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138a1bfb0f6b169ee65e5a20efb7efbefe0586b88be7de24f6af78f14b32998a`  
		Last Modified: Thu, 06 Jul 2023 19:42:28 GMT  
		Size: 15.4 MB (15435069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fb6fd88347451934d0082d9c9a9bd060cc6956ad81f4383fbe5fafea69d676`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 15.8 MB (15759501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181ea99d9b3a3ea4ef43717a4dfa3e9aa03ea6ba3486302dc50e4f0305c9461`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 16.3 MB (16312956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee7977acecd2644fba3d007147c5e3b04abf32fa82d0ef6980e2addd6be948d`  
		Last Modified: Thu, 06 Jul 2023 19:42:24 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909d160bcaa21899b740ecf14d6ee51bbe9f839d0d85f908bbbaad8b9fa3b7c1`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1c4d47beb50032ea66762ccdfc20f6152b72a07f9e80b83eca2f0e4bc0918a`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeb0ef44ad7debf4180e87a10ea2002be4e01aeda327970ff29c5bfbd65c2e7`  
		Last Modified: Thu, 06 Jul 2023 19:42:44 GMT  
		Size: 7.3 MB (7291386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0d48658bc22db36bb84a46d5df20bc9752ff5b07fe125e4a13a9b3d0bd5cdb`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23815654a9b80c2e5d021f7949089b57fa11b0c1d0142ade7db5e2fb2ce416f8`  
		Last Modified: Thu, 06 Jul 2023 19:42:48 GMT  
		Size: 49.5 MB (49485797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffaff52c24235510cee867d28793f9f3d2c3e61d6f12d3584cff8a96b2882f0`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a95386d6a8f394c0ecd1f77ab00fab627db31ea9ead9caba667e87671d8bb51`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 2.8 KB (2792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c042a310de5c2f6450c02438b35cc0f5094f63e3d485a8572a346f386699d0e2`  
		Last Modified: Thu, 06 Jul 2023 19:43:18 GMT  
		Size: 1.4 MB (1413238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfd46e0bc98f20fd18fa46c68ab6bde20f9e3da0b046ecd7397b69415205646`  
		Last Modified: Thu, 06 Jul 2023 19:43:18 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a53c68d9732d03c650deea803d295f0cb7755e5e7a56bccea42aa4c698d58d`  
		Last Modified: Thu, 06 Jul 2023 19:43:19 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd2df083914deeada6a2d428f2329858807d6627e6ebaec1dd448caa658a51c`  
		Last Modified: Thu, 06 Jul 2023 19:43:21 GMT  
		Size: 22.5 MB (22450742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73160a7bc4290cbb1265a17afaab5e40e183006e5e96b4eab646be5e79c9f80f`  
		Last Modified: Thu, 06 Jul 2023 19:43:18 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24-git`

```console
$ docker pull docker@sha256:f5545c2d805d4305686fc015c2598e9bb57d50f0484b97b01cb0c5cf54523103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:24-git` - linux; amd64

```console
$ docker pull docker@sha256:4e51cfdd3974770c40184831d7f7bc13fc9f7c62f5a8e24600cc8c30122ca88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123440672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8336a6d9c2a5f3c3f2af9c3b39c6c8af0f761926237c5fd5e5d99c6ae39fef`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417625960f4eb232ff8f3c3c3c7466465957015bcb89ef3c065eeef1c297c63`  
		Last Modified: Thu, 06 Jul 2023 20:20:59 GMT  
		Size: 16.4 MB (16389605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897e976d1bc25ad87bf3bc0fc2fccea2dfd64a17b84c8ca84ac706cb06a01c32`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea3511797c57c128bbc7f13cde057bc2342792e1a74505110f5bbaf1a46252`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 18.0 MB (17980095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb167a9f2ed16642a240002a0084af086982ae9ea25df89e058ed0909630afd2`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26505e5ff7f014a740ba6d568c3a66941216e9075d788676625c608f68fdedad`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5959ab5c26b6b799bbf2edfcccda947cc9a991935504a736575796ef6cfbc7cd`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dee904fe330cea37e269897fc7d4f60071040bee3c9c62c840e2addf3ae80d`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 7.1 MB (7080821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4605fd7c180c48c0119af314b08c7f44cea60c2e158df2ee92620374d18b3`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e4046b12ba084fcd4bc6186263c4c8582665222f81806277e5ec9348c2abce`  
		Last Modified: Thu, 06 Jul 2023 20:21:23 GMT  
		Size: 54.2 MB (54182575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593971f39a74770044342d937af0589b370e628d67268791e6fc0a21da05761c`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab1fe34bfb27e76f04d40ee77c6b9a7ef89bd1382eed94c960e54e21dd04cb8`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 2.8 KB (2791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cf7411c8dc4a4b50659d07545570ec924492b3c332977ac680b8f8dd34442f`  
		Last Modified: Thu, 06 Jul 2023 20:22:13 GMT  
		Size: 4.9 MB (4934754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dbdbd485df5e901ba6421d316a90b70d0d0c591bbcfd576b3e936f886c201b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114666566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907da1d50ee9a9d68449a225389de0679597b02911c6b10184a5a2ccd69d8aea`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138a1bfb0f6b169ee65e5a20efb7efbefe0586b88be7de24f6af78f14b32998a`  
		Last Modified: Thu, 06 Jul 2023 19:42:28 GMT  
		Size: 15.4 MB (15435069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fb6fd88347451934d0082d9c9a9bd060cc6956ad81f4383fbe5fafea69d676`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 15.8 MB (15759501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181ea99d9b3a3ea4ef43717a4dfa3e9aa03ea6ba3486302dc50e4f0305c9461`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 16.3 MB (16312956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee7977acecd2644fba3d007147c5e3b04abf32fa82d0ef6980e2addd6be948d`  
		Last Modified: Thu, 06 Jul 2023 19:42:24 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909d160bcaa21899b740ecf14d6ee51bbe9f839d0d85f908bbbaad8b9fa3b7c1`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1c4d47beb50032ea66762ccdfc20f6152b72a07f9e80b83eca2f0e4bc0918a`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeb0ef44ad7debf4180e87a10ea2002be4e01aeda327970ff29c5bfbd65c2e7`  
		Last Modified: Thu, 06 Jul 2023 19:42:44 GMT  
		Size: 7.3 MB (7291386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0d48658bc22db36bb84a46d5df20bc9752ff5b07fe125e4a13a9b3d0bd5cdb`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23815654a9b80c2e5d021f7949089b57fa11b0c1d0142ade7db5e2fb2ce416f8`  
		Last Modified: Thu, 06 Jul 2023 19:42:48 GMT  
		Size: 49.5 MB (49485797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffaff52c24235510cee867d28793f9f3d2c3e61d6f12d3584cff8a96b2882f0`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a95386d6a8f394c0ecd1f77ab00fab627db31ea9ead9caba667e87671d8bb51`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 2.8 KB (2792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962a119574903f96d3d7470be0241fc2636062db4d08baa6d61793ce9a361b2c`  
		Last Modified: Thu, 06 Jul 2023 19:43:36 GMT  
		Size: 5.0 MB (5021090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24-windowsservercore`

```console
$ docker pull docker@sha256:e97f3340b4b597c70a321e2485ab06f289f99477f1e667097a6b8e476f851fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1787; amd64
	-	windows version 10.0.17763.4499; amd64

### `docker:24-windowsservercore` - windows version 10.0.20348.1787; amd64

```console
$ docker pull docker@sha256:edf247a340baea4e8c2d622fb5af1598abe85113b713dd6a3cd5bc5e40506a42
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1480426537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd92513f922f244389d26853ae3f9cabce18252ff320f58d25bc03adebf7fb3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:33:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 Jul 2023 20:15:10 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 20:15:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.3.zip
# Thu, 06 Jul 2023 20:15:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:15:40 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:15:41 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:15:42 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:16:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:16:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:16:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:16:09 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:16:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27db350c833f7fe0378bc977cd819c1ffe4133ff02ff69f1531f8ddc552c2366`  
		Last Modified: Sat, 24 Jun 2023 01:15:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c818796445a77806e10e6c159d076d6b0f5105edd8e7f27848042efb890970dd`  
		Last Modified: Sat, 24 Jun 2023 03:41:36 GMT  
		Size: 326.7 KB (326673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343faf4d8143dadaf9de6d52c214909510a19d32a2ef2f90860d9aaf4a919692`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8ab0e8f6197c22da65ebbadcd1fe496b029f0fadf873bc625f887c7580a75b`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49d31da5904ec14a1003079c30d7a269f65706ca9af5e2d6ea0cbe7a2762d2d`  
		Last Modified: Thu, 06 Jul 2023 20:21:22 GMT  
		Size: 17.5 MB (17458414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b059f4f69ae92c7ab553a89fe911075af37b363f07301b5821fa58e14158ed9d`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dd12c4af4dd1eda3383bc2e1023236c4a9d31ad0483bd80ff541d5ca92aaf7`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b223fadd37e4d376cc64a69c7c31a7c10bd36cfd3d4c74e85ebe780d2add0c`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ef3be65907ccf52605b51db71fe3b3b12292bad11ab1a49a78a699b004ab06`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 17.9 MB (17883688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f9df1df7303a9e93905852c6fd3c1183da3654ea42a86788484596b0c52a5d`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a0de7a4b55054578241a4e2ec66ccf03b270537b6a18c4e0b3b4250ed14a1c`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c928426eb1e8b4be9068775a7abafdca91118e43ac375399595fe896c759b189`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78728e406ce8bdc2b7dfab0c83103ff85dcf7d19630d4dfd18450e5f13fa2128`  
		Last Modified: Thu, 06 Jul 2023 20:21:21 GMT  
		Size: 18.4 MB (18447298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24-windowsservercore` - windows version 10.0.17763.4499; amd64

```console
$ docker pull docker@sha256:f75763c02bfd57528d7f924d779e24e6185ba787ce630fc22b39e936aa91a34e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1704850908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8f774bf3cac154e13a3e7fdda3d391274075199b35f1410c2691ec20f72a36`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:40:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:35:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 Jul 2023 20:16:52 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 20:16:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.3.zip
# Thu, 06 Jul 2023 20:17:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:17:28 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:17:28 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:17:29 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:17:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:17:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:17:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:17:58 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:18:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58717a727cd3a756d7c1180dfb74e95d49735ed12628bd25d2058bc90fa96991`  
		Last Modified: Sat, 24 Jun 2023 01:20:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb210483c7a5877c9d4e754a46a0085ff94bc31d9e32e64c37e1ed4d6e30162e`  
		Last Modified: Sat, 24 Jun 2023 03:41:56 GMT  
		Size: 306.0 KB (305975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220d673a500d122873877d4a4be342cb40e07ee47a4a508dee2dcba97bfe4723`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70790617356246e318492973e7c751cc8fb9199ed00349374fb264e4566ced04`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae1f34dbac2b79a6a652b8926077c0e41dda895cab9b1ac5c75c29db1cde7a6`  
		Last Modified: Thu, 06 Jul 2023 20:21:45 GMT  
		Size: 17.5 MB (17466854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25abab3ba7887100f6f8a30c3316f9a3dc51b171a81f1703159c27c07c25dd82`  
		Last Modified: Thu, 06 Jul 2023 20:21:40 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b56866387a48d55494e41e21da221a0a5fe4b3239dc940b5b75984e14f9cc5`  
		Last Modified: Thu, 06 Jul 2023 20:21:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4cc15bb518b5c263f5d52c7b7761bb36681b7fab382fd34aa9a21042d5055`  
		Last Modified: Thu, 06 Jul 2023 20:21:39 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00adc5a657ac1846710c85cc2992c68dcc4389c3d24d4f5be85599e64aac8e4`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 17.9 MB (17882284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dfe7cd1c7b16458db2fa8613b9b5e2161397d26647a6b16d618bc92922d9868`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb59442896100faf18d8b1d475701d8a7bab03de0ddcd6606a00cffda2665e7a`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a533ef75401c06ad9ab423047654f037ae36177f6bccfbef4bdeb5f98e9c149`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9329ff40635fac09f33414e395d71d781533d78016ebfc61b706c13da4e1e6`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 18.4 MB (18447195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24-windowsservercore-1809`

```console
$ docker pull docker@sha256:e84f671e17b7a624b2fe9857ce730d961a9746a3312bb0b29b963fd7c1104f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `docker:24-windowsservercore-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull docker@sha256:f75763c02bfd57528d7f924d779e24e6185ba787ce630fc22b39e936aa91a34e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1704850908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8f774bf3cac154e13a3e7fdda3d391274075199b35f1410c2691ec20f72a36`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:40:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:35:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 Jul 2023 20:16:52 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 20:16:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.3.zip
# Thu, 06 Jul 2023 20:17:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:17:28 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:17:28 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:17:29 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:17:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:17:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:17:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:17:58 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:18:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58717a727cd3a756d7c1180dfb74e95d49735ed12628bd25d2058bc90fa96991`  
		Last Modified: Sat, 24 Jun 2023 01:20:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb210483c7a5877c9d4e754a46a0085ff94bc31d9e32e64c37e1ed4d6e30162e`  
		Last Modified: Sat, 24 Jun 2023 03:41:56 GMT  
		Size: 306.0 KB (305975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220d673a500d122873877d4a4be342cb40e07ee47a4a508dee2dcba97bfe4723`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70790617356246e318492973e7c751cc8fb9199ed00349374fb264e4566ced04`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae1f34dbac2b79a6a652b8926077c0e41dda895cab9b1ac5c75c29db1cde7a6`  
		Last Modified: Thu, 06 Jul 2023 20:21:45 GMT  
		Size: 17.5 MB (17466854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25abab3ba7887100f6f8a30c3316f9a3dc51b171a81f1703159c27c07c25dd82`  
		Last Modified: Thu, 06 Jul 2023 20:21:40 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b56866387a48d55494e41e21da221a0a5fe4b3239dc940b5b75984e14f9cc5`  
		Last Modified: Thu, 06 Jul 2023 20:21:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4cc15bb518b5c263f5d52c7b7761bb36681b7fab382fd34aa9a21042d5055`  
		Last Modified: Thu, 06 Jul 2023 20:21:39 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00adc5a657ac1846710c85cc2992c68dcc4389c3d24d4f5be85599e64aac8e4`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 17.9 MB (17882284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dfe7cd1c7b16458db2fa8613b9b5e2161397d26647a6b16d618bc92922d9868`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb59442896100faf18d8b1d475701d8a7bab03de0ddcd6606a00cffda2665e7a`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a533ef75401c06ad9ab423047654f037ae36177f6bccfbef4bdeb5f98e9c149`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9329ff40635fac09f33414e395d71d781533d78016ebfc61b706c13da4e1e6`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 18.4 MB (18447195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:f10cd504d09011ac66e85ad70c551a4bb16edb03f9c5c994349037b63be211be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1787; amd64

### `docker:24-windowsservercore-ltsc2022` - windows version 10.0.20348.1787; amd64

```console
$ docker pull docker@sha256:edf247a340baea4e8c2d622fb5af1598abe85113b713dd6a3cd5bc5e40506a42
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1480426537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd92513f922f244389d26853ae3f9cabce18252ff320f58d25bc03adebf7fb3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:33:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 Jul 2023 20:15:10 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 20:15:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.3.zip
# Thu, 06 Jul 2023 20:15:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:15:40 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:15:41 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:15:42 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:16:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:16:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:16:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:16:09 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:16:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27db350c833f7fe0378bc977cd819c1ffe4133ff02ff69f1531f8ddc552c2366`  
		Last Modified: Sat, 24 Jun 2023 01:15:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c818796445a77806e10e6c159d076d6b0f5105edd8e7f27848042efb890970dd`  
		Last Modified: Sat, 24 Jun 2023 03:41:36 GMT  
		Size: 326.7 KB (326673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343faf4d8143dadaf9de6d52c214909510a19d32a2ef2f90860d9aaf4a919692`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8ab0e8f6197c22da65ebbadcd1fe496b029f0fadf873bc625f887c7580a75b`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49d31da5904ec14a1003079c30d7a269f65706ca9af5e2d6ea0cbe7a2762d2d`  
		Last Modified: Thu, 06 Jul 2023 20:21:22 GMT  
		Size: 17.5 MB (17458414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b059f4f69ae92c7ab553a89fe911075af37b363f07301b5821fa58e14158ed9d`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dd12c4af4dd1eda3383bc2e1023236c4a9d31ad0483bd80ff541d5ca92aaf7`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b223fadd37e4d376cc64a69c7c31a7c10bd36cfd3d4c74e85ebe780d2add0c`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ef3be65907ccf52605b51db71fe3b3b12292bad11ab1a49a78a699b004ab06`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 17.9 MB (17883688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f9df1df7303a9e93905852c6fd3c1183da3654ea42a86788484596b0c52a5d`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a0de7a4b55054578241a4e2ec66ccf03b270537b6a18c4e0b3b4250ed14a1c`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c928426eb1e8b4be9068775a7abafdca91118e43ac375399595fe896c759b189`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78728e406ce8bdc2b7dfab0c83103ff85dcf7d19630d4dfd18450e5f13fa2128`  
		Last Modified: Thu, 06 Jul 2023 20:21:21 GMT  
		Size: 18.4 MB (18447298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0`

```console
$ docker pull docker@sha256:8c39dc84d3a2cf61545c50689140f0cb29a672b8bccac1a5ebce12b402c9b32f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:24.0` - linux; amd64

```console
$ docker pull docker@sha256:cd573a0e55aa7ef9f2b767816baabd96f1b7e0edb4e3409ed14b2247a75e978d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118505918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b102eb731a4a7323f0ec6d928a5c68a7ab09b0a0230fe2416692f0080f8cd24b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417625960f4eb232ff8f3c3c3c7466465957015bcb89ef3c065eeef1c297c63`  
		Last Modified: Thu, 06 Jul 2023 20:20:59 GMT  
		Size: 16.4 MB (16389605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897e976d1bc25ad87bf3bc0fc2fccea2dfd64a17b84c8ca84ac706cb06a01c32`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea3511797c57c128bbc7f13cde057bc2342792e1a74505110f5bbaf1a46252`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 18.0 MB (17980095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb167a9f2ed16642a240002a0084af086982ae9ea25df89e058ed0909630afd2`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26505e5ff7f014a740ba6d568c3a66941216e9075d788676625c608f68fdedad`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5959ab5c26b6b799bbf2edfcccda947cc9a991935504a736575796ef6cfbc7cd`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dee904fe330cea37e269897fc7d4f60071040bee3c9c62c840e2addf3ae80d`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 7.1 MB (7080821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4605fd7c180c48c0119af314b08c7f44cea60c2e158df2ee92620374d18b3`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e4046b12ba084fcd4bc6186263c4c8582665222f81806277e5ec9348c2abce`  
		Last Modified: Thu, 06 Jul 2023 20:21:23 GMT  
		Size: 54.2 MB (54182575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593971f39a74770044342d937af0589b370e628d67268791e6fc0a21da05761c`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab1fe34bfb27e76f04d40ee77c6b9a7ef89bd1382eed94c960e54e21dd04cb8`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 2.8 KB (2791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7a0abbf5e8f6711b11680ac63e811b2cb9021178f9f33274b1e19e8863fa2c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109645476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8d6284fedab4472799ada0958c4f8933b7ad583ce1ce8d4a9cbdda36ec2022`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138a1bfb0f6b169ee65e5a20efb7efbefe0586b88be7de24f6af78f14b32998a`  
		Last Modified: Thu, 06 Jul 2023 19:42:28 GMT  
		Size: 15.4 MB (15435069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fb6fd88347451934d0082d9c9a9bd060cc6956ad81f4383fbe5fafea69d676`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 15.8 MB (15759501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181ea99d9b3a3ea4ef43717a4dfa3e9aa03ea6ba3486302dc50e4f0305c9461`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 16.3 MB (16312956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee7977acecd2644fba3d007147c5e3b04abf32fa82d0ef6980e2addd6be948d`  
		Last Modified: Thu, 06 Jul 2023 19:42:24 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909d160bcaa21899b740ecf14d6ee51bbe9f839d0d85f908bbbaad8b9fa3b7c1`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1c4d47beb50032ea66762ccdfc20f6152b72a07f9e80b83eca2f0e4bc0918a`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeb0ef44ad7debf4180e87a10ea2002be4e01aeda327970ff29c5bfbd65c2e7`  
		Last Modified: Thu, 06 Jul 2023 19:42:44 GMT  
		Size: 7.3 MB (7291386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0d48658bc22db36bb84a46d5df20bc9752ff5b07fe125e4a13a9b3d0bd5cdb`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23815654a9b80c2e5d021f7949089b57fa11b0c1d0142ade7db5e2fb2ce416f8`  
		Last Modified: Thu, 06 Jul 2023 19:42:48 GMT  
		Size: 49.5 MB (49485797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffaff52c24235510cee867d28793f9f3d2c3e61d6f12d3584cff8a96b2882f0`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a95386d6a8f394c0ecd1f77ab00fab627db31ea9ead9caba667e87671d8bb51`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 2.8 KB (2792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0-cli`

```console
$ docker pull docker@sha256:03560e8a49bed0fcf4c95faa6d6bfcbabaec9a9fddb0d4021e2529911a3ecee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:24.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:c5eb2895781a0f4dbd69e06592a83e06d0bcae82738ec6222947f6d097ee9c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57237362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d3c497c4020c189c0451838f1350661dcab40a016ca3834fb26ec7589f288d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417625960f4eb232ff8f3c3c3c7466465957015bcb89ef3c065eeef1c297c63`  
		Last Modified: Thu, 06 Jul 2023 20:20:59 GMT  
		Size: 16.4 MB (16389605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897e976d1bc25ad87bf3bc0fc2fccea2dfd64a17b84c8ca84ac706cb06a01c32`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea3511797c57c128bbc7f13cde057bc2342792e1a74505110f5bbaf1a46252`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 18.0 MB (17980095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb167a9f2ed16642a240002a0084af086982ae9ea25df89e058ed0909630afd2`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26505e5ff7f014a740ba6d568c3a66941216e9075d788676625c608f68fdedad`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5959ab5c26b6b799bbf2edfcccda947cc9a991935504a736575796ef6cfbc7cd`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2486e25cc930eb7262299c21cbb0e30fc0f33adb3e3eb90ea12b8a0cb9f1a20b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52863134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930466f01330adb4e89d3a391447368f0b41bd54f01dbf5ef428af5438cf90e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138a1bfb0f6b169ee65e5a20efb7efbefe0586b88be7de24f6af78f14b32998a`  
		Last Modified: Thu, 06 Jul 2023 19:42:28 GMT  
		Size: 15.4 MB (15435069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fb6fd88347451934d0082d9c9a9bd060cc6956ad81f4383fbe5fafea69d676`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 15.8 MB (15759501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181ea99d9b3a3ea4ef43717a4dfa3e9aa03ea6ba3486302dc50e4f0305c9461`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 16.3 MB (16312956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee7977acecd2644fba3d007147c5e3b04abf32fa82d0ef6980e2addd6be948d`  
		Last Modified: Thu, 06 Jul 2023 19:42:24 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909d160bcaa21899b740ecf14d6ee51bbe9f839d0d85f908bbbaad8b9fa3b7c1`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1c4d47beb50032ea66762ccdfc20f6152b72a07f9e80b83eca2f0e4bc0918a`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0-dind`

```console
$ docker pull docker@sha256:8c39dc84d3a2cf61545c50689140f0cb29a672b8bccac1a5ebce12b402c9b32f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:24.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:cd573a0e55aa7ef9f2b767816baabd96f1b7e0edb4e3409ed14b2247a75e978d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118505918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b102eb731a4a7323f0ec6d928a5c68a7ab09b0a0230fe2416692f0080f8cd24b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417625960f4eb232ff8f3c3c3c7466465957015bcb89ef3c065eeef1c297c63`  
		Last Modified: Thu, 06 Jul 2023 20:20:59 GMT  
		Size: 16.4 MB (16389605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897e976d1bc25ad87bf3bc0fc2fccea2dfd64a17b84c8ca84ac706cb06a01c32`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea3511797c57c128bbc7f13cde057bc2342792e1a74505110f5bbaf1a46252`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 18.0 MB (17980095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb167a9f2ed16642a240002a0084af086982ae9ea25df89e058ed0909630afd2`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26505e5ff7f014a740ba6d568c3a66941216e9075d788676625c608f68fdedad`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5959ab5c26b6b799bbf2edfcccda947cc9a991935504a736575796ef6cfbc7cd`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dee904fe330cea37e269897fc7d4f60071040bee3c9c62c840e2addf3ae80d`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 7.1 MB (7080821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4605fd7c180c48c0119af314b08c7f44cea60c2e158df2ee92620374d18b3`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e4046b12ba084fcd4bc6186263c4c8582665222f81806277e5ec9348c2abce`  
		Last Modified: Thu, 06 Jul 2023 20:21:23 GMT  
		Size: 54.2 MB (54182575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593971f39a74770044342d937af0589b370e628d67268791e6fc0a21da05761c`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab1fe34bfb27e76f04d40ee77c6b9a7ef89bd1382eed94c960e54e21dd04cb8`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 2.8 KB (2791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7a0abbf5e8f6711b11680ac63e811b2cb9021178f9f33274b1e19e8863fa2c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109645476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8d6284fedab4472799ada0958c4f8933b7ad583ce1ce8d4a9cbdda36ec2022`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138a1bfb0f6b169ee65e5a20efb7efbefe0586b88be7de24f6af78f14b32998a`  
		Last Modified: Thu, 06 Jul 2023 19:42:28 GMT  
		Size: 15.4 MB (15435069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fb6fd88347451934d0082d9c9a9bd060cc6956ad81f4383fbe5fafea69d676`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 15.8 MB (15759501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181ea99d9b3a3ea4ef43717a4dfa3e9aa03ea6ba3486302dc50e4f0305c9461`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 16.3 MB (16312956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee7977acecd2644fba3d007147c5e3b04abf32fa82d0ef6980e2addd6be948d`  
		Last Modified: Thu, 06 Jul 2023 19:42:24 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909d160bcaa21899b740ecf14d6ee51bbe9f839d0d85f908bbbaad8b9fa3b7c1`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1c4d47beb50032ea66762ccdfc20f6152b72a07f9e80b83eca2f0e4bc0918a`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeb0ef44ad7debf4180e87a10ea2002be4e01aeda327970ff29c5bfbd65c2e7`  
		Last Modified: Thu, 06 Jul 2023 19:42:44 GMT  
		Size: 7.3 MB (7291386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0d48658bc22db36bb84a46d5df20bc9752ff5b07fe125e4a13a9b3d0bd5cdb`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23815654a9b80c2e5d021f7949089b57fa11b0c1d0142ade7db5e2fb2ce416f8`  
		Last Modified: Thu, 06 Jul 2023 19:42:48 GMT  
		Size: 49.5 MB (49485797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffaff52c24235510cee867d28793f9f3d2c3e61d6f12d3584cff8a96b2882f0`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a95386d6a8f394c0ecd1f77ab00fab627db31ea9ead9caba667e87671d8bb51`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 2.8 KB (2792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0-dind-rootless`

```console
$ docker pull docker@sha256:eb5cee8eeecc5b5a2f7757200b903fb48ff6decf135068367425edbc8c7dd7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:24.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:f092337b953d62b8d64b97f7eb44290811cbecc77b44fd9b2ed2b01eab39862c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140520384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313742b11beb8009157dbc242bae085f12de358e14f7b130b353cbc7d471706c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
USER rootless
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417625960f4eb232ff8f3c3c3c7466465957015bcb89ef3c065eeef1c297c63`  
		Last Modified: Thu, 06 Jul 2023 20:20:59 GMT  
		Size: 16.4 MB (16389605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897e976d1bc25ad87bf3bc0fc2fccea2dfd64a17b84c8ca84ac706cb06a01c32`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea3511797c57c128bbc7f13cde057bc2342792e1a74505110f5bbaf1a46252`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 18.0 MB (17980095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb167a9f2ed16642a240002a0084af086982ae9ea25df89e058ed0909630afd2`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26505e5ff7f014a740ba6d568c3a66941216e9075d788676625c608f68fdedad`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5959ab5c26b6b799bbf2edfcccda947cc9a991935504a736575796ef6cfbc7cd`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dee904fe330cea37e269897fc7d4f60071040bee3c9c62c840e2addf3ae80d`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 7.1 MB (7080821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4605fd7c180c48c0119af314b08c7f44cea60c2e158df2ee92620374d18b3`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e4046b12ba084fcd4bc6186263c4c8582665222f81806277e5ec9348c2abce`  
		Last Modified: Thu, 06 Jul 2023 20:21:23 GMT  
		Size: 54.2 MB (54182575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593971f39a74770044342d937af0589b370e628d67268791e6fc0a21da05761c`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab1fe34bfb27e76f04d40ee77c6b9a7ef89bd1382eed94c960e54e21dd04cb8`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 2.8 KB (2791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bc35a0dc3eb3e494e9bc68c57a01b07b4bef93e143a639d5973c394dca71b4`  
		Last Modified: Thu, 06 Jul 2023 20:21:54 GMT  
		Size: 1.4 MB (1362372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcb6ace6229c8a616b83b359ea04d5e2f95cb702d531da29bca3185b13f1ce0`  
		Last Modified: Thu, 06 Jul 2023 20:21:53 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c7035e55b9c75d1406886fc8f9cf808e88ed8cd02e3b489f30bfdffd6661b8`  
		Last Modified: Thu, 06 Jul 2023 20:21:53 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc9cc3e18eff8c744b78fb60f9b01d0b397433309d1fa90b72ce939bad40288`  
		Last Modified: Thu, 06 Jul 2023 20:21:57 GMT  
		Size: 20.7 MB (20650355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db87cb1cd3c112f8657f04b1ea20ccf06d330bd4d80196966f4eb8fa23205ee0`  
		Last Modified: Thu, 06 Jul 2023 20:21:53 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:49d71ba16a6e4899bad3069608b61d7117ae6cd1e48f813f8314a4d42d01011b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133511196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f605f34be1d9f7c3a910078506e30058c387d191f60900e8543a1a58f55e7a7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
USER rootless
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138a1bfb0f6b169ee65e5a20efb7efbefe0586b88be7de24f6af78f14b32998a`  
		Last Modified: Thu, 06 Jul 2023 19:42:28 GMT  
		Size: 15.4 MB (15435069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fb6fd88347451934d0082d9c9a9bd060cc6956ad81f4383fbe5fafea69d676`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 15.8 MB (15759501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181ea99d9b3a3ea4ef43717a4dfa3e9aa03ea6ba3486302dc50e4f0305c9461`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 16.3 MB (16312956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee7977acecd2644fba3d007147c5e3b04abf32fa82d0ef6980e2addd6be948d`  
		Last Modified: Thu, 06 Jul 2023 19:42:24 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909d160bcaa21899b740ecf14d6ee51bbe9f839d0d85f908bbbaad8b9fa3b7c1`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1c4d47beb50032ea66762ccdfc20f6152b72a07f9e80b83eca2f0e4bc0918a`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeb0ef44ad7debf4180e87a10ea2002be4e01aeda327970ff29c5bfbd65c2e7`  
		Last Modified: Thu, 06 Jul 2023 19:42:44 GMT  
		Size: 7.3 MB (7291386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0d48658bc22db36bb84a46d5df20bc9752ff5b07fe125e4a13a9b3d0bd5cdb`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23815654a9b80c2e5d021f7949089b57fa11b0c1d0142ade7db5e2fb2ce416f8`  
		Last Modified: Thu, 06 Jul 2023 19:42:48 GMT  
		Size: 49.5 MB (49485797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffaff52c24235510cee867d28793f9f3d2c3e61d6f12d3584cff8a96b2882f0`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a95386d6a8f394c0ecd1f77ab00fab627db31ea9ead9caba667e87671d8bb51`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 2.8 KB (2792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c042a310de5c2f6450c02438b35cc0f5094f63e3d485a8572a346f386699d0e2`  
		Last Modified: Thu, 06 Jul 2023 19:43:18 GMT  
		Size: 1.4 MB (1413238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfd46e0bc98f20fd18fa46c68ab6bde20f9e3da0b046ecd7397b69415205646`  
		Last Modified: Thu, 06 Jul 2023 19:43:18 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a53c68d9732d03c650deea803d295f0cb7755e5e7a56bccea42aa4c698d58d`  
		Last Modified: Thu, 06 Jul 2023 19:43:19 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd2df083914deeada6a2d428f2329858807d6627e6ebaec1dd448caa658a51c`  
		Last Modified: Thu, 06 Jul 2023 19:43:21 GMT  
		Size: 22.5 MB (22450742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73160a7bc4290cbb1265a17afaab5e40e183006e5e96b4eab646be5e79c9f80f`  
		Last Modified: Thu, 06 Jul 2023 19:43:18 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0-git`

```console
$ docker pull docker@sha256:f5545c2d805d4305686fc015c2598e9bb57d50f0484b97b01cb0c5cf54523103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:24.0-git` - linux; amd64

```console
$ docker pull docker@sha256:4e51cfdd3974770c40184831d7f7bc13fc9f7c62f5a8e24600cc8c30122ca88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123440672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8336a6d9c2a5f3c3f2af9c3b39c6c8af0f761926237c5fd5e5d99c6ae39fef`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417625960f4eb232ff8f3c3c3c7466465957015bcb89ef3c065eeef1c297c63`  
		Last Modified: Thu, 06 Jul 2023 20:20:59 GMT  
		Size: 16.4 MB (16389605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897e976d1bc25ad87bf3bc0fc2fccea2dfd64a17b84c8ca84ac706cb06a01c32`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea3511797c57c128bbc7f13cde057bc2342792e1a74505110f5bbaf1a46252`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 18.0 MB (17980095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb167a9f2ed16642a240002a0084af086982ae9ea25df89e058ed0909630afd2`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26505e5ff7f014a740ba6d568c3a66941216e9075d788676625c608f68fdedad`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5959ab5c26b6b799bbf2edfcccda947cc9a991935504a736575796ef6cfbc7cd`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dee904fe330cea37e269897fc7d4f60071040bee3c9c62c840e2addf3ae80d`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 7.1 MB (7080821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4605fd7c180c48c0119af314b08c7f44cea60c2e158df2ee92620374d18b3`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e4046b12ba084fcd4bc6186263c4c8582665222f81806277e5ec9348c2abce`  
		Last Modified: Thu, 06 Jul 2023 20:21:23 GMT  
		Size: 54.2 MB (54182575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593971f39a74770044342d937af0589b370e628d67268791e6fc0a21da05761c`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab1fe34bfb27e76f04d40ee77c6b9a7ef89bd1382eed94c960e54e21dd04cb8`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 2.8 KB (2791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cf7411c8dc4a4b50659d07545570ec924492b3c332977ac680b8f8dd34442f`  
		Last Modified: Thu, 06 Jul 2023 20:22:13 GMT  
		Size: 4.9 MB (4934754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24.0-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dbdbd485df5e901ba6421d316a90b70d0d0c591bbcfd576b3e936f886c201b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114666566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907da1d50ee9a9d68449a225389de0679597b02911c6b10184a5a2ccd69d8aea`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138a1bfb0f6b169ee65e5a20efb7efbefe0586b88be7de24f6af78f14b32998a`  
		Last Modified: Thu, 06 Jul 2023 19:42:28 GMT  
		Size: 15.4 MB (15435069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fb6fd88347451934d0082d9c9a9bd060cc6956ad81f4383fbe5fafea69d676`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 15.8 MB (15759501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181ea99d9b3a3ea4ef43717a4dfa3e9aa03ea6ba3486302dc50e4f0305c9461`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 16.3 MB (16312956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee7977acecd2644fba3d007147c5e3b04abf32fa82d0ef6980e2addd6be948d`  
		Last Modified: Thu, 06 Jul 2023 19:42:24 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909d160bcaa21899b740ecf14d6ee51bbe9f839d0d85f908bbbaad8b9fa3b7c1`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1c4d47beb50032ea66762ccdfc20f6152b72a07f9e80b83eca2f0e4bc0918a`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeb0ef44ad7debf4180e87a10ea2002be4e01aeda327970ff29c5bfbd65c2e7`  
		Last Modified: Thu, 06 Jul 2023 19:42:44 GMT  
		Size: 7.3 MB (7291386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0d48658bc22db36bb84a46d5df20bc9752ff5b07fe125e4a13a9b3d0bd5cdb`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23815654a9b80c2e5d021f7949089b57fa11b0c1d0142ade7db5e2fb2ce416f8`  
		Last Modified: Thu, 06 Jul 2023 19:42:48 GMT  
		Size: 49.5 MB (49485797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffaff52c24235510cee867d28793f9f3d2c3e61d6f12d3584cff8a96b2882f0`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a95386d6a8f394c0ecd1f77ab00fab627db31ea9ead9caba667e87671d8bb51`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 2.8 KB (2792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962a119574903f96d3d7470be0241fc2636062db4d08baa6d61793ce9a361b2c`  
		Last Modified: Thu, 06 Jul 2023 19:43:36 GMT  
		Size: 5.0 MB (5021090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0-windowsservercore`

```console
$ docker pull docker@sha256:e97f3340b4b597c70a321e2485ab06f289f99477f1e667097a6b8e476f851fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1787; amd64
	-	windows version 10.0.17763.4499; amd64

### `docker:24.0-windowsservercore` - windows version 10.0.20348.1787; amd64

```console
$ docker pull docker@sha256:edf247a340baea4e8c2d622fb5af1598abe85113b713dd6a3cd5bc5e40506a42
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1480426537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd92513f922f244389d26853ae3f9cabce18252ff320f58d25bc03adebf7fb3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:33:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 Jul 2023 20:15:10 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 20:15:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.3.zip
# Thu, 06 Jul 2023 20:15:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:15:40 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:15:41 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:15:42 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:16:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:16:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:16:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:16:09 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:16:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27db350c833f7fe0378bc977cd819c1ffe4133ff02ff69f1531f8ddc552c2366`  
		Last Modified: Sat, 24 Jun 2023 01:15:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c818796445a77806e10e6c159d076d6b0f5105edd8e7f27848042efb890970dd`  
		Last Modified: Sat, 24 Jun 2023 03:41:36 GMT  
		Size: 326.7 KB (326673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343faf4d8143dadaf9de6d52c214909510a19d32a2ef2f90860d9aaf4a919692`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8ab0e8f6197c22da65ebbadcd1fe496b029f0fadf873bc625f887c7580a75b`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49d31da5904ec14a1003079c30d7a269f65706ca9af5e2d6ea0cbe7a2762d2d`  
		Last Modified: Thu, 06 Jul 2023 20:21:22 GMT  
		Size: 17.5 MB (17458414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b059f4f69ae92c7ab553a89fe911075af37b363f07301b5821fa58e14158ed9d`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dd12c4af4dd1eda3383bc2e1023236c4a9d31ad0483bd80ff541d5ca92aaf7`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b223fadd37e4d376cc64a69c7c31a7c10bd36cfd3d4c74e85ebe780d2add0c`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ef3be65907ccf52605b51db71fe3b3b12292bad11ab1a49a78a699b004ab06`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 17.9 MB (17883688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f9df1df7303a9e93905852c6fd3c1183da3654ea42a86788484596b0c52a5d`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a0de7a4b55054578241a4e2ec66ccf03b270537b6a18c4e0b3b4250ed14a1c`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c928426eb1e8b4be9068775a7abafdca91118e43ac375399595fe896c759b189`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78728e406ce8bdc2b7dfab0c83103ff85dcf7d19630d4dfd18450e5f13fa2128`  
		Last Modified: Thu, 06 Jul 2023 20:21:21 GMT  
		Size: 18.4 MB (18447298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24.0-windowsservercore` - windows version 10.0.17763.4499; amd64

```console
$ docker pull docker@sha256:f75763c02bfd57528d7f924d779e24e6185ba787ce630fc22b39e936aa91a34e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1704850908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8f774bf3cac154e13a3e7fdda3d391274075199b35f1410c2691ec20f72a36`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:40:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:35:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 Jul 2023 20:16:52 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 20:16:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.3.zip
# Thu, 06 Jul 2023 20:17:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:17:28 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:17:28 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:17:29 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:17:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:17:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:17:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:17:58 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:18:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58717a727cd3a756d7c1180dfb74e95d49735ed12628bd25d2058bc90fa96991`  
		Last Modified: Sat, 24 Jun 2023 01:20:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb210483c7a5877c9d4e754a46a0085ff94bc31d9e32e64c37e1ed4d6e30162e`  
		Last Modified: Sat, 24 Jun 2023 03:41:56 GMT  
		Size: 306.0 KB (305975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220d673a500d122873877d4a4be342cb40e07ee47a4a508dee2dcba97bfe4723`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70790617356246e318492973e7c751cc8fb9199ed00349374fb264e4566ced04`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae1f34dbac2b79a6a652b8926077c0e41dda895cab9b1ac5c75c29db1cde7a6`  
		Last Modified: Thu, 06 Jul 2023 20:21:45 GMT  
		Size: 17.5 MB (17466854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25abab3ba7887100f6f8a30c3316f9a3dc51b171a81f1703159c27c07c25dd82`  
		Last Modified: Thu, 06 Jul 2023 20:21:40 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b56866387a48d55494e41e21da221a0a5fe4b3239dc940b5b75984e14f9cc5`  
		Last Modified: Thu, 06 Jul 2023 20:21:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4cc15bb518b5c263f5d52c7b7761bb36681b7fab382fd34aa9a21042d5055`  
		Last Modified: Thu, 06 Jul 2023 20:21:39 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00adc5a657ac1846710c85cc2992c68dcc4389c3d24d4f5be85599e64aac8e4`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 17.9 MB (17882284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dfe7cd1c7b16458db2fa8613b9b5e2161397d26647a6b16d618bc92922d9868`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb59442896100faf18d8b1d475701d8a7bab03de0ddcd6606a00cffda2665e7a`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a533ef75401c06ad9ab423047654f037ae36177f6bccfbef4bdeb5f98e9c149`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9329ff40635fac09f33414e395d71d781533d78016ebfc61b706c13da4e1e6`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 18.4 MB (18447195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:e84f671e17b7a624b2fe9857ce730d961a9746a3312bb0b29b963fd7c1104f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `docker:24.0-windowsservercore-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull docker@sha256:f75763c02bfd57528d7f924d779e24e6185ba787ce630fc22b39e936aa91a34e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1704850908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8f774bf3cac154e13a3e7fdda3d391274075199b35f1410c2691ec20f72a36`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:40:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:35:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 Jul 2023 20:16:52 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 20:16:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.3.zip
# Thu, 06 Jul 2023 20:17:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:17:28 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:17:28 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:17:29 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:17:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:17:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:17:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:17:58 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:18:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58717a727cd3a756d7c1180dfb74e95d49735ed12628bd25d2058bc90fa96991`  
		Last Modified: Sat, 24 Jun 2023 01:20:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb210483c7a5877c9d4e754a46a0085ff94bc31d9e32e64c37e1ed4d6e30162e`  
		Last Modified: Sat, 24 Jun 2023 03:41:56 GMT  
		Size: 306.0 KB (305975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220d673a500d122873877d4a4be342cb40e07ee47a4a508dee2dcba97bfe4723`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70790617356246e318492973e7c751cc8fb9199ed00349374fb264e4566ced04`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae1f34dbac2b79a6a652b8926077c0e41dda895cab9b1ac5c75c29db1cde7a6`  
		Last Modified: Thu, 06 Jul 2023 20:21:45 GMT  
		Size: 17.5 MB (17466854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25abab3ba7887100f6f8a30c3316f9a3dc51b171a81f1703159c27c07c25dd82`  
		Last Modified: Thu, 06 Jul 2023 20:21:40 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b56866387a48d55494e41e21da221a0a5fe4b3239dc940b5b75984e14f9cc5`  
		Last Modified: Thu, 06 Jul 2023 20:21:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4cc15bb518b5c263f5d52c7b7761bb36681b7fab382fd34aa9a21042d5055`  
		Last Modified: Thu, 06 Jul 2023 20:21:39 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00adc5a657ac1846710c85cc2992c68dcc4389c3d24d4f5be85599e64aac8e4`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 17.9 MB (17882284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dfe7cd1c7b16458db2fa8613b9b5e2161397d26647a6b16d618bc92922d9868`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb59442896100faf18d8b1d475701d8a7bab03de0ddcd6606a00cffda2665e7a`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a533ef75401c06ad9ab423047654f037ae36177f6bccfbef4bdeb5f98e9c149`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9329ff40635fac09f33414e395d71d781533d78016ebfc61b706c13da4e1e6`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 18.4 MB (18447195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:f10cd504d09011ac66e85ad70c551a4bb16edb03f9c5c994349037b63be211be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1787; amd64

### `docker:24.0-windowsservercore-ltsc2022` - windows version 10.0.20348.1787; amd64

```console
$ docker pull docker@sha256:edf247a340baea4e8c2d622fb5af1598abe85113b713dd6a3cd5bc5e40506a42
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1480426537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd92513f922f244389d26853ae3f9cabce18252ff320f58d25bc03adebf7fb3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:33:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 Jul 2023 20:15:10 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 20:15:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.3.zip
# Thu, 06 Jul 2023 20:15:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:15:40 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:15:41 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:15:42 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:16:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:16:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:16:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:16:09 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:16:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27db350c833f7fe0378bc977cd819c1ffe4133ff02ff69f1531f8ddc552c2366`  
		Last Modified: Sat, 24 Jun 2023 01:15:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c818796445a77806e10e6c159d076d6b0f5105edd8e7f27848042efb890970dd`  
		Last Modified: Sat, 24 Jun 2023 03:41:36 GMT  
		Size: 326.7 KB (326673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343faf4d8143dadaf9de6d52c214909510a19d32a2ef2f90860d9aaf4a919692`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8ab0e8f6197c22da65ebbadcd1fe496b029f0fadf873bc625f887c7580a75b`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49d31da5904ec14a1003079c30d7a269f65706ca9af5e2d6ea0cbe7a2762d2d`  
		Last Modified: Thu, 06 Jul 2023 20:21:22 GMT  
		Size: 17.5 MB (17458414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b059f4f69ae92c7ab553a89fe911075af37b363f07301b5821fa58e14158ed9d`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dd12c4af4dd1eda3383bc2e1023236c4a9d31ad0483bd80ff541d5ca92aaf7`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b223fadd37e4d376cc64a69c7c31a7c10bd36cfd3d4c74e85ebe780d2add0c`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ef3be65907ccf52605b51db71fe3b3b12292bad11ab1a49a78a699b004ab06`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 17.9 MB (17883688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f9df1df7303a9e93905852c6fd3c1183da3654ea42a86788484596b0c52a5d`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a0de7a4b55054578241a4e2ec66ccf03b270537b6a18c4e0b3b4250ed14a1c`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c928426eb1e8b4be9068775a7abafdca91118e43ac375399595fe896c759b189`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78728e406ce8bdc2b7dfab0c83103ff85dcf7d19630d4dfd18450e5f13fa2128`  
		Last Modified: Thu, 06 Jul 2023 20:21:21 GMT  
		Size: 18.4 MB (18447298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0.4`

**does not exist** (yet?)

## `docker:24.0.4-alpine3.18`

**does not exist** (yet?)

## `docker:24.0.4-cli`

**does not exist** (yet?)

## `docker:24.0.4-cli-alpine3.18`

**does not exist** (yet?)

## `docker:24.0.4-dind`

**does not exist** (yet?)

## `docker:24.0.4-dind-alpine3.18`

**does not exist** (yet?)

## `docker:24.0.4-dind-rootless`

**does not exist** (yet?)

## `docker:24.0.4-git`

**does not exist** (yet?)

## `docker:24.0.4-windowsservercore`

**does not exist** (yet?)

## `docker:24.0.4-windowsservercore-1809`

**does not exist** (yet?)

## `docker:24.0.4-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `docker:cli`

```console
$ docker pull docker@sha256:03560e8a49bed0fcf4c95faa6d6bfcbabaec9a9fddb0d4021e2529911a3ecee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:cli` - linux; amd64

```console
$ docker pull docker@sha256:c5eb2895781a0f4dbd69e06592a83e06d0bcae82738ec6222947f6d097ee9c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57237362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d3c497c4020c189c0451838f1350661dcab40a016ca3834fb26ec7589f288d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417625960f4eb232ff8f3c3c3c7466465957015bcb89ef3c065eeef1c297c63`  
		Last Modified: Thu, 06 Jul 2023 20:20:59 GMT  
		Size: 16.4 MB (16389605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897e976d1bc25ad87bf3bc0fc2fccea2dfd64a17b84c8ca84ac706cb06a01c32`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea3511797c57c128bbc7f13cde057bc2342792e1a74505110f5bbaf1a46252`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 18.0 MB (17980095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb167a9f2ed16642a240002a0084af086982ae9ea25df89e058ed0909630afd2`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26505e5ff7f014a740ba6d568c3a66941216e9075d788676625c608f68fdedad`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5959ab5c26b6b799bbf2edfcccda947cc9a991935504a736575796ef6cfbc7cd`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2486e25cc930eb7262299c21cbb0e30fc0f33adb3e3eb90ea12b8a0cb9f1a20b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52863134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930466f01330adb4e89d3a391447368f0b41bd54f01dbf5ef428af5438cf90e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138a1bfb0f6b169ee65e5a20efb7efbefe0586b88be7de24f6af78f14b32998a`  
		Last Modified: Thu, 06 Jul 2023 19:42:28 GMT  
		Size: 15.4 MB (15435069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fb6fd88347451934d0082d9c9a9bd060cc6956ad81f4383fbe5fafea69d676`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 15.8 MB (15759501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181ea99d9b3a3ea4ef43717a4dfa3e9aa03ea6ba3486302dc50e4f0305c9461`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 16.3 MB (16312956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee7977acecd2644fba3d007147c5e3b04abf32fa82d0ef6980e2addd6be948d`  
		Last Modified: Thu, 06 Jul 2023 19:42:24 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909d160bcaa21899b740ecf14d6ee51bbe9f839d0d85f908bbbaad8b9fa3b7c1`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1c4d47beb50032ea66762ccdfc20f6152b72a07f9e80b83eca2f0e4bc0918a`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind`

```console
$ docker pull docker@sha256:8c39dc84d3a2cf61545c50689140f0cb29a672b8bccac1a5ebce12b402c9b32f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:cd573a0e55aa7ef9f2b767816baabd96f1b7e0edb4e3409ed14b2247a75e978d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118505918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b102eb731a4a7323f0ec6d928a5c68a7ab09b0a0230fe2416692f0080f8cd24b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417625960f4eb232ff8f3c3c3c7466465957015bcb89ef3c065eeef1c297c63`  
		Last Modified: Thu, 06 Jul 2023 20:20:59 GMT  
		Size: 16.4 MB (16389605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897e976d1bc25ad87bf3bc0fc2fccea2dfd64a17b84c8ca84ac706cb06a01c32`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea3511797c57c128bbc7f13cde057bc2342792e1a74505110f5bbaf1a46252`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 18.0 MB (17980095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb167a9f2ed16642a240002a0084af086982ae9ea25df89e058ed0909630afd2`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26505e5ff7f014a740ba6d568c3a66941216e9075d788676625c608f68fdedad`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5959ab5c26b6b799bbf2edfcccda947cc9a991935504a736575796ef6cfbc7cd`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dee904fe330cea37e269897fc7d4f60071040bee3c9c62c840e2addf3ae80d`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 7.1 MB (7080821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4605fd7c180c48c0119af314b08c7f44cea60c2e158df2ee92620374d18b3`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e4046b12ba084fcd4bc6186263c4c8582665222f81806277e5ec9348c2abce`  
		Last Modified: Thu, 06 Jul 2023 20:21:23 GMT  
		Size: 54.2 MB (54182575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593971f39a74770044342d937af0589b370e628d67268791e6fc0a21da05761c`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab1fe34bfb27e76f04d40ee77c6b9a7ef89bd1382eed94c960e54e21dd04cb8`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 2.8 KB (2791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7a0abbf5e8f6711b11680ac63e811b2cb9021178f9f33274b1e19e8863fa2c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109645476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8d6284fedab4472799ada0958c4f8933b7ad583ce1ce8d4a9cbdda36ec2022`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138a1bfb0f6b169ee65e5a20efb7efbefe0586b88be7de24f6af78f14b32998a`  
		Last Modified: Thu, 06 Jul 2023 19:42:28 GMT  
		Size: 15.4 MB (15435069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fb6fd88347451934d0082d9c9a9bd060cc6956ad81f4383fbe5fafea69d676`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 15.8 MB (15759501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181ea99d9b3a3ea4ef43717a4dfa3e9aa03ea6ba3486302dc50e4f0305c9461`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 16.3 MB (16312956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee7977acecd2644fba3d007147c5e3b04abf32fa82d0ef6980e2addd6be948d`  
		Last Modified: Thu, 06 Jul 2023 19:42:24 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909d160bcaa21899b740ecf14d6ee51bbe9f839d0d85f908bbbaad8b9fa3b7c1`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1c4d47beb50032ea66762ccdfc20f6152b72a07f9e80b83eca2f0e4bc0918a`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeb0ef44ad7debf4180e87a10ea2002be4e01aeda327970ff29c5bfbd65c2e7`  
		Last Modified: Thu, 06 Jul 2023 19:42:44 GMT  
		Size: 7.3 MB (7291386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0d48658bc22db36bb84a46d5df20bc9752ff5b07fe125e4a13a9b3d0bd5cdb`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23815654a9b80c2e5d021f7949089b57fa11b0c1d0142ade7db5e2fb2ce416f8`  
		Last Modified: Thu, 06 Jul 2023 19:42:48 GMT  
		Size: 49.5 MB (49485797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffaff52c24235510cee867d28793f9f3d2c3e61d6f12d3584cff8a96b2882f0`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a95386d6a8f394c0ecd1f77ab00fab627db31ea9ead9caba667e87671d8bb51`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 2.8 KB (2792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:eb5cee8eeecc5b5a2f7757200b903fb48ff6decf135068367425edbc8c7dd7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:f092337b953d62b8d64b97f7eb44290811cbecc77b44fd9b2ed2b01eab39862c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140520384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313742b11beb8009157dbc242bae085f12de358e14f7b130b353cbc7d471706c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
USER rootless
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417625960f4eb232ff8f3c3c3c7466465957015bcb89ef3c065eeef1c297c63`  
		Last Modified: Thu, 06 Jul 2023 20:20:59 GMT  
		Size: 16.4 MB (16389605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897e976d1bc25ad87bf3bc0fc2fccea2dfd64a17b84c8ca84ac706cb06a01c32`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea3511797c57c128bbc7f13cde057bc2342792e1a74505110f5bbaf1a46252`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 18.0 MB (17980095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb167a9f2ed16642a240002a0084af086982ae9ea25df89e058ed0909630afd2`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26505e5ff7f014a740ba6d568c3a66941216e9075d788676625c608f68fdedad`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5959ab5c26b6b799bbf2edfcccda947cc9a991935504a736575796ef6cfbc7cd`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dee904fe330cea37e269897fc7d4f60071040bee3c9c62c840e2addf3ae80d`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 7.1 MB (7080821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4605fd7c180c48c0119af314b08c7f44cea60c2e158df2ee92620374d18b3`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e4046b12ba084fcd4bc6186263c4c8582665222f81806277e5ec9348c2abce`  
		Last Modified: Thu, 06 Jul 2023 20:21:23 GMT  
		Size: 54.2 MB (54182575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593971f39a74770044342d937af0589b370e628d67268791e6fc0a21da05761c`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab1fe34bfb27e76f04d40ee77c6b9a7ef89bd1382eed94c960e54e21dd04cb8`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 2.8 KB (2791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bc35a0dc3eb3e494e9bc68c57a01b07b4bef93e143a639d5973c394dca71b4`  
		Last Modified: Thu, 06 Jul 2023 20:21:54 GMT  
		Size: 1.4 MB (1362372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcb6ace6229c8a616b83b359ea04d5e2f95cb702d531da29bca3185b13f1ce0`  
		Last Modified: Thu, 06 Jul 2023 20:21:53 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c7035e55b9c75d1406886fc8f9cf808e88ed8cd02e3b489f30bfdffd6661b8`  
		Last Modified: Thu, 06 Jul 2023 20:21:53 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc9cc3e18eff8c744b78fb60f9b01d0b397433309d1fa90b72ce939bad40288`  
		Last Modified: Thu, 06 Jul 2023 20:21:57 GMT  
		Size: 20.7 MB (20650355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db87cb1cd3c112f8657f04b1ea20ccf06d330bd4d80196966f4eb8fa23205ee0`  
		Last Modified: Thu, 06 Jul 2023 20:21:53 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:49d71ba16a6e4899bad3069608b61d7117ae6cd1e48f813f8314a4d42d01011b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133511196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f605f34be1d9f7c3a910078506e30058c387d191f60900e8543a1a58f55e7a7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
USER rootless
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138a1bfb0f6b169ee65e5a20efb7efbefe0586b88be7de24f6af78f14b32998a`  
		Last Modified: Thu, 06 Jul 2023 19:42:28 GMT  
		Size: 15.4 MB (15435069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fb6fd88347451934d0082d9c9a9bd060cc6956ad81f4383fbe5fafea69d676`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 15.8 MB (15759501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181ea99d9b3a3ea4ef43717a4dfa3e9aa03ea6ba3486302dc50e4f0305c9461`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 16.3 MB (16312956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee7977acecd2644fba3d007147c5e3b04abf32fa82d0ef6980e2addd6be948d`  
		Last Modified: Thu, 06 Jul 2023 19:42:24 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909d160bcaa21899b740ecf14d6ee51bbe9f839d0d85f908bbbaad8b9fa3b7c1`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1c4d47beb50032ea66762ccdfc20f6152b72a07f9e80b83eca2f0e4bc0918a`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeb0ef44ad7debf4180e87a10ea2002be4e01aeda327970ff29c5bfbd65c2e7`  
		Last Modified: Thu, 06 Jul 2023 19:42:44 GMT  
		Size: 7.3 MB (7291386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0d48658bc22db36bb84a46d5df20bc9752ff5b07fe125e4a13a9b3d0bd5cdb`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23815654a9b80c2e5d021f7949089b57fa11b0c1d0142ade7db5e2fb2ce416f8`  
		Last Modified: Thu, 06 Jul 2023 19:42:48 GMT  
		Size: 49.5 MB (49485797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffaff52c24235510cee867d28793f9f3d2c3e61d6f12d3584cff8a96b2882f0`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a95386d6a8f394c0ecd1f77ab00fab627db31ea9ead9caba667e87671d8bb51`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 2.8 KB (2792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c042a310de5c2f6450c02438b35cc0f5094f63e3d485a8572a346f386699d0e2`  
		Last Modified: Thu, 06 Jul 2023 19:43:18 GMT  
		Size: 1.4 MB (1413238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfd46e0bc98f20fd18fa46c68ab6bde20f9e3da0b046ecd7397b69415205646`  
		Last Modified: Thu, 06 Jul 2023 19:43:18 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a53c68d9732d03c650deea803d295f0cb7755e5e7a56bccea42aa4c698d58d`  
		Last Modified: Thu, 06 Jul 2023 19:43:19 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd2df083914deeada6a2d428f2329858807d6627e6ebaec1dd448caa658a51c`  
		Last Modified: Thu, 06 Jul 2023 19:43:21 GMT  
		Size: 22.5 MB (22450742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73160a7bc4290cbb1265a17afaab5e40e183006e5e96b4eab646be5e79c9f80f`  
		Last Modified: Thu, 06 Jul 2023 19:43:18 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:git`

```console
$ docker pull docker@sha256:f5545c2d805d4305686fc015c2598e9bb57d50f0484b97b01cb0c5cf54523103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:4e51cfdd3974770c40184831d7f7bc13fc9f7c62f5a8e24600cc8c30122ca88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123440672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8336a6d9c2a5f3c3f2af9c3b39c6c8af0f761926237c5fd5e5d99c6ae39fef`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417625960f4eb232ff8f3c3c3c7466465957015bcb89ef3c065eeef1c297c63`  
		Last Modified: Thu, 06 Jul 2023 20:20:59 GMT  
		Size: 16.4 MB (16389605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897e976d1bc25ad87bf3bc0fc2fccea2dfd64a17b84c8ca84ac706cb06a01c32`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea3511797c57c128bbc7f13cde057bc2342792e1a74505110f5bbaf1a46252`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 18.0 MB (17980095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb167a9f2ed16642a240002a0084af086982ae9ea25df89e058ed0909630afd2`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26505e5ff7f014a740ba6d568c3a66941216e9075d788676625c608f68fdedad`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5959ab5c26b6b799bbf2edfcccda947cc9a991935504a736575796ef6cfbc7cd`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dee904fe330cea37e269897fc7d4f60071040bee3c9c62c840e2addf3ae80d`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 7.1 MB (7080821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4605fd7c180c48c0119af314b08c7f44cea60c2e158df2ee92620374d18b3`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e4046b12ba084fcd4bc6186263c4c8582665222f81806277e5ec9348c2abce`  
		Last Modified: Thu, 06 Jul 2023 20:21:23 GMT  
		Size: 54.2 MB (54182575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593971f39a74770044342d937af0589b370e628d67268791e6fc0a21da05761c`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab1fe34bfb27e76f04d40ee77c6b9a7ef89bd1382eed94c960e54e21dd04cb8`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 2.8 KB (2791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cf7411c8dc4a4b50659d07545570ec924492b3c332977ac680b8f8dd34442f`  
		Last Modified: Thu, 06 Jul 2023 20:22:13 GMT  
		Size: 4.9 MB (4934754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dbdbd485df5e901ba6421d316a90b70d0d0c591bbcfd576b3e936f886c201b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114666566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907da1d50ee9a9d68449a225389de0679597b02911c6b10184a5a2ccd69d8aea`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138a1bfb0f6b169ee65e5a20efb7efbefe0586b88be7de24f6af78f14b32998a`  
		Last Modified: Thu, 06 Jul 2023 19:42:28 GMT  
		Size: 15.4 MB (15435069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fb6fd88347451934d0082d9c9a9bd060cc6956ad81f4383fbe5fafea69d676`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 15.8 MB (15759501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181ea99d9b3a3ea4ef43717a4dfa3e9aa03ea6ba3486302dc50e4f0305c9461`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 16.3 MB (16312956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee7977acecd2644fba3d007147c5e3b04abf32fa82d0ef6980e2addd6be948d`  
		Last Modified: Thu, 06 Jul 2023 19:42:24 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909d160bcaa21899b740ecf14d6ee51bbe9f839d0d85f908bbbaad8b9fa3b7c1`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1c4d47beb50032ea66762ccdfc20f6152b72a07f9e80b83eca2f0e4bc0918a`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeb0ef44ad7debf4180e87a10ea2002be4e01aeda327970ff29c5bfbd65c2e7`  
		Last Modified: Thu, 06 Jul 2023 19:42:44 GMT  
		Size: 7.3 MB (7291386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0d48658bc22db36bb84a46d5df20bc9752ff5b07fe125e4a13a9b3d0bd5cdb`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23815654a9b80c2e5d021f7949089b57fa11b0c1d0142ade7db5e2fb2ce416f8`  
		Last Modified: Thu, 06 Jul 2023 19:42:48 GMT  
		Size: 49.5 MB (49485797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffaff52c24235510cee867d28793f9f3d2c3e61d6f12d3584cff8a96b2882f0`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a95386d6a8f394c0ecd1f77ab00fab627db31ea9ead9caba667e87671d8bb51`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 2.8 KB (2792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962a119574903f96d3d7470be0241fc2636062db4d08baa6d61793ce9a361b2c`  
		Last Modified: Thu, 06 Jul 2023 19:43:36 GMT  
		Size: 5.0 MB (5021090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:latest`

```console
$ docker pull docker@sha256:8c39dc84d3a2cf61545c50689140f0cb29a672b8bccac1a5ebce12b402c9b32f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:cd573a0e55aa7ef9f2b767816baabd96f1b7e0edb4e3409ed14b2247a75e978d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118505918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b102eb731a4a7323f0ec6d928a5c68a7ab09b0a0230fe2416692f0080f8cd24b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417625960f4eb232ff8f3c3c3c7466465957015bcb89ef3c065eeef1c297c63`  
		Last Modified: Thu, 06 Jul 2023 20:20:59 GMT  
		Size: 16.4 MB (16389605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897e976d1bc25ad87bf3bc0fc2fccea2dfd64a17b84c8ca84ac706cb06a01c32`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea3511797c57c128bbc7f13cde057bc2342792e1a74505110f5bbaf1a46252`  
		Last Modified: Thu, 06 Jul 2023 20:20:58 GMT  
		Size: 18.0 MB (17980095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb167a9f2ed16642a240002a0084af086982ae9ea25df89e058ed0909630afd2`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26505e5ff7f014a740ba6d568c3a66941216e9075d788676625c608f68fdedad`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5959ab5c26b6b799bbf2edfcccda947cc9a991935504a736575796ef6cfbc7cd`  
		Last Modified: Thu, 06 Jul 2023 20:20:55 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dee904fe330cea37e269897fc7d4f60071040bee3c9c62c840e2addf3ae80d`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 7.1 MB (7080821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4605fd7c180c48c0119af314b08c7f44cea60c2e158df2ee92620374d18b3`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e4046b12ba084fcd4bc6186263c4c8582665222f81806277e5ec9348c2abce`  
		Last Modified: Thu, 06 Jul 2023 20:21:23 GMT  
		Size: 54.2 MB (54182575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593971f39a74770044342d937af0589b370e628d67268791e6fc0a21da05761c`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab1fe34bfb27e76f04d40ee77c6b9a7ef89bd1382eed94c960e54e21dd04cb8`  
		Last Modified: Thu, 06 Jul 2023 20:21:15 GMT  
		Size: 2.8 KB (2791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7a0abbf5e8f6711b11680ac63e811b2cb9021178f9f33274b1e19e8863fa2c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109645476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8d6284fedab4472799ada0958c4f8933b7ad583ce1ce8d4a9cbdda36ec2022`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 06 Jul 2023 17:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD ["sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Thu, 06 Jul 2023 17:56:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jul 2023 17:56:11 GMT
VOLUME [/var/lib/docker]
# Thu, 06 Jul 2023 17:56:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 06 Jul 2023 17:56:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 06 Jul 2023 17:56:11 GMT
CMD []
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138a1bfb0f6b169ee65e5a20efb7efbefe0586b88be7de24f6af78f14b32998a`  
		Last Modified: Thu, 06 Jul 2023 19:42:28 GMT  
		Size: 15.4 MB (15435069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fb6fd88347451934d0082d9c9a9bd060cc6956ad81f4383fbe5fafea69d676`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 15.8 MB (15759501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181ea99d9b3a3ea4ef43717a4dfa3e9aa03ea6ba3486302dc50e4f0305c9461`  
		Last Modified: Thu, 06 Jul 2023 19:42:27 GMT  
		Size: 16.3 MB (16312956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee7977acecd2644fba3d007147c5e3b04abf32fa82d0ef6980e2addd6be948d`  
		Last Modified: Thu, 06 Jul 2023 19:42:24 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909d160bcaa21899b740ecf14d6ee51bbe9f839d0d85f908bbbaad8b9fa3b7c1`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1c4d47beb50032ea66762ccdfc20f6152b72a07f9e80b83eca2f0e4bc0918a`  
		Last Modified: Thu, 06 Jul 2023 19:42:25 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeb0ef44ad7debf4180e87a10ea2002be4e01aeda327970ff29c5bfbd65c2e7`  
		Last Modified: Thu, 06 Jul 2023 19:42:44 GMT  
		Size: 7.3 MB (7291386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0d48658bc22db36bb84a46d5df20bc9752ff5b07fe125e4a13a9b3d0bd5cdb`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23815654a9b80c2e5d021f7949089b57fa11b0c1d0142ade7db5e2fb2ce416f8`  
		Last Modified: Thu, 06 Jul 2023 19:42:48 GMT  
		Size: 49.5 MB (49485797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffaff52c24235510cee867d28793f9f3d2c3e61d6f12d3584cff8a96b2882f0`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a95386d6a8f394c0ecd1f77ab00fab627db31ea9ead9caba667e87671d8bb51`  
		Last Modified: Thu, 06 Jul 2023 19:42:43 GMT  
		Size: 2.8 KB (2792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:e97f3340b4b597c70a321e2485ab06f289f99477f1e667097a6b8e476f851fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1787; amd64
	-	windows version 10.0.17763.4499; amd64

### `docker:windowsservercore` - windows version 10.0.20348.1787; amd64

```console
$ docker pull docker@sha256:edf247a340baea4e8c2d622fb5af1598abe85113b713dd6a3cd5bc5e40506a42
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1480426537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd92513f922f244389d26853ae3f9cabce18252ff320f58d25bc03adebf7fb3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:33:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 Jul 2023 20:15:10 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 20:15:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.3.zip
# Thu, 06 Jul 2023 20:15:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:15:40 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:15:41 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:15:42 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:16:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:16:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:16:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:16:09 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:16:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27db350c833f7fe0378bc977cd819c1ffe4133ff02ff69f1531f8ddc552c2366`  
		Last Modified: Sat, 24 Jun 2023 01:15:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c818796445a77806e10e6c159d076d6b0f5105edd8e7f27848042efb890970dd`  
		Last Modified: Sat, 24 Jun 2023 03:41:36 GMT  
		Size: 326.7 KB (326673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343faf4d8143dadaf9de6d52c214909510a19d32a2ef2f90860d9aaf4a919692`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8ab0e8f6197c22da65ebbadcd1fe496b029f0fadf873bc625f887c7580a75b`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49d31da5904ec14a1003079c30d7a269f65706ca9af5e2d6ea0cbe7a2762d2d`  
		Last Modified: Thu, 06 Jul 2023 20:21:22 GMT  
		Size: 17.5 MB (17458414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b059f4f69ae92c7ab553a89fe911075af37b363f07301b5821fa58e14158ed9d`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dd12c4af4dd1eda3383bc2e1023236c4a9d31ad0483bd80ff541d5ca92aaf7`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b223fadd37e4d376cc64a69c7c31a7c10bd36cfd3d4c74e85ebe780d2add0c`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ef3be65907ccf52605b51db71fe3b3b12292bad11ab1a49a78a699b004ab06`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 17.9 MB (17883688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f9df1df7303a9e93905852c6fd3c1183da3654ea42a86788484596b0c52a5d`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a0de7a4b55054578241a4e2ec66ccf03b270537b6a18c4e0b3b4250ed14a1c`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c928426eb1e8b4be9068775a7abafdca91118e43ac375399595fe896c759b189`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78728e406ce8bdc2b7dfab0c83103ff85dcf7d19630d4dfd18450e5f13fa2128`  
		Last Modified: Thu, 06 Jul 2023 20:21:21 GMT  
		Size: 18.4 MB (18447298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.4499; amd64

```console
$ docker pull docker@sha256:f75763c02bfd57528d7f924d779e24e6185ba787ce630fc22b39e936aa91a34e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1704850908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8f774bf3cac154e13a3e7fdda3d391274075199b35f1410c2691ec20f72a36`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:40:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:35:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 Jul 2023 20:16:52 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 20:16:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.3.zip
# Thu, 06 Jul 2023 20:17:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:17:28 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:17:28 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:17:29 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:17:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:17:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:17:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:17:58 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:18:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58717a727cd3a756d7c1180dfb74e95d49735ed12628bd25d2058bc90fa96991`  
		Last Modified: Sat, 24 Jun 2023 01:20:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb210483c7a5877c9d4e754a46a0085ff94bc31d9e32e64c37e1ed4d6e30162e`  
		Last Modified: Sat, 24 Jun 2023 03:41:56 GMT  
		Size: 306.0 KB (305975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220d673a500d122873877d4a4be342cb40e07ee47a4a508dee2dcba97bfe4723`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70790617356246e318492973e7c751cc8fb9199ed00349374fb264e4566ced04`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae1f34dbac2b79a6a652b8926077c0e41dda895cab9b1ac5c75c29db1cde7a6`  
		Last Modified: Thu, 06 Jul 2023 20:21:45 GMT  
		Size: 17.5 MB (17466854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25abab3ba7887100f6f8a30c3316f9a3dc51b171a81f1703159c27c07c25dd82`  
		Last Modified: Thu, 06 Jul 2023 20:21:40 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b56866387a48d55494e41e21da221a0a5fe4b3239dc940b5b75984e14f9cc5`  
		Last Modified: Thu, 06 Jul 2023 20:21:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4cc15bb518b5c263f5d52c7b7761bb36681b7fab382fd34aa9a21042d5055`  
		Last Modified: Thu, 06 Jul 2023 20:21:39 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00adc5a657ac1846710c85cc2992c68dcc4389c3d24d4f5be85599e64aac8e4`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 17.9 MB (17882284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dfe7cd1c7b16458db2fa8613b9b5e2161397d26647a6b16d618bc92922d9868`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb59442896100faf18d8b1d475701d8a7bab03de0ddcd6606a00cffda2665e7a`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a533ef75401c06ad9ab423047654f037ae36177f6bccfbef4bdeb5f98e9c149`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9329ff40635fac09f33414e395d71d781533d78016ebfc61b706c13da4e1e6`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 18.4 MB (18447195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:e84f671e17b7a624b2fe9857ce730d961a9746a3312bb0b29b963fd7c1104f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull docker@sha256:f75763c02bfd57528d7f924d779e24e6185ba787ce630fc22b39e936aa91a34e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1704850908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8f774bf3cac154e13a3e7fdda3d391274075199b35f1410c2691ec20f72a36`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:40:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:35:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 Jul 2023 20:16:52 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 20:16:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.3.zip
# Thu, 06 Jul 2023 20:17:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:17:28 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:17:28 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:17:29 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:17:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:17:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:17:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:17:58 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:18:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58717a727cd3a756d7c1180dfb74e95d49735ed12628bd25d2058bc90fa96991`  
		Last Modified: Sat, 24 Jun 2023 01:20:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb210483c7a5877c9d4e754a46a0085ff94bc31d9e32e64c37e1ed4d6e30162e`  
		Last Modified: Sat, 24 Jun 2023 03:41:56 GMT  
		Size: 306.0 KB (305975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220d673a500d122873877d4a4be342cb40e07ee47a4a508dee2dcba97bfe4723`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70790617356246e318492973e7c751cc8fb9199ed00349374fb264e4566ced04`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae1f34dbac2b79a6a652b8926077c0e41dda895cab9b1ac5c75c29db1cde7a6`  
		Last Modified: Thu, 06 Jul 2023 20:21:45 GMT  
		Size: 17.5 MB (17466854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25abab3ba7887100f6f8a30c3316f9a3dc51b171a81f1703159c27c07c25dd82`  
		Last Modified: Thu, 06 Jul 2023 20:21:40 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b56866387a48d55494e41e21da221a0a5fe4b3239dc940b5b75984e14f9cc5`  
		Last Modified: Thu, 06 Jul 2023 20:21:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4cc15bb518b5c263f5d52c7b7761bb36681b7fab382fd34aa9a21042d5055`  
		Last Modified: Thu, 06 Jul 2023 20:21:39 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00adc5a657ac1846710c85cc2992c68dcc4389c3d24d4f5be85599e64aac8e4`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 17.9 MB (17882284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dfe7cd1c7b16458db2fa8613b9b5e2161397d26647a6b16d618bc92922d9868`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb59442896100faf18d8b1d475701d8a7bab03de0ddcd6606a00cffda2665e7a`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a533ef75401c06ad9ab423047654f037ae36177f6bccfbef4bdeb5f98e9c149`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9329ff40635fac09f33414e395d71d781533d78016ebfc61b706c13da4e1e6`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 18.4 MB (18447195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:f10cd504d09011ac66e85ad70c551a4bb16edb03f9c5c994349037b63be211be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1787; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.1787; amd64

```console
$ docker pull docker@sha256:edf247a340baea4e8c2d622fb5af1598abe85113b713dd6a3cd5bc5e40506a42
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1480426537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd92513f922f244389d26853ae3f9cabce18252ff320f58d25bc03adebf7fb3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:33:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 Jul 2023 20:15:10 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 20:15:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.3.zip
# Thu, 06 Jul 2023 20:15:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:15:40 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:15:41 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:15:42 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:16:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:16:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:16:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:16:09 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:16:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27db350c833f7fe0378bc977cd819c1ffe4133ff02ff69f1531f8ddc552c2366`  
		Last Modified: Sat, 24 Jun 2023 01:15:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c818796445a77806e10e6c159d076d6b0f5105edd8e7f27848042efb890970dd`  
		Last Modified: Sat, 24 Jun 2023 03:41:36 GMT  
		Size: 326.7 KB (326673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343faf4d8143dadaf9de6d52c214909510a19d32a2ef2f90860d9aaf4a919692`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8ab0e8f6197c22da65ebbadcd1fe496b029f0fadf873bc625f887c7580a75b`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49d31da5904ec14a1003079c30d7a269f65706ca9af5e2d6ea0cbe7a2762d2d`  
		Last Modified: Thu, 06 Jul 2023 20:21:22 GMT  
		Size: 17.5 MB (17458414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b059f4f69ae92c7ab553a89fe911075af37b363f07301b5821fa58e14158ed9d`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dd12c4af4dd1eda3383bc2e1023236c4a9d31ad0483bd80ff541d5ca92aaf7`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b223fadd37e4d376cc64a69c7c31a7c10bd36cfd3d4c74e85ebe780d2add0c`  
		Last Modified: Thu, 06 Jul 2023 20:21:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ef3be65907ccf52605b51db71fe3b3b12292bad11ab1a49a78a699b004ab06`  
		Last Modified: Thu, 06 Jul 2023 20:21:20 GMT  
		Size: 17.9 MB (17883688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f9df1df7303a9e93905852c6fd3c1183da3654ea42a86788484596b0c52a5d`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a0de7a4b55054578241a4e2ec66ccf03b270537b6a18c4e0b3b4250ed14a1c`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c928426eb1e8b4be9068775a7abafdca91118e43ac375399595fe896c759b189`  
		Last Modified: Thu, 06 Jul 2023 20:21:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78728e406ce8bdc2b7dfab0c83103ff85dcf7d19630d4dfd18450e5f13fa2128`  
		Last Modified: Thu, 06 Jul 2023 20:21:21 GMT  
		Size: 18.4 MB (18447298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
