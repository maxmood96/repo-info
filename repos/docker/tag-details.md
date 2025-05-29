<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:28`](#docker28)
-	[`docker:28-cli`](#docker28-cli)
-	[`docker:28-dind`](#docker28-dind)
-	[`docker:28-dind-rootless`](#docker28-dind-rootless)
-	[`docker:28-windowsservercore`](#docker28-windowsservercore)
-	[`docker:28-windowsservercore-1809`](#docker28-windowsservercore-1809)
-	[`docker:28-windowsservercore-ltsc2022`](#docker28-windowsservercore-ltsc2022)
-	[`docker:28-windowsservercore-ltsc2025`](#docker28-windowsservercore-ltsc2025)
-	[`docker:28.2`](#docker282)
-	[`docker:28.2-cli`](#docker282-cli)
-	[`docker:28.2-dind`](#docker282-dind)
-	[`docker:28.2-dind-rootless`](#docker282-dind-rootless)
-	[`docker:28.2-windowsservercore`](#docker282-windowsservercore)
-	[`docker:28.2-windowsservercore-1809`](#docker282-windowsservercore-1809)
-	[`docker:28.2-windowsservercore-ltsc2022`](#docker282-windowsservercore-ltsc2022)
-	[`docker:28.2-windowsservercore-ltsc2025`](#docker282-windowsservercore-ltsc2025)
-	[`docker:28.2.1`](#docker2821)
-	[`docker:28.2.1-alpine3.21`](#docker2821-alpine321)
-	[`docker:28.2.1-cli`](#docker2821-cli)
-	[`docker:28.2.1-cli-alpine3.21`](#docker2821-cli-alpine321)
-	[`docker:28.2.1-dind`](#docker2821-dind)
-	[`docker:28.2.1-dind-alpine3.21`](#docker2821-dind-alpine321)
-	[`docker:28.2.1-dind-rootless`](#docker2821-dind-rootless)
-	[`docker:28.2.1-windowsservercore`](#docker2821-windowsservercore)
-	[`docker:28.2.1-windowsservercore-1809`](#docker2821-windowsservercore-1809)
-	[`docker:28.2.1-windowsservercore-ltsc2022`](#docker2821-windowsservercore-ltsc2022)
-	[`docker:28.2.1-windowsservercore-ltsc2025`](#docker2821-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:28`

```console
$ docker pull docker@sha256:eceba5b0fc2fcf83a74c298391c2ed9e1adbdaf04ee173611bd6282ec973e7ba
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
$ docker pull docker@sha256:8c45ce8d05a9f86533788783b53b8ffeb3879b4986821374a47277a3d042712d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140858792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da0bd7ecf78eacd7de485edf3565b12c1f71facbeceb4f9b8bfc60805d7b4e9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_VERSION=28.1.1
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 13:33:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD ["sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 13:33:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e042f627aaa2e08ffa25faa469ca18f2198038fc4932851b2f329d5a2e4c250`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 8.1 MB (8062910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c009050f36fc86b4a5d22c783277d16784f21871bde598b74c14dfc2e5a40578`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cda18d16a5ac7ae653316eb406a8a6a258ad16485b726d9bcc626bcc0b60559`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 19.6 MB (19565543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f820e1601fb54e7d65885ec40027c02c756b86b091f5a210b9f3d6e1ab49ee`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e8d96fda21401fea2fd33b5d1adcee4967c2c0ff29afaa20fbe12d343d034f`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 21.1 MB (21083733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2815dbb80ca2f121f2d2591da15c360f630ec9087a66c2c5014f401b35caf60`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a175aea1c1bd25acfb07b7036875cf212ee6d5563e794e8e7e169e5f1b735ffe`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022724d8daf099af53850445a26d124bbb4b2cf4e22add7175da0edfc6f92cdb`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c800b7b29c8b8258f0ab46cf3cbb0b648980aa5e3bcac56f20777272dcebda`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 6.7 MB (6732967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afacf05f6cdf9675c65697d62ee25c2303349a0fb2415b5e753d9b609d961df9`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 90.3 KB (90340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cd656fb912a04f70482dac94990296a8ea5505ade0ddcb964fa867e6c5591b`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325b1dd2d33f5ad4c2796cb6a7c62c8c06821322deffd672d858a3419a02ee70`  
		Last Modified: Fri, 23 May 2025 19:07:40 GMT  
		Size: 60.4 MB (60382717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc3dc2c1be1d9a1e1032c48bf32d57ed2fa529d428fb48ee72152a9d5723ad3`  
		Last Modified: Fri, 23 May 2025 19:07:40 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7415b0eadc3d09ef3f24725532a24d831ec5db1f4aa360ab39637e374542aef7`  
		Last Modified: Fri, 23 May 2025 19:07:40 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:b51334f1b6817131cd1704455a7d4299bfc8493c454556770f78f21e3e3d9b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a338ba01c8e16857da57b979e5a035efc4b151bd1268c2418373142d35271aa4`

```dockerfile
```

-	Layers:
	-	`sha256:35b2c68133a2d3b32652c58d17e19ce56f74cee512b7bec66541bb6e0d74d3b2`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v6

```console
$ docker pull docker@sha256:f2f3b37878c2cef486112d6709ed490891dbcbe5cb4e5859814eaf3982c98c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131533723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2581c43c12094bd2d323b5b072712bb81d4d0aed375776192b14e67796d6d497`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_VERSION=28.1.1
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 13:33:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD ["sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 13:33:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabe4b1be1d57ade8a16d24392424cb161acf4950ab94290ffde72d3b5148f78`  
		Last Modified: Fri, 18 Apr 2025 18:17:13 GMT  
		Size: 17.5 MB (17512361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff0ccd74e971a297930c6be175f70d43ed067a0de538727bca466a13ceb643`  
		Last Modified: Wed, 21 May 2025 21:18:17 GMT  
		Size: 19.9 MB (19943295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d83113106710875ce29f2258ab21ebad6c44b2e193b2bc3f5ff4b73a39a980`  
		Last Modified: Fri, 23 May 2025 18:52:23 GMT  
		Size: 19.8 MB (19820971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736e0c62aa126461393325d9483a13fd78d8994237bc3928e7c4537231dc1c80`  
		Last Modified: Fri, 23 May 2025 18:52:22 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2851abd4ce55cacf042cceb3b838ec32deb7c903ef64e8d3fb8c8a5590773c36`  
		Last Modified: Fri, 23 May 2025 18:52:22 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8afa7b4de0e37d32729b746fb3e6cb804aa2abe68d0d87668a76c4de34e001`  
		Last Modified: Fri, 23 May 2025 18:52:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab8704cd41c89b9fe82e8b1d58198a350c3181f9aec97eef87f07d1b9ce131a`  
		Last Modified: Fri, 23 May 2025 19:07:58 GMT  
		Size: 7.0 MB (7036883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b93adb2cb3180aa31c504a81097a2d93a341c1c0d879a599665fa82f0dfe77`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 89.9 KB (89863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6140070484c6461f5ceb2356c7ee0bac0a058fca232206741b091de3c81a35fe`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72db719af6b08d755704df35f14b35d710003a9f3c743b4fb66c310db98fb45`  
		Last Modified: Fri, 23 May 2025 19:07:59 GMT  
		Size: 55.8 MB (55779304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d0b490f215a68203ed977969da4c3967fdcb29d005e4654c4405e859b2afc`  
		Last Modified: Fri, 23 May 2025 19:07:58 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411314b0d81073dbc0e30f1a171383d16dd3b7e4b967fd0525def3b36dde97f0`  
		Last Modified: Fri, 23 May 2025 19:07:58 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:b16f0e71687751189276a8a0985f042f0d934138253e5550c8178ebcd0a5af5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5c3902beffb0a12be2fe1fd65f99ca9ee2881eac0ba4defec5d3be67ab318f`

```dockerfile
```

-	Layers:
	-	`sha256:e428e33537b38b5161d6a05ea6d88988ebe30ab9e63066cc425fa8a456e9b866`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v7

```console
$ docker pull docker@sha256:c1427d3bf59bd4df265e1178c1081b2ca964b38d597773ddb984f14aab170e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129868078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee53e5e7f4e42c9074544280ae6b31e67dfc506266c49369e28b49127fcefdf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_VERSION=28.1.1
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 13:33:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD ["sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 13:33:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033d7ad6a0a73e30d2ed9b7f50d58df9ccd5cf1c841686a61954232996470ef3`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 17.5 MB (17499382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d295095655bde8c64c1e9c038682853e8245f33967c39505fe29091b73ed589`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 19.9 MB (19927224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df770c71c3a921038274a8ea122d85b3600f6506116091c714f69a77970e6f5`  
		Last Modified: Fri, 23 May 2025 18:52:39 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d649ed28060282c28387144d88dd7f78c15831547e245dbac20a2d60ed92623`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3e438f4531085ce8b48caeffab55675975435e246a3683cf7541008384855`  
		Last Modified: Fri, 23 May 2025 18:52:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a605a46249419dd243f55315b4b6acbfa0c8a21f2e2a4bffa6dbfb75a52b26a`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fda75f23643c26026a7e77ac15339c2fec8435d11a879692dc5480328d9a7d`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 6.4 MB (6366096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6a9ff2ecd023da05d42caba7630d54dc6ea17beb4947a58adbaa70de427787`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 86.3 KB (86349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637d051ba9ea3a89cdc4ee6a5ee3f4a2b78e4f97da6100c5a1f530c16445f98e`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1444096bf5bc77244cc89ca937766603ddc2f20b05acce36c1ff07dc44588d11`  
		Last Modified: Fri, 23 May 2025 19:07:59 GMT  
		Size: 55.8 MB (55779320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd8ba43d24002dd777b812766ec2e1c91bbd201c39572d2533622f54a3fbcba`  
		Last Modified: Fri, 23 May 2025 19:07:58 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9db48766ab94cb7813fa258f77c586ae657a0d750fb515fb65b1874ba1ea5e2`  
		Last Modified: Fri, 23 May 2025 19:07:58 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:8b958b41421a9549c215aa2466febf420b2409e4d8f7a7677f0e77a028898aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa6a8e1d2ea8282de30b1eabd6e72a7d6866c03f53a630f7e19aa685aa19a19`

```dockerfile
```

-	Layers:
	-	`sha256:ffabf6631a8a680ea4ea5826cc4b6eedd4055a8eac48eac1647b86247ca7365e`  
		Last Modified: Fri, 23 May 2025 19:07:56 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:20c1597efb7bd7d7ae7f9e71fa4374f2a1ef3d18635628aa3b95b63fa2fd870e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132177846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f79bbb1bc448955bb1a77ce9ee12a31d7652f533fc91a50c4769ecc2a8f2d0f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_VERSION=28.1.1
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 13:33:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD ["sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 13:33:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec789962e1d09e3595a12eaba70cf6990b21c47621b527e53891f6631f5b19e`  
		Last Modified: Fri, 23 May 2025 18:52:16 GMT  
		Size: 8.1 MB (8077209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bc2d8b228f644ba279e0d51a7161afb4d0fb930d7fca177583095f71ec1f8b`  
		Last Modified: Fri, 23 May 2025 18:52:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a18b4be218242299d5fd9ea2951f9d24db47157d435e3f96805cfbed31ff40`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 18.5 MB (18485713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9277d456ea9edabe19a8f86e89ecfd2d8a10433cd65079b3deae2d2726b4f8`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 19.5 MB (19469841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d25353f65ebab93094b75127ae91d6e8b7526084d11aeb2d6cc6b14aaeb800a`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 19.3 MB (19324588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c8e76e13bed3cee591f54ec598a8dbf87f5a30ef009904d398ee1b97cbd31d`  
		Last Modified: Fri, 23 May 2025 18:52:35 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e06d38657934337f45ba90a17197d8fdd0f6dc7fc4e51a9453e25a55e81d53`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a605a46249419dd243f55315b4b6acbfa0c8a21f2e2a4bffa6dbfb75a52b26a`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7c10540f66ae08ba872ef0b8b2ac5b0d8e2f734d49953d9866543cfd19298f`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 7.0 MB (6978936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c23c50e160dba55151940d23aa190841f10bca12a34b34b1a3129ae4f57a89`  
		Last Modified: Fri, 23 May 2025 19:07:41 GMT  
		Size: 99.4 KB (99398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c3b2576819b89a08031e832bba46a29d5dd1ff310dfbd2b5b94a2989bb3d7e`  
		Last Modified: Fri, 23 May 2025 19:07:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a103a2dd279a848eae5a76703c3da8acac2fbd215dcf30a0a85aa3d028c8b3a0`  
		Last Modified: Fri, 23 May 2025 19:07:43 GMT  
		Size: 55.7 MB (55740981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d126e1c1bb1a79f07755473da059e7462ddf04a567a1f23e35f00c3061c9bed`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371388cdf0d156bde8edbfdf54112cd6070593421a693de91426ab1d006f3ec3`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:1a877ccee155396813b360f849a1a51d31b80a62c3def3fcb5ccbe2ae6c8f461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e620bfe003fc0f5d7f64e06c4dc7669d4e17a38502f2a14d80940cdc0ddb181`

```dockerfile
```

-	Layers:
	-	`sha256:9d10dbb65fe125c2be69cb77c1594daa333e359dc48512883efe6f681df2ea9f`  
		Last Modified: Fri, 23 May 2025 19:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-cli`

```console
$ docker pull docker@sha256:f4ca5cab1815946d04c814d564828af0869c2fc23a7ef014d07cab1694d93cae
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
$ docker pull docker@sha256:ef96449be45166d2f237b0fe6f235084e914f75a039ec4a37e7c6c6f63b88e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73646770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd839d54fb4c32180f69dd76455c0b72cc91054164466f1c47ab1ed52681ee1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 17:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 23 May 2025 17:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 May 2025 17:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 May 2025 17:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 May 2025 17:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e042f627aaa2e08ffa25faa469ca18f2198038fc4932851b2f329d5a2e4c250`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 8.1 MB (8062910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c009050f36fc86b4a5d22c783277d16784f21871bde598b74c14dfc2e5a40578`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cda18d16a5ac7ae653316eb406a8a6a258ad16485b726d9bcc626bcc0b60559`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 19.6 MB (19565543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f820e1601fb54e7d65885ec40027c02c756b86b091f5a210b9f3d6e1ab49ee`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e8d96fda21401fea2fd33b5d1adcee4967c2c0ff29afaa20fbe12d343d034f`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 21.1 MB (21083733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2815dbb80ca2f121f2d2591da15c360f630ec9087a66c2c5014f401b35caf60`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a175aea1c1bd25acfb07b7036875cf212ee6d5563e794e8e7e169e5f1b735ffe`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022724d8daf099af53850445a26d124bbb4b2cf4e22add7175da0edfc6f92cdb`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:b42934e9c1c55832657e8f18651ce91e766a78bc2d5bf55d7b583443a555d19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04997d3d06a48a051eccc8793e756af4b6516c53b2034b28f3b5efcca260b567`

```dockerfile
```

-	Layers:
	-	`sha256:2d11b2764e3f096279c03dfb45cfca610d1a9b01aea7617841d001f4ceb2221d`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:71690141341de00829f77d87a0e3e0085e76224f26c1835f9c90276ed401e735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68621664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5ae826dac0c36de2007a69924f9c3137f25d95a1dd7f4d17273bd286850c13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 17:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 23 May 2025 17:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 May 2025 17:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 May 2025 17:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 May 2025 17:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabe4b1be1d57ade8a16d24392424cb161acf4950ab94290ffde72d3b5148f78`  
		Last Modified: Fri, 18 Apr 2025 18:17:13 GMT  
		Size: 17.5 MB (17512361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff0ccd74e971a297930c6be175f70d43ed067a0de538727bca466a13ceb643`  
		Last Modified: Wed, 21 May 2025 21:18:17 GMT  
		Size: 19.9 MB (19943295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d83113106710875ce29f2258ab21ebad6c44b2e193b2bc3f5ff4b73a39a980`  
		Last Modified: Fri, 23 May 2025 18:52:23 GMT  
		Size: 19.8 MB (19820971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736e0c62aa126461393325d9483a13fd78d8994237bc3928e7c4537231dc1c80`  
		Last Modified: Fri, 23 May 2025 18:52:22 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2851abd4ce55cacf042cceb3b838ec32deb7c903ef64e8d3fb8c8a5590773c36`  
		Last Modified: Fri, 23 May 2025 18:52:22 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8afa7b4de0e37d32729b746fb3e6cb804aa2abe68d0d87668a76c4de34e001`  
		Last Modified: Fri, 23 May 2025 18:52:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1921d85e2ba5a848452190188887c8ec2d59dd19798ec7aeda3d09a0ba577614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0eedb15203606d772f5ef79412bbfa6345c8444fdfb3ae6c34342197768923f`

```dockerfile
```

-	Layers:
	-	`sha256:760515fc2a85ae306b4c22ef9454855c7b84f9931faeb4c9fe93ed661e8b4dc1`  
		Last Modified: Fri, 23 May 2025 18:52:22 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:ef16fbe9a8a8e08552403272e80a543197744c65d4635764c169548f7392a84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67630319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae531ec09bdea7e854e0f1c9abd50397be505fc93cf845339a015b00b74e842`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 17:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 23 May 2025 17:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 May 2025 17:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 May 2025 17:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 May 2025 17:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033d7ad6a0a73e30d2ed9b7f50d58df9ccd5cf1c841686a61954232996470ef3`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 17.5 MB (17499382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d295095655bde8c64c1e9c038682853e8245f33967c39505fe29091b73ed589`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 19.9 MB (19927224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df770c71c3a921038274a8ea122d85b3600f6506116091c714f69a77970e6f5`  
		Last Modified: Fri, 23 May 2025 18:52:39 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d649ed28060282c28387144d88dd7f78c15831547e245dbac20a2d60ed92623`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3e438f4531085ce8b48caeffab55675975435e246a3683cf7541008384855`  
		Last Modified: Fri, 23 May 2025 18:52:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a605a46249419dd243f55315b4b6acbfa0c8a21f2e2a4bffa6dbfb75a52b26a`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:7e5fdbeae2977709661498c009d68f2087b58723481749ab7917157b12b5df6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30689c8d81b6f39ba60aaa4133a01b7d93e6911828db0eea17129b56ffef98ea`

```dockerfile
```

-	Layers:
	-	`sha256:ec6bb9106471c8ce8bcb46071183d806a686a654a63b30c4d7f2d9f7c4ed70d9`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:661b8d3411c90eb2310913294ae3625858a022b28191ef59e43024857062d974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69352533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a3614a069b2244c7e6ae46c71701f4dfbd5495f3d0f7b71d1dffc6bd713983`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 17:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 23 May 2025 17:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 May 2025 17:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 May 2025 17:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 May 2025 17:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec789962e1d09e3595a12eaba70cf6990b21c47621b527e53891f6631f5b19e`  
		Last Modified: Fri, 23 May 2025 18:52:16 GMT  
		Size: 8.1 MB (8077209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bc2d8b228f644ba279e0d51a7161afb4d0fb930d7fca177583095f71ec1f8b`  
		Last Modified: Fri, 23 May 2025 18:52:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a18b4be218242299d5fd9ea2951f9d24db47157d435e3f96805cfbed31ff40`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 18.5 MB (18485713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9277d456ea9edabe19a8f86e89ecfd2d8a10433cd65079b3deae2d2726b4f8`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 19.5 MB (19469841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d25353f65ebab93094b75127ae91d6e8b7526084d11aeb2d6cc6b14aaeb800a`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 19.3 MB (19324588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c8e76e13bed3cee591f54ec598a8dbf87f5a30ef009904d398ee1b97cbd31d`  
		Last Modified: Fri, 23 May 2025 18:52:35 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e06d38657934337f45ba90a17197d8fdd0f6dc7fc4e51a9453e25a55e81d53`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a605a46249419dd243f55315b4b6acbfa0c8a21f2e2a4bffa6dbfb75a52b26a`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e6372cea82fb415ff4c565b872ad243a834f6f7acb0204d12396e7ac0ba9f41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454f22d3d8cb65d73a8cc834bb3557bd3ea7b6bc20e2cae6725d96f9aa92833c`

```dockerfile
```

-	Layers:
	-	`sha256:f49c4b7d923f8ff1e911342fb6e30089ec451f35278623fdde7a786c078ae7f6`  
		Last Modified: Fri, 23 May 2025 18:52:35 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind`

```console
$ docker pull docker@sha256:eceba5b0fc2fcf83a74c298391c2ed9e1adbdaf04ee173611bd6282ec973e7ba
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
$ docker pull docker@sha256:8c45ce8d05a9f86533788783b53b8ffeb3879b4986821374a47277a3d042712d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140858792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da0bd7ecf78eacd7de485edf3565b12c1f71facbeceb4f9b8bfc60805d7b4e9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_VERSION=28.1.1
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 13:33:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD ["sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 13:33:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e042f627aaa2e08ffa25faa469ca18f2198038fc4932851b2f329d5a2e4c250`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 8.1 MB (8062910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c009050f36fc86b4a5d22c783277d16784f21871bde598b74c14dfc2e5a40578`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cda18d16a5ac7ae653316eb406a8a6a258ad16485b726d9bcc626bcc0b60559`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 19.6 MB (19565543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f820e1601fb54e7d65885ec40027c02c756b86b091f5a210b9f3d6e1ab49ee`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e8d96fda21401fea2fd33b5d1adcee4967c2c0ff29afaa20fbe12d343d034f`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 21.1 MB (21083733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2815dbb80ca2f121f2d2591da15c360f630ec9087a66c2c5014f401b35caf60`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a175aea1c1bd25acfb07b7036875cf212ee6d5563e794e8e7e169e5f1b735ffe`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022724d8daf099af53850445a26d124bbb4b2cf4e22add7175da0edfc6f92cdb`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c800b7b29c8b8258f0ab46cf3cbb0b648980aa5e3bcac56f20777272dcebda`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 6.7 MB (6732967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afacf05f6cdf9675c65697d62ee25c2303349a0fb2415b5e753d9b609d961df9`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 90.3 KB (90340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cd656fb912a04f70482dac94990296a8ea5505ade0ddcb964fa867e6c5591b`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325b1dd2d33f5ad4c2796cb6a7c62c8c06821322deffd672d858a3419a02ee70`  
		Last Modified: Fri, 23 May 2025 19:07:40 GMT  
		Size: 60.4 MB (60382717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc3dc2c1be1d9a1e1032c48bf32d57ed2fa529d428fb48ee72152a9d5723ad3`  
		Last Modified: Fri, 23 May 2025 19:07:40 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7415b0eadc3d09ef3f24725532a24d831ec5db1f4aa360ab39637e374542aef7`  
		Last Modified: Fri, 23 May 2025 19:07:40 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b51334f1b6817131cd1704455a7d4299bfc8493c454556770f78f21e3e3d9b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a338ba01c8e16857da57b979e5a035efc4b151bd1268c2418373142d35271aa4`

```dockerfile
```

-	Layers:
	-	`sha256:35b2c68133a2d3b32652c58d17e19ce56f74cee512b7bec66541bb6e0d74d3b2`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:f2f3b37878c2cef486112d6709ed490891dbcbe5cb4e5859814eaf3982c98c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131533723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2581c43c12094bd2d323b5b072712bb81d4d0aed375776192b14e67796d6d497`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_VERSION=28.1.1
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 13:33:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD ["sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 13:33:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabe4b1be1d57ade8a16d24392424cb161acf4950ab94290ffde72d3b5148f78`  
		Last Modified: Fri, 18 Apr 2025 18:17:13 GMT  
		Size: 17.5 MB (17512361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff0ccd74e971a297930c6be175f70d43ed067a0de538727bca466a13ceb643`  
		Last Modified: Wed, 21 May 2025 21:18:17 GMT  
		Size: 19.9 MB (19943295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d83113106710875ce29f2258ab21ebad6c44b2e193b2bc3f5ff4b73a39a980`  
		Last Modified: Fri, 23 May 2025 18:52:23 GMT  
		Size: 19.8 MB (19820971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736e0c62aa126461393325d9483a13fd78d8994237bc3928e7c4537231dc1c80`  
		Last Modified: Fri, 23 May 2025 18:52:22 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2851abd4ce55cacf042cceb3b838ec32deb7c903ef64e8d3fb8c8a5590773c36`  
		Last Modified: Fri, 23 May 2025 18:52:22 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8afa7b4de0e37d32729b746fb3e6cb804aa2abe68d0d87668a76c4de34e001`  
		Last Modified: Fri, 23 May 2025 18:52:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab8704cd41c89b9fe82e8b1d58198a350c3181f9aec97eef87f07d1b9ce131a`  
		Last Modified: Fri, 23 May 2025 19:07:58 GMT  
		Size: 7.0 MB (7036883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b93adb2cb3180aa31c504a81097a2d93a341c1c0d879a599665fa82f0dfe77`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 89.9 KB (89863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6140070484c6461f5ceb2356c7ee0bac0a058fca232206741b091de3c81a35fe`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72db719af6b08d755704df35f14b35d710003a9f3c743b4fb66c310db98fb45`  
		Last Modified: Fri, 23 May 2025 19:07:59 GMT  
		Size: 55.8 MB (55779304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d0b490f215a68203ed977969da4c3967fdcb29d005e4654c4405e859b2afc`  
		Last Modified: Fri, 23 May 2025 19:07:58 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411314b0d81073dbc0e30f1a171383d16dd3b7e4b967fd0525def3b36dde97f0`  
		Last Modified: Fri, 23 May 2025 19:07:58 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b16f0e71687751189276a8a0985f042f0d934138253e5550c8178ebcd0a5af5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5c3902beffb0a12be2fe1fd65f99ca9ee2881eac0ba4defec5d3be67ab318f`

```dockerfile
```

-	Layers:
	-	`sha256:e428e33537b38b5161d6a05ea6d88988ebe30ab9e63066cc425fa8a456e9b866`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:c1427d3bf59bd4df265e1178c1081b2ca964b38d597773ddb984f14aab170e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129868078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee53e5e7f4e42c9074544280ae6b31e67dfc506266c49369e28b49127fcefdf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_VERSION=28.1.1
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 13:33:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD ["sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 13:33:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033d7ad6a0a73e30d2ed9b7f50d58df9ccd5cf1c841686a61954232996470ef3`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 17.5 MB (17499382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d295095655bde8c64c1e9c038682853e8245f33967c39505fe29091b73ed589`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 19.9 MB (19927224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df770c71c3a921038274a8ea122d85b3600f6506116091c714f69a77970e6f5`  
		Last Modified: Fri, 23 May 2025 18:52:39 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d649ed28060282c28387144d88dd7f78c15831547e245dbac20a2d60ed92623`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3e438f4531085ce8b48caeffab55675975435e246a3683cf7541008384855`  
		Last Modified: Fri, 23 May 2025 18:52:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a605a46249419dd243f55315b4b6acbfa0c8a21f2e2a4bffa6dbfb75a52b26a`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fda75f23643c26026a7e77ac15339c2fec8435d11a879692dc5480328d9a7d`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 6.4 MB (6366096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6a9ff2ecd023da05d42caba7630d54dc6ea17beb4947a58adbaa70de427787`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 86.3 KB (86349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637d051ba9ea3a89cdc4ee6a5ee3f4a2b78e4f97da6100c5a1f530c16445f98e`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1444096bf5bc77244cc89ca937766603ddc2f20b05acce36c1ff07dc44588d11`  
		Last Modified: Fri, 23 May 2025 19:07:59 GMT  
		Size: 55.8 MB (55779320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd8ba43d24002dd777b812766ec2e1c91bbd201c39572d2533622f54a3fbcba`  
		Last Modified: Fri, 23 May 2025 19:07:58 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9db48766ab94cb7813fa258f77c586ae657a0d750fb515fb65b1874ba1ea5e2`  
		Last Modified: Fri, 23 May 2025 19:07:58 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8b958b41421a9549c215aa2466febf420b2409e4d8f7a7677f0e77a028898aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa6a8e1d2ea8282de30b1eabd6e72a7d6866c03f53a630f7e19aa685aa19a19`

```dockerfile
```

-	Layers:
	-	`sha256:ffabf6631a8a680ea4ea5826cc4b6eedd4055a8eac48eac1647b86247ca7365e`  
		Last Modified: Fri, 23 May 2025 19:07:56 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:20c1597efb7bd7d7ae7f9e71fa4374f2a1ef3d18635628aa3b95b63fa2fd870e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132177846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f79bbb1bc448955bb1a77ce9ee12a31d7652f533fc91a50c4769ecc2a8f2d0f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_VERSION=28.1.1
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 13:33:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD ["sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 13:33:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec789962e1d09e3595a12eaba70cf6990b21c47621b527e53891f6631f5b19e`  
		Last Modified: Fri, 23 May 2025 18:52:16 GMT  
		Size: 8.1 MB (8077209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bc2d8b228f644ba279e0d51a7161afb4d0fb930d7fca177583095f71ec1f8b`  
		Last Modified: Fri, 23 May 2025 18:52:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a18b4be218242299d5fd9ea2951f9d24db47157d435e3f96805cfbed31ff40`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 18.5 MB (18485713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9277d456ea9edabe19a8f86e89ecfd2d8a10433cd65079b3deae2d2726b4f8`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 19.5 MB (19469841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d25353f65ebab93094b75127ae91d6e8b7526084d11aeb2d6cc6b14aaeb800a`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 19.3 MB (19324588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c8e76e13bed3cee591f54ec598a8dbf87f5a30ef009904d398ee1b97cbd31d`  
		Last Modified: Fri, 23 May 2025 18:52:35 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e06d38657934337f45ba90a17197d8fdd0f6dc7fc4e51a9453e25a55e81d53`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a605a46249419dd243f55315b4b6acbfa0c8a21f2e2a4bffa6dbfb75a52b26a`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7c10540f66ae08ba872ef0b8b2ac5b0d8e2f734d49953d9866543cfd19298f`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 7.0 MB (6978936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c23c50e160dba55151940d23aa190841f10bca12a34b34b1a3129ae4f57a89`  
		Last Modified: Fri, 23 May 2025 19:07:41 GMT  
		Size: 99.4 KB (99398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c3b2576819b89a08031e832bba46a29d5dd1ff310dfbd2b5b94a2989bb3d7e`  
		Last Modified: Fri, 23 May 2025 19:07:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a103a2dd279a848eae5a76703c3da8acac2fbd215dcf30a0a85aa3d028c8b3a0`  
		Last Modified: Fri, 23 May 2025 19:07:43 GMT  
		Size: 55.7 MB (55740981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d126e1c1bb1a79f07755473da059e7462ddf04a567a1f23e35f00c3061c9bed`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371388cdf0d156bde8edbfdf54112cd6070593421a693de91426ab1d006f3ec3`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:1a877ccee155396813b360f849a1a51d31b80a62c3def3fcb5ccbe2ae6c8f461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e620bfe003fc0f5d7f64e06c4dc7669d4e17a38502f2a14d80940cdc0ddb181`

```dockerfile
```

-	Layers:
	-	`sha256:9d10dbb65fe125c2be69cb77c1594daa333e359dc48512883efe6f681df2ea9f`  
		Last Modified: Fri, 23 May 2025 19:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:921cf550ca1fda0b9e6999ffd4a97cc0e248207479c73febbf5bf105108c2fe5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:c9df353135269c77465ec9d0942c2d4e3ed4e97bab5d6e0d19dc2e3b4938250d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159027807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7cc90b2bab867e297a8a21358550fa62669ea52bc47b57c972a8dcd86cf328`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 18 Apr 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 18 Apr 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 18 Apr 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
CMD []
# Fri, 18 Apr 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 18 Apr 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e042f627aaa2e08ffa25faa469ca18f2198038fc4932851b2f329d5a2e4c250`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 8.1 MB (8062910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c009050f36fc86b4a5d22c783277d16784f21871bde598b74c14dfc2e5a40578`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cda18d16a5ac7ae653316eb406a8a6a258ad16485b726d9bcc626bcc0b60559`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 19.6 MB (19565543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f820e1601fb54e7d65885ec40027c02c756b86b091f5a210b9f3d6e1ab49ee`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e8d96fda21401fea2fd33b5d1adcee4967c2c0ff29afaa20fbe12d343d034f`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 21.1 MB (21083733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2815dbb80ca2f121f2d2591da15c360f630ec9087a66c2c5014f401b35caf60`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a175aea1c1bd25acfb07b7036875cf212ee6d5563e794e8e7e169e5f1b735ffe`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022724d8daf099af53850445a26d124bbb4b2cf4e22add7175da0edfc6f92cdb`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c800b7b29c8b8258f0ab46cf3cbb0b648980aa5e3bcac56f20777272dcebda`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 6.7 MB (6732967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afacf05f6cdf9675c65697d62ee25c2303349a0fb2415b5e753d9b609d961df9`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 90.3 KB (90340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cd656fb912a04f70482dac94990296a8ea5505ade0ddcb964fa867e6c5591b`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325b1dd2d33f5ad4c2796cb6a7c62c8c06821322deffd672d858a3419a02ee70`  
		Last Modified: Fri, 23 May 2025 19:07:40 GMT  
		Size: 60.4 MB (60382717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc3dc2c1be1d9a1e1032c48bf32d57ed2fa529d428fb48ee72152a9d5723ad3`  
		Last Modified: Fri, 23 May 2025 19:07:40 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7415b0eadc3d09ef3f24725532a24d831ec5db1f4aa360ab39637e374542aef7`  
		Last Modified: Fri, 23 May 2025 19:07:40 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a9c2d523809dce76b86a91c0ed95368765a257dfc6f590255a94e0aa27e716`  
		Last Modified: Fri, 23 May 2025 19:11:27 GMT  
		Size: 986.6 KB (986580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde36f5279bdb146502d38af2f2a197f114143c056abd5917c9567154f059505`  
		Last Modified: Fri, 23 May 2025 19:11:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998d9b9c40f654bfa47ceb97106b4c7b37780296f4136d2a43250fea81a7e720`  
		Last Modified: Fri, 23 May 2025 19:11:27 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601eb16f8ece416418117cac322505ee85cba687105d54359eecedbd9bfb9165`  
		Last Modified: Fri, 23 May 2025 19:11:28 GMT  
		Size: 17.2 MB (17181095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0204094804864b8a6854849479031c50941f7772452b62117a532a39044f4352`  
		Last Modified: Fri, 23 May 2025 19:11:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9538f4d38c02c7b47e2e293230bdd1c32e563cfae5a50c041430491b0d2e5b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79adc4e8e21eb0b72c471b30caaabc936e72616bb59480f70d26750d1fc2d25e`

```dockerfile
```

-	Layers:
	-	`sha256:63188c451aad3f3952f2afa6339dc67123ed2f7f14b88abb0990f1d0f8e2bca3`  
		Last Modified: Fri, 23 May 2025 19:11:27 GMT  
		Size: 30.5 KB (30451 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0e7d9f4a6504a9186c8050383f64e6e54371898615d5a07fbf4fd41725144579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152469192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3935173f00b14d546f527d8d55b84adef198749b08f17652765681726f546d2e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 18 Apr 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 18 Apr 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 18 Apr 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
CMD []
# Fri, 18 Apr 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 18 Apr 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec789962e1d09e3595a12eaba70cf6990b21c47621b527e53891f6631f5b19e`  
		Last Modified: Fri, 23 May 2025 18:52:16 GMT  
		Size: 8.1 MB (8077209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bc2d8b228f644ba279e0d51a7161afb4d0fb930d7fca177583095f71ec1f8b`  
		Last Modified: Fri, 23 May 2025 18:52:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a18b4be218242299d5fd9ea2951f9d24db47157d435e3f96805cfbed31ff40`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 18.5 MB (18485713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9277d456ea9edabe19a8f86e89ecfd2d8a10433cd65079b3deae2d2726b4f8`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 19.5 MB (19469841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d25353f65ebab93094b75127ae91d6e8b7526084d11aeb2d6cc6b14aaeb800a`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 19.3 MB (19324588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c8e76e13bed3cee591f54ec598a8dbf87f5a30ef009904d398ee1b97cbd31d`  
		Last Modified: Fri, 23 May 2025 18:52:35 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e06d38657934337f45ba90a17197d8fdd0f6dc7fc4e51a9453e25a55e81d53`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a605a46249419dd243f55315b4b6acbfa0c8a21f2e2a4bffa6dbfb75a52b26a`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7c10540f66ae08ba872ef0b8b2ac5b0d8e2f734d49953d9866543cfd19298f`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 7.0 MB (6978936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c23c50e160dba55151940d23aa190841f10bca12a34b34b1a3129ae4f57a89`  
		Last Modified: Fri, 23 May 2025 19:07:41 GMT  
		Size: 99.4 KB (99398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c3b2576819b89a08031e832bba46a29d5dd1ff310dfbd2b5b94a2989bb3d7e`  
		Last Modified: Fri, 23 May 2025 19:07:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a103a2dd279a848eae5a76703c3da8acac2fbd215dcf30a0a85aa3d028c8b3a0`  
		Last Modified: Fri, 23 May 2025 19:07:43 GMT  
		Size: 55.7 MB (55740981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d126e1c1bb1a79f07755473da059e7462ddf04a567a1f23e35f00c3061c9bed`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371388cdf0d156bde8edbfdf54112cd6070593421a693de91426ab1d006f3ec3`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b167f53dbc3c10a0fee54cd2fbc21c63ef560ccfbaf70a5eb637eb6ee9232c`  
		Last Modified: Fri, 23 May 2025 19:11:13 GMT  
		Size: 1.0 MB (1014221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28433ac331737f34dbbe50ca0d68fe786412a83cfae898842b93fee6f83c0629`  
		Last Modified: Fri, 23 May 2025 19:11:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e732c11713043a1eb8eace9f1d8a37ae40d750048f70a7b2ffeda99d6f7f32`  
		Last Modified: Fri, 23 May 2025 19:11:13 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431b43a91dd2d769b9dafcdc38404aa1312f51239bf23b9d7d691cd5591ee3ba`  
		Last Modified: Fri, 23 May 2025 19:11:14 GMT  
		Size: 19.3 MB (19275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8897570bceeb3a64d126c34833b4fb058d296ba8fa13c7a8e253e9d9b83a40a`  
		Last Modified: Fri, 23 May 2025 19:11:14 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:d1438b41e0f227d68b064f2965104ae8e831821e6ec2ec7a1023df4de92f31af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e127ef7c7db9e45d20ddf05ab157ed4d70b5d592716308ef635ec465915d1af`

```dockerfile
```

-	Layers:
	-	`sha256:a201eb3d474956b219bc5733079966db14d7278d36a20ee198b03780dd3fe45a`  
		Last Modified: Fri, 23 May 2025 19:11:13 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:acbfc84216ddfe0f2e1e229303ba08301857beea9b2ec87068a96827251fca45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:2762cf87a5b42c6876093051307646874ff01ad812ca4189df1dcfef154701a9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3495499097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec779341b953e8c9821ae09f43ae763f69658d1dae6a2b71c939bd1219133eca`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Fri, 23 May 2025 18:57:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 18:57:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 23 May 2025 18:57:44 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 18:57:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Fri, 23 May 2025 18:57:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 18:57:55 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 18:57:56 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Fri, 23 May 2025 18:57:57 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Fri, 23 May 2025 18:58:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 18:58:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 18:58:07 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Fri, 23 May 2025 18:58:08 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Fri, 23 May 2025 18:58:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996aa5fabf587504c303e732d25d9c379fa94d7ab3daa6fbd77090c9f92aaf26`  
		Last Modified: Fri, 23 May 2025 18:58:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e6587e4dfb610200936369102507f9840984b1e56ab5cd559376ba420eff8f`  
		Last Modified: Fri, 23 May 2025 18:58:21 GMT  
		Size: 412.0 KB (411954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f48fa8095e030252604fcbd3f05bc0bc59f2deb32f9a5ca7f9084aa2e40afa`  
		Last Modified: Fri, 23 May 2025 18:58:20 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c00ae96d330e5727c33826d8b8682b456ec00c2d21e16aa797782b7577120cd`  
		Last Modified: Fri, 23 May 2025 18:58:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3d7bc86a5f829992033a0fbbb312c5b134f67c0736f9c7eb1c6578c765db0e`  
		Last Modified: Fri, 23 May 2025 18:58:22 GMT  
		Size: 19.9 MB (19943805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fed8661f8fb5636e6a0b0fea08a085e9097c2ac07504992705a0962ee60da23`  
		Last Modified: Fri, 23 May 2025 18:58:19 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e371b396591894a6e2e888f91e5d1dc9ae45c0b5e0959d5b6bf3715d004b06`  
		Last Modified: Fri, 23 May 2025 18:58:20 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe73034f512fdc35671e7762da54cc9505217565e8a97903f63bc0ac50a717e`  
		Last Modified: Fri, 23 May 2025 18:58:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eed631a98bfcd26df581168d3d2143f26a16c25bde327d8445eac17df267d95`  
		Last Modified: Fri, 23 May 2025 18:58:21 GMT  
		Size: 22.3 MB (22306294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25b9975b1dd2b0c4799e56a89cb73a98df44b17ecfa70b1dc73c999f36b7beb`  
		Last Modified: Fri, 23 May 2025 18:58:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b8d85ab9daa30cc6d41bdeb5975df741a8eb806816b3f40514e9bf69eda7ef`  
		Last Modified: Fri, 23 May 2025 18:58:18 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1681b20439ff829956eb8bdb178f353664ca8bafad18a176660464c4d77fb60`  
		Last Modified: Fri, 23 May 2025 18:58:18 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0a46189849ab2315070c0fd52ec3e39bb5ad50106260a5fb8a50cb343fae5`  
		Last Modified: Fri, 23 May 2025 18:58:21 GMT  
		Size: 22.1 MB (22059480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:26f1beea13ebb8b829a07d31e74201b2e9cb37c3bbb79496b1b957d7cd1c8e7c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338164194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1964f795ab4183db46af07466d0aca95ed1a740cea196410ac30507d7cf62d60`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Fri, 23 May 2025 19:00:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 19:00:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 23 May 2025 19:00:45 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 19:00:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Fri, 23 May 2025 19:00:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:00:56 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 19:00:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Fri, 23 May 2025 19:00:58 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Fri, 23 May 2025 19:01:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:01:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 19:01:07 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Fri, 23 May 2025 19:01:07 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Fri, 23 May 2025 19:01:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70a8534276f45966357169a3bb5537ba803f56b95eef6146951b815540b6d1b`  
		Last Modified: Fri, 23 May 2025 19:01:24 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fe74c6747cded88a9e5d2d831ab16a9463a089c02ca63fcb91ba2ed25c3e58`  
		Last Modified: Fri, 23 May 2025 19:01:24 GMT  
		Size: 356.8 KB (356794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16f223670595d48ad5968dddad0fc471e6a5fdbb62f33ddf526676679964c8c`  
		Last Modified: Fri, 23 May 2025 19:01:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23366a0b381a6bece0c0ba6bf588b437d414ca27d5e14228dcb59d0690d11477`  
		Last Modified: Fri, 23 May 2025 19:01:22 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa4693b4884d15fc0948b35fade6c2240a77c5cddd7b435888d8bf0ca12b321`  
		Last Modified: Fri, 23 May 2025 19:01:24 GMT  
		Size: 19.9 MB (19894034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88d68e0628616b1c65f26d440d18220a2e90bfc63d02ad388b5b53dd216b7a8`  
		Last Modified: Fri, 23 May 2025 19:01:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c61e50ac159733fa620b6acbac621b7b1949eb1b1486dedf74a6e42cba2173a`  
		Last Modified: Fri, 23 May 2025 19:01:20 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9969d7457944c740e5887d9aab74a3fbf9170664db7011d4d24ba58d54f2fa6`  
		Last Modified: Fri, 23 May 2025 19:01:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40830942f745e07c7400fb4e533f4164137901ca8678d7a645e4b0e6937fd9ac`  
		Last Modified: Fri, 23 May 2025 19:01:22 GMT  
		Size: 22.3 MB (22262139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db357aae97a3f218941416707f5eac12dc7216078335536fa9b8e3799679e60`  
		Last Modified: Fri, 23 May 2025 19:01:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc782ea48a4c2f08f3d2cb3dbe80864de1c0ae5a951085196b9258512626418`  
		Last Modified: Fri, 23 May 2025 19:01:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f543e62daba700ef0075b7cd61e86c1fdfb807e054c12d8806db6abebe781933`  
		Last Modified: Fri, 23 May 2025 19:01:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245d5a64afd293741ccb48079ea1449f570572d7838ab4bc03bb4cac87e2c1fb`  
		Last Modified: Fri, 23 May 2025 19:01:22 GMT  
		Size: 22.0 MB (22011529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:d8c9d0051e906b65e6b274145bb1a6bf42c01be2b584e015b2450061a831fb7a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248271030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bc6320aabd791b70a61076d88e78589d31d99b579e296e6d9ed671db172f92`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Fri, 23 May 2025 19:01:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 19:01:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 23 May 2025 19:01:51 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 19:01:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Fri, 23 May 2025 19:02:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:02:05 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 19:02:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Fri, 23 May 2025 19:02:06 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Fri, 23 May 2025 19:02:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:02:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 19:02:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Fri, 23 May 2025 19:02:17 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Fri, 23 May 2025 19:02:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bedba5d8bb10709897be0ca11c0fd7aa652325aa9e1ae6cb99499ffb5348423`  
		Last Modified: Fri, 23 May 2025 19:02:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1eda583ca07b2852595a7dfa1f3ffae9eef5e9e4299901df7656452d88015f`  
		Last Modified: Fri, 23 May 2025 19:02:32 GMT  
		Size: 364.7 KB (364665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72420287a02085c94def4c22f2ca2f8b3360457c2df6304a88c9286147d4ddc`  
		Last Modified: Fri, 23 May 2025 19:02:31 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaa2052518fa53328cd0f816e795f6c556cbb16b8e631ada84d61bc3b7e2f0e`  
		Last Modified: Fri, 23 May 2025 19:02:30 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886ee17b8998b7b6c685ec11fc8880863992fdfb32bbbeb7228b4c2ded3dd72b`  
		Last Modified: Fri, 23 May 2025 19:02:32 GMT  
		Size: 19.9 MB (19901768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1b2fe179779a92d665c0ea748ce755d333ba2072b76552a3bb6705554b8763`  
		Last Modified: Fri, 23 May 2025 19:02:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85068da4803dc6274a2db2661b92f564624bdf460cba85c56c400e054648ee14`  
		Last Modified: Fri, 23 May 2025 19:02:29 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d8c76e0c60a668e8f2ed3d2aa9b644e0d25faee78c68cc796ba836d041cc62`  
		Last Modified: Fri, 23 May 2025 19:02:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4321b3be2b8f9845f01f6a0503043622534fada9d1f6e960e4067926089509`  
		Last Modified: Fri, 23 May 2025 19:02:31 GMT  
		Size: 22.3 MB (22266672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47afe0e541f0c501cfc4e2b3fa3d95dd7123ff584e51d0a9e126547eb8009a4b`  
		Last Modified: Fri, 23 May 2025 19:02:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdf962e512c522c9753deba814e6a0b63ebaf74fc3beb95bb5f268c88e2e09e`  
		Last Modified: Fri, 23 May 2025 19:02:29 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93a31e65a4686b2102d0fe84c29161dc421cfe1af37756cc4d6555f1e033c40`  
		Last Modified: Fri, 23 May 2025 19:02:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921c35cd822abe89a11c931d38819a21ff6e6f984acaf3de4b3f3242002e2bbe`  
		Last Modified: Fri, 23 May 2025 19:02:32 GMT  
		Size: 22.0 MB (22008812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-1809`

```console
$ docker pull docker@sha256:c3dda8e1cfe3b7ff0ae0a6031cc8736fc23d0df01a68ba7b26463720270b7d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `docker:28-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:d8c9d0051e906b65e6b274145bb1a6bf42c01be2b584e015b2450061a831fb7a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248271030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bc6320aabd791b70a61076d88e78589d31d99b579e296e6d9ed671db172f92`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Fri, 23 May 2025 19:01:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 19:01:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 23 May 2025 19:01:51 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 19:01:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Fri, 23 May 2025 19:02:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:02:05 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 19:02:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Fri, 23 May 2025 19:02:06 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Fri, 23 May 2025 19:02:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:02:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 19:02:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Fri, 23 May 2025 19:02:17 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Fri, 23 May 2025 19:02:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bedba5d8bb10709897be0ca11c0fd7aa652325aa9e1ae6cb99499ffb5348423`  
		Last Modified: Fri, 23 May 2025 19:02:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1eda583ca07b2852595a7dfa1f3ffae9eef5e9e4299901df7656452d88015f`  
		Last Modified: Fri, 23 May 2025 19:02:32 GMT  
		Size: 364.7 KB (364665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72420287a02085c94def4c22f2ca2f8b3360457c2df6304a88c9286147d4ddc`  
		Last Modified: Fri, 23 May 2025 19:02:31 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaa2052518fa53328cd0f816e795f6c556cbb16b8e631ada84d61bc3b7e2f0e`  
		Last Modified: Fri, 23 May 2025 19:02:30 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886ee17b8998b7b6c685ec11fc8880863992fdfb32bbbeb7228b4c2ded3dd72b`  
		Last Modified: Fri, 23 May 2025 19:02:32 GMT  
		Size: 19.9 MB (19901768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1b2fe179779a92d665c0ea748ce755d333ba2072b76552a3bb6705554b8763`  
		Last Modified: Fri, 23 May 2025 19:02:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85068da4803dc6274a2db2661b92f564624bdf460cba85c56c400e054648ee14`  
		Last Modified: Fri, 23 May 2025 19:02:29 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d8c76e0c60a668e8f2ed3d2aa9b644e0d25faee78c68cc796ba836d041cc62`  
		Last Modified: Fri, 23 May 2025 19:02:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4321b3be2b8f9845f01f6a0503043622534fada9d1f6e960e4067926089509`  
		Last Modified: Fri, 23 May 2025 19:02:31 GMT  
		Size: 22.3 MB (22266672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47afe0e541f0c501cfc4e2b3fa3d95dd7123ff584e51d0a9e126547eb8009a4b`  
		Last Modified: Fri, 23 May 2025 19:02:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdf962e512c522c9753deba814e6a0b63ebaf74fc3beb95bb5f268c88e2e09e`  
		Last Modified: Fri, 23 May 2025 19:02:29 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93a31e65a4686b2102d0fe84c29161dc421cfe1af37756cc4d6555f1e033c40`  
		Last Modified: Fri, 23 May 2025 19:02:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921c35cd822abe89a11c931d38819a21ff6e6f984acaf3de4b3f3242002e2bbe`  
		Last Modified: Fri, 23 May 2025 19:02:32 GMT  
		Size: 22.0 MB (22008812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:4f3494b5abc8262da231195ca96646c79f643363fd211bd6fdfaf1f3b2c22600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:26f1beea13ebb8b829a07d31e74201b2e9cb37c3bbb79496b1b957d7cd1c8e7c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338164194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1964f795ab4183db46af07466d0aca95ed1a740cea196410ac30507d7cf62d60`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Fri, 23 May 2025 19:00:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 19:00:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 23 May 2025 19:00:45 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 19:00:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Fri, 23 May 2025 19:00:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:00:56 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 19:00:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Fri, 23 May 2025 19:00:58 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Fri, 23 May 2025 19:01:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:01:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 19:01:07 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Fri, 23 May 2025 19:01:07 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Fri, 23 May 2025 19:01:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70a8534276f45966357169a3bb5537ba803f56b95eef6146951b815540b6d1b`  
		Last Modified: Fri, 23 May 2025 19:01:24 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fe74c6747cded88a9e5d2d831ab16a9463a089c02ca63fcb91ba2ed25c3e58`  
		Last Modified: Fri, 23 May 2025 19:01:24 GMT  
		Size: 356.8 KB (356794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16f223670595d48ad5968dddad0fc471e6a5fdbb62f33ddf526676679964c8c`  
		Last Modified: Fri, 23 May 2025 19:01:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23366a0b381a6bece0c0ba6bf588b437d414ca27d5e14228dcb59d0690d11477`  
		Last Modified: Fri, 23 May 2025 19:01:22 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa4693b4884d15fc0948b35fade6c2240a77c5cddd7b435888d8bf0ca12b321`  
		Last Modified: Fri, 23 May 2025 19:01:24 GMT  
		Size: 19.9 MB (19894034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88d68e0628616b1c65f26d440d18220a2e90bfc63d02ad388b5b53dd216b7a8`  
		Last Modified: Fri, 23 May 2025 19:01:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c61e50ac159733fa620b6acbac621b7b1949eb1b1486dedf74a6e42cba2173a`  
		Last Modified: Fri, 23 May 2025 19:01:20 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9969d7457944c740e5887d9aab74a3fbf9170664db7011d4d24ba58d54f2fa6`  
		Last Modified: Fri, 23 May 2025 19:01:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40830942f745e07c7400fb4e533f4164137901ca8678d7a645e4b0e6937fd9ac`  
		Last Modified: Fri, 23 May 2025 19:01:22 GMT  
		Size: 22.3 MB (22262139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db357aae97a3f218941416707f5eac12dc7216078335536fa9b8e3799679e60`  
		Last Modified: Fri, 23 May 2025 19:01:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc782ea48a4c2f08f3d2cb3dbe80864de1c0ae5a951085196b9258512626418`  
		Last Modified: Fri, 23 May 2025 19:01:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f543e62daba700ef0075b7cd61e86c1fdfb807e054c12d8806db6abebe781933`  
		Last Modified: Fri, 23 May 2025 19:01:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245d5a64afd293741ccb48079ea1449f570572d7838ab4bc03bb4cac87e2c1fb`  
		Last Modified: Fri, 23 May 2025 19:01:22 GMT  
		Size: 22.0 MB (22011529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:2dfc3072b23698276ed7d3b69df2849d7335638e4c1514b3b9170192f01272bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:2762cf87a5b42c6876093051307646874ff01ad812ca4189df1dcfef154701a9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3495499097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec779341b953e8c9821ae09f43ae763f69658d1dae6a2b71c939bd1219133eca`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Fri, 23 May 2025 18:57:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 18:57:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 23 May 2025 18:57:44 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 18:57:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Fri, 23 May 2025 18:57:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 18:57:55 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 18:57:56 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Fri, 23 May 2025 18:57:57 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Fri, 23 May 2025 18:58:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 18:58:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 18:58:07 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Fri, 23 May 2025 18:58:08 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Fri, 23 May 2025 18:58:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996aa5fabf587504c303e732d25d9c379fa94d7ab3daa6fbd77090c9f92aaf26`  
		Last Modified: Fri, 23 May 2025 18:58:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e6587e4dfb610200936369102507f9840984b1e56ab5cd559376ba420eff8f`  
		Last Modified: Fri, 23 May 2025 18:58:21 GMT  
		Size: 412.0 KB (411954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f48fa8095e030252604fcbd3f05bc0bc59f2deb32f9a5ca7f9084aa2e40afa`  
		Last Modified: Fri, 23 May 2025 18:58:20 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c00ae96d330e5727c33826d8b8682b456ec00c2d21e16aa797782b7577120cd`  
		Last Modified: Fri, 23 May 2025 18:58:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3d7bc86a5f829992033a0fbbb312c5b134f67c0736f9c7eb1c6578c765db0e`  
		Last Modified: Fri, 23 May 2025 18:58:22 GMT  
		Size: 19.9 MB (19943805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fed8661f8fb5636e6a0b0fea08a085e9097c2ac07504992705a0962ee60da23`  
		Last Modified: Fri, 23 May 2025 18:58:19 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e371b396591894a6e2e888f91e5d1dc9ae45c0b5e0959d5b6bf3715d004b06`  
		Last Modified: Fri, 23 May 2025 18:58:20 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe73034f512fdc35671e7762da54cc9505217565e8a97903f63bc0ac50a717e`  
		Last Modified: Fri, 23 May 2025 18:58:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eed631a98bfcd26df581168d3d2143f26a16c25bde327d8445eac17df267d95`  
		Last Modified: Fri, 23 May 2025 18:58:21 GMT  
		Size: 22.3 MB (22306294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25b9975b1dd2b0c4799e56a89cb73a98df44b17ecfa70b1dc73c999f36b7beb`  
		Last Modified: Fri, 23 May 2025 18:58:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b8d85ab9daa30cc6d41bdeb5975df741a8eb806816b3f40514e9bf69eda7ef`  
		Last Modified: Fri, 23 May 2025 18:58:18 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1681b20439ff829956eb8bdb178f353664ca8bafad18a176660464c4d77fb60`  
		Last Modified: Fri, 23 May 2025 18:58:18 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0a46189849ab2315070c0fd52ec3e39bb5ad50106260a5fb8a50cb343fae5`  
		Last Modified: Fri, 23 May 2025 18:58:21 GMT  
		Size: 22.1 MB (22059480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2`

**does not exist** (yet?)

## `docker:28.2-cli`

**does not exist** (yet?)

## `docker:28.2-dind`

**does not exist** (yet?)

## `docker:28.2-dind-rootless`

**does not exist** (yet?)

## `docker:28.2-windowsservercore`

**does not exist** (yet?)

## `docker:28.2-windowsservercore-1809`

**does not exist** (yet?)

## `docker:28.2-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `docker:28.2-windowsservercore-ltsc2025`

**does not exist** (yet?)

## `docker:28.2.1`

**does not exist** (yet?)

## `docker:28.2.1-alpine3.21`

**does not exist** (yet?)

## `docker:28.2.1-cli`

**does not exist** (yet?)

## `docker:28.2.1-cli-alpine3.21`

**does not exist** (yet?)

## `docker:28.2.1-dind`

**does not exist** (yet?)

## `docker:28.2.1-dind-alpine3.21`

**does not exist** (yet?)

## `docker:28.2.1-dind-rootless`

**does not exist** (yet?)

## `docker:28.2.1-windowsservercore`

**does not exist** (yet?)

## `docker:28.2.1-windowsservercore-1809`

**does not exist** (yet?)

## `docker:28.2.1-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `docker:28.2.1-windowsservercore-ltsc2025`

**does not exist** (yet?)

## `docker:cli`

```console
$ docker pull docker@sha256:f4ca5cab1815946d04c814d564828af0869c2fc23a7ef014d07cab1694d93cae
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
$ docker pull docker@sha256:ef96449be45166d2f237b0fe6f235084e914f75a039ec4a37e7c6c6f63b88e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73646770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd839d54fb4c32180f69dd76455c0b72cc91054164466f1c47ab1ed52681ee1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 17:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 23 May 2025 17:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 May 2025 17:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 May 2025 17:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 May 2025 17:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e042f627aaa2e08ffa25faa469ca18f2198038fc4932851b2f329d5a2e4c250`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 8.1 MB (8062910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c009050f36fc86b4a5d22c783277d16784f21871bde598b74c14dfc2e5a40578`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cda18d16a5ac7ae653316eb406a8a6a258ad16485b726d9bcc626bcc0b60559`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 19.6 MB (19565543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f820e1601fb54e7d65885ec40027c02c756b86b091f5a210b9f3d6e1ab49ee`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e8d96fda21401fea2fd33b5d1adcee4967c2c0ff29afaa20fbe12d343d034f`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 21.1 MB (21083733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2815dbb80ca2f121f2d2591da15c360f630ec9087a66c2c5014f401b35caf60`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a175aea1c1bd25acfb07b7036875cf212ee6d5563e794e8e7e169e5f1b735ffe`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022724d8daf099af53850445a26d124bbb4b2cf4e22add7175da0edfc6f92cdb`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:b42934e9c1c55832657e8f18651ce91e766a78bc2d5bf55d7b583443a555d19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04997d3d06a48a051eccc8793e756af4b6516c53b2034b28f3b5efcca260b567`

```dockerfile
```

-	Layers:
	-	`sha256:2d11b2764e3f096279c03dfb45cfca610d1a9b01aea7617841d001f4ceb2221d`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:71690141341de00829f77d87a0e3e0085e76224f26c1835f9c90276ed401e735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68621664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5ae826dac0c36de2007a69924f9c3137f25d95a1dd7f4d17273bd286850c13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 17:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 23 May 2025 17:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 May 2025 17:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 May 2025 17:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 May 2025 17:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabe4b1be1d57ade8a16d24392424cb161acf4950ab94290ffde72d3b5148f78`  
		Last Modified: Fri, 18 Apr 2025 18:17:13 GMT  
		Size: 17.5 MB (17512361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff0ccd74e971a297930c6be175f70d43ed067a0de538727bca466a13ceb643`  
		Last Modified: Wed, 21 May 2025 21:18:17 GMT  
		Size: 19.9 MB (19943295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d83113106710875ce29f2258ab21ebad6c44b2e193b2bc3f5ff4b73a39a980`  
		Last Modified: Fri, 23 May 2025 18:52:23 GMT  
		Size: 19.8 MB (19820971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736e0c62aa126461393325d9483a13fd78d8994237bc3928e7c4537231dc1c80`  
		Last Modified: Fri, 23 May 2025 18:52:22 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2851abd4ce55cacf042cceb3b838ec32deb7c903ef64e8d3fb8c8a5590773c36`  
		Last Modified: Fri, 23 May 2025 18:52:22 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8afa7b4de0e37d32729b746fb3e6cb804aa2abe68d0d87668a76c4de34e001`  
		Last Modified: Fri, 23 May 2025 18:52:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:1921d85e2ba5a848452190188887c8ec2d59dd19798ec7aeda3d09a0ba577614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0eedb15203606d772f5ef79412bbfa6345c8444fdfb3ae6c34342197768923f`

```dockerfile
```

-	Layers:
	-	`sha256:760515fc2a85ae306b4c22ef9454855c7b84f9931faeb4c9fe93ed661e8b4dc1`  
		Last Modified: Fri, 23 May 2025 18:52:22 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:ef16fbe9a8a8e08552403272e80a543197744c65d4635764c169548f7392a84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67630319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae531ec09bdea7e854e0f1c9abd50397be505fc93cf845339a015b00b74e842`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 17:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 23 May 2025 17:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 May 2025 17:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 May 2025 17:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 May 2025 17:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033d7ad6a0a73e30d2ed9b7f50d58df9ccd5cf1c841686a61954232996470ef3`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 17.5 MB (17499382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d295095655bde8c64c1e9c038682853e8245f33967c39505fe29091b73ed589`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 19.9 MB (19927224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df770c71c3a921038274a8ea122d85b3600f6506116091c714f69a77970e6f5`  
		Last Modified: Fri, 23 May 2025 18:52:39 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d649ed28060282c28387144d88dd7f78c15831547e245dbac20a2d60ed92623`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3e438f4531085ce8b48caeffab55675975435e246a3683cf7541008384855`  
		Last Modified: Fri, 23 May 2025 18:52:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a605a46249419dd243f55315b4b6acbfa0c8a21f2e2a4bffa6dbfb75a52b26a`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:7e5fdbeae2977709661498c009d68f2087b58723481749ab7917157b12b5df6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30689c8d81b6f39ba60aaa4133a01b7d93e6911828db0eea17129b56ffef98ea`

```dockerfile
```

-	Layers:
	-	`sha256:ec6bb9106471c8ce8bcb46071183d806a686a654a63b30c4d7f2d9f7c4ed70d9`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:661b8d3411c90eb2310913294ae3625858a022b28191ef59e43024857062d974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69352533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a3614a069b2244c7e6ae46c71701f4dfbd5495f3d0f7b71d1dffc6bd713983`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 17:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 23 May 2025 17:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 17:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 May 2025 17:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 May 2025 17:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 May 2025 17:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 May 2025 17:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 May 2025 17:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec789962e1d09e3595a12eaba70cf6990b21c47621b527e53891f6631f5b19e`  
		Last Modified: Fri, 23 May 2025 18:52:16 GMT  
		Size: 8.1 MB (8077209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bc2d8b228f644ba279e0d51a7161afb4d0fb930d7fca177583095f71ec1f8b`  
		Last Modified: Fri, 23 May 2025 18:52:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a18b4be218242299d5fd9ea2951f9d24db47157d435e3f96805cfbed31ff40`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 18.5 MB (18485713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9277d456ea9edabe19a8f86e89ecfd2d8a10433cd65079b3deae2d2726b4f8`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 19.5 MB (19469841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d25353f65ebab93094b75127ae91d6e8b7526084d11aeb2d6cc6b14aaeb800a`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 19.3 MB (19324588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c8e76e13bed3cee591f54ec598a8dbf87f5a30ef009904d398ee1b97cbd31d`  
		Last Modified: Fri, 23 May 2025 18:52:35 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e06d38657934337f45ba90a17197d8fdd0f6dc7fc4e51a9453e25a55e81d53`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a605a46249419dd243f55315b4b6acbfa0c8a21f2e2a4bffa6dbfb75a52b26a`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:e6372cea82fb415ff4c565b872ad243a834f6f7acb0204d12396e7ac0ba9f41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454f22d3d8cb65d73a8cc834bb3557bd3ea7b6bc20e2cae6725d96f9aa92833c`

```dockerfile
```

-	Layers:
	-	`sha256:f49c4b7d923f8ff1e911342fb6e30089ec451f35278623fdde7a786c078ae7f6`  
		Last Modified: Fri, 23 May 2025 18:52:35 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:eceba5b0fc2fcf83a74c298391c2ed9e1adbdaf04ee173611bd6282ec973e7ba
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
$ docker pull docker@sha256:8c45ce8d05a9f86533788783b53b8ffeb3879b4986821374a47277a3d042712d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140858792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da0bd7ecf78eacd7de485edf3565b12c1f71facbeceb4f9b8bfc60805d7b4e9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_VERSION=28.1.1
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 13:33:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD ["sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 13:33:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e042f627aaa2e08ffa25faa469ca18f2198038fc4932851b2f329d5a2e4c250`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 8.1 MB (8062910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c009050f36fc86b4a5d22c783277d16784f21871bde598b74c14dfc2e5a40578`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cda18d16a5ac7ae653316eb406a8a6a258ad16485b726d9bcc626bcc0b60559`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 19.6 MB (19565543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f820e1601fb54e7d65885ec40027c02c756b86b091f5a210b9f3d6e1ab49ee`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e8d96fda21401fea2fd33b5d1adcee4967c2c0ff29afaa20fbe12d343d034f`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 21.1 MB (21083733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2815dbb80ca2f121f2d2591da15c360f630ec9087a66c2c5014f401b35caf60`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a175aea1c1bd25acfb07b7036875cf212ee6d5563e794e8e7e169e5f1b735ffe`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022724d8daf099af53850445a26d124bbb4b2cf4e22add7175da0edfc6f92cdb`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c800b7b29c8b8258f0ab46cf3cbb0b648980aa5e3bcac56f20777272dcebda`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 6.7 MB (6732967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afacf05f6cdf9675c65697d62ee25c2303349a0fb2415b5e753d9b609d961df9`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 90.3 KB (90340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cd656fb912a04f70482dac94990296a8ea5505ade0ddcb964fa867e6c5591b`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325b1dd2d33f5ad4c2796cb6a7c62c8c06821322deffd672d858a3419a02ee70`  
		Last Modified: Fri, 23 May 2025 19:07:40 GMT  
		Size: 60.4 MB (60382717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc3dc2c1be1d9a1e1032c48bf32d57ed2fa529d428fb48ee72152a9d5723ad3`  
		Last Modified: Fri, 23 May 2025 19:07:40 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7415b0eadc3d09ef3f24725532a24d831ec5db1f4aa360ab39637e374542aef7`  
		Last Modified: Fri, 23 May 2025 19:07:40 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:b51334f1b6817131cd1704455a7d4299bfc8493c454556770f78f21e3e3d9b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a338ba01c8e16857da57b979e5a035efc4b151bd1268c2418373142d35271aa4`

```dockerfile
```

-	Layers:
	-	`sha256:35b2c68133a2d3b32652c58d17e19ce56f74cee512b7bec66541bb6e0d74d3b2`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:f2f3b37878c2cef486112d6709ed490891dbcbe5cb4e5859814eaf3982c98c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131533723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2581c43c12094bd2d323b5b072712bb81d4d0aed375776192b14e67796d6d497`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_VERSION=28.1.1
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 13:33:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD ["sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 13:33:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabe4b1be1d57ade8a16d24392424cb161acf4950ab94290ffde72d3b5148f78`  
		Last Modified: Fri, 18 Apr 2025 18:17:13 GMT  
		Size: 17.5 MB (17512361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff0ccd74e971a297930c6be175f70d43ed067a0de538727bca466a13ceb643`  
		Last Modified: Wed, 21 May 2025 21:18:17 GMT  
		Size: 19.9 MB (19943295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d83113106710875ce29f2258ab21ebad6c44b2e193b2bc3f5ff4b73a39a980`  
		Last Modified: Fri, 23 May 2025 18:52:23 GMT  
		Size: 19.8 MB (19820971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736e0c62aa126461393325d9483a13fd78d8994237bc3928e7c4537231dc1c80`  
		Last Modified: Fri, 23 May 2025 18:52:22 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2851abd4ce55cacf042cceb3b838ec32deb7c903ef64e8d3fb8c8a5590773c36`  
		Last Modified: Fri, 23 May 2025 18:52:22 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8afa7b4de0e37d32729b746fb3e6cb804aa2abe68d0d87668a76c4de34e001`  
		Last Modified: Fri, 23 May 2025 18:52:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab8704cd41c89b9fe82e8b1d58198a350c3181f9aec97eef87f07d1b9ce131a`  
		Last Modified: Fri, 23 May 2025 19:07:58 GMT  
		Size: 7.0 MB (7036883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b93adb2cb3180aa31c504a81097a2d93a341c1c0d879a599665fa82f0dfe77`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 89.9 KB (89863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6140070484c6461f5ceb2356c7ee0bac0a058fca232206741b091de3c81a35fe`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72db719af6b08d755704df35f14b35d710003a9f3c743b4fb66c310db98fb45`  
		Last Modified: Fri, 23 May 2025 19:07:59 GMT  
		Size: 55.8 MB (55779304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d0b490f215a68203ed977969da4c3967fdcb29d005e4654c4405e859b2afc`  
		Last Modified: Fri, 23 May 2025 19:07:58 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411314b0d81073dbc0e30f1a171383d16dd3b7e4b967fd0525def3b36dde97f0`  
		Last Modified: Fri, 23 May 2025 19:07:58 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:b16f0e71687751189276a8a0985f042f0d934138253e5550c8178ebcd0a5af5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5c3902beffb0a12be2fe1fd65f99ca9ee2881eac0ba4defec5d3be67ab318f`

```dockerfile
```

-	Layers:
	-	`sha256:e428e33537b38b5161d6a05ea6d88988ebe30ab9e63066cc425fa8a456e9b866`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:c1427d3bf59bd4df265e1178c1081b2ca964b38d597773ddb984f14aab170e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129868078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee53e5e7f4e42c9074544280ae6b31e67dfc506266c49369e28b49127fcefdf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_VERSION=28.1.1
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 13:33:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD ["sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 13:33:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033d7ad6a0a73e30d2ed9b7f50d58df9ccd5cf1c841686a61954232996470ef3`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 17.5 MB (17499382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d295095655bde8c64c1e9c038682853e8245f33967c39505fe29091b73ed589`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 19.9 MB (19927224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df770c71c3a921038274a8ea122d85b3600f6506116091c714f69a77970e6f5`  
		Last Modified: Fri, 23 May 2025 18:52:39 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d649ed28060282c28387144d88dd7f78c15831547e245dbac20a2d60ed92623`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3e438f4531085ce8b48caeffab55675975435e246a3683cf7541008384855`  
		Last Modified: Fri, 23 May 2025 18:52:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a605a46249419dd243f55315b4b6acbfa0c8a21f2e2a4bffa6dbfb75a52b26a`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fda75f23643c26026a7e77ac15339c2fec8435d11a879692dc5480328d9a7d`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 6.4 MB (6366096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6a9ff2ecd023da05d42caba7630d54dc6ea17beb4947a58adbaa70de427787`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 86.3 KB (86349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637d051ba9ea3a89cdc4ee6a5ee3f4a2b78e4f97da6100c5a1f530c16445f98e`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1444096bf5bc77244cc89ca937766603ddc2f20b05acce36c1ff07dc44588d11`  
		Last Modified: Fri, 23 May 2025 19:07:59 GMT  
		Size: 55.8 MB (55779320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd8ba43d24002dd777b812766ec2e1c91bbd201c39572d2533622f54a3fbcba`  
		Last Modified: Fri, 23 May 2025 19:07:58 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9db48766ab94cb7813fa258f77c586ae657a0d750fb515fb65b1874ba1ea5e2`  
		Last Modified: Fri, 23 May 2025 19:07:58 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:8b958b41421a9549c215aa2466febf420b2409e4d8f7a7677f0e77a028898aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa6a8e1d2ea8282de30b1eabd6e72a7d6866c03f53a630f7e19aa685aa19a19`

```dockerfile
```

-	Layers:
	-	`sha256:ffabf6631a8a680ea4ea5826cc4b6eedd4055a8eac48eac1647b86247ca7365e`  
		Last Modified: Fri, 23 May 2025 19:07:56 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:20c1597efb7bd7d7ae7f9e71fa4374f2a1ef3d18635628aa3b95b63fa2fd870e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132177846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f79bbb1bc448955bb1a77ce9ee12a31d7652f533fc91a50c4769ecc2a8f2d0f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_VERSION=28.1.1
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 13:33:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD ["sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 13:33:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec789962e1d09e3595a12eaba70cf6990b21c47621b527e53891f6631f5b19e`  
		Last Modified: Fri, 23 May 2025 18:52:16 GMT  
		Size: 8.1 MB (8077209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bc2d8b228f644ba279e0d51a7161afb4d0fb930d7fca177583095f71ec1f8b`  
		Last Modified: Fri, 23 May 2025 18:52:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a18b4be218242299d5fd9ea2951f9d24db47157d435e3f96805cfbed31ff40`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 18.5 MB (18485713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9277d456ea9edabe19a8f86e89ecfd2d8a10433cd65079b3deae2d2726b4f8`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 19.5 MB (19469841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d25353f65ebab93094b75127ae91d6e8b7526084d11aeb2d6cc6b14aaeb800a`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 19.3 MB (19324588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c8e76e13bed3cee591f54ec598a8dbf87f5a30ef009904d398ee1b97cbd31d`  
		Last Modified: Fri, 23 May 2025 18:52:35 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e06d38657934337f45ba90a17197d8fdd0f6dc7fc4e51a9453e25a55e81d53`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a605a46249419dd243f55315b4b6acbfa0c8a21f2e2a4bffa6dbfb75a52b26a`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7c10540f66ae08ba872ef0b8b2ac5b0d8e2f734d49953d9866543cfd19298f`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 7.0 MB (6978936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c23c50e160dba55151940d23aa190841f10bca12a34b34b1a3129ae4f57a89`  
		Last Modified: Fri, 23 May 2025 19:07:41 GMT  
		Size: 99.4 KB (99398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c3b2576819b89a08031e832bba46a29d5dd1ff310dfbd2b5b94a2989bb3d7e`  
		Last Modified: Fri, 23 May 2025 19:07:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a103a2dd279a848eae5a76703c3da8acac2fbd215dcf30a0a85aa3d028c8b3a0`  
		Last Modified: Fri, 23 May 2025 19:07:43 GMT  
		Size: 55.7 MB (55740981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d126e1c1bb1a79f07755473da059e7462ddf04a567a1f23e35f00c3061c9bed`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371388cdf0d156bde8edbfdf54112cd6070593421a693de91426ab1d006f3ec3`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:1a877ccee155396813b360f849a1a51d31b80a62c3def3fcb5ccbe2ae6c8f461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e620bfe003fc0f5d7f64e06c4dc7669d4e17a38502f2a14d80940cdc0ddb181`

```dockerfile
```

-	Layers:
	-	`sha256:9d10dbb65fe125c2be69cb77c1594daa333e359dc48512883efe6f681df2ea9f`  
		Last Modified: Fri, 23 May 2025 19:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:921cf550ca1fda0b9e6999ffd4a97cc0e248207479c73febbf5bf105108c2fe5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:c9df353135269c77465ec9d0942c2d4e3ed4e97bab5d6e0d19dc2e3b4938250d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159027807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7cc90b2bab867e297a8a21358550fa62669ea52bc47b57c972a8dcd86cf328`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 18 Apr 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 18 Apr 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 18 Apr 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
CMD []
# Fri, 18 Apr 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 18 Apr 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e042f627aaa2e08ffa25faa469ca18f2198038fc4932851b2f329d5a2e4c250`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 8.1 MB (8062910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c009050f36fc86b4a5d22c783277d16784f21871bde598b74c14dfc2e5a40578`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cda18d16a5ac7ae653316eb406a8a6a258ad16485b726d9bcc626bcc0b60559`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 19.6 MB (19565543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f820e1601fb54e7d65885ec40027c02c756b86b091f5a210b9f3d6e1ab49ee`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e8d96fda21401fea2fd33b5d1adcee4967c2c0ff29afaa20fbe12d343d034f`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 21.1 MB (21083733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2815dbb80ca2f121f2d2591da15c360f630ec9087a66c2c5014f401b35caf60`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a175aea1c1bd25acfb07b7036875cf212ee6d5563e794e8e7e169e5f1b735ffe`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022724d8daf099af53850445a26d124bbb4b2cf4e22add7175da0edfc6f92cdb`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c800b7b29c8b8258f0ab46cf3cbb0b648980aa5e3bcac56f20777272dcebda`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 6.7 MB (6732967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afacf05f6cdf9675c65697d62ee25c2303349a0fb2415b5e753d9b609d961df9`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 90.3 KB (90340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cd656fb912a04f70482dac94990296a8ea5505ade0ddcb964fa867e6c5591b`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325b1dd2d33f5ad4c2796cb6a7c62c8c06821322deffd672d858a3419a02ee70`  
		Last Modified: Fri, 23 May 2025 19:07:40 GMT  
		Size: 60.4 MB (60382717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc3dc2c1be1d9a1e1032c48bf32d57ed2fa529d428fb48ee72152a9d5723ad3`  
		Last Modified: Fri, 23 May 2025 19:07:40 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7415b0eadc3d09ef3f24725532a24d831ec5db1f4aa360ab39637e374542aef7`  
		Last Modified: Fri, 23 May 2025 19:07:40 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a9c2d523809dce76b86a91c0ed95368765a257dfc6f590255a94e0aa27e716`  
		Last Modified: Fri, 23 May 2025 19:11:27 GMT  
		Size: 986.6 KB (986580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde36f5279bdb146502d38af2f2a197f114143c056abd5917c9567154f059505`  
		Last Modified: Fri, 23 May 2025 19:11:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998d9b9c40f654bfa47ceb97106b4c7b37780296f4136d2a43250fea81a7e720`  
		Last Modified: Fri, 23 May 2025 19:11:27 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601eb16f8ece416418117cac322505ee85cba687105d54359eecedbd9bfb9165`  
		Last Modified: Fri, 23 May 2025 19:11:28 GMT  
		Size: 17.2 MB (17181095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0204094804864b8a6854849479031c50941f7772452b62117a532a39044f4352`  
		Last Modified: Fri, 23 May 2025 19:11:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9538f4d38c02c7b47e2e293230bdd1c32e563cfae5a50c041430491b0d2e5b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79adc4e8e21eb0b72c471b30caaabc936e72616bb59480f70d26750d1fc2d25e`

```dockerfile
```

-	Layers:
	-	`sha256:63188c451aad3f3952f2afa6339dc67123ed2f7f14b88abb0990f1d0f8e2bca3`  
		Last Modified: Fri, 23 May 2025 19:11:27 GMT  
		Size: 30.5 KB (30451 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0e7d9f4a6504a9186c8050383f64e6e54371898615d5a07fbf4fd41725144579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152469192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3935173f00b14d546f527d8d55b84adef198749b08f17652765681726f546d2e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 18 Apr 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 18 Apr 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 18 Apr 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
CMD []
# Fri, 18 Apr 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 18 Apr 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec789962e1d09e3595a12eaba70cf6990b21c47621b527e53891f6631f5b19e`  
		Last Modified: Fri, 23 May 2025 18:52:16 GMT  
		Size: 8.1 MB (8077209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bc2d8b228f644ba279e0d51a7161afb4d0fb930d7fca177583095f71ec1f8b`  
		Last Modified: Fri, 23 May 2025 18:52:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a18b4be218242299d5fd9ea2951f9d24db47157d435e3f96805cfbed31ff40`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 18.5 MB (18485713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9277d456ea9edabe19a8f86e89ecfd2d8a10433cd65079b3deae2d2726b4f8`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 19.5 MB (19469841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d25353f65ebab93094b75127ae91d6e8b7526084d11aeb2d6cc6b14aaeb800a`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 19.3 MB (19324588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c8e76e13bed3cee591f54ec598a8dbf87f5a30ef009904d398ee1b97cbd31d`  
		Last Modified: Fri, 23 May 2025 18:52:35 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e06d38657934337f45ba90a17197d8fdd0f6dc7fc4e51a9453e25a55e81d53`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a605a46249419dd243f55315b4b6acbfa0c8a21f2e2a4bffa6dbfb75a52b26a`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7c10540f66ae08ba872ef0b8b2ac5b0d8e2f734d49953d9866543cfd19298f`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 7.0 MB (6978936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c23c50e160dba55151940d23aa190841f10bca12a34b34b1a3129ae4f57a89`  
		Last Modified: Fri, 23 May 2025 19:07:41 GMT  
		Size: 99.4 KB (99398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c3b2576819b89a08031e832bba46a29d5dd1ff310dfbd2b5b94a2989bb3d7e`  
		Last Modified: Fri, 23 May 2025 19:07:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a103a2dd279a848eae5a76703c3da8acac2fbd215dcf30a0a85aa3d028c8b3a0`  
		Last Modified: Fri, 23 May 2025 19:07:43 GMT  
		Size: 55.7 MB (55740981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d126e1c1bb1a79f07755473da059e7462ddf04a567a1f23e35f00c3061c9bed`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371388cdf0d156bde8edbfdf54112cd6070593421a693de91426ab1d006f3ec3`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b167f53dbc3c10a0fee54cd2fbc21c63ef560ccfbaf70a5eb637eb6ee9232c`  
		Last Modified: Fri, 23 May 2025 19:11:13 GMT  
		Size: 1.0 MB (1014221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28433ac331737f34dbbe50ca0d68fe786412a83cfae898842b93fee6f83c0629`  
		Last Modified: Fri, 23 May 2025 19:11:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e732c11713043a1eb8eace9f1d8a37ae40d750048f70a7b2ffeda99d6f7f32`  
		Last Modified: Fri, 23 May 2025 19:11:13 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431b43a91dd2d769b9dafcdc38404aa1312f51239bf23b9d7d691cd5591ee3ba`  
		Last Modified: Fri, 23 May 2025 19:11:14 GMT  
		Size: 19.3 MB (19275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8897570bceeb3a64d126c34833b4fb058d296ba8fa13c7a8e253e9d9b83a40a`  
		Last Modified: Fri, 23 May 2025 19:11:14 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:d1438b41e0f227d68b064f2965104ae8e831821e6ec2ec7a1023df4de92f31af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e127ef7c7db9e45d20ddf05ab157ed4d70b5d592716308ef635ec465915d1af`

```dockerfile
```

-	Layers:
	-	`sha256:a201eb3d474956b219bc5733079966db14d7278d36a20ee198b03780dd3fe45a`  
		Last Modified: Fri, 23 May 2025 19:11:13 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:eceba5b0fc2fcf83a74c298391c2ed9e1adbdaf04ee173611bd6282ec973e7ba
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
$ docker pull docker@sha256:8c45ce8d05a9f86533788783b53b8ffeb3879b4986821374a47277a3d042712d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140858792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da0bd7ecf78eacd7de485edf3565b12c1f71facbeceb4f9b8bfc60805d7b4e9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_VERSION=28.1.1
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 13:33:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD ["sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 13:33:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e042f627aaa2e08ffa25faa469ca18f2198038fc4932851b2f329d5a2e4c250`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 8.1 MB (8062910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c009050f36fc86b4a5d22c783277d16784f21871bde598b74c14dfc2e5a40578`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cda18d16a5ac7ae653316eb406a8a6a258ad16485b726d9bcc626bcc0b60559`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 19.6 MB (19565543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f820e1601fb54e7d65885ec40027c02c756b86b091f5a210b9f3d6e1ab49ee`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e8d96fda21401fea2fd33b5d1adcee4967c2c0ff29afaa20fbe12d343d034f`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 21.1 MB (21083733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2815dbb80ca2f121f2d2591da15c360f630ec9087a66c2c5014f401b35caf60`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a175aea1c1bd25acfb07b7036875cf212ee6d5563e794e8e7e169e5f1b735ffe`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022724d8daf099af53850445a26d124bbb4b2cf4e22add7175da0edfc6f92cdb`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c800b7b29c8b8258f0ab46cf3cbb0b648980aa5e3bcac56f20777272dcebda`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 6.7 MB (6732967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afacf05f6cdf9675c65697d62ee25c2303349a0fb2415b5e753d9b609d961df9`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 90.3 KB (90340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cd656fb912a04f70482dac94990296a8ea5505ade0ddcb964fa867e6c5591b`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325b1dd2d33f5ad4c2796cb6a7c62c8c06821322deffd672d858a3419a02ee70`  
		Last Modified: Fri, 23 May 2025 19:07:40 GMT  
		Size: 60.4 MB (60382717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc3dc2c1be1d9a1e1032c48bf32d57ed2fa529d428fb48ee72152a9d5723ad3`  
		Last Modified: Fri, 23 May 2025 19:07:40 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7415b0eadc3d09ef3f24725532a24d831ec5db1f4aa360ab39637e374542aef7`  
		Last Modified: Fri, 23 May 2025 19:07:40 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:b51334f1b6817131cd1704455a7d4299bfc8493c454556770f78f21e3e3d9b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a338ba01c8e16857da57b979e5a035efc4b151bd1268c2418373142d35271aa4`

```dockerfile
```

-	Layers:
	-	`sha256:35b2c68133a2d3b32652c58d17e19ce56f74cee512b7bec66541bb6e0d74d3b2`  
		Last Modified: Fri, 23 May 2025 19:07:39 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:f2f3b37878c2cef486112d6709ed490891dbcbe5cb4e5859814eaf3982c98c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131533723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2581c43c12094bd2d323b5b072712bb81d4d0aed375776192b14e67796d6d497`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_VERSION=28.1.1
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 13:33:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD ["sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 13:33:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabe4b1be1d57ade8a16d24392424cb161acf4950ab94290ffde72d3b5148f78`  
		Last Modified: Fri, 18 Apr 2025 18:17:13 GMT  
		Size: 17.5 MB (17512361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ff0ccd74e971a297930c6be175f70d43ed067a0de538727bca466a13ceb643`  
		Last Modified: Wed, 21 May 2025 21:18:17 GMT  
		Size: 19.9 MB (19943295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d83113106710875ce29f2258ab21ebad6c44b2e193b2bc3f5ff4b73a39a980`  
		Last Modified: Fri, 23 May 2025 18:52:23 GMT  
		Size: 19.8 MB (19820971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736e0c62aa126461393325d9483a13fd78d8994237bc3928e7c4537231dc1c80`  
		Last Modified: Fri, 23 May 2025 18:52:22 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2851abd4ce55cacf042cceb3b838ec32deb7c903ef64e8d3fb8c8a5590773c36`  
		Last Modified: Fri, 23 May 2025 18:52:22 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8afa7b4de0e37d32729b746fb3e6cb804aa2abe68d0d87668a76c4de34e001`  
		Last Modified: Fri, 23 May 2025 18:52:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab8704cd41c89b9fe82e8b1d58198a350c3181f9aec97eef87f07d1b9ce131a`  
		Last Modified: Fri, 23 May 2025 19:07:58 GMT  
		Size: 7.0 MB (7036883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b93adb2cb3180aa31c504a81097a2d93a341c1c0d879a599665fa82f0dfe77`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 89.9 KB (89863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6140070484c6461f5ceb2356c7ee0bac0a058fca232206741b091de3c81a35fe`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72db719af6b08d755704df35f14b35d710003a9f3c743b4fb66c310db98fb45`  
		Last Modified: Fri, 23 May 2025 19:07:59 GMT  
		Size: 55.8 MB (55779304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d0b490f215a68203ed977969da4c3967fdcb29d005e4654c4405e859b2afc`  
		Last Modified: Fri, 23 May 2025 19:07:58 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411314b0d81073dbc0e30f1a171383d16dd3b7e4b967fd0525def3b36dde97f0`  
		Last Modified: Fri, 23 May 2025 19:07:58 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:b16f0e71687751189276a8a0985f042f0d934138253e5550c8178ebcd0a5af5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5c3902beffb0a12be2fe1fd65f99ca9ee2881eac0ba4defec5d3be67ab318f`

```dockerfile
```

-	Layers:
	-	`sha256:e428e33537b38b5161d6a05ea6d88988ebe30ab9e63066cc425fa8a456e9b866`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:c1427d3bf59bd4df265e1178c1081b2ca964b38d597773ddb984f14aab170e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129868078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee53e5e7f4e42c9074544280ae6b31e67dfc506266c49369e28b49127fcefdf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_VERSION=28.1.1
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 13:33:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD ["sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 13:33:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b7d1b82cd6cfed8f273cf6e53fdf614a1a8529e47f3d82e891794f879a1dd`  
		Last Modified: Fri, 23 May 2025 18:52:15 GMT  
		Size: 7.3 MB (7301797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec81fbe1b5a6366ad8d5c217d58f4cec781304db7eeb3128192d0391d9f162b0`  
		Last Modified: Fri, 23 May 2025 18:52:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033d7ad6a0a73e30d2ed9b7f50d58df9ccd5cf1c841686a61954232996470ef3`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 17.5 MB (17499382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d295095655bde8c64c1e9c038682853e8245f33967c39505fe29091b73ed589`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 19.9 MB (19927224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df770c71c3a921038274a8ea122d85b3600f6506116091c714f69a77970e6f5`  
		Last Modified: Fri, 23 May 2025 18:52:39 GMT  
		Size: 19.8 MB (19801640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d649ed28060282c28387144d88dd7f78c15831547e245dbac20a2d60ed92623`  
		Last Modified: Fri, 23 May 2025 18:52:38 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3e438f4531085ce8b48caeffab55675975435e246a3683cf7541008384855`  
		Last Modified: Fri, 23 May 2025 18:52:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a605a46249419dd243f55315b4b6acbfa0c8a21f2e2a4bffa6dbfb75a52b26a`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fda75f23643c26026a7e77ac15339c2fec8435d11a879692dc5480328d9a7d`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 6.4 MB (6366096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6a9ff2ecd023da05d42caba7630d54dc6ea17beb4947a58adbaa70de427787`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 86.3 KB (86349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637d051ba9ea3a89cdc4ee6a5ee3f4a2b78e4f97da6100c5a1f530c16445f98e`  
		Last Modified: Fri, 23 May 2025 19:07:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1444096bf5bc77244cc89ca937766603ddc2f20b05acce36c1ff07dc44588d11`  
		Last Modified: Fri, 23 May 2025 19:07:59 GMT  
		Size: 55.8 MB (55779320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd8ba43d24002dd777b812766ec2e1c91bbd201c39572d2533622f54a3fbcba`  
		Last Modified: Fri, 23 May 2025 19:07:58 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9db48766ab94cb7813fa258f77c586ae657a0d750fb515fb65b1874ba1ea5e2`  
		Last Modified: Fri, 23 May 2025 19:07:58 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:8b958b41421a9549c215aa2466febf420b2409e4d8f7a7677f0e77a028898aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa6a8e1d2ea8282de30b1eabd6e72a7d6866c03f53a630f7e19aa685aa19a19`

```dockerfile
```

-	Layers:
	-	`sha256:ffabf6631a8a680ea4ea5826cc4b6eedd4055a8eac48eac1647b86247ca7365e`  
		Last Modified: Fri, 23 May 2025 19:07:56 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:20c1597efb7bd7d7ae7f9e71fa4374f2a1ef3d18635628aa3b95b63fa2fd870e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132177846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f79bbb1bc448955bb1a77ce9ee12a31d7652f533fc91a50c4769ecc2a8f2d0f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_VERSION=28.1.1
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64'; 			sha256='9040bd35b2cc0783ce6c5de491de7e52e24d4137dbfc5de8a524f718fc23556c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv6'; 			sha256='8260c11228337291dd2adcc1ee957756581047c5f40ad5ff6917660e8ebe7e61'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-armv7'; 			sha256='9e9d20ebc4a094ee7788fbb5bddf70b0b319a55eee134db195d1e47f078ae0dc'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-aarch64'; 			sha256='d1148609319706a57b755ff0f61d604a63a8cf57adb24c17535baa766ff14b4f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-ppc64le'; 			sha256='14b5db45d45808ece42066e4c978a6dddeb0c7ceffd656abfcb8182515fb9c7c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-riscv64'; 			sha256='17b86e88985f7ac6f282ea36e585d15a586584bc4f853466f92a9aed031772ed'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-s390x'; 			sha256='65fe31a89326fb6de9f0e0c93c9abb0e88e407febc16b3551b92507e1ffbc965'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 13:33:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD ["sh"]
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 13:33:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 13:33:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 13:33:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 13:33:06 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 13:33:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 13:33:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 13:33:06 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec789962e1d09e3595a12eaba70cf6990b21c47621b527e53891f6631f5b19e`  
		Last Modified: Fri, 23 May 2025 18:52:16 GMT  
		Size: 8.1 MB (8077209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bc2d8b228f644ba279e0d51a7161afb4d0fb930d7fca177583095f71ec1f8b`  
		Last Modified: Fri, 23 May 2025 18:52:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a18b4be218242299d5fd9ea2951f9d24db47157d435e3f96805cfbed31ff40`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 18.5 MB (18485713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9277d456ea9edabe19a8f86e89ecfd2d8a10433cd65079b3deae2d2726b4f8`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 19.5 MB (19469841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d25353f65ebab93094b75127ae91d6e8b7526084d11aeb2d6cc6b14aaeb800a`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 19.3 MB (19324588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c8e76e13bed3cee591f54ec598a8dbf87f5a30ef009904d398ee1b97cbd31d`  
		Last Modified: Fri, 23 May 2025 18:52:35 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e06d38657934337f45ba90a17197d8fdd0f6dc7fc4e51a9453e25a55e81d53`  
		Last Modified: Fri, 23 May 2025 18:52:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a605a46249419dd243f55315b4b6acbfa0c8a21f2e2a4bffa6dbfb75a52b26a`  
		Last Modified: Fri, 23 May 2025 18:52:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7c10540f66ae08ba872ef0b8b2ac5b0d8e2f734d49953d9866543cfd19298f`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 7.0 MB (6978936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c23c50e160dba55151940d23aa190841f10bca12a34b34b1a3129ae4f57a89`  
		Last Modified: Fri, 23 May 2025 19:07:41 GMT  
		Size: 99.4 KB (99398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c3b2576819b89a08031e832bba46a29d5dd1ff310dfbd2b5b94a2989bb3d7e`  
		Last Modified: Fri, 23 May 2025 19:07:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a103a2dd279a848eae5a76703c3da8acac2fbd215dcf30a0a85aa3d028c8b3a0`  
		Last Modified: Fri, 23 May 2025 19:07:43 GMT  
		Size: 55.7 MB (55740981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d126e1c1bb1a79f07755473da059e7462ddf04a567a1f23e35f00c3061c9bed`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371388cdf0d156bde8edbfdf54112cd6070593421a693de91426ab1d006f3ec3`  
		Last Modified: Fri, 23 May 2025 19:07:42 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:1a877ccee155396813b360f849a1a51d31b80a62c3def3fcb5ccbe2ae6c8f461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e620bfe003fc0f5d7f64e06c4dc7669d4e17a38502f2a14d80940cdc0ddb181`

```dockerfile
```

-	Layers:
	-	`sha256:9d10dbb65fe125c2be69cb77c1594daa333e359dc48512883efe6f681df2ea9f`  
		Last Modified: Fri, 23 May 2025 19:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:acbfc84216ddfe0f2e1e229303ba08301857beea9b2ec87068a96827251fca45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `docker:windowsservercore` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:2762cf87a5b42c6876093051307646874ff01ad812ca4189df1dcfef154701a9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3495499097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec779341b953e8c9821ae09f43ae763f69658d1dae6a2b71c939bd1219133eca`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Fri, 23 May 2025 18:57:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 18:57:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 23 May 2025 18:57:44 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 18:57:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Fri, 23 May 2025 18:57:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 18:57:55 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 18:57:56 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Fri, 23 May 2025 18:57:57 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Fri, 23 May 2025 18:58:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 18:58:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 18:58:07 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Fri, 23 May 2025 18:58:08 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Fri, 23 May 2025 18:58:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996aa5fabf587504c303e732d25d9c379fa94d7ab3daa6fbd77090c9f92aaf26`  
		Last Modified: Fri, 23 May 2025 18:58:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e6587e4dfb610200936369102507f9840984b1e56ab5cd559376ba420eff8f`  
		Last Modified: Fri, 23 May 2025 18:58:21 GMT  
		Size: 412.0 KB (411954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f48fa8095e030252604fcbd3f05bc0bc59f2deb32f9a5ca7f9084aa2e40afa`  
		Last Modified: Fri, 23 May 2025 18:58:20 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c00ae96d330e5727c33826d8b8682b456ec00c2d21e16aa797782b7577120cd`  
		Last Modified: Fri, 23 May 2025 18:58:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3d7bc86a5f829992033a0fbbb312c5b134f67c0736f9c7eb1c6578c765db0e`  
		Last Modified: Fri, 23 May 2025 18:58:22 GMT  
		Size: 19.9 MB (19943805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fed8661f8fb5636e6a0b0fea08a085e9097c2ac07504992705a0962ee60da23`  
		Last Modified: Fri, 23 May 2025 18:58:19 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e371b396591894a6e2e888f91e5d1dc9ae45c0b5e0959d5b6bf3715d004b06`  
		Last Modified: Fri, 23 May 2025 18:58:20 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe73034f512fdc35671e7762da54cc9505217565e8a97903f63bc0ac50a717e`  
		Last Modified: Fri, 23 May 2025 18:58:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eed631a98bfcd26df581168d3d2143f26a16c25bde327d8445eac17df267d95`  
		Last Modified: Fri, 23 May 2025 18:58:21 GMT  
		Size: 22.3 MB (22306294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25b9975b1dd2b0c4799e56a89cb73a98df44b17ecfa70b1dc73c999f36b7beb`  
		Last Modified: Fri, 23 May 2025 18:58:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b8d85ab9daa30cc6d41bdeb5975df741a8eb806816b3f40514e9bf69eda7ef`  
		Last Modified: Fri, 23 May 2025 18:58:18 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1681b20439ff829956eb8bdb178f353664ca8bafad18a176660464c4d77fb60`  
		Last Modified: Fri, 23 May 2025 18:58:18 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0a46189849ab2315070c0fd52ec3e39bb5ad50106260a5fb8a50cb343fae5`  
		Last Modified: Fri, 23 May 2025 18:58:21 GMT  
		Size: 22.1 MB (22059480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:26f1beea13ebb8b829a07d31e74201b2e9cb37c3bbb79496b1b957d7cd1c8e7c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338164194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1964f795ab4183db46af07466d0aca95ed1a740cea196410ac30507d7cf62d60`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Fri, 23 May 2025 19:00:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 19:00:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 23 May 2025 19:00:45 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 19:00:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Fri, 23 May 2025 19:00:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:00:56 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 19:00:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Fri, 23 May 2025 19:00:58 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Fri, 23 May 2025 19:01:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:01:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 19:01:07 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Fri, 23 May 2025 19:01:07 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Fri, 23 May 2025 19:01:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70a8534276f45966357169a3bb5537ba803f56b95eef6146951b815540b6d1b`  
		Last Modified: Fri, 23 May 2025 19:01:24 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fe74c6747cded88a9e5d2d831ab16a9463a089c02ca63fcb91ba2ed25c3e58`  
		Last Modified: Fri, 23 May 2025 19:01:24 GMT  
		Size: 356.8 KB (356794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16f223670595d48ad5968dddad0fc471e6a5fdbb62f33ddf526676679964c8c`  
		Last Modified: Fri, 23 May 2025 19:01:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23366a0b381a6bece0c0ba6bf588b437d414ca27d5e14228dcb59d0690d11477`  
		Last Modified: Fri, 23 May 2025 19:01:22 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa4693b4884d15fc0948b35fade6c2240a77c5cddd7b435888d8bf0ca12b321`  
		Last Modified: Fri, 23 May 2025 19:01:24 GMT  
		Size: 19.9 MB (19894034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88d68e0628616b1c65f26d440d18220a2e90bfc63d02ad388b5b53dd216b7a8`  
		Last Modified: Fri, 23 May 2025 19:01:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c61e50ac159733fa620b6acbac621b7b1949eb1b1486dedf74a6e42cba2173a`  
		Last Modified: Fri, 23 May 2025 19:01:20 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9969d7457944c740e5887d9aab74a3fbf9170664db7011d4d24ba58d54f2fa6`  
		Last Modified: Fri, 23 May 2025 19:01:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40830942f745e07c7400fb4e533f4164137901ca8678d7a645e4b0e6937fd9ac`  
		Last Modified: Fri, 23 May 2025 19:01:22 GMT  
		Size: 22.3 MB (22262139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db357aae97a3f218941416707f5eac12dc7216078335536fa9b8e3799679e60`  
		Last Modified: Fri, 23 May 2025 19:01:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc782ea48a4c2f08f3d2cb3dbe80864de1c0ae5a951085196b9258512626418`  
		Last Modified: Fri, 23 May 2025 19:01:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f543e62daba700ef0075b7cd61e86c1fdfb807e054c12d8806db6abebe781933`  
		Last Modified: Fri, 23 May 2025 19:01:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245d5a64afd293741ccb48079ea1449f570572d7838ab4bc03bb4cac87e2c1fb`  
		Last Modified: Fri, 23 May 2025 19:01:22 GMT  
		Size: 22.0 MB (22011529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:d8c9d0051e906b65e6b274145bb1a6bf42c01be2b584e015b2450061a831fb7a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248271030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bc6320aabd791b70a61076d88e78589d31d99b579e296e6d9ed671db172f92`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Fri, 23 May 2025 19:01:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 19:01:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 23 May 2025 19:01:51 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 19:01:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Fri, 23 May 2025 19:02:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:02:05 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 19:02:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Fri, 23 May 2025 19:02:06 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Fri, 23 May 2025 19:02:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:02:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 19:02:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Fri, 23 May 2025 19:02:17 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Fri, 23 May 2025 19:02:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bedba5d8bb10709897be0ca11c0fd7aa652325aa9e1ae6cb99499ffb5348423`  
		Last Modified: Fri, 23 May 2025 19:02:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1eda583ca07b2852595a7dfa1f3ffae9eef5e9e4299901df7656452d88015f`  
		Last Modified: Fri, 23 May 2025 19:02:32 GMT  
		Size: 364.7 KB (364665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72420287a02085c94def4c22f2ca2f8b3360457c2df6304a88c9286147d4ddc`  
		Last Modified: Fri, 23 May 2025 19:02:31 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaa2052518fa53328cd0f816e795f6c556cbb16b8e631ada84d61bc3b7e2f0e`  
		Last Modified: Fri, 23 May 2025 19:02:30 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886ee17b8998b7b6c685ec11fc8880863992fdfb32bbbeb7228b4c2ded3dd72b`  
		Last Modified: Fri, 23 May 2025 19:02:32 GMT  
		Size: 19.9 MB (19901768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1b2fe179779a92d665c0ea748ce755d333ba2072b76552a3bb6705554b8763`  
		Last Modified: Fri, 23 May 2025 19:02:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85068da4803dc6274a2db2661b92f564624bdf460cba85c56c400e054648ee14`  
		Last Modified: Fri, 23 May 2025 19:02:29 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d8c76e0c60a668e8f2ed3d2aa9b644e0d25faee78c68cc796ba836d041cc62`  
		Last Modified: Fri, 23 May 2025 19:02:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4321b3be2b8f9845f01f6a0503043622534fada9d1f6e960e4067926089509`  
		Last Modified: Fri, 23 May 2025 19:02:31 GMT  
		Size: 22.3 MB (22266672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47afe0e541f0c501cfc4e2b3fa3d95dd7123ff584e51d0a9e126547eb8009a4b`  
		Last Modified: Fri, 23 May 2025 19:02:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdf962e512c522c9753deba814e6a0b63ebaf74fc3beb95bb5f268c88e2e09e`  
		Last Modified: Fri, 23 May 2025 19:02:29 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93a31e65a4686b2102d0fe84c29161dc421cfe1af37756cc4d6555f1e033c40`  
		Last Modified: Fri, 23 May 2025 19:02:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921c35cd822abe89a11c931d38819a21ff6e6f984acaf3de4b3f3242002e2bbe`  
		Last Modified: Fri, 23 May 2025 19:02:32 GMT  
		Size: 22.0 MB (22008812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:c3dda8e1cfe3b7ff0ae0a6031cc8736fc23d0df01a68ba7b26463720270b7d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:d8c9d0051e906b65e6b274145bb1a6bf42c01be2b584e015b2450061a831fb7a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248271030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bc6320aabd791b70a61076d88e78589d31d99b579e296e6d9ed671db172f92`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Fri, 23 May 2025 19:01:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 19:01:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 23 May 2025 19:01:51 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 19:01:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Fri, 23 May 2025 19:02:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:02:05 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 19:02:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Fri, 23 May 2025 19:02:06 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Fri, 23 May 2025 19:02:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:02:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 19:02:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Fri, 23 May 2025 19:02:17 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Fri, 23 May 2025 19:02:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bedba5d8bb10709897be0ca11c0fd7aa652325aa9e1ae6cb99499ffb5348423`  
		Last Modified: Fri, 23 May 2025 19:02:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1eda583ca07b2852595a7dfa1f3ffae9eef5e9e4299901df7656452d88015f`  
		Last Modified: Fri, 23 May 2025 19:02:32 GMT  
		Size: 364.7 KB (364665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72420287a02085c94def4c22f2ca2f8b3360457c2df6304a88c9286147d4ddc`  
		Last Modified: Fri, 23 May 2025 19:02:31 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaa2052518fa53328cd0f816e795f6c556cbb16b8e631ada84d61bc3b7e2f0e`  
		Last Modified: Fri, 23 May 2025 19:02:30 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886ee17b8998b7b6c685ec11fc8880863992fdfb32bbbeb7228b4c2ded3dd72b`  
		Last Modified: Fri, 23 May 2025 19:02:32 GMT  
		Size: 19.9 MB (19901768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1b2fe179779a92d665c0ea748ce755d333ba2072b76552a3bb6705554b8763`  
		Last Modified: Fri, 23 May 2025 19:02:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85068da4803dc6274a2db2661b92f564624bdf460cba85c56c400e054648ee14`  
		Last Modified: Fri, 23 May 2025 19:02:29 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d8c76e0c60a668e8f2ed3d2aa9b644e0d25faee78c68cc796ba836d041cc62`  
		Last Modified: Fri, 23 May 2025 19:02:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4321b3be2b8f9845f01f6a0503043622534fada9d1f6e960e4067926089509`  
		Last Modified: Fri, 23 May 2025 19:02:31 GMT  
		Size: 22.3 MB (22266672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47afe0e541f0c501cfc4e2b3fa3d95dd7123ff584e51d0a9e126547eb8009a4b`  
		Last Modified: Fri, 23 May 2025 19:02:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdf962e512c522c9753deba814e6a0b63ebaf74fc3beb95bb5f268c88e2e09e`  
		Last Modified: Fri, 23 May 2025 19:02:29 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93a31e65a4686b2102d0fe84c29161dc421cfe1af37756cc4d6555f1e033c40`  
		Last Modified: Fri, 23 May 2025 19:02:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921c35cd822abe89a11c931d38819a21ff6e6f984acaf3de4b3f3242002e2bbe`  
		Last Modified: Fri, 23 May 2025 19:02:32 GMT  
		Size: 22.0 MB (22008812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:4f3494b5abc8262da231195ca96646c79f643363fd211bd6fdfaf1f3b2c22600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:26f1beea13ebb8b829a07d31e74201b2e9cb37c3bbb79496b1b957d7cd1c8e7c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338164194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1964f795ab4183db46af07466d0aca95ed1a740cea196410ac30507d7cf62d60`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Fri, 23 May 2025 19:00:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 19:00:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 23 May 2025 19:00:45 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 19:00:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Fri, 23 May 2025 19:00:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:00:56 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 19:00:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Fri, 23 May 2025 19:00:58 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Fri, 23 May 2025 19:01:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:01:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 19:01:07 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Fri, 23 May 2025 19:01:07 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Fri, 23 May 2025 19:01:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70a8534276f45966357169a3bb5537ba803f56b95eef6146951b815540b6d1b`  
		Last Modified: Fri, 23 May 2025 19:01:24 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fe74c6747cded88a9e5d2d831ab16a9463a089c02ca63fcb91ba2ed25c3e58`  
		Last Modified: Fri, 23 May 2025 19:01:24 GMT  
		Size: 356.8 KB (356794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16f223670595d48ad5968dddad0fc471e6a5fdbb62f33ddf526676679964c8c`  
		Last Modified: Fri, 23 May 2025 19:01:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23366a0b381a6bece0c0ba6bf588b437d414ca27d5e14228dcb59d0690d11477`  
		Last Modified: Fri, 23 May 2025 19:01:22 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa4693b4884d15fc0948b35fade6c2240a77c5cddd7b435888d8bf0ca12b321`  
		Last Modified: Fri, 23 May 2025 19:01:24 GMT  
		Size: 19.9 MB (19894034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88d68e0628616b1c65f26d440d18220a2e90bfc63d02ad388b5b53dd216b7a8`  
		Last Modified: Fri, 23 May 2025 19:01:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c61e50ac159733fa620b6acbac621b7b1949eb1b1486dedf74a6e42cba2173a`  
		Last Modified: Fri, 23 May 2025 19:01:20 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9969d7457944c740e5887d9aab74a3fbf9170664db7011d4d24ba58d54f2fa6`  
		Last Modified: Fri, 23 May 2025 19:01:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40830942f745e07c7400fb4e533f4164137901ca8678d7a645e4b0e6937fd9ac`  
		Last Modified: Fri, 23 May 2025 19:01:22 GMT  
		Size: 22.3 MB (22262139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db357aae97a3f218941416707f5eac12dc7216078335536fa9b8e3799679e60`  
		Last Modified: Fri, 23 May 2025 19:01:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc782ea48a4c2f08f3d2cb3dbe80864de1c0ae5a951085196b9258512626418`  
		Last Modified: Fri, 23 May 2025 19:01:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f543e62daba700ef0075b7cd61e86c1fdfb807e054c12d8806db6abebe781933`  
		Last Modified: Fri, 23 May 2025 19:01:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245d5a64afd293741ccb48079ea1449f570572d7838ab4bc03bb4cac87e2c1fb`  
		Last Modified: Fri, 23 May 2025 19:01:22 GMT  
		Size: 22.0 MB (22011529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:2dfc3072b23698276ed7d3b69df2849d7335638e4c1514b3b9170192f01272bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:2762cf87a5b42c6876093051307646874ff01ad812ca4189df1dcfef154701a9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3495499097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec779341b953e8c9821ae09f43ae763f69658d1dae6a2b71c939bd1219133eca`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Fri, 23 May 2025 18:57:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 18:57:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 23 May 2025 18:57:44 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 23 May 2025 18:57:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Fri, 23 May 2025 18:57:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 18:57:55 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 18:57:56 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Fri, 23 May 2025 18:57:57 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Fri, 23 May 2025 18:58:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 18:58:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 18:58:07 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Fri, 23 May 2025 18:58:08 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Fri, 23 May 2025 18:58:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996aa5fabf587504c303e732d25d9c379fa94d7ab3daa6fbd77090c9f92aaf26`  
		Last Modified: Fri, 23 May 2025 18:58:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e6587e4dfb610200936369102507f9840984b1e56ab5cd559376ba420eff8f`  
		Last Modified: Fri, 23 May 2025 18:58:21 GMT  
		Size: 412.0 KB (411954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f48fa8095e030252604fcbd3f05bc0bc59f2deb32f9a5ca7f9084aa2e40afa`  
		Last Modified: Fri, 23 May 2025 18:58:20 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c00ae96d330e5727c33826d8b8682b456ec00c2d21e16aa797782b7577120cd`  
		Last Modified: Fri, 23 May 2025 18:58:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3d7bc86a5f829992033a0fbbb312c5b134f67c0736f9c7eb1c6578c765db0e`  
		Last Modified: Fri, 23 May 2025 18:58:22 GMT  
		Size: 19.9 MB (19943805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fed8661f8fb5636e6a0b0fea08a085e9097c2ac07504992705a0962ee60da23`  
		Last Modified: Fri, 23 May 2025 18:58:19 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e371b396591894a6e2e888f91e5d1dc9ae45c0b5e0959d5b6bf3715d004b06`  
		Last Modified: Fri, 23 May 2025 18:58:20 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe73034f512fdc35671e7762da54cc9505217565e8a97903f63bc0ac50a717e`  
		Last Modified: Fri, 23 May 2025 18:58:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eed631a98bfcd26df581168d3d2143f26a16c25bde327d8445eac17df267d95`  
		Last Modified: Fri, 23 May 2025 18:58:21 GMT  
		Size: 22.3 MB (22306294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25b9975b1dd2b0c4799e56a89cb73a98df44b17ecfa70b1dc73c999f36b7beb`  
		Last Modified: Fri, 23 May 2025 18:58:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b8d85ab9daa30cc6d41bdeb5975df741a8eb806816b3f40514e9bf69eda7ef`  
		Last Modified: Fri, 23 May 2025 18:58:18 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1681b20439ff829956eb8bdb178f353664ca8bafad18a176660464c4d77fb60`  
		Last Modified: Fri, 23 May 2025 18:58:18 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0a46189849ab2315070c0fd52ec3e39bb5ad50106260a5fb8a50cb343fae5`  
		Last Modified: Fri, 23 May 2025 18:58:21 GMT  
		Size: 22.1 MB (22059480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
