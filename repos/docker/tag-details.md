<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:29`](#docker29)
-	[`docker:29-cli`](#docker29-cli)
-	[`docker:29-dind`](#docker29-dind)
-	[`docker:29-dind-rootless`](#docker29-dind-rootless)
-	[`docker:29-windowsservercore`](#docker29-windowsservercore)
-	[`docker:29-windowsservercore-ltsc2022`](#docker29-windowsservercore-ltsc2022)
-	[`docker:29-windowsservercore-ltsc2025`](#docker29-windowsservercore-ltsc2025)
-	[`docker:29.3`](#docker293)
-	[`docker:29.3-cli`](#docker293-cli)
-	[`docker:29.3-dind`](#docker293-dind)
-	[`docker:29.3-dind-rootless`](#docker293-dind-rootless)
-	[`docker:29.3-windowsservercore`](#docker293-windowsservercore)
-	[`docker:29.3-windowsservercore-ltsc2022`](#docker293-windowsservercore-ltsc2022)
-	[`docker:29.3-windowsservercore-ltsc2025`](#docker293-windowsservercore-ltsc2025)
-	[`docker:29.3.1`](#docker2931)
-	[`docker:29.3.1-alpine3.23`](#docker2931-alpine323)
-	[`docker:29.3.1-cli`](#docker2931-cli)
-	[`docker:29.3.1-cli-alpine3.23`](#docker2931-cli-alpine323)
-	[`docker:29.3.1-dind`](#docker2931-dind)
-	[`docker:29.3.1-dind-alpine3.23`](#docker2931-dind-alpine323)
-	[`docker:29.3.1-dind-rootless`](#docker2931-dind-rootless)
-	[`docker:29.3.1-windowsservercore`](#docker2931-windowsservercore)
-	[`docker:29.3.1-windowsservercore-ltsc2022`](#docker2931-windowsservercore-ltsc2022)
-	[`docker:29.3.1-windowsservercore-ltsc2025`](#docker2931-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:29`

```console
$ docker pull docker@sha256:1ba18449911d01f477a3fc104123c85d677addc60701b14b3fcb5381f9c4a537
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
$ docker pull docker@sha256:e60900b4413a183173b0c12a7c34bfa7ba511fd074147a1b7974ebb296a0050b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144453044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5b3ee3882d4d0af9fc139d2545bf1d17e251c849e98b98da2fe418431e2ad8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:46:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:46:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:46:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:46:28 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:46:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:46:28 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:46:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:46:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:46:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:46:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:46:30 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:10:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:10:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:10:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:10:30 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f1c7a58cda4399b7be2fb8427c3b756917df1abb433e17a98888259aa70c83`  
		Last Modified: Thu, 05 Mar 2026 18:46:37 GMT  
		Size: 8.4 MB (8399691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba58ca1e42e5eeec21273f066c06e25afee78a5211c7d6deb38ba545b7d6240`  
		Last Modified: Thu, 05 Mar 2026 18:46:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f8c3243c30359f68ee8e1f96a24d246ca1357a82d8b30de9a33e9d282d93e1`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 18.9 MB (18919365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e9c4ffbcbf205284b573f955de57155f10b92234b491b2127720a57c90c1ce`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 28.5 MB (28516523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34962ed90623b311790e104f78a280cdc54a1ce559635328476148c6fc522888`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 11.0 MB (10953934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a9731c772a36b5ae18988bc0c1c69aff62cb86d597f2de367c5b330fb8d459`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a294ee3d24d1214f1944e57dadb6ef9c4b434a1a170e348838dafb16d31127`  
		Last Modified: Thu, 05 Mar 2026 18:46:39 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df03e33ed496925038509c0abcd9f087ab5ec4e4b917ed51730d71d63a87c91`  
		Last Modified: Thu, 05 Mar 2026 18:46:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fbd819f55b555293ac19eaaa17fd0ff75f9812f924da0a56610f334b1db8e6`  
		Last Modified: Thu, 05 Mar 2026 19:10:41 GMT  
		Size: 6.9 MB (6934736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524d6d9cccdc6fa4c04046756dada64359f4445d625ae2d4653714afad9044c`  
		Last Modified: Thu, 05 Mar 2026 19:10:40 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4da28e0bc44f1c47c50aab943753bc5626ab338c9dacd7cff96381acf13793`  
		Last Modified: Thu, 05 Mar 2026 19:10:41 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503f0e2071dd914a67c23aa1b570c3fccb863ebac670fa0d253ff15658adaf0a`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 66.8 MB (66766357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdcbaa55207a60126845f61a87ad8fbea9e87874674046ea2133cb2f3159d36`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bd5217468716f0f037bdb54d7c022dbf95c6896f29dc171a9677f86f621c25`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:51f66381d79e85e83914402852c9997eddc9b6c3b280e0aa86c37f2a4ba27738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8ef8f35ce741ad2c83d3a11a6b0eabe3616860c0a9fd2deba0d9b603978bf0`

```dockerfile
```

-	Layers:
	-	`sha256:9de809ee0c1e4804fb0ce3ce24f183e971a8f1020e5d25d1eba9202ecfb23554`  
		Last Modified: Thu, 05 Mar 2026 19:10:40 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v6

```console
$ docker pull docker@sha256:921ed9ba3b685e60ee0cdcd138b4aa718d396a4e4e1418de3348b766229448c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136262850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739701c78bbbb4755e7b5694d8e2032e7edaca1f5ab49ddc7c1bcef1e289abbe`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:45:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:45:36 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:45:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:45:39 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:45:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:45:39 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:45:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:45:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:45:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:45:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:45:43 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:08:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:08:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:08:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:08:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:08:49 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:08:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:08:49 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0593a5009b5f1611e29afa031add0caa8e17436567b91fa0cd2b29e51d22c89`  
		Last Modified: Thu, 05 Mar 2026 18:45:50 GMT  
		Size: 8.3 MB (8300931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aae9fbc3eb9720394677e4ecd6aab19d036b3e73b352fb74b67d6b3a2fc9fa6`  
		Last Modified: Thu, 05 Mar 2026 18:45:50 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d66dff73ca29a47e9b6b4c6c761a4d7aa8867dca97bc28872f55bf9f47e2c6`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 17.7 MB (17698879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2808c066fd3febfd5f5674816180176477b47da3158ad376e658eb6d8136fab1`  
		Last Modified: Thu, 05 Mar 2026 18:45:51 GMT  
		Size: 26.8 MB (26774787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663b0b4076c27408b2184d77a831c36817e8a8d8d4897cb92fce9cdd0165335a`  
		Last Modified: Thu, 05 Mar 2026 18:45:51 GMT  
		Size: 10.4 MB (10385429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3615b056b4ef975abfd3ae24796393abcb6cd5c819f1c8a6e68c1488f641f1a`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32f9cb2f283cf611fe753cefc9ac89c970b2a82e793b029047ec9a74dd88da4`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5dc68331a182d6047cc64dc01811876321654c40481e65df941bf21d1129ff`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281309e002e2014f85aa6e60f8f56d3a46cd826258710ea23f02ebd55fa56d86`  
		Last Modified: Thu, 05 Mar 2026 19:08:59 GMT  
		Size: 7.3 MB (7271697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d5638366f0629a45399b2da5bc12e7eaec99cd43a172c0e00a061cbad07fd9`  
		Last Modified: Thu, 05 Mar 2026 19:08:58 GMT  
		Size: 91.8 KB (91788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db525e8a11303b587a4637ce4f7e8cf2e27b87515229e415c66b907d6857c14`  
		Last Modified: Thu, 05 Mar 2026 19:08:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b41beca4d05ad9f4f8a0af06864a9b0bd92eb236aae78aec36d96eee3e972e7`  
		Last Modified: Thu, 05 Mar 2026 19:09:00 GMT  
		Size: 62.2 MB (62161362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c988857a21079067d802211bb65b801edbebcc1e6e21bd8e6e7eea98dc58fc`  
		Last Modified: Thu, 05 Mar 2026 19:09:00 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0de727742fa3feb2ba852cdaa770c212967433c39bb41ebfe1865a9ffcc78e`  
		Last Modified: Thu, 05 Mar 2026 19:09:00 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:01e39cec6c99783d318713cb96e9d665690e384f821039d02ecc3d40d501c51d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c18a85619e7433b908f936509e5dbd40bb98ace79929f60a844a1db3c93374`

```dockerfile
```

-	Layers:
	-	`sha256:d37d617810772a2c79e6330f2dbaf0e418ffcc3f2db333b8443afe97f45e219b`  
		Last Modified: Thu, 05 Mar 2026 19:08:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v7

```console
$ docker pull docker@sha256:74ea5cdbe2fe4518d73e3ac0241167a38c7616c3dd6be011cf48fc0a61189c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134355560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9d940d504e1f821c76a9e400c405dfbc51b3d58990d7abaae29dd773c08694`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:46:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:46:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:46:32 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:46:36 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:46:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:46:36 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:46:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:46:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:46:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:46:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:46:40 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:09:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:09:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:09:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:09:20 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:09:20 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:09:20 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:09:20 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95152b95c4ccfeb5059ced14a96c4f1c17872baa3e875c18056cb5bed1b56676`  
		Last Modified: Thu, 05 Mar 2026 18:46:46 GMT  
		Size: 7.6 MB (7597774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d532e57eb4774540148a1cccd311fc10645e4dc68e8512d6b4f5a07d77498e82`  
		Last Modified: Thu, 05 Mar 2026 18:46:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64983bc952c232855d431fc0da6e3080f4c4c64fc0dce721c1086cc916d3037`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 17.7 MB (17691333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0552f021a975b88c2f33fc3057737b716d29921dcf12fff1a7bd017272ee52bf`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 26.8 MB (26754433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe274cdce52e0d95eda23b7407fdd0cd8a861a2014d8a240bda6be387b22c74`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 10.4 MB (10369783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28feee09383ef1673e7a0cec5e45cf0ad41f8b64208682ad535da48f8de7e08e`  
		Last Modified: Thu, 05 Mar 2026 18:46:48 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c266b2e92e5c06c3362ac89279eac9742220da712ded40590f3312de938eb16a`  
		Last Modified: Thu, 05 Mar 2026 18:46:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b204129a9de694faa70c2c825548fbe88d190e24ecc2d949a3ea099c0ac40d3`  
		Last Modified: Thu, 05 Mar 2026 18:46:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6011a406c6080a98a187e060555bd77450686dc8a0a3a1bd21a8b635e7a7c7c5`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 6.6 MB (6573025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63255cd848e2b7900e0177b225137079a3c0e9bde16e58d50a40edba81e6b028`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 88.2 KB (88150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3758bf28f38de089029226cd958aeeb1d75194761390a5bd605206ae3d4092e3`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbec48042bff8bd1621f0f9cd3d2ec81bc03fdba86235b7e6586dec177d82907`  
		Last Modified: Thu, 05 Mar 2026 19:09:32 GMT  
		Size: 62.0 MB (61991183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f8030e199452b1b297f3a4acc28ce81ecd590b3b41343eb4dbb260d0a03684`  
		Last Modified: Thu, 05 Mar 2026 19:09:31 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a7939d77fae184c61e7cbceee2129945aff07b2c8ba46170605cd266cdee9f`  
		Last Modified: Thu, 05 Mar 2026 19:09:31 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:0d74abb912009d5524b2bc08d235dd65785a6a9c105843b2d5f2e38d9740c01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e7a73ef832c7e6998b93ef231c73a0f5a4b733dd27635018b7ccc4808f8859`

```dockerfile
```

-	Layers:
	-	`sha256:dfe982715ef650b1926988aa185ecef3d257673538c7392c6271f6a59a023df3`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 34.7 KB (34721 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1d1d67ba557d1ccedcd46d05ba832276e65260a518c240b087c71849cd6cbce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133716998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2468f972a259c78d9053fa37f4ca40d54c8071086fecff98d4e0f4829c120c36`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:44:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:44:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:44:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:44:32 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:44:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:44:32 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:44:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:44:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:44:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:44:34 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:10:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:10:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:10:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:10:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:10:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:10:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:10:13 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74f52f7948b98f731cc47a7da43a1a028f38396d447d93fa458cc7b1ee9ade0`  
		Last Modified: Thu, 05 Mar 2026 18:44:41 GMT  
		Size: 8.5 MB (8453572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50de1b9f6ee9b0bb47a9cb5e7877595782f60dc2d6c014088cfb72c4dca02106`  
		Last Modified: Thu, 05 Mar 2026 18:44:40 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8cd16e98d03b1081e8606a566c45e24d404e6738ce672011e2f5e3fe3b637b`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 17.5 MB (17472694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a548a65df6cf925e933ead68a3677913c3c9586d7115d161b6afd378cd8b1836`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 25.7 MB (25732665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09bdc4530b81e1aa74fe3d0322209932119b3cb64a72447d5442bd9c50cd4ed`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 10.0 MB (9974089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b96e65028eacc3700698877e774e4bfbca321b41420638481e753d07449225c`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faab51bb66faa3b0c0d737ebc09cfb486e94acbcdc20e883d8022102e4fc2fd`  
		Last Modified: Thu, 05 Mar 2026 18:44:43 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd02735b351188e3d18abc71b56816ddc7406e1d55c433166d34e8fd46aa5692`  
		Last Modified: Thu, 05 Mar 2026 18:44:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bd6c43d314f7ba1970375218d37bf189ee9e325f65b8a993a3846b8b081490`  
		Last Modified: Thu, 05 Mar 2026 19:10:23 GMT  
		Size: 7.2 MB (7213319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447b7408aabced1a21d26cecd53e54c14e75f0c7fa49a892e88b3faa8618791d`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 101.3 KB (101302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a4786ffc77dd17db34d4bd2edde2706bdb8bde49e2f5c532ffdb910ab16ee9`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce02e419a084f596f3e92c28731f67e0f113c3464b10ce77db5f722f7da9d1d`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 60.6 MB (60564110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf5b1f083f16666d8e3ef65369ed92093b78752eb5146941526e49b6d31965e`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720b8605e7f2e52dd9a65c8e463ab396a44abc68a0a689a3eda9a497503540fb`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:f842673f5ac13d592cac6534e468f00a1d0270c7b8b686dff5ede372d952ad2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aec29e8d6f9254e8a5488aabb8ce917d657467f43e13af6528879dc1f2bfe02`

```dockerfile
```

-	Layers:
	-	`sha256:d59a3392ae448d26d8ed94f620ba9496be18d97cce5dc57e5943d287b049c800`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:70303ed0d265aee7bf4be0ddffe20b0b6e4f69ffa125e2a20cbb3718b99688db
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
$ docker pull docker@sha256:3459e4b0c6702acfdc23b2a48e4e8bdcfc51ef96bac2d0af3ea3edac4044192c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70660468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f34f75af30162c2d6b68fa089dac03a627ba7303e9758184d9d26dacb913ca7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:31:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:31:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:31:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:31:34 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:31:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:31:34 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:31:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:31:36 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:31:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:31:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:31:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f783f43bd0c479eca4a605cd057214fd4d32195579fd3858ea619042787418`  
		Last Modified: Wed, 25 Mar 2026 18:31:45 GMT  
		Size: 8.4 MB (8399805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dc00f58fe8675ce338442f1f3924e7575b889140324f529e6f7b7b552e6a8b`  
		Last Modified: Wed, 25 Mar 2026 18:31:44 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed7cc89d7e24509b5ecc2a876b68c336cc533fccd578553f96c40bd5977acaa`  
		Last Modified: Wed, 25 Mar 2026 18:31:45 GMT  
		Size: 18.9 MB (18925059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59f566876aae23a8d4ded9382841f58305b92c7453a48044734ac35241c5e5d`  
		Last Modified: Wed, 25 Mar 2026 18:31:46 GMT  
		Size: 28.5 MB (28516527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f27ff511c85a43e9a75a388dbd32088a24592f41c6987999fbcf0165672071d`  
		Last Modified: Wed, 25 Mar 2026 18:31:46 GMT  
		Size: 11.0 MB (10955101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac4601d8546b2a6477f79a9bff1a05ec9add30bf96dc48fcd27457170f39b07`  
		Last Modified: Wed, 25 Mar 2026 18:31:46 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b922537b6a3dd95fc487130c0ca4896eb541d70d4a9438dd39590ccb7b65943`  
		Last Modified: Wed, 25 Mar 2026 18:31:47 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62fa46a186b2dc7d1a25e70eb2c2653aa0431485adb908a7cf943d28c49cdf1`  
		Last Modified: Wed, 25 Mar 2026 18:31:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:827d9483e2a64b8c44523708ca54adaeec69e1ee40b1f275bb657e51828404f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587b7070e426c0932cb45f162874ea0917cc386aa52282a4e864f0aceeac21c5`

```dockerfile
```

-	Layers:
	-	`sha256:9c77ec231f2b5c72293c670da21cfc5dc7c509522268cc74c92f9098859cef6a`  
		Last Modified: Wed, 25 Mar 2026 18:31:44 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:ab088b3f5efe676c33f3339eeefbb2228b5e4b45cc6189a7ee8d717f98d47796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66741259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6299617540122589abca8da49bf316efc08ef3e0e4632b70f20e47121c8e7a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:20:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:20:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:20:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:20:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:20:55 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:20:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:20:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:20:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7327f5bd7b20a7c0c384c9bed111c54ed041e23650f2789ce160520bd54e7d64`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 8.3 MB (8300847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad441b201d110caa6bbae91773542ed3038e833916ab8fdbdee2efdd096951d`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a9b3570b577d5bd7b5702ea3b038bd6d6736da52c7e4cfa9204254b3ef6889`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 17.7 MB (17704832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687acedd268ebaa81d467b79f662cb296f999d5edc939573fc235718f10b3d5`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 26.8 MB (26774785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6738b4fa70496e709329c400187d16a1e6dcd9323aa0597219b36caeffbf73`  
		Last Modified: Wed, 25 Mar 2026 18:21:12 GMT  
		Size: 10.4 MB (10388825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0425cd14663ea2989a267ae635da01c39877aac17e1b4a26049c6e8584e9b7`  
		Last Modified: Wed, 25 Mar 2026 18:21:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7154483d9dd47aca8dda22548f6ac6381d6f297c1afcbda1c72dba31279d96f7`  
		Last Modified: Wed, 25 Mar 2026 18:21:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbfd7d41a6aa1e531936a17e36405a287262345307d1769bbf5e514f1f4955a`  
		Last Modified: Wed, 25 Mar 2026 18:21:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4a04a0fb0422d24efcd71966c2ec778971b5a49ba8fb1934681a3c061a4f7bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8881255256c5bafe467ec0dffa5cdafa965971effe17aab0e66a451dbac7b198`

```dockerfile
```

-	Layers:
	-	`sha256:e6eb00c7bd1756168105295aa8a9f0546960e7bf78727f47d669e70e1096cc65`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:b4cf24daf2e960893a39d2f0a13a0b2b889e626725f5704295ff3c7a80e2ce56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65702900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e770b04316507e289fdbe463af8dd53873a490a5215e9664d3c38a2387b9b0bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:20:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:20:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:20:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:20:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:20:55 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:20:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:20:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:20:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9a25e5bfb326bc75a71b460d0544e0abe70b0c6c1498521b7fd245df901627`  
		Last Modified: Wed, 25 Mar 2026 18:21:05 GMT  
		Size: 7.6 MB (7597792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bd4d27cb3827cca3206705328c83ee80e164a78dc2aa97099d480bb1ded087`  
		Last Modified: Wed, 25 Mar 2026 18:21:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57192b9959272e69a74f1600a28d23141f96a9856eb275612e66d96aed4cb23`  
		Last Modified: Wed, 25 Mar 2026 18:21:05 GMT  
		Size: 17.7 MB (17694926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7afb84b0bb6525824e7b41a3eb6ca04fbd8a378336dace66c201e7f0a9fdfd`  
		Last Modified: Wed, 25 Mar 2026 18:21:06 GMT  
		Size: 26.8 MB (26754421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34cbd0d9bfc6a2fbae47c23f0d1c832eaf8aacf91c370cd7d44df319b6dcf32`  
		Last Modified: Wed, 25 Mar 2026 18:21:06 GMT  
		Size: 10.4 MB (10371888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92b6554d10f78775d85c869fd50243ef34c2f7fb06170e9bfd0f6cb1d8c722f`  
		Last Modified: Wed, 25 Mar 2026 18:21:06 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a550d751a72e95d6b192c5aa49bc54135cd12eaac778e2494033d746481e4e`  
		Last Modified: Wed, 25 Mar 2026 18:21:07 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbfd7d41a6aa1e531936a17e36405a287262345307d1769bbf5e514f1f4955a`  
		Last Modified: Wed, 25 Mar 2026 18:21:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:b36c22ea07bd32cf40c3233fe677b6cfd0b141b3c63f391124eed2843c5fe9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17c08feca64baed542d11807ef5bdc316ef9f6816d6d0e695109048771339bc`

```dockerfile
```

-	Layers:
	-	`sha256:d9a26fdeeceae1cd37f2b33208c330bcbaaa632331e7950fad92cdb05c62b6ea`  
		Last Modified: Wed, 25 Mar 2026 18:21:05 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:56cff04ad8dcf376a96423ddf5515c8bdcd171e683265335da57f17aa020ad1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65845112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee59cb9a3f85ae950ab85efdd43672abd503dbe5adcd1a55b95687f24e990ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:28:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:28:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:28:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:28:13 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:28:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:28:13 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:28:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:28:14 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:28:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:28:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:28:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7edc56943efc5fd8ceeeec0973e7862a22eef8479f31e4506aaa7683706598`  
		Last Modified: Wed, 25 Mar 2026 18:28:21 GMT  
		Size: 8.5 MB (8453635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d7bdfa7dc871c3af6f5b34ef1ef53c930b2fde5801879b794f1849da1dc4d`  
		Last Modified: Wed, 25 Mar 2026 18:28:20 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c366b69bd090a1557acbb6f1ebdab176751b61ca7e1c82af675fd5dd30436a`  
		Last Modified: Wed, 25 Mar 2026 18:28:21 GMT  
		Size: 17.5 MB (17476961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b74c99f62156a67a1a2f1edfa046c0c13825a6cdef351e68e41cbbffd8badb`  
		Last Modified: Wed, 25 Mar 2026 18:28:22 GMT  
		Size: 25.7 MB (25732670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fed48b65e655b617bf78f3b0c6df9994322561de4c1c4a706e621ec83f8fb84`  
		Last Modified: Wed, 25 Mar 2026 18:28:22 GMT  
		Size: 10.0 MB (9982606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318a3b2c176f6893caa80c95a652634492e38503c58e091a916b6d9c341a0648`  
		Last Modified: Wed, 25 Mar 2026 18:28:23 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c910ec30db0949d800f54bb9c1b3c4e2af20695bf5b14f43f4f9be42a0ecb2c`  
		Last Modified: Wed, 25 Mar 2026 18:28:23 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd0d057ad753e2ef837845dd9504265e602e0802dceee1b0083e05f00291b8c`  
		Last Modified: Wed, 25 Mar 2026 18:28:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a3331dd737a9d4ad382fff64040bbad2660884a99286e44af8338a00851aec68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ed74d502ab8399d1e1a43c9de66bf070e1741c40c8a187c876aa031385bd08`

```dockerfile
```

-	Layers:
	-	`sha256:5de0f8302079e7f4909158e85e3fcabf6c532e1b84c2c25003b4bf3343ea0e94`  
		Last Modified: Wed, 25 Mar 2026 18:28:21 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind`

```console
$ docker pull docker@sha256:1ba18449911d01f477a3fc104123c85d677addc60701b14b3fcb5381f9c4a537
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
$ docker pull docker@sha256:e60900b4413a183173b0c12a7c34bfa7ba511fd074147a1b7974ebb296a0050b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144453044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5b3ee3882d4d0af9fc139d2545bf1d17e251c849e98b98da2fe418431e2ad8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:46:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:46:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:46:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:46:28 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:46:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:46:28 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:46:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:46:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:46:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:46:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:46:30 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:10:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:10:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:10:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:10:30 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f1c7a58cda4399b7be2fb8427c3b756917df1abb433e17a98888259aa70c83`  
		Last Modified: Thu, 05 Mar 2026 18:46:37 GMT  
		Size: 8.4 MB (8399691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba58ca1e42e5eeec21273f066c06e25afee78a5211c7d6deb38ba545b7d6240`  
		Last Modified: Thu, 05 Mar 2026 18:46:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f8c3243c30359f68ee8e1f96a24d246ca1357a82d8b30de9a33e9d282d93e1`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 18.9 MB (18919365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e9c4ffbcbf205284b573f955de57155f10b92234b491b2127720a57c90c1ce`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 28.5 MB (28516523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34962ed90623b311790e104f78a280cdc54a1ce559635328476148c6fc522888`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 11.0 MB (10953934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a9731c772a36b5ae18988bc0c1c69aff62cb86d597f2de367c5b330fb8d459`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a294ee3d24d1214f1944e57dadb6ef9c4b434a1a170e348838dafb16d31127`  
		Last Modified: Thu, 05 Mar 2026 18:46:39 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df03e33ed496925038509c0abcd9f087ab5ec4e4b917ed51730d71d63a87c91`  
		Last Modified: Thu, 05 Mar 2026 18:46:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fbd819f55b555293ac19eaaa17fd0ff75f9812f924da0a56610f334b1db8e6`  
		Last Modified: Thu, 05 Mar 2026 19:10:41 GMT  
		Size: 6.9 MB (6934736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524d6d9cccdc6fa4c04046756dada64359f4445d625ae2d4653714afad9044c`  
		Last Modified: Thu, 05 Mar 2026 19:10:40 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4da28e0bc44f1c47c50aab943753bc5626ab338c9dacd7cff96381acf13793`  
		Last Modified: Thu, 05 Mar 2026 19:10:41 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503f0e2071dd914a67c23aa1b570c3fccb863ebac670fa0d253ff15658adaf0a`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 66.8 MB (66766357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdcbaa55207a60126845f61a87ad8fbea9e87874674046ea2133cb2f3159d36`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bd5217468716f0f037bdb54d7c022dbf95c6896f29dc171a9677f86f621c25`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:51f66381d79e85e83914402852c9997eddc9b6c3b280e0aa86c37f2a4ba27738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8ef8f35ce741ad2c83d3a11a6b0eabe3616860c0a9fd2deba0d9b603978bf0`

```dockerfile
```

-	Layers:
	-	`sha256:9de809ee0c1e4804fb0ce3ce24f183e971a8f1020e5d25d1eba9202ecfb23554`  
		Last Modified: Thu, 05 Mar 2026 19:10:40 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:921ed9ba3b685e60ee0cdcd138b4aa718d396a4e4e1418de3348b766229448c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136262850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739701c78bbbb4755e7b5694d8e2032e7edaca1f5ab49ddc7c1bcef1e289abbe`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:45:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:45:36 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:45:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:45:39 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:45:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:45:39 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:45:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:45:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:45:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:45:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:45:43 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:08:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:08:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:08:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:08:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:08:49 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:08:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:08:49 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0593a5009b5f1611e29afa031add0caa8e17436567b91fa0cd2b29e51d22c89`  
		Last Modified: Thu, 05 Mar 2026 18:45:50 GMT  
		Size: 8.3 MB (8300931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aae9fbc3eb9720394677e4ecd6aab19d036b3e73b352fb74b67d6b3a2fc9fa6`  
		Last Modified: Thu, 05 Mar 2026 18:45:50 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d66dff73ca29a47e9b6b4c6c761a4d7aa8867dca97bc28872f55bf9f47e2c6`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 17.7 MB (17698879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2808c066fd3febfd5f5674816180176477b47da3158ad376e658eb6d8136fab1`  
		Last Modified: Thu, 05 Mar 2026 18:45:51 GMT  
		Size: 26.8 MB (26774787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663b0b4076c27408b2184d77a831c36817e8a8d8d4897cb92fce9cdd0165335a`  
		Last Modified: Thu, 05 Mar 2026 18:45:51 GMT  
		Size: 10.4 MB (10385429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3615b056b4ef975abfd3ae24796393abcb6cd5c819f1c8a6e68c1488f641f1a`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32f9cb2f283cf611fe753cefc9ac89c970b2a82e793b029047ec9a74dd88da4`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5dc68331a182d6047cc64dc01811876321654c40481e65df941bf21d1129ff`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281309e002e2014f85aa6e60f8f56d3a46cd826258710ea23f02ebd55fa56d86`  
		Last Modified: Thu, 05 Mar 2026 19:08:59 GMT  
		Size: 7.3 MB (7271697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d5638366f0629a45399b2da5bc12e7eaec99cd43a172c0e00a061cbad07fd9`  
		Last Modified: Thu, 05 Mar 2026 19:08:58 GMT  
		Size: 91.8 KB (91788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db525e8a11303b587a4637ce4f7e8cf2e27b87515229e415c66b907d6857c14`  
		Last Modified: Thu, 05 Mar 2026 19:08:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b41beca4d05ad9f4f8a0af06864a9b0bd92eb236aae78aec36d96eee3e972e7`  
		Last Modified: Thu, 05 Mar 2026 19:09:00 GMT  
		Size: 62.2 MB (62161362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c988857a21079067d802211bb65b801edbebcc1e6e21bd8e6e7eea98dc58fc`  
		Last Modified: Thu, 05 Mar 2026 19:09:00 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0de727742fa3feb2ba852cdaa770c212967433c39bb41ebfe1865a9ffcc78e`  
		Last Modified: Thu, 05 Mar 2026 19:09:00 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:01e39cec6c99783d318713cb96e9d665690e384f821039d02ecc3d40d501c51d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c18a85619e7433b908f936509e5dbd40bb98ace79929f60a844a1db3c93374`

```dockerfile
```

-	Layers:
	-	`sha256:d37d617810772a2c79e6330f2dbaf0e418ffcc3f2db333b8443afe97f45e219b`  
		Last Modified: Thu, 05 Mar 2026 19:08:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:74ea5cdbe2fe4518d73e3ac0241167a38c7616c3dd6be011cf48fc0a61189c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134355560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9d940d504e1f821c76a9e400c405dfbc51b3d58990d7abaae29dd773c08694`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:46:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:46:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:46:32 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:46:36 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:46:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:46:36 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:46:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:46:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:46:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:46:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:46:40 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:09:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:09:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:09:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:09:20 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:09:20 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:09:20 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:09:20 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95152b95c4ccfeb5059ced14a96c4f1c17872baa3e875c18056cb5bed1b56676`  
		Last Modified: Thu, 05 Mar 2026 18:46:46 GMT  
		Size: 7.6 MB (7597774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d532e57eb4774540148a1cccd311fc10645e4dc68e8512d6b4f5a07d77498e82`  
		Last Modified: Thu, 05 Mar 2026 18:46:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64983bc952c232855d431fc0da6e3080f4c4c64fc0dce721c1086cc916d3037`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 17.7 MB (17691333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0552f021a975b88c2f33fc3057737b716d29921dcf12fff1a7bd017272ee52bf`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 26.8 MB (26754433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe274cdce52e0d95eda23b7407fdd0cd8a861a2014d8a240bda6be387b22c74`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 10.4 MB (10369783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28feee09383ef1673e7a0cec5e45cf0ad41f8b64208682ad535da48f8de7e08e`  
		Last Modified: Thu, 05 Mar 2026 18:46:48 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c266b2e92e5c06c3362ac89279eac9742220da712ded40590f3312de938eb16a`  
		Last Modified: Thu, 05 Mar 2026 18:46:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b204129a9de694faa70c2c825548fbe88d190e24ecc2d949a3ea099c0ac40d3`  
		Last Modified: Thu, 05 Mar 2026 18:46:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6011a406c6080a98a187e060555bd77450686dc8a0a3a1bd21a8b635e7a7c7c5`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 6.6 MB (6573025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63255cd848e2b7900e0177b225137079a3c0e9bde16e58d50a40edba81e6b028`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 88.2 KB (88150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3758bf28f38de089029226cd958aeeb1d75194761390a5bd605206ae3d4092e3`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbec48042bff8bd1621f0f9cd3d2ec81bc03fdba86235b7e6586dec177d82907`  
		Last Modified: Thu, 05 Mar 2026 19:09:32 GMT  
		Size: 62.0 MB (61991183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f8030e199452b1b297f3a4acc28ce81ecd590b3b41343eb4dbb260d0a03684`  
		Last Modified: Thu, 05 Mar 2026 19:09:31 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a7939d77fae184c61e7cbceee2129945aff07b2c8ba46170605cd266cdee9f`  
		Last Modified: Thu, 05 Mar 2026 19:09:31 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:0d74abb912009d5524b2bc08d235dd65785a6a9c105843b2d5f2e38d9740c01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e7a73ef832c7e6998b93ef231c73a0f5a4b733dd27635018b7ccc4808f8859`

```dockerfile
```

-	Layers:
	-	`sha256:dfe982715ef650b1926988aa185ecef3d257673538c7392c6271f6a59a023df3`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 34.7 KB (34721 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1d1d67ba557d1ccedcd46d05ba832276e65260a518c240b087c71849cd6cbce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133716998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2468f972a259c78d9053fa37f4ca40d54c8071086fecff98d4e0f4829c120c36`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:44:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:44:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:44:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:44:32 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:44:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:44:32 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:44:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:44:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:44:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:44:34 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:10:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:10:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:10:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:10:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:10:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:10:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:10:13 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74f52f7948b98f731cc47a7da43a1a028f38396d447d93fa458cc7b1ee9ade0`  
		Last Modified: Thu, 05 Mar 2026 18:44:41 GMT  
		Size: 8.5 MB (8453572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50de1b9f6ee9b0bb47a9cb5e7877595782f60dc2d6c014088cfb72c4dca02106`  
		Last Modified: Thu, 05 Mar 2026 18:44:40 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8cd16e98d03b1081e8606a566c45e24d404e6738ce672011e2f5e3fe3b637b`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 17.5 MB (17472694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a548a65df6cf925e933ead68a3677913c3c9586d7115d161b6afd378cd8b1836`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 25.7 MB (25732665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09bdc4530b81e1aa74fe3d0322209932119b3cb64a72447d5442bd9c50cd4ed`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 10.0 MB (9974089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b96e65028eacc3700698877e774e4bfbca321b41420638481e753d07449225c`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faab51bb66faa3b0c0d737ebc09cfb486e94acbcdc20e883d8022102e4fc2fd`  
		Last Modified: Thu, 05 Mar 2026 18:44:43 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd02735b351188e3d18abc71b56816ddc7406e1d55c433166d34e8fd46aa5692`  
		Last Modified: Thu, 05 Mar 2026 18:44:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bd6c43d314f7ba1970375218d37bf189ee9e325f65b8a993a3846b8b081490`  
		Last Modified: Thu, 05 Mar 2026 19:10:23 GMT  
		Size: 7.2 MB (7213319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447b7408aabced1a21d26cecd53e54c14e75f0c7fa49a892e88b3faa8618791d`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 101.3 KB (101302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a4786ffc77dd17db34d4bd2edde2706bdb8bde49e2f5c532ffdb910ab16ee9`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce02e419a084f596f3e92c28731f67e0f113c3464b10ce77db5f722f7da9d1d`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 60.6 MB (60564110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf5b1f083f16666d8e3ef65369ed92093b78752eb5146941526e49b6d31965e`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720b8605e7f2e52dd9a65c8e463ab396a44abc68a0a689a3eda9a497503540fb`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f842673f5ac13d592cac6534e468f00a1d0270c7b8b686dff5ede372d952ad2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aec29e8d6f9254e8a5488aabb8ce917d657467f43e13af6528879dc1f2bfe02`

```dockerfile
```

-	Layers:
	-	`sha256:d59a3392ae448d26d8ed94f620ba9496be18d97cce5dc57e5943d287b049c800`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:7b90623a6a8d610e766d0dda84f20c7fbafeefe68a83ba01ecb4d6921b777b49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:aeab8c8ba5bd982ecd69b6f302e87c02eb66dd2fa3db5a8c5e81366e35960cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165252061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089ebb0bf68cbe13e627bb94ebca07973c936be52099f607c90ededbd35a2a90`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:46:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:46:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:46:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:46:28 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:46:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:46:28 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:46:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:46:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:46:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:46:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:46:30 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:10:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:10:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:10:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:10:30 GMT
CMD []
# Thu, 05 Mar 2026 19:51:35 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 05 Mar 2026 19:51:35 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 05 Mar 2026 19:51:35 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:51:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 05 Mar 2026 19:51:36 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 05 Mar 2026 19:51:36 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 05 Mar 2026 19:51:36 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f1c7a58cda4399b7be2fb8427c3b756917df1abb433e17a98888259aa70c83`  
		Last Modified: Thu, 05 Mar 2026 18:46:37 GMT  
		Size: 8.4 MB (8399691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba58ca1e42e5eeec21273f066c06e25afee78a5211c7d6deb38ba545b7d6240`  
		Last Modified: Thu, 05 Mar 2026 18:46:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f8c3243c30359f68ee8e1f96a24d246ca1357a82d8b30de9a33e9d282d93e1`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 18.9 MB (18919365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e9c4ffbcbf205284b573f955de57155f10b92234b491b2127720a57c90c1ce`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 28.5 MB (28516523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34962ed90623b311790e104f78a280cdc54a1ce559635328476148c6fc522888`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 11.0 MB (10953934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a9731c772a36b5ae18988bc0c1c69aff62cb86d597f2de367c5b330fb8d459`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a294ee3d24d1214f1944e57dadb6ef9c4b434a1a170e348838dafb16d31127`  
		Last Modified: Thu, 05 Mar 2026 18:46:39 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df03e33ed496925038509c0abcd9f087ab5ec4e4b917ed51730d71d63a87c91`  
		Last Modified: Thu, 05 Mar 2026 18:46:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fbd819f55b555293ac19eaaa17fd0ff75f9812f924da0a56610f334b1db8e6`  
		Last Modified: Thu, 05 Mar 2026 19:10:41 GMT  
		Size: 6.9 MB (6934736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524d6d9cccdc6fa4c04046756dada64359f4445d625ae2d4653714afad9044c`  
		Last Modified: Thu, 05 Mar 2026 19:10:40 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4da28e0bc44f1c47c50aab943753bc5626ab338c9dacd7cff96381acf13793`  
		Last Modified: Thu, 05 Mar 2026 19:10:41 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503f0e2071dd914a67c23aa1b570c3fccb863ebac670fa0d253ff15658adaf0a`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 66.8 MB (66766357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdcbaa55207a60126845f61a87ad8fbea9e87874674046ea2133cb2f3159d36`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bd5217468716f0f037bdb54d7c022dbf95c6896f29dc171a9677f86f621c25`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624e0d70ccddab2837c7579988be593d7d2c14e98ecc0951b4b4b1d0159ea2e8`  
		Last Modified: Thu, 05 Mar 2026 19:51:42 GMT  
		Size: 3.4 MB (3419929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed14991c62b9a9ef3cfc532d6532e4fd5343461fd35c558d71b52fe601b961`  
		Last Modified: Thu, 05 Mar 2026 19:51:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ac276d93a270a03f1cf58e6899d6a02fad81464e22001619436513cbe7e0e8`  
		Last Modified: Thu, 05 Mar 2026 19:51:42 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0161c5d6b742bdaefd9ac5d339340963166794c14b9e069af0f39fac4010597a`  
		Last Modified: Thu, 05 Mar 2026 19:51:42 GMT  
		Size: 17.4 MB (17377747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cf600d07eddbd5c5e7f2c80032ccc565bdd549c0193703940b5508312e509a`  
		Last Modified: Thu, 05 Mar 2026 19:51:43 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c3581ae9fc196cbf20a722387b0d4f4395cdf30ea836abc781891c9019939fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b9e467c6ab22b4a83c306b278852334102b54e6919ef4adfeaf8977ad9641b`

```dockerfile
```

-	Layers:
	-	`sha256:4b084f57f37ad05ae58136fd5d64bd79f05ca02c03ff4358cb8c35475b49240e`  
		Last Modified: Thu, 05 Mar 2026 19:51:41 GMT  
		Size: 30.6 KB (30588 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:363611f480e6222f4c95e0fe9b92d68e16add9b4f390fc53d681084c4b60caee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154825064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05963d5fac11223eb3f65b15aa06ef12c1a799eeb4b5bb56d79bd428436e0cd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:44:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:44:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:44:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:44:32 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:44:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:44:32 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:44:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:44:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:44:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:44:34 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:10:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:10:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:10:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:10:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:10:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:10:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:10:13 GMT
CMD []
# Thu, 05 Mar 2026 19:52:11 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 05 Mar 2026 19:52:11 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 05 Mar 2026 19:52:11 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:52:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 05 Mar 2026 19:52:12 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 05 Mar 2026 19:52:12 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 05 Mar 2026 19:52:12 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74f52f7948b98f731cc47a7da43a1a028f38396d447d93fa458cc7b1ee9ade0`  
		Last Modified: Thu, 05 Mar 2026 18:44:41 GMT  
		Size: 8.5 MB (8453572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50de1b9f6ee9b0bb47a9cb5e7877595782f60dc2d6c014088cfb72c4dca02106`  
		Last Modified: Thu, 05 Mar 2026 18:44:40 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8cd16e98d03b1081e8606a566c45e24d404e6738ce672011e2f5e3fe3b637b`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 17.5 MB (17472694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a548a65df6cf925e933ead68a3677913c3c9586d7115d161b6afd378cd8b1836`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 25.7 MB (25732665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09bdc4530b81e1aa74fe3d0322209932119b3cb64a72447d5442bd9c50cd4ed`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 10.0 MB (9974089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b96e65028eacc3700698877e774e4bfbca321b41420638481e753d07449225c`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faab51bb66faa3b0c0d737ebc09cfb486e94acbcdc20e883d8022102e4fc2fd`  
		Last Modified: Thu, 05 Mar 2026 18:44:43 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd02735b351188e3d18abc71b56816ddc7406e1d55c433166d34e8fd46aa5692`  
		Last Modified: Thu, 05 Mar 2026 18:44:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bd6c43d314f7ba1970375218d37bf189ee9e325f65b8a993a3846b8b081490`  
		Last Modified: Thu, 05 Mar 2026 19:10:23 GMT  
		Size: 7.2 MB (7213319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447b7408aabced1a21d26cecd53e54c14e75f0c7fa49a892e88b3faa8618791d`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 101.3 KB (101302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a4786ffc77dd17db34d4bd2edde2706bdb8bde49e2f5c532ffdb910ab16ee9`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce02e419a084f596f3e92c28731f67e0f113c3464b10ce77db5f722f7da9d1d`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 60.6 MB (60564110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf5b1f083f16666d8e3ef65369ed92093b78752eb5146941526e49b6d31965e`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720b8605e7f2e52dd9a65c8e463ab396a44abc68a0a689a3eda9a497503540fb`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113a99610f0313cefac114163c823cc19536cc5ad728c999ce1c42a08df7b73e`  
		Last Modified: Thu, 05 Mar 2026 19:52:19 GMT  
		Size: 3.4 MB (3394381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f83f706c62205d1a7b78b43438268f91f5a1c97ce0aa6d9e895c6ccb93e6aaa`  
		Last Modified: Thu, 05 Mar 2026 19:52:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8ea4b65def4cea71f744e7c03f2bd0f14403430efba1dde697830900fd9220`  
		Last Modified: Thu, 05 Mar 2026 19:52:19 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d663f5f609d1ca281ed28345736bdf222b960707ccb29edd7d2fca31fffcce`  
		Last Modified: Thu, 05 Mar 2026 19:52:19 GMT  
		Size: 17.7 MB (17712346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fc8e3e13278240d699ba378e763c538e98fc43342e3c86b0625b503863f3f0`  
		Last Modified: Thu, 05 Mar 2026 19:52:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:419ad745bdc70ba4c204674efbc833c2b1eaff3596fbdf95c23b80444589037d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8693634da1b98934154ee830afbd8beb888c8ede561915c13c94c94ca449c750`

```dockerfile
```

-	Layers:
	-	`sha256:df3b03f6dd4be8fab2827638b57709b438a0bab274edac98ada56265237fec2c`  
		Last Modified: Thu, 05 Mar 2026 19:52:18 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:fdd48859b2b14b2fa4af458fcea153cfd95e8ce7429e66286229f28b47e507b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:42419a818a06c8b0bdb32d28efe864c1965f849d4d58dac6450fb35578530636
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2142463243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095982a564f926ffd785368388022d0f792a5f393f83c25b2b334b3f0ee3c25f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Wed, 25 Mar 2026 18:28:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Mar 2026 18:29:47 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Mar 2026 18:29:48 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.1.zip
# Wed, 25 Mar 2026 18:30:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Mar 2026 18:30:11 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:30:12 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.windows-amd64.exe
# Wed, 25 Mar 2026 18:30:13 GMT
ENV DOCKER_BUILDX_SHA256=47d76e47acf3c7611dd594c4b0909fec680ae6406b6fa775f6077b195837e2b9
# Wed, 25 Mar 2026 18:30:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Mar 2026 18:30:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:30:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Wed, 25 Mar 2026 18:30:37 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Wed, 25 Mar 2026 18:30:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c48ff63fd51e54c1621e1ef191ba1ffb5babb91295c52763e73038877ddbcc0`  
		Last Modified: Wed, 25 Mar 2026 18:30:56 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05646e87bcc7eebcf75f1a96ca80aa255bd6868601cdf94768601c8078d9b4b7`  
		Last Modified: Wed, 25 Mar 2026 18:30:55 GMT  
		Size: 374.0 KB (373997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edba92fa22a5c1bc563c18f651db43bfdc9c0720c21fff8d046d759875e121d1`  
		Last Modified: Wed, 25 Mar 2026 18:30:54 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b934d13e109edc08e9a08ca989659aded111b61867e75aa39cc626586e14b6d`  
		Last Modified: Wed, 25 Mar 2026 18:30:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff304ba5506cff7b400064688c74084a2ff60a244b484160e1be812e7672e3d`  
		Last Modified: Wed, 25 Mar 2026 18:30:56 GMT  
		Size: 19.6 MB (19594910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47622b1e857ba4fe582334af32ea59c3b58783ab368030f1d2259ae216996aaa`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a676a9fc9cb7650a5a61aad602e864237a2410b300b3babac5f0cfb4c9f31bf9`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d698051d32bbd456b5de7801253c16270739faf8954ce78f45f3a7e95830067`  
		Last Modified: Wed, 25 Mar 2026 18:30:52 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b8f6f29800e2912ff8cd1d9696f47141cb71560b98c73b71157c6b39d77665`  
		Last Modified: Wed, 25 Mar 2026 18:31:04 GMT  
		Size: 29.6 MB (29639971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbee4f4914616df04e2f56d66e020a4ca506723690da654928872871a3d1130`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36549e61114f7f53657411a2bc956fd69c15ae2f08beb6f977143978b7447c7a`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111317c19214d92002469ac71ea269b2b838ae7163f090cf6796b17aeccea76d`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee1dd44d7e561101a0c094be20961ded0b2b663201441b16b06bbace8b589ab`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 11.6 MB (11646539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:9504c71617f036da76201851ee9ad86ea91a1f572837a6e9e49023ace0612bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull docker@sha256:7218b6c6fbe208207908f94f1ed696b4bd01423d2c443586c5f65031c5e0e93e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2043597626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378ba248bb85f2c6fe57c779e2da6f4c4498116174b27197870a8f9ee1d337d4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 21:55:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Mar 2026 21:55:45 GMT
ENV DOCKER_VERSION=29.3.0
# Tue, 10 Mar 2026 21:55:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.0.zip
# Tue, 10 Mar 2026 21:56:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 21:56:04 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Tue, 10 Mar 2026 21:56:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.windows-amd64.exe
# Tue, 10 Mar 2026 21:56:05 GMT
ENV DOCKER_BUILDX_SHA256=47d76e47acf3c7611dd594c4b0909fec680ae6406b6fa775f6077b195837e2b9
# Tue, 10 Mar 2026 21:56:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 21:56:22 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Tue, 10 Mar 2026 21:56:23 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-windows-x86_64.exe
# Tue, 10 Mar 2026 21:56:24 GMT
ENV DOCKER_COMPOSE_SHA256=ee84e42b93c501cb0aa2caa84d76b5f30ca6fb92f070e289fc37be7332c5822a
# Tue, 10 Mar 2026 21:56:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17a66011dcb9c38eedc922e2d718b0cff4e70ce31e167daaa8dfee148d9c195`  
		Last Modified: Tue, 10 Mar 2026 21:56:42 GMT  
		Size: 486.8 KB (486826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f159d4d5d7e56333bfd6e2e7b16344a0e872adf0b93acebefa53c4247fbc9396`  
		Last Modified: Tue, 10 Mar 2026 21:56:41 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccb66eda533f994dbbb9ff81d57c851758147e1a0630eea05e16a0716ff87ad`  
		Last Modified: Tue, 10 Mar 2026 21:56:41 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0cd965bfbb200c967e8ee796997bdd4cdb587a833c56d7a49317544aab06cc6`  
		Last Modified: Tue, 10 Mar 2026 21:56:44 GMT  
		Size: 19.6 MB (19571347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edc8f49358e8d56eb2e56b6ac13be2048a3a016717f24c53f49dc1fc9bde0f7`  
		Last Modified: Tue, 10 Mar 2026 21:56:40 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8ac62b592ebb8bae48e8d31dadb875c021f30a09defc65097fb06249ef2e6a`  
		Last Modified: Tue, 10 Mar 2026 21:56:40 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554c2edbde552817f409d72b85a719f3c34ddc1651c3a110b24b1d3aa4570cc3`  
		Last Modified: Tue, 10 Mar 2026 21:56:40 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90bad317fa3a54913b9758ee2e45f94e02a64cc9e4e0c693589b644de126d33`  
		Last Modified: Tue, 10 Mar 2026 21:56:46 GMT  
		Size: 29.6 MB (29623149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dbad83ed52d0db02d4f30b2e0a88e026dd56c68a61c0a3a99f4d64bc5b14d1`  
		Last Modified: Tue, 10 Mar 2026 21:56:38 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d05240889a0e152fce0f29182840145e329281d7d52b384e0251bb1a9abfa8`  
		Last Modified: Tue, 10 Mar 2026 21:56:38 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ac67609452a0105c993416f50fb486c0260df99ed76d920c31b1ab2aa344ab`  
		Last Modified: Tue, 10 Mar 2026 21:56:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3aff282c60575fe0964ee93b76dd77692c3ed1f6cbeeb91ecb807cfa30421b8`  
		Last Modified: Tue, 10 Mar 2026 21:56:40 GMT  
		Size: 11.6 MB (11623130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:fdd48859b2b14b2fa4af458fcea153cfd95e8ce7429e66286229f28b47e507b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:42419a818a06c8b0bdb32d28efe864c1965f849d4d58dac6450fb35578530636
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2142463243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095982a564f926ffd785368388022d0f792a5f393f83c25b2b334b3f0ee3c25f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Wed, 25 Mar 2026 18:28:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Mar 2026 18:29:47 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Mar 2026 18:29:48 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.1.zip
# Wed, 25 Mar 2026 18:30:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Mar 2026 18:30:11 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:30:12 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.windows-amd64.exe
# Wed, 25 Mar 2026 18:30:13 GMT
ENV DOCKER_BUILDX_SHA256=47d76e47acf3c7611dd594c4b0909fec680ae6406b6fa775f6077b195837e2b9
# Wed, 25 Mar 2026 18:30:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Mar 2026 18:30:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:30:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Wed, 25 Mar 2026 18:30:37 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Wed, 25 Mar 2026 18:30:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c48ff63fd51e54c1621e1ef191ba1ffb5babb91295c52763e73038877ddbcc0`  
		Last Modified: Wed, 25 Mar 2026 18:30:56 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05646e87bcc7eebcf75f1a96ca80aa255bd6868601cdf94768601c8078d9b4b7`  
		Last Modified: Wed, 25 Mar 2026 18:30:55 GMT  
		Size: 374.0 KB (373997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edba92fa22a5c1bc563c18f651db43bfdc9c0720c21fff8d046d759875e121d1`  
		Last Modified: Wed, 25 Mar 2026 18:30:54 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b934d13e109edc08e9a08ca989659aded111b61867e75aa39cc626586e14b6d`  
		Last Modified: Wed, 25 Mar 2026 18:30:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff304ba5506cff7b400064688c74084a2ff60a244b484160e1be812e7672e3d`  
		Last Modified: Wed, 25 Mar 2026 18:30:56 GMT  
		Size: 19.6 MB (19594910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47622b1e857ba4fe582334af32ea59c3b58783ab368030f1d2259ae216996aaa`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a676a9fc9cb7650a5a61aad602e864237a2410b300b3babac5f0cfb4c9f31bf9`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d698051d32bbd456b5de7801253c16270739faf8954ce78f45f3a7e95830067`  
		Last Modified: Wed, 25 Mar 2026 18:30:52 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b8f6f29800e2912ff8cd1d9696f47141cb71560b98c73b71157c6b39d77665`  
		Last Modified: Wed, 25 Mar 2026 18:31:04 GMT  
		Size: 29.6 MB (29639971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbee4f4914616df04e2f56d66e020a4ca506723690da654928872871a3d1130`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36549e61114f7f53657411a2bc956fd69c15ae2f08beb6f977143978b7447c7a`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111317c19214d92002469ac71ea269b2b838ae7163f090cf6796b17aeccea76d`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee1dd44d7e561101a0c094be20961ded0b2b663201441b16b06bbace8b589ab`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 11.6 MB (11646539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.3`

```console
$ docker pull docker@sha256:1ba18449911d01f477a3fc104123c85d677addc60701b14b3fcb5381f9c4a537
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

### `docker:29.3` - linux; amd64

```console
$ docker pull docker@sha256:e60900b4413a183173b0c12a7c34bfa7ba511fd074147a1b7974ebb296a0050b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144453044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5b3ee3882d4d0af9fc139d2545bf1d17e251c849e98b98da2fe418431e2ad8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:46:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:46:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:46:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:46:28 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:46:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:46:28 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:46:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:46:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:46:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:46:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:46:30 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:10:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:10:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:10:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:10:30 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f1c7a58cda4399b7be2fb8427c3b756917df1abb433e17a98888259aa70c83`  
		Last Modified: Thu, 05 Mar 2026 18:46:37 GMT  
		Size: 8.4 MB (8399691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba58ca1e42e5eeec21273f066c06e25afee78a5211c7d6deb38ba545b7d6240`  
		Last Modified: Thu, 05 Mar 2026 18:46:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f8c3243c30359f68ee8e1f96a24d246ca1357a82d8b30de9a33e9d282d93e1`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 18.9 MB (18919365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e9c4ffbcbf205284b573f955de57155f10b92234b491b2127720a57c90c1ce`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 28.5 MB (28516523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34962ed90623b311790e104f78a280cdc54a1ce559635328476148c6fc522888`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 11.0 MB (10953934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a9731c772a36b5ae18988bc0c1c69aff62cb86d597f2de367c5b330fb8d459`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a294ee3d24d1214f1944e57dadb6ef9c4b434a1a170e348838dafb16d31127`  
		Last Modified: Thu, 05 Mar 2026 18:46:39 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df03e33ed496925038509c0abcd9f087ab5ec4e4b917ed51730d71d63a87c91`  
		Last Modified: Thu, 05 Mar 2026 18:46:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fbd819f55b555293ac19eaaa17fd0ff75f9812f924da0a56610f334b1db8e6`  
		Last Modified: Thu, 05 Mar 2026 19:10:41 GMT  
		Size: 6.9 MB (6934736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524d6d9cccdc6fa4c04046756dada64359f4445d625ae2d4653714afad9044c`  
		Last Modified: Thu, 05 Mar 2026 19:10:40 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4da28e0bc44f1c47c50aab943753bc5626ab338c9dacd7cff96381acf13793`  
		Last Modified: Thu, 05 Mar 2026 19:10:41 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503f0e2071dd914a67c23aa1b570c3fccb863ebac670fa0d253ff15658adaf0a`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 66.8 MB (66766357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdcbaa55207a60126845f61a87ad8fbea9e87874674046ea2133cb2f3159d36`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bd5217468716f0f037bdb54d7c022dbf95c6896f29dc171a9677f86f621c25`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3` - unknown; unknown

```console
$ docker pull docker@sha256:51f66381d79e85e83914402852c9997eddc9b6c3b280e0aa86c37f2a4ba27738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8ef8f35ce741ad2c83d3a11a6b0eabe3616860c0a9fd2deba0d9b603978bf0`

```dockerfile
```

-	Layers:
	-	`sha256:9de809ee0c1e4804fb0ce3ce24f183e971a8f1020e5d25d1eba9202ecfb23554`  
		Last Modified: Thu, 05 Mar 2026 19:10:40 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.3` - linux; arm variant v6

```console
$ docker pull docker@sha256:921ed9ba3b685e60ee0cdcd138b4aa718d396a4e4e1418de3348b766229448c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136262850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739701c78bbbb4755e7b5694d8e2032e7edaca1f5ab49ddc7c1bcef1e289abbe`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:45:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:45:36 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:45:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:45:39 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:45:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:45:39 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:45:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:45:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:45:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:45:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:45:43 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:08:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:08:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:08:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:08:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:08:49 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:08:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:08:49 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0593a5009b5f1611e29afa031add0caa8e17436567b91fa0cd2b29e51d22c89`  
		Last Modified: Thu, 05 Mar 2026 18:45:50 GMT  
		Size: 8.3 MB (8300931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aae9fbc3eb9720394677e4ecd6aab19d036b3e73b352fb74b67d6b3a2fc9fa6`  
		Last Modified: Thu, 05 Mar 2026 18:45:50 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d66dff73ca29a47e9b6b4c6c761a4d7aa8867dca97bc28872f55bf9f47e2c6`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 17.7 MB (17698879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2808c066fd3febfd5f5674816180176477b47da3158ad376e658eb6d8136fab1`  
		Last Modified: Thu, 05 Mar 2026 18:45:51 GMT  
		Size: 26.8 MB (26774787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663b0b4076c27408b2184d77a831c36817e8a8d8d4897cb92fce9cdd0165335a`  
		Last Modified: Thu, 05 Mar 2026 18:45:51 GMT  
		Size: 10.4 MB (10385429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3615b056b4ef975abfd3ae24796393abcb6cd5c819f1c8a6e68c1488f641f1a`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32f9cb2f283cf611fe753cefc9ac89c970b2a82e793b029047ec9a74dd88da4`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5dc68331a182d6047cc64dc01811876321654c40481e65df941bf21d1129ff`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281309e002e2014f85aa6e60f8f56d3a46cd826258710ea23f02ebd55fa56d86`  
		Last Modified: Thu, 05 Mar 2026 19:08:59 GMT  
		Size: 7.3 MB (7271697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d5638366f0629a45399b2da5bc12e7eaec99cd43a172c0e00a061cbad07fd9`  
		Last Modified: Thu, 05 Mar 2026 19:08:58 GMT  
		Size: 91.8 KB (91788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db525e8a11303b587a4637ce4f7e8cf2e27b87515229e415c66b907d6857c14`  
		Last Modified: Thu, 05 Mar 2026 19:08:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b41beca4d05ad9f4f8a0af06864a9b0bd92eb236aae78aec36d96eee3e972e7`  
		Last Modified: Thu, 05 Mar 2026 19:09:00 GMT  
		Size: 62.2 MB (62161362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c988857a21079067d802211bb65b801edbebcc1e6e21bd8e6e7eea98dc58fc`  
		Last Modified: Thu, 05 Mar 2026 19:09:00 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0de727742fa3feb2ba852cdaa770c212967433c39bb41ebfe1865a9ffcc78e`  
		Last Modified: Thu, 05 Mar 2026 19:09:00 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3` - unknown; unknown

```console
$ docker pull docker@sha256:01e39cec6c99783d318713cb96e9d665690e384f821039d02ecc3d40d501c51d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c18a85619e7433b908f936509e5dbd40bb98ace79929f60a844a1db3c93374`

```dockerfile
```

-	Layers:
	-	`sha256:d37d617810772a2c79e6330f2dbaf0e418ffcc3f2db333b8443afe97f45e219b`  
		Last Modified: Thu, 05 Mar 2026 19:08:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.3` - linux; arm variant v7

```console
$ docker pull docker@sha256:74ea5cdbe2fe4518d73e3ac0241167a38c7616c3dd6be011cf48fc0a61189c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134355560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9d940d504e1f821c76a9e400c405dfbc51b3d58990d7abaae29dd773c08694`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:46:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:46:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:46:32 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:46:36 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:46:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:46:36 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:46:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:46:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:46:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:46:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:46:40 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:09:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:09:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:09:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:09:20 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:09:20 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:09:20 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:09:20 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95152b95c4ccfeb5059ced14a96c4f1c17872baa3e875c18056cb5bed1b56676`  
		Last Modified: Thu, 05 Mar 2026 18:46:46 GMT  
		Size: 7.6 MB (7597774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d532e57eb4774540148a1cccd311fc10645e4dc68e8512d6b4f5a07d77498e82`  
		Last Modified: Thu, 05 Mar 2026 18:46:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64983bc952c232855d431fc0da6e3080f4c4c64fc0dce721c1086cc916d3037`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 17.7 MB (17691333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0552f021a975b88c2f33fc3057737b716d29921dcf12fff1a7bd017272ee52bf`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 26.8 MB (26754433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe274cdce52e0d95eda23b7407fdd0cd8a861a2014d8a240bda6be387b22c74`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 10.4 MB (10369783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28feee09383ef1673e7a0cec5e45cf0ad41f8b64208682ad535da48f8de7e08e`  
		Last Modified: Thu, 05 Mar 2026 18:46:48 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c266b2e92e5c06c3362ac89279eac9742220da712ded40590f3312de938eb16a`  
		Last Modified: Thu, 05 Mar 2026 18:46:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b204129a9de694faa70c2c825548fbe88d190e24ecc2d949a3ea099c0ac40d3`  
		Last Modified: Thu, 05 Mar 2026 18:46:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6011a406c6080a98a187e060555bd77450686dc8a0a3a1bd21a8b635e7a7c7c5`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 6.6 MB (6573025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63255cd848e2b7900e0177b225137079a3c0e9bde16e58d50a40edba81e6b028`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 88.2 KB (88150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3758bf28f38de089029226cd958aeeb1d75194761390a5bd605206ae3d4092e3`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbec48042bff8bd1621f0f9cd3d2ec81bc03fdba86235b7e6586dec177d82907`  
		Last Modified: Thu, 05 Mar 2026 19:09:32 GMT  
		Size: 62.0 MB (61991183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f8030e199452b1b297f3a4acc28ce81ecd590b3b41343eb4dbb260d0a03684`  
		Last Modified: Thu, 05 Mar 2026 19:09:31 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a7939d77fae184c61e7cbceee2129945aff07b2c8ba46170605cd266cdee9f`  
		Last Modified: Thu, 05 Mar 2026 19:09:31 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3` - unknown; unknown

```console
$ docker pull docker@sha256:0d74abb912009d5524b2bc08d235dd65785a6a9c105843b2d5f2e38d9740c01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e7a73ef832c7e6998b93ef231c73a0f5a4b733dd27635018b7ccc4808f8859`

```dockerfile
```

-	Layers:
	-	`sha256:dfe982715ef650b1926988aa185ecef3d257673538c7392c6271f6a59a023df3`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 34.7 KB (34721 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.3` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1d1d67ba557d1ccedcd46d05ba832276e65260a518c240b087c71849cd6cbce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133716998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2468f972a259c78d9053fa37f4ca40d54c8071086fecff98d4e0f4829c120c36`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:44:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:44:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:44:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:44:32 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:44:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:44:32 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:44:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:44:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:44:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:44:34 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:10:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:10:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:10:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:10:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:10:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:10:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:10:13 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74f52f7948b98f731cc47a7da43a1a028f38396d447d93fa458cc7b1ee9ade0`  
		Last Modified: Thu, 05 Mar 2026 18:44:41 GMT  
		Size: 8.5 MB (8453572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50de1b9f6ee9b0bb47a9cb5e7877595782f60dc2d6c014088cfb72c4dca02106`  
		Last Modified: Thu, 05 Mar 2026 18:44:40 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8cd16e98d03b1081e8606a566c45e24d404e6738ce672011e2f5e3fe3b637b`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 17.5 MB (17472694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a548a65df6cf925e933ead68a3677913c3c9586d7115d161b6afd378cd8b1836`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 25.7 MB (25732665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09bdc4530b81e1aa74fe3d0322209932119b3cb64a72447d5442bd9c50cd4ed`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 10.0 MB (9974089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b96e65028eacc3700698877e774e4bfbca321b41420638481e753d07449225c`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faab51bb66faa3b0c0d737ebc09cfb486e94acbcdc20e883d8022102e4fc2fd`  
		Last Modified: Thu, 05 Mar 2026 18:44:43 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd02735b351188e3d18abc71b56816ddc7406e1d55c433166d34e8fd46aa5692`  
		Last Modified: Thu, 05 Mar 2026 18:44:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bd6c43d314f7ba1970375218d37bf189ee9e325f65b8a993a3846b8b081490`  
		Last Modified: Thu, 05 Mar 2026 19:10:23 GMT  
		Size: 7.2 MB (7213319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447b7408aabced1a21d26cecd53e54c14e75f0c7fa49a892e88b3faa8618791d`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 101.3 KB (101302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a4786ffc77dd17db34d4bd2edde2706bdb8bde49e2f5c532ffdb910ab16ee9`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce02e419a084f596f3e92c28731f67e0f113c3464b10ce77db5f722f7da9d1d`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 60.6 MB (60564110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf5b1f083f16666d8e3ef65369ed92093b78752eb5146941526e49b6d31965e`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720b8605e7f2e52dd9a65c8e463ab396a44abc68a0a689a3eda9a497503540fb`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3` - unknown; unknown

```console
$ docker pull docker@sha256:f842673f5ac13d592cac6534e468f00a1d0270c7b8b686dff5ede372d952ad2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aec29e8d6f9254e8a5488aabb8ce917d657467f43e13af6528879dc1f2bfe02`

```dockerfile
```

-	Layers:
	-	`sha256:d59a3392ae448d26d8ed94f620ba9496be18d97cce5dc57e5943d287b049c800`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.3-cli`

```console
$ docker pull docker@sha256:70303ed0d265aee7bf4be0ddffe20b0b6e4f69ffa125e2a20cbb3718b99688db
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

### `docker:29.3-cli` - linux; amd64

```console
$ docker pull docker@sha256:3459e4b0c6702acfdc23b2a48e4e8bdcfc51ef96bac2d0af3ea3edac4044192c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70660468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f34f75af30162c2d6b68fa089dac03a627ba7303e9758184d9d26dacb913ca7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:31:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:31:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:31:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:31:34 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:31:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:31:34 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:31:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:31:36 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:31:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:31:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:31:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f783f43bd0c479eca4a605cd057214fd4d32195579fd3858ea619042787418`  
		Last Modified: Wed, 25 Mar 2026 18:31:45 GMT  
		Size: 8.4 MB (8399805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dc00f58fe8675ce338442f1f3924e7575b889140324f529e6f7b7b552e6a8b`  
		Last Modified: Wed, 25 Mar 2026 18:31:44 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed7cc89d7e24509b5ecc2a876b68c336cc533fccd578553f96c40bd5977acaa`  
		Last Modified: Wed, 25 Mar 2026 18:31:45 GMT  
		Size: 18.9 MB (18925059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59f566876aae23a8d4ded9382841f58305b92c7453a48044734ac35241c5e5d`  
		Last Modified: Wed, 25 Mar 2026 18:31:46 GMT  
		Size: 28.5 MB (28516527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f27ff511c85a43e9a75a388dbd32088a24592f41c6987999fbcf0165672071d`  
		Last Modified: Wed, 25 Mar 2026 18:31:46 GMT  
		Size: 11.0 MB (10955101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac4601d8546b2a6477f79a9bff1a05ec9add30bf96dc48fcd27457170f39b07`  
		Last Modified: Wed, 25 Mar 2026 18:31:46 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b922537b6a3dd95fc487130c0ca4896eb541d70d4a9438dd39590ccb7b65943`  
		Last Modified: Wed, 25 Mar 2026 18:31:47 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62fa46a186b2dc7d1a25e70eb2c2653aa0431485adb908a7cf943d28c49cdf1`  
		Last Modified: Wed, 25 Mar 2026 18:31:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:827d9483e2a64b8c44523708ca54adaeec69e1ee40b1f275bb657e51828404f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587b7070e426c0932cb45f162874ea0917cc386aa52282a4e864f0aceeac21c5`

```dockerfile
```

-	Layers:
	-	`sha256:9c77ec231f2b5c72293c670da21cfc5dc7c509522268cc74c92f9098859cef6a`  
		Last Modified: Wed, 25 Mar 2026 18:31:44 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.3-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:ab088b3f5efe676c33f3339eeefbb2228b5e4b45cc6189a7ee8d717f98d47796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66741259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6299617540122589abca8da49bf316efc08ef3e0e4632b70f20e47121c8e7a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:20:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:20:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:20:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:20:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:20:55 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:20:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:20:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:20:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7327f5bd7b20a7c0c384c9bed111c54ed041e23650f2789ce160520bd54e7d64`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 8.3 MB (8300847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad441b201d110caa6bbae91773542ed3038e833916ab8fdbdee2efdd096951d`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a9b3570b577d5bd7b5702ea3b038bd6d6736da52c7e4cfa9204254b3ef6889`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 17.7 MB (17704832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687acedd268ebaa81d467b79f662cb296f999d5edc939573fc235718f10b3d5`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 26.8 MB (26774785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6738b4fa70496e709329c400187d16a1e6dcd9323aa0597219b36caeffbf73`  
		Last Modified: Wed, 25 Mar 2026 18:21:12 GMT  
		Size: 10.4 MB (10388825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0425cd14663ea2989a267ae635da01c39877aac17e1b4a26049c6e8584e9b7`  
		Last Modified: Wed, 25 Mar 2026 18:21:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7154483d9dd47aca8dda22548f6ac6381d6f297c1afcbda1c72dba31279d96f7`  
		Last Modified: Wed, 25 Mar 2026 18:21:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbfd7d41a6aa1e531936a17e36405a287262345307d1769bbf5e514f1f4955a`  
		Last Modified: Wed, 25 Mar 2026 18:21:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4a04a0fb0422d24efcd71966c2ec778971b5a49ba8fb1934681a3c061a4f7bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8881255256c5bafe467ec0dffa5cdafa965971effe17aab0e66a451dbac7b198`

```dockerfile
```

-	Layers:
	-	`sha256:e6eb00c7bd1756168105295aa8a9f0546960e7bf78727f47d669e70e1096cc65`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.3-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:b4cf24daf2e960893a39d2f0a13a0b2b889e626725f5704295ff3c7a80e2ce56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65702900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e770b04316507e289fdbe463af8dd53873a490a5215e9664d3c38a2387b9b0bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:20:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:20:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:20:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:20:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:20:55 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:20:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:20:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:20:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9a25e5bfb326bc75a71b460d0544e0abe70b0c6c1498521b7fd245df901627`  
		Last Modified: Wed, 25 Mar 2026 18:21:05 GMT  
		Size: 7.6 MB (7597792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bd4d27cb3827cca3206705328c83ee80e164a78dc2aa97099d480bb1ded087`  
		Last Modified: Wed, 25 Mar 2026 18:21:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57192b9959272e69a74f1600a28d23141f96a9856eb275612e66d96aed4cb23`  
		Last Modified: Wed, 25 Mar 2026 18:21:05 GMT  
		Size: 17.7 MB (17694926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7afb84b0bb6525824e7b41a3eb6ca04fbd8a378336dace66c201e7f0a9fdfd`  
		Last Modified: Wed, 25 Mar 2026 18:21:06 GMT  
		Size: 26.8 MB (26754421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34cbd0d9bfc6a2fbae47c23f0d1c832eaf8aacf91c370cd7d44df319b6dcf32`  
		Last Modified: Wed, 25 Mar 2026 18:21:06 GMT  
		Size: 10.4 MB (10371888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92b6554d10f78775d85c869fd50243ef34c2f7fb06170e9bfd0f6cb1d8c722f`  
		Last Modified: Wed, 25 Mar 2026 18:21:06 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a550d751a72e95d6b192c5aa49bc54135cd12eaac778e2494033d746481e4e`  
		Last Modified: Wed, 25 Mar 2026 18:21:07 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbfd7d41a6aa1e531936a17e36405a287262345307d1769bbf5e514f1f4955a`  
		Last Modified: Wed, 25 Mar 2026 18:21:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:b36c22ea07bd32cf40c3233fe677b6cfd0b141b3c63f391124eed2843c5fe9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17c08feca64baed542d11807ef5bdc316ef9f6816d6d0e695109048771339bc`

```dockerfile
```

-	Layers:
	-	`sha256:d9a26fdeeceae1cd37f2b33208c330bcbaaa632331e7950fad92cdb05c62b6ea`  
		Last Modified: Wed, 25 Mar 2026 18:21:05 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.3-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:56cff04ad8dcf376a96423ddf5515c8bdcd171e683265335da57f17aa020ad1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65845112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee59cb9a3f85ae950ab85efdd43672abd503dbe5adcd1a55b95687f24e990ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:28:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:28:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:28:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:28:13 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:28:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:28:13 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:28:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:28:14 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:28:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:28:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:28:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7edc56943efc5fd8ceeeec0973e7862a22eef8479f31e4506aaa7683706598`  
		Last Modified: Wed, 25 Mar 2026 18:28:21 GMT  
		Size: 8.5 MB (8453635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d7bdfa7dc871c3af6f5b34ef1ef53c930b2fde5801879b794f1849da1dc4d`  
		Last Modified: Wed, 25 Mar 2026 18:28:20 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c366b69bd090a1557acbb6f1ebdab176751b61ca7e1c82af675fd5dd30436a`  
		Last Modified: Wed, 25 Mar 2026 18:28:21 GMT  
		Size: 17.5 MB (17476961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b74c99f62156a67a1a2f1edfa046c0c13825a6cdef351e68e41cbbffd8badb`  
		Last Modified: Wed, 25 Mar 2026 18:28:22 GMT  
		Size: 25.7 MB (25732670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fed48b65e655b617bf78f3b0c6df9994322561de4c1c4a706e621ec83f8fb84`  
		Last Modified: Wed, 25 Mar 2026 18:28:22 GMT  
		Size: 10.0 MB (9982606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318a3b2c176f6893caa80c95a652634492e38503c58e091a916b6d9c341a0648`  
		Last Modified: Wed, 25 Mar 2026 18:28:23 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c910ec30db0949d800f54bb9c1b3c4e2af20695bf5b14f43f4f9be42a0ecb2c`  
		Last Modified: Wed, 25 Mar 2026 18:28:23 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd0d057ad753e2ef837845dd9504265e602e0802dceee1b0083e05f00291b8c`  
		Last Modified: Wed, 25 Mar 2026 18:28:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a3331dd737a9d4ad382fff64040bbad2660884a99286e44af8338a00851aec68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ed74d502ab8399d1e1a43c9de66bf070e1741c40c8a187c876aa031385bd08`

```dockerfile
```

-	Layers:
	-	`sha256:5de0f8302079e7f4909158e85e3fcabf6c532e1b84c2c25003b4bf3343ea0e94`  
		Last Modified: Wed, 25 Mar 2026 18:28:21 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.3-dind`

```console
$ docker pull docker@sha256:1ba18449911d01f477a3fc104123c85d677addc60701b14b3fcb5381f9c4a537
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

### `docker:29.3-dind` - linux; amd64

```console
$ docker pull docker@sha256:e60900b4413a183173b0c12a7c34bfa7ba511fd074147a1b7974ebb296a0050b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144453044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5b3ee3882d4d0af9fc139d2545bf1d17e251c849e98b98da2fe418431e2ad8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:46:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:46:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:46:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:46:28 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:46:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:46:28 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:46:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:46:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:46:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:46:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:46:30 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:10:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:10:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:10:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:10:30 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f1c7a58cda4399b7be2fb8427c3b756917df1abb433e17a98888259aa70c83`  
		Last Modified: Thu, 05 Mar 2026 18:46:37 GMT  
		Size: 8.4 MB (8399691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba58ca1e42e5eeec21273f066c06e25afee78a5211c7d6deb38ba545b7d6240`  
		Last Modified: Thu, 05 Mar 2026 18:46:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f8c3243c30359f68ee8e1f96a24d246ca1357a82d8b30de9a33e9d282d93e1`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 18.9 MB (18919365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e9c4ffbcbf205284b573f955de57155f10b92234b491b2127720a57c90c1ce`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 28.5 MB (28516523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34962ed90623b311790e104f78a280cdc54a1ce559635328476148c6fc522888`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 11.0 MB (10953934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a9731c772a36b5ae18988bc0c1c69aff62cb86d597f2de367c5b330fb8d459`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a294ee3d24d1214f1944e57dadb6ef9c4b434a1a170e348838dafb16d31127`  
		Last Modified: Thu, 05 Mar 2026 18:46:39 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df03e33ed496925038509c0abcd9f087ab5ec4e4b917ed51730d71d63a87c91`  
		Last Modified: Thu, 05 Mar 2026 18:46:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fbd819f55b555293ac19eaaa17fd0ff75f9812f924da0a56610f334b1db8e6`  
		Last Modified: Thu, 05 Mar 2026 19:10:41 GMT  
		Size: 6.9 MB (6934736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524d6d9cccdc6fa4c04046756dada64359f4445d625ae2d4653714afad9044c`  
		Last Modified: Thu, 05 Mar 2026 19:10:40 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4da28e0bc44f1c47c50aab943753bc5626ab338c9dacd7cff96381acf13793`  
		Last Modified: Thu, 05 Mar 2026 19:10:41 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503f0e2071dd914a67c23aa1b570c3fccb863ebac670fa0d253ff15658adaf0a`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 66.8 MB (66766357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdcbaa55207a60126845f61a87ad8fbea9e87874674046ea2133cb2f3159d36`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bd5217468716f0f037bdb54d7c022dbf95c6896f29dc171a9677f86f621c25`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:51f66381d79e85e83914402852c9997eddc9b6c3b280e0aa86c37f2a4ba27738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8ef8f35ce741ad2c83d3a11a6b0eabe3616860c0a9fd2deba0d9b603978bf0`

```dockerfile
```

-	Layers:
	-	`sha256:9de809ee0c1e4804fb0ce3ce24f183e971a8f1020e5d25d1eba9202ecfb23554`  
		Last Modified: Thu, 05 Mar 2026 19:10:40 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.3-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:921ed9ba3b685e60ee0cdcd138b4aa718d396a4e4e1418de3348b766229448c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136262850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739701c78bbbb4755e7b5694d8e2032e7edaca1f5ab49ddc7c1bcef1e289abbe`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:45:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:45:36 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:45:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:45:39 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:45:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:45:39 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:45:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:45:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:45:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:45:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:45:43 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:08:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:08:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:08:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:08:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:08:49 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:08:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:08:49 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0593a5009b5f1611e29afa031add0caa8e17436567b91fa0cd2b29e51d22c89`  
		Last Modified: Thu, 05 Mar 2026 18:45:50 GMT  
		Size: 8.3 MB (8300931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aae9fbc3eb9720394677e4ecd6aab19d036b3e73b352fb74b67d6b3a2fc9fa6`  
		Last Modified: Thu, 05 Mar 2026 18:45:50 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d66dff73ca29a47e9b6b4c6c761a4d7aa8867dca97bc28872f55bf9f47e2c6`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 17.7 MB (17698879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2808c066fd3febfd5f5674816180176477b47da3158ad376e658eb6d8136fab1`  
		Last Modified: Thu, 05 Mar 2026 18:45:51 GMT  
		Size: 26.8 MB (26774787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663b0b4076c27408b2184d77a831c36817e8a8d8d4897cb92fce9cdd0165335a`  
		Last Modified: Thu, 05 Mar 2026 18:45:51 GMT  
		Size: 10.4 MB (10385429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3615b056b4ef975abfd3ae24796393abcb6cd5c819f1c8a6e68c1488f641f1a`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32f9cb2f283cf611fe753cefc9ac89c970b2a82e793b029047ec9a74dd88da4`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5dc68331a182d6047cc64dc01811876321654c40481e65df941bf21d1129ff`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281309e002e2014f85aa6e60f8f56d3a46cd826258710ea23f02ebd55fa56d86`  
		Last Modified: Thu, 05 Mar 2026 19:08:59 GMT  
		Size: 7.3 MB (7271697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d5638366f0629a45399b2da5bc12e7eaec99cd43a172c0e00a061cbad07fd9`  
		Last Modified: Thu, 05 Mar 2026 19:08:58 GMT  
		Size: 91.8 KB (91788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db525e8a11303b587a4637ce4f7e8cf2e27b87515229e415c66b907d6857c14`  
		Last Modified: Thu, 05 Mar 2026 19:08:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b41beca4d05ad9f4f8a0af06864a9b0bd92eb236aae78aec36d96eee3e972e7`  
		Last Modified: Thu, 05 Mar 2026 19:09:00 GMT  
		Size: 62.2 MB (62161362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c988857a21079067d802211bb65b801edbebcc1e6e21bd8e6e7eea98dc58fc`  
		Last Modified: Thu, 05 Mar 2026 19:09:00 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0de727742fa3feb2ba852cdaa770c212967433c39bb41ebfe1865a9ffcc78e`  
		Last Modified: Thu, 05 Mar 2026 19:09:00 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:01e39cec6c99783d318713cb96e9d665690e384f821039d02ecc3d40d501c51d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c18a85619e7433b908f936509e5dbd40bb98ace79929f60a844a1db3c93374`

```dockerfile
```

-	Layers:
	-	`sha256:d37d617810772a2c79e6330f2dbaf0e418ffcc3f2db333b8443afe97f45e219b`  
		Last Modified: Thu, 05 Mar 2026 19:08:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.3-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:74ea5cdbe2fe4518d73e3ac0241167a38c7616c3dd6be011cf48fc0a61189c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134355560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9d940d504e1f821c76a9e400c405dfbc51b3d58990d7abaae29dd773c08694`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:46:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:46:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:46:32 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:46:36 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:46:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:46:36 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:46:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:46:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:46:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:46:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:46:40 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:09:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:09:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:09:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:09:20 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:09:20 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:09:20 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:09:20 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95152b95c4ccfeb5059ced14a96c4f1c17872baa3e875c18056cb5bed1b56676`  
		Last Modified: Thu, 05 Mar 2026 18:46:46 GMT  
		Size: 7.6 MB (7597774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d532e57eb4774540148a1cccd311fc10645e4dc68e8512d6b4f5a07d77498e82`  
		Last Modified: Thu, 05 Mar 2026 18:46:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64983bc952c232855d431fc0da6e3080f4c4c64fc0dce721c1086cc916d3037`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 17.7 MB (17691333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0552f021a975b88c2f33fc3057737b716d29921dcf12fff1a7bd017272ee52bf`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 26.8 MB (26754433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe274cdce52e0d95eda23b7407fdd0cd8a861a2014d8a240bda6be387b22c74`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 10.4 MB (10369783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28feee09383ef1673e7a0cec5e45cf0ad41f8b64208682ad535da48f8de7e08e`  
		Last Modified: Thu, 05 Mar 2026 18:46:48 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c266b2e92e5c06c3362ac89279eac9742220da712ded40590f3312de938eb16a`  
		Last Modified: Thu, 05 Mar 2026 18:46:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b204129a9de694faa70c2c825548fbe88d190e24ecc2d949a3ea099c0ac40d3`  
		Last Modified: Thu, 05 Mar 2026 18:46:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6011a406c6080a98a187e060555bd77450686dc8a0a3a1bd21a8b635e7a7c7c5`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 6.6 MB (6573025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63255cd848e2b7900e0177b225137079a3c0e9bde16e58d50a40edba81e6b028`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 88.2 KB (88150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3758bf28f38de089029226cd958aeeb1d75194761390a5bd605206ae3d4092e3`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbec48042bff8bd1621f0f9cd3d2ec81bc03fdba86235b7e6586dec177d82907`  
		Last Modified: Thu, 05 Mar 2026 19:09:32 GMT  
		Size: 62.0 MB (61991183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f8030e199452b1b297f3a4acc28ce81ecd590b3b41343eb4dbb260d0a03684`  
		Last Modified: Thu, 05 Mar 2026 19:09:31 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a7939d77fae184c61e7cbceee2129945aff07b2c8ba46170605cd266cdee9f`  
		Last Modified: Thu, 05 Mar 2026 19:09:31 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:0d74abb912009d5524b2bc08d235dd65785a6a9c105843b2d5f2e38d9740c01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e7a73ef832c7e6998b93ef231c73a0f5a4b733dd27635018b7ccc4808f8859`

```dockerfile
```

-	Layers:
	-	`sha256:dfe982715ef650b1926988aa185ecef3d257673538c7392c6271f6a59a023df3`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 34.7 KB (34721 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.3-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1d1d67ba557d1ccedcd46d05ba832276e65260a518c240b087c71849cd6cbce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133716998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2468f972a259c78d9053fa37f4ca40d54c8071086fecff98d4e0f4829c120c36`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:44:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:44:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:44:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:44:32 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:44:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:44:32 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:44:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:44:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:44:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:44:34 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:10:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:10:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:10:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:10:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:10:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:10:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:10:13 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74f52f7948b98f731cc47a7da43a1a028f38396d447d93fa458cc7b1ee9ade0`  
		Last Modified: Thu, 05 Mar 2026 18:44:41 GMT  
		Size: 8.5 MB (8453572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50de1b9f6ee9b0bb47a9cb5e7877595782f60dc2d6c014088cfb72c4dca02106`  
		Last Modified: Thu, 05 Mar 2026 18:44:40 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8cd16e98d03b1081e8606a566c45e24d404e6738ce672011e2f5e3fe3b637b`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 17.5 MB (17472694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a548a65df6cf925e933ead68a3677913c3c9586d7115d161b6afd378cd8b1836`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 25.7 MB (25732665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09bdc4530b81e1aa74fe3d0322209932119b3cb64a72447d5442bd9c50cd4ed`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 10.0 MB (9974089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b96e65028eacc3700698877e774e4bfbca321b41420638481e753d07449225c`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faab51bb66faa3b0c0d737ebc09cfb486e94acbcdc20e883d8022102e4fc2fd`  
		Last Modified: Thu, 05 Mar 2026 18:44:43 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd02735b351188e3d18abc71b56816ddc7406e1d55c433166d34e8fd46aa5692`  
		Last Modified: Thu, 05 Mar 2026 18:44:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bd6c43d314f7ba1970375218d37bf189ee9e325f65b8a993a3846b8b081490`  
		Last Modified: Thu, 05 Mar 2026 19:10:23 GMT  
		Size: 7.2 MB (7213319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447b7408aabced1a21d26cecd53e54c14e75f0c7fa49a892e88b3faa8618791d`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 101.3 KB (101302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a4786ffc77dd17db34d4bd2edde2706bdb8bde49e2f5c532ffdb910ab16ee9`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce02e419a084f596f3e92c28731f67e0f113c3464b10ce77db5f722f7da9d1d`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 60.6 MB (60564110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf5b1f083f16666d8e3ef65369ed92093b78752eb5146941526e49b6d31965e`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720b8605e7f2e52dd9a65c8e463ab396a44abc68a0a689a3eda9a497503540fb`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f842673f5ac13d592cac6534e468f00a1d0270c7b8b686dff5ede372d952ad2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aec29e8d6f9254e8a5488aabb8ce917d657467f43e13af6528879dc1f2bfe02`

```dockerfile
```

-	Layers:
	-	`sha256:d59a3392ae448d26d8ed94f620ba9496be18d97cce5dc57e5943d287b049c800`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.3-dind-rootless`

```console
$ docker pull docker@sha256:7b90623a6a8d610e766d0dda84f20c7fbafeefe68a83ba01ecb4d6921b777b49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.3-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:aeab8c8ba5bd982ecd69b6f302e87c02eb66dd2fa3db5a8c5e81366e35960cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165252061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089ebb0bf68cbe13e627bb94ebca07973c936be52099f607c90ededbd35a2a90`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:46:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:46:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:46:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:46:28 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:46:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:46:28 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:46:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:46:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:46:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:46:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:46:30 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:10:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:10:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:10:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:10:30 GMT
CMD []
# Thu, 05 Mar 2026 19:51:35 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 05 Mar 2026 19:51:35 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 05 Mar 2026 19:51:35 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:51:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 05 Mar 2026 19:51:36 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 05 Mar 2026 19:51:36 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 05 Mar 2026 19:51:36 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f1c7a58cda4399b7be2fb8427c3b756917df1abb433e17a98888259aa70c83`  
		Last Modified: Thu, 05 Mar 2026 18:46:37 GMT  
		Size: 8.4 MB (8399691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba58ca1e42e5eeec21273f066c06e25afee78a5211c7d6deb38ba545b7d6240`  
		Last Modified: Thu, 05 Mar 2026 18:46:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f8c3243c30359f68ee8e1f96a24d246ca1357a82d8b30de9a33e9d282d93e1`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 18.9 MB (18919365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e9c4ffbcbf205284b573f955de57155f10b92234b491b2127720a57c90c1ce`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 28.5 MB (28516523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34962ed90623b311790e104f78a280cdc54a1ce559635328476148c6fc522888`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 11.0 MB (10953934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a9731c772a36b5ae18988bc0c1c69aff62cb86d597f2de367c5b330fb8d459`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a294ee3d24d1214f1944e57dadb6ef9c4b434a1a170e348838dafb16d31127`  
		Last Modified: Thu, 05 Mar 2026 18:46:39 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df03e33ed496925038509c0abcd9f087ab5ec4e4b917ed51730d71d63a87c91`  
		Last Modified: Thu, 05 Mar 2026 18:46:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fbd819f55b555293ac19eaaa17fd0ff75f9812f924da0a56610f334b1db8e6`  
		Last Modified: Thu, 05 Mar 2026 19:10:41 GMT  
		Size: 6.9 MB (6934736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524d6d9cccdc6fa4c04046756dada64359f4445d625ae2d4653714afad9044c`  
		Last Modified: Thu, 05 Mar 2026 19:10:40 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4da28e0bc44f1c47c50aab943753bc5626ab338c9dacd7cff96381acf13793`  
		Last Modified: Thu, 05 Mar 2026 19:10:41 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503f0e2071dd914a67c23aa1b570c3fccb863ebac670fa0d253ff15658adaf0a`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 66.8 MB (66766357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdcbaa55207a60126845f61a87ad8fbea9e87874674046ea2133cb2f3159d36`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bd5217468716f0f037bdb54d7c022dbf95c6896f29dc171a9677f86f621c25`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624e0d70ccddab2837c7579988be593d7d2c14e98ecc0951b4b4b1d0159ea2e8`  
		Last Modified: Thu, 05 Mar 2026 19:51:42 GMT  
		Size: 3.4 MB (3419929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed14991c62b9a9ef3cfc532d6532e4fd5343461fd35c558d71b52fe601b961`  
		Last Modified: Thu, 05 Mar 2026 19:51:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ac276d93a270a03f1cf58e6899d6a02fad81464e22001619436513cbe7e0e8`  
		Last Modified: Thu, 05 Mar 2026 19:51:42 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0161c5d6b742bdaefd9ac5d339340963166794c14b9e069af0f39fac4010597a`  
		Last Modified: Thu, 05 Mar 2026 19:51:42 GMT  
		Size: 17.4 MB (17377747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cf600d07eddbd5c5e7f2c80032ccc565bdd549c0193703940b5508312e509a`  
		Last Modified: Thu, 05 Mar 2026 19:51:43 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c3581ae9fc196cbf20a722387b0d4f4395cdf30ea836abc781891c9019939fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b9e467c6ab22b4a83c306b278852334102b54e6919ef4adfeaf8977ad9641b`

```dockerfile
```

-	Layers:
	-	`sha256:4b084f57f37ad05ae58136fd5d64bd79f05ca02c03ff4358cb8c35475b49240e`  
		Last Modified: Thu, 05 Mar 2026 19:51:41 GMT  
		Size: 30.6 KB (30588 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.3-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:363611f480e6222f4c95e0fe9b92d68e16add9b4f390fc53d681084c4b60caee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154825064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05963d5fac11223eb3f65b15aa06ef12c1a799eeb4b5bb56d79bd428436e0cd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:44:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:44:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:44:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:44:32 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:44:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:44:32 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:44:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:44:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:44:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:44:34 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:10:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:10:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:10:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:10:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:10:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:10:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:10:13 GMT
CMD []
# Thu, 05 Mar 2026 19:52:11 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 05 Mar 2026 19:52:11 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 05 Mar 2026 19:52:11 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:52:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 05 Mar 2026 19:52:12 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 05 Mar 2026 19:52:12 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 05 Mar 2026 19:52:12 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74f52f7948b98f731cc47a7da43a1a028f38396d447d93fa458cc7b1ee9ade0`  
		Last Modified: Thu, 05 Mar 2026 18:44:41 GMT  
		Size: 8.5 MB (8453572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50de1b9f6ee9b0bb47a9cb5e7877595782f60dc2d6c014088cfb72c4dca02106`  
		Last Modified: Thu, 05 Mar 2026 18:44:40 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8cd16e98d03b1081e8606a566c45e24d404e6738ce672011e2f5e3fe3b637b`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 17.5 MB (17472694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a548a65df6cf925e933ead68a3677913c3c9586d7115d161b6afd378cd8b1836`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 25.7 MB (25732665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09bdc4530b81e1aa74fe3d0322209932119b3cb64a72447d5442bd9c50cd4ed`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 10.0 MB (9974089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b96e65028eacc3700698877e774e4bfbca321b41420638481e753d07449225c`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faab51bb66faa3b0c0d737ebc09cfb486e94acbcdc20e883d8022102e4fc2fd`  
		Last Modified: Thu, 05 Mar 2026 18:44:43 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd02735b351188e3d18abc71b56816ddc7406e1d55c433166d34e8fd46aa5692`  
		Last Modified: Thu, 05 Mar 2026 18:44:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bd6c43d314f7ba1970375218d37bf189ee9e325f65b8a993a3846b8b081490`  
		Last Modified: Thu, 05 Mar 2026 19:10:23 GMT  
		Size: 7.2 MB (7213319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447b7408aabced1a21d26cecd53e54c14e75f0c7fa49a892e88b3faa8618791d`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 101.3 KB (101302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a4786ffc77dd17db34d4bd2edde2706bdb8bde49e2f5c532ffdb910ab16ee9`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce02e419a084f596f3e92c28731f67e0f113c3464b10ce77db5f722f7da9d1d`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 60.6 MB (60564110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf5b1f083f16666d8e3ef65369ed92093b78752eb5146941526e49b6d31965e`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720b8605e7f2e52dd9a65c8e463ab396a44abc68a0a689a3eda9a497503540fb`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113a99610f0313cefac114163c823cc19536cc5ad728c999ce1c42a08df7b73e`  
		Last Modified: Thu, 05 Mar 2026 19:52:19 GMT  
		Size: 3.4 MB (3394381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f83f706c62205d1a7b78b43438268f91f5a1c97ce0aa6d9e895c6ccb93e6aaa`  
		Last Modified: Thu, 05 Mar 2026 19:52:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8ea4b65def4cea71f744e7c03f2bd0f14403430efba1dde697830900fd9220`  
		Last Modified: Thu, 05 Mar 2026 19:52:19 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d663f5f609d1ca281ed28345736bdf222b960707ccb29edd7d2fca31fffcce`  
		Last Modified: Thu, 05 Mar 2026 19:52:19 GMT  
		Size: 17.7 MB (17712346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fc8e3e13278240d699ba378e763c538e98fc43342e3c86b0625b503863f3f0`  
		Last Modified: Thu, 05 Mar 2026 19:52:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:419ad745bdc70ba4c204674efbc833c2b1eaff3596fbdf95c23b80444589037d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8693634da1b98934154ee830afbd8beb888c8ede561915c13c94c94ca449c750`

```dockerfile
```

-	Layers:
	-	`sha256:df3b03f6dd4be8fab2827638b57709b438a0bab274edac98ada56265237fec2c`  
		Last Modified: Thu, 05 Mar 2026 19:52:18 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.3-windowsservercore`

```console
$ docker pull docker@sha256:fdd48859b2b14b2fa4af458fcea153cfd95e8ce7429e66286229f28b47e507b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `docker:29.3-windowsservercore` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:42419a818a06c8b0bdb32d28efe864c1965f849d4d58dac6450fb35578530636
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2142463243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095982a564f926ffd785368388022d0f792a5f393f83c25b2b334b3f0ee3c25f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Wed, 25 Mar 2026 18:28:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Mar 2026 18:29:47 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Mar 2026 18:29:48 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.1.zip
# Wed, 25 Mar 2026 18:30:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Mar 2026 18:30:11 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:30:12 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.windows-amd64.exe
# Wed, 25 Mar 2026 18:30:13 GMT
ENV DOCKER_BUILDX_SHA256=47d76e47acf3c7611dd594c4b0909fec680ae6406b6fa775f6077b195837e2b9
# Wed, 25 Mar 2026 18:30:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Mar 2026 18:30:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:30:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Wed, 25 Mar 2026 18:30:37 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Wed, 25 Mar 2026 18:30:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c48ff63fd51e54c1621e1ef191ba1ffb5babb91295c52763e73038877ddbcc0`  
		Last Modified: Wed, 25 Mar 2026 18:30:56 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05646e87bcc7eebcf75f1a96ca80aa255bd6868601cdf94768601c8078d9b4b7`  
		Last Modified: Wed, 25 Mar 2026 18:30:55 GMT  
		Size: 374.0 KB (373997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edba92fa22a5c1bc563c18f651db43bfdc9c0720c21fff8d046d759875e121d1`  
		Last Modified: Wed, 25 Mar 2026 18:30:54 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b934d13e109edc08e9a08ca989659aded111b61867e75aa39cc626586e14b6d`  
		Last Modified: Wed, 25 Mar 2026 18:30:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff304ba5506cff7b400064688c74084a2ff60a244b484160e1be812e7672e3d`  
		Last Modified: Wed, 25 Mar 2026 18:30:56 GMT  
		Size: 19.6 MB (19594910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47622b1e857ba4fe582334af32ea59c3b58783ab368030f1d2259ae216996aaa`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a676a9fc9cb7650a5a61aad602e864237a2410b300b3babac5f0cfb4c9f31bf9`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d698051d32bbd456b5de7801253c16270739faf8954ce78f45f3a7e95830067`  
		Last Modified: Wed, 25 Mar 2026 18:30:52 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b8f6f29800e2912ff8cd1d9696f47141cb71560b98c73b71157c6b39d77665`  
		Last Modified: Wed, 25 Mar 2026 18:31:04 GMT  
		Size: 29.6 MB (29639971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbee4f4914616df04e2f56d66e020a4ca506723690da654928872871a3d1130`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36549e61114f7f53657411a2bc956fd69c15ae2f08beb6f977143978b7447c7a`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111317c19214d92002469ac71ea269b2b838ae7163f090cf6796b17aeccea76d`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee1dd44d7e561101a0c094be20961ded0b2b663201441b16b06bbace8b589ab`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 11.6 MB (11646539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.3-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:9504c71617f036da76201851ee9ad86ea91a1f572837a6e9e49023ace0612bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `docker:29.3-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull docker@sha256:7218b6c6fbe208207908f94f1ed696b4bd01423d2c443586c5f65031c5e0e93e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2043597626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378ba248bb85f2c6fe57c779e2da6f4c4498116174b27197870a8f9ee1d337d4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 21:55:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Mar 2026 21:55:45 GMT
ENV DOCKER_VERSION=29.3.0
# Tue, 10 Mar 2026 21:55:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.0.zip
# Tue, 10 Mar 2026 21:56:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 21:56:04 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Tue, 10 Mar 2026 21:56:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.windows-amd64.exe
# Tue, 10 Mar 2026 21:56:05 GMT
ENV DOCKER_BUILDX_SHA256=47d76e47acf3c7611dd594c4b0909fec680ae6406b6fa775f6077b195837e2b9
# Tue, 10 Mar 2026 21:56:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 21:56:22 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Tue, 10 Mar 2026 21:56:23 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-windows-x86_64.exe
# Tue, 10 Mar 2026 21:56:24 GMT
ENV DOCKER_COMPOSE_SHA256=ee84e42b93c501cb0aa2caa84d76b5f30ca6fb92f070e289fc37be7332c5822a
# Tue, 10 Mar 2026 21:56:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17a66011dcb9c38eedc922e2d718b0cff4e70ce31e167daaa8dfee148d9c195`  
		Last Modified: Tue, 10 Mar 2026 21:56:42 GMT  
		Size: 486.8 KB (486826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f159d4d5d7e56333bfd6e2e7b16344a0e872adf0b93acebefa53c4247fbc9396`  
		Last Modified: Tue, 10 Mar 2026 21:56:41 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccb66eda533f994dbbb9ff81d57c851758147e1a0630eea05e16a0716ff87ad`  
		Last Modified: Tue, 10 Mar 2026 21:56:41 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0cd965bfbb200c967e8ee796997bdd4cdb587a833c56d7a49317544aab06cc6`  
		Last Modified: Tue, 10 Mar 2026 21:56:44 GMT  
		Size: 19.6 MB (19571347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edc8f49358e8d56eb2e56b6ac13be2048a3a016717f24c53f49dc1fc9bde0f7`  
		Last Modified: Tue, 10 Mar 2026 21:56:40 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8ac62b592ebb8bae48e8d31dadb875c021f30a09defc65097fb06249ef2e6a`  
		Last Modified: Tue, 10 Mar 2026 21:56:40 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554c2edbde552817f409d72b85a719f3c34ddc1651c3a110b24b1d3aa4570cc3`  
		Last Modified: Tue, 10 Mar 2026 21:56:40 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90bad317fa3a54913b9758ee2e45f94e02a64cc9e4e0c693589b644de126d33`  
		Last Modified: Tue, 10 Mar 2026 21:56:46 GMT  
		Size: 29.6 MB (29623149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dbad83ed52d0db02d4f30b2e0a88e026dd56c68a61c0a3a99f4d64bc5b14d1`  
		Last Modified: Tue, 10 Mar 2026 21:56:38 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d05240889a0e152fce0f29182840145e329281d7d52b384e0251bb1a9abfa8`  
		Last Modified: Tue, 10 Mar 2026 21:56:38 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ac67609452a0105c993416f50fb486c0260df99ed76d920c31b1ab2aa344ab`  
		Last Modified: Tue, 10 Mar 2026 21:56:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3aff282c60575fe0964ee93b76dd77692c3ed1f6cbeeb91ecb807cfa30421b8`  
		Last Modified: Tue, 10 Mar 2026 21:56:40 GMT  
		Size: 11.6 MB (11623130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.3-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:fdd48859b2b14b2fa4af458fcea153cfd95e8ce7429e66286229f28b47e507b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `docker:29.3-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:42419a818a06c8b0bdb32d28efe864c1965f849d4d58dac6450fb35578530636
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2142463243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095982a564f926ffd785368388022d0f792a5f393f83c25b2b334b3f0ee3c25f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Wed, 25 Mar 2026 18:28:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Mar 2026 18:29:47 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Mar 2026 18:29:48 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.1.zip
# Wed, 25 Mar 2026 18:30:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Mar 2026 18:30:11 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:30:12 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.windows-amd64.exe
# Wed, 25 Mar 2026 18:30:13 GMT
ENV DOCKER_BUILDX_SHA256=47d76e47acf3c7611dd594c4b0909fec680ae6406b6fa775f6077b195837e2b9
# Wed, 25 Mar 2026 18:30:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Mar 2026 18:30:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:30:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Wed, 25 Mar 2026 18:30:37 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Wed, 25 Mar 2026 18:30:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c48ff63fd51e54c1621e1ef191ba1ffb5babb91295c52763e73038877ddbcc0`  
		Last Modified: Wed, 25 Mar 2026 18:30:56 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05646e87bcc7eebcf75f1a96ca80aa255bd6868601cdf94768601c8078d9b4b7`  
		Last Modified: Wed, 25 Mar 2026 18:30:55 GMT  
		Size: 374.0 KB (373997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edba92fa22a5c1bc563c18f651db43bfdc9c0720c21fff8d046d759875e121d1`  
		Last Modified: Wed, 25 Mar 2026 18:30:54 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b934d13e109edc08e9a08ca989659aded111b61867e75aa39cc626586e14b6d`  
		Last Modified: Wed, 25 Mar 2026 18:30:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff304ba5506cff7b400064688c74084a2ff60a244b484160e1be812e7672e3d`  
		Last Modified: Wed, 25 Mar 2026 18:30:56 GMT  
		Size: 19.6 MB (19594910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47622b1e857ba4fe582334af32ea59c3b58783ab368030f1d2259ae216996aaa`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a676a9fc9cb7650a5a61aad602e864237a2410b300b3babac5f0cfb4c9f31bf9`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d698051d32bbd456b5de7801253c16270739faf8954ce78f45f3a7e95830067`  
		Last Modified: Wed, 25 Mar 2026 18:30:52 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b8f6f29800e2912ff8cd1d9696f47141cb71560b98c73b71157c6b39d77665`  
		Last Modified: Wed, 25 Mar 2026 18:31:04 GMT  
		Size: 29.6 MB (29639971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbee4f4914616df04e2f56d66e020a4ca506723690da654928872871a3d1130`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36549e61114f7f53657411a2bc956fd69c15ae2f08beb6f977143978b7447c7a`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111317c19214d92002469ac71ea269b2b838ae7163f090cf6796b17aeccea76d`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee1dd44d7e561101a0c094be20961ded0b2b663201441b16b06bbace8b589ab`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 11.6 MB (11646539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.3.1`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3.1-alpine3.23`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3.1-cli`

```console
$ docker pull docker@sha256:70303ed0d265aee7bf4be0ddffe20b0b6e4f69ffa125e2a20cbb3718b99688db
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

### `docker:29.3.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:3459e4b0c6702acfdc23b2a48e4e8bdcfc51ef96bac2d0af3ea3edac4044192c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70660468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f34f75af30162c2d6b68fa089dac03a627ba7303e9758184d9d26dacb913ca7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:31:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:31:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:31:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:31:34 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:31:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:31:34 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:31:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:31:36 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:31:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:31:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:31:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f783f43bd0c479eca4a605cd057214fd4d32195579fd3858ea619042787418`  
		Last Modified: Wed, 25 Mar 2026 18:31:45 GMT  
		Size: 8.4 MB (8399805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dc00f58fe8675ce338442f1f3924e7575b889140324f529e6f7b7b552e6a8b`  
		Last Modified: Wed, 25 Mar 2026 18:31:44 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed7cc89d7e24509b5ecc2a876b68c336cc533fccd578553f96c40bd5977acaa`  
		Last Modified: Wed, 25 Mar 2026 18:31:45 GMT  
		Size: 18.9 MB (18925059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59f566876aae23a8d4ded9382841f58305b92c7453a48044734ac35241c5e5d`  
		Last Modified: Wed, 25 Mar 2026 18:31:46 GMT  
		Size: 28.5 MB (28516527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f27ff511c85a43e9a75a388dbd32088a24592f41c6987999fbcf0165672071d`  
		Last Modified: Wed, 25 Mar 2026 18:31:46 GMT  
		Size: 11.0 MB (10955101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac4601d8546b2a6477f79a9bff1a05ec9add30bf96dc48fcd27457170f39b07`  
		Last Modified: Wed, 25 Mar 2026 18:31:46 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b922537b6a3dd95fc487130c0ca4896eb541d70d4a9438dd39590ccb7b65943`  
		Last Modified: Wed, 25 Mar 2026 18:31:47 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62fa46a186b2dc7d1a25e70eb2c2653aa0431485adb908a7cf943d28c49cdf1`  
		Last Modified: Wed, 25 Mar 2026 18:31:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:827d9483e2a64b8c44523708ca54adaeec69e1ee40b1f275bb657e51828404f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587b7070e426c0932cb45f162874ea0917cc386aa52282a4e864f0aceeac21c5`

```dockerfile
```

-	Layers:
	-	`sha256:9c77ec231f2b5c72293c670da21cfc5dc7c509522268cc74c92f9098859cef6a`  
		Last Modified: Wed, 25 Mar 2026 18:31:44 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.3.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:ab088b3f5efe676c33f3339eeefbb2228b5e4b45cc6189a7ee8d717f98d47796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66741259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6299617540122589abca8da49bf316efc08ef3e0e4632b70f20e47121c8e7a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:20:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:20:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:20:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:20:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:20:55 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:20:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:20:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:20:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7327f5bd7b20a7c0c384c9bed111c54ed041e23650f2789ce160520bd54e7d64`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 8.3 MB (8300847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad441b201d110caa6bbae91773542ed3038e833916ab8fdbdee2efdd096951d`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a9b3570b577d5bd7b5702ea3b038bd6d6736da52c7e4cfa9204254b3ef6889`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 17.7 MB (17704832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687acedd268ebaa81d467b79f662cb296f999d5edc939573fc235718f10b3d5`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 26.8 MB (26774785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6738b4fa70496e709329c400187d16a1e6dcd9323aa0597219b36caeffbf73`  
		Last Modified: Wed, 25 Mar 2026 18:21:12 GMT  
		Size: 10.4 MB (10388825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0425cd14663ea2989a267ae635da01c39877aac17e1b4a26049c6e8584e9b7`  
		Last Modified: Wed, 25 Mar 2026 18:21:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7154483d9dd47aca8dda22548f6ac6381d6f297c1afcbda1c72dba31279d96f7`  
		Last Modified: Wed, 25 Mar 2026 18:21:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbfd7d41a6aa1e531936a17e36405a287262345307d1769bbf5e514f1f4955a`  
		Last Modified: Wed, 25 Mar 2026 18:21:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4a04a0fb0422d24efcd71966c2ec778971b5a49ba8fb1934681a3c061a4f7bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8881255256c5bafe467ec0dffa5cdafa965971effe17aab0e66a451dbac7b198`

```dockerfile
```

-	Layers:
	-	`sha256:e6eb00c7bd1756168105295aa8a9f0546960e7bf78727f47d669e70e1096cc65`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.3.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:b4cf24daf2e960893a39d2f0a13a0b2b889e626725f5704295ff3c7a80e2ce56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65702900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e770b04316507e289fdbe463af8dd53873a490a5215e9664d3c38a2387b9b0bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:20:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:20:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:20:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:20:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:20:55 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:20:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:20:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:20:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9a25e5bfb326bc75a71b460d0544e0abe70b0c6c1498521b7fd245df901627`  
		Last Modified: Wed, 25 Mar 2026 18:21:05 GMT  
		Size: 7.6 MB (7597792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bd4d27cb3827cca3206705328c83ee80e164a78dc2aa97099d480bb1ded087`  
		Last Modified: Wed, 25 Mar 2026 18:21:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57192b9959272e69a74f1600a28d23141f96a9856eb275612e66d96aed4cb23`  
		Last Modified: Wed, 25 Mar 2026 18:21:05 GMT  
		Size: 17.7 MB (17694926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7afb84b0bb6525824e7b41a3eb6ca04fbd8a378336dace66c201e7f0a9fdfd`  
		Last Modified: Wed, 25 Mar 2026 18:21:06 GMT  
		Size: 26.8 MB (26754421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34cbd0d9bfc6a2fbae47c23f0d1c832eaf8aacf91c370cd7d44df319b6dcf32`  
		Last Modified: Wed, 25 Mar 2026 18:21:06 GMT  
		Size: 10.4 MB (10371888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92b6554d10f78775d85c869fd50243ef34c2f7fb06170e9bfd0f6cb1d8c722f`  
		Last Modified: Wed, 25 Mar 2026 18:21:06 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a550d751a72e95d6b192c5aa49bc54135cd12eaac778e2494033d746481e4e`  
		Last Modified: Wed, 25 Mar 2026 18:21:07 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbfd7d41a6aa1e531936a17e36405a287262345307d1769bbf5e514f1f4955a`  
		Last Modified: Wed, 25 Mar 2026 18:21:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:b36c22ea07bd32cf40c3233fe677b6cfd0b141b3c63f391124eed2843c5fe9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17c08feca64baed542d11807ef5bdc316ef9f6816d6d0e695109048771339bc`

```dockerfile
```

-	Layers:
	-	`sha256:d9a26fdeeceae1cd37f2b33208c330bcbaaa632331e7950fad92cdb05c62b6ea`  
		Last Modified: Wed, 25 Mar 2026 18:21:05 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.3.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:56cff04ad8dcf376a96423ddf5515c8bdcd171e683265335da57f17aa020ad1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65845112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee59cb9a3f85ae950ab85efdd43672abd503dbe5adcd1a55b95687f24e990ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:28:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:28:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:28:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:28:13 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:28:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:28:13 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:28:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:28:14 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:28:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:28:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:28:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7edc56943efc5fd8ceeeec0973e7862a22eef8479f31e4506aaa7683706598`  
		Last Modified: Wed, 25 Mar 2026 18:28:21 GMT  
		Size: 8.5 MB (8453635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d7bdfa7dc871c3af6f5b34ef1ef53c930b2fde5801879b794f1849da1dc4d`  
		Last Modified: Wed, 25 Mar 2026 18:28:20 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c366b69bd090a1557acbb6f1ebdab176751b61ca7e1c82af675fd5dd30436a`  
		Last Modified: Wed, 25 Mar 2026 18:28:21 GMT  
		Size: 17.5 MB (17476961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b74c99f62156a67a1a2f1edfa046c0c13825a6cdef351e68e41cbbffd8badb`  
		Last Modified: Wed, 25 Mar 2026 18:28:22 GMT  
		Size: 25.7 MB (25732670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fed48b65e655b617bf78f3b0c6df9994322561de4c1c4a706e621ec83f8fb84`  
		Last Modified: Wed, 25 Mar 2026 18:28:22 GMT  
		Size: 10.0 MB (9982606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318a3b2c176f6893caa80c95a652634492e38503c58e091a916b6d9c341a0648`  
		Last Modified: Wed, 25 Mar 2026 18:28:23 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c910ec30db0949d800f54bb9c1b3c4e2af20695bf5b14f43f4f9be42a0ecb2c`  
		Last Modified: Wed, 25 Mar 2026 18:28:23 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd0d057ad753e2ef837845dd9504265e602e0802dceee1b0083e05f00291b8c`  
		Last Modified: Wed, 25 Mar 2026 18:28:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a3331dd737a9d4ad382fff64040bbad2660884a99286e44af8338a00851aec68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ed74d502ab8399d1e1a43c9de66bf070e1741c40c8a187c876aa031385bd08`

```dockerfile
```

-	Layers:
	-	`sha256:5de0f8302079e7f4909158e85e3fcabf6c532e1b84c2c25003b4bf3343ea0e94`  
		Last Modified: Wed, 25 Mar 2026 18:28:21 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.3.1-cli-alpine3.23`

```console
$ docker pull docker@sha256:70303ed0d265aee7bf4be0ddffe20b0b6e4f69ffa125e2a20cbb3718b99688db
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

### `docker:29.3.1-cli-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:3459e4b0c6702acfdc23b2a48e4e8bdcfc51ef96bac2d0af3ea3edac4044192c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70660468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f34f75af30162c2d6b68fa089dac03a627ba7303e9758184d9d26dacb913ca7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:31:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:31:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:31:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:31:34 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:31:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:31:34 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:31:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:31:36 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:31:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:31:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:31:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f783f43bd0c479eca4a605cd057214fd4d32195579fd3858ea619042787418`  
		Last Modified: Wed, 25 Mar 2026 18:31:45 GMT  
		Size: 8.4 MB (8399805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dc00f58fe8675ce338442f1f3924e7575b889140324f529e6f7b7b552e6a8b`  
		Last Modified: Wed, 25 Mar 2026 18:31:44 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed7cc89d7e24509b5ecc2a876b68c336cc533fccd578553f96c40bd5977acaa`  
		Last Modified: Wed, 25 Mar 2026 18:31:45 GMT  
		Size: 18.9 MB (18925059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59f566876aae23a8d4ded9382841f58305b92c7453a48044734ac35241c5e5d`  
		Last Modified: Wed, 25 Mar 2026 18:31:46 GMT  
		Size: 28.5 MB (28516527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f27ff511c85a43e9a75a388dbd32088a24592f41c6987999fbcf0165672071d`  
		Last Modified: Wed, 25 Mar 2026 18:31:46 GMT  
		Size: 11.0 MB (10955101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac4601d8546b2a6477f79a9bff1a05ec9add30bf96dc48fcd27457170f39b07`  
		Last Modified: Wed, 25 Mar 2026 18:31:46 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b922537b6a3dd95fc487130c0ca4896eb541d70d4a9438dd39590ccb7b65943`  
		Last Modified: Wed, 25 Mar 2026 18:31:47 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62fa46a186b2dc7d1a25e70eb2c2653aa0431485adb908a7cf943d28c49cdf1`  
		Last Modified: Wed, 25 Mar 2026 18:31:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3.1-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:827d9483e2a64b8c44523708ca54adaeec69e1ee40b1f275bb657e51828404f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587b7070e426c0932cb45f162874ea0917cc386aa52282a4e864f0aceeac21c5`

```dockerfile
```

-	Layers:
	-	`sha256:9c77ec231f2b5c72293c670da21cfc5dc7c509522268cc74c92f9098859cef6a`  
		Last Modified: Wed, 25 Mar 2026 18:31:44 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.3.1-cli-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:ab088b3f5efe676c33f3339eeefbb2228b5e4b45cc6189a7ee8d717f98d47796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66741259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6299617540122589abca8da49bf316efc08ef3e0e4632b70f20e47121c8e7a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:20:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:20:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:20:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:20:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:20:55 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:20:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:20:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:20:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7327f5bd7b20a7c0c384c9bed111c54ed041e23650f2789ce160520bd54e7d64`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 8.3 MB (8300847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad441b201d110caa6bbae91773542ed3038e833916ab8fdbdee2efdd096951d`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a9b3570b577d5bd7b5702ea3b038bd6d6736da52c7e4cfa9204254b3ef6889`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 17.7 MB (17704832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687acedd268ebaa81d467b79f662cb296f999d5edc939573fc235718f10b3d5`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 26.8 MB (26774785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6738b4fa70496e709329c400187d16a1e6dcd9323aa0597219b36caeffbf73`  
		Last Modified: Wed, 25 Mar 2026 18:21:12 GMT  
		Size: 10.4 MB (10388825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0425cd14663ea2989a267ae635da01c39877aac17e1b4a26049c6e8584e9b7`  
		Last Modified: Wed, 25 Mar 2026 18:21:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7154483d9dd47aca8dda22548f6ac6381d6f297c1afcbda1c72dba31279d96f7`  
		Last Modified: Wed, 25 Mar 2026 18:21:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbfd7d41a6aa1e531936a17e36405a287262345307d1769bbf5e514f1f4955a`  
		Last Modified: Wed, 25 Mar 2026 18:21:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3.1-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:4a04a0fb0422d24efcd71966c2ec778971b5a49ba8fb1934681a3c061a4f7bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8881255256c5bafe467ec0dffa5cdafa965971effe17aab0e66a451dbac7b198`

```dockerfile
```

-	Layers:
	-	`sha256:e6eb00c7bd1756168105295aa8a9f0546960e7bf78727f47d669e70e1096cc65`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.3.1-cli-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:b4cf24daf2e960893a39d2f0a13a0b2b889e626725f5704295ff3c7a80e2ce56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65702900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e770b04316507e289fdbe463af8dd53873a490a5215e9664d3c38a2387b9b0bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:20:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:20:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:20:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:20:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:20:55 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:20:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:20:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:20:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9a25e5bfb326bc75a71b460d0544e0abe70b0c6c1498521b7fd245df901627`  
		Last Modified: Wed, 25 Mar 2026 18:21:05 GMT  
		Size: 7.6 MB (7597792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bd4d27cb3827cca3206705328c83ee80e164a78dc2aa97099d480bb1ded087`  
		Last Modified: Wed, 25 Mar 2026 18:21:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57192b9959272e69a74f1600a28d23141f96a9856eb275612e66d96aed4cb23`  
		Last Modified: Wed, 25 Mar 2026 18:21:05 GMT  
		Size: 17.7 MB (17694926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7afb84b0bb6525824e7b41a3eb6ca04fbd8a378336dace66c201e7f0a9fdfd`  
		Last Modified: Wed, 25 Mar 2026 18:21:06 GMT  
		Size: 26.8 MB (26754421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34cbd0d9bfc6a2fbae47c23f0d1c832eaf8aacf91c370cd7d44df319b6dcf32`  
		Last Modified: Wed, 25 Mar 2026 18:21:06 GMT  
		Size: 10.4 MB (10371888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92b6554d10f78775d85c869fd50243ef34c2f7fb06170e9bfd0f6cb1d8c722f`  
		Last Modified: Wed, 25 Mar 2026 18:21:06 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a550d751a72e95d6b192c5aa49bc54135cd12eaac778e2494033d746481e4e`  
		Last Modified: Wed, 25 Mar 2026 18:21:07 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbfd7d41a6aa1e531936a17e36405a287262345307d1769bbf5e514f1f4955a`  
		Last Modified: Wed, 25 Mar 2026 18:21:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3.1-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:b36c22ea07bd32cf40c3233fe677b6cfd0b141b3c63f391124eed2843c5fe9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17c08feca64baed542d11807ef5bdc316ef9f6816d6d0e695109048771339bc`

```dockerfile
```

-	Layers:
	-	`sha256:d9a26fdeeceae1cd37f2b33208c330bcbaaa632331e7950fad92cdb05c62b6ea`  
		Last Modified: Wed, 25 Mar 2026 18:21:05 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.3.1-cli-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:56cff04ad8dcf376a96423ddf5515c8bdcd171e683265335da57f17aa020ad1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65845112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee59cb9a3f85ae950ab85efdd43672abd503dbe5adcd1a55b95687f24e990ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:28:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:28:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:28:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:28:13 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:28:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:28:13 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:28:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:28:14 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:28:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:28:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:28:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7edc56943efc5fd8ceeeec0973e7862a22eef8479f31e4506aaa7683706598`  
		Last Modified: Wed, 25 Mar 2026 18:28:21 GMT  
		Size: 8.5 MB (8453635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d7bdfa7dc871c3af6f5b34ef1ef53c930b2fde5801879b794f1849da1dc4d`  
		Last Modified: Wed, 25 Mar 2026 18:28:20 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c366b69bd090a1557acbb6f1ebdab176751b61ca7e1c82af675fd5dd30436a`  
		Last Modified: Wed, 25 Mar 2026 18:28:21 GMT  
		Size: 17.5 MB (17476961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b74c99f62156a67a1a2f1edfa046c0c13825a6cdef351e68e41cbbffd8badb`  
		Last Modified: Wed, 25 Mar 2026 18:28:22 GMT  
		Size: 25.7 MB (25732670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fed48b65e655b617bf78f3b0c6df9994322561de4c1c4a706e621ec83f8fb84`  
		Last Modified: Wed, 25 Mar 2026 18:28:22 GMT  
		Size: 10.0 MB (9982606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318a3b2c176f6893caa80c95a652634492e38503c58e091a916b6d9c341a0648`  
		Last Modified: Wed, 25 Mar 2026 18:28:23 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c910ec30db0949d800f54bb9c1b3c4e2af20695bf5b14f43f4f9be42a0ecb2c`  
		Last Modified: Wed, 25 Mar 2026 18:28:23 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd0d057ad753e2ef837845dd9504265e602e0802dceee1b0083e05f00291b8c`  
		Last Modified: Wed, 25 Mar 2026 18:28:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.3.1-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:a3331dd737a9d4ad382fff64040bbad2660884a99286e44af8338a00851aec68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ed74d502ab8399d1e1a43c9de66bf070e1741c40c8a187c876aa031385bd08`

```dockerfile
```

-	Layers:
	-	`sha256:5de0f8302079e7f4909158e85e3fcabf6c532e1b84c2c25003b4bf3343ea0e94`  
		Last Modified: Wed, 25 Mar 2026 18:28:21 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.3.1-dind`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3.1-dind-alpine3.23`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3.1-dind-rootless`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3.1-windowsservercore`

```console
$ docker pull docker@sha256:fdd48859b2b14b2fa4af458fcea153cfd95e8ce7429e66286229f28b47e507b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `docker:29.3.1-windowsservercore` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:42419a818a06c8b0bdb32d28efe864c1965f849d4d58dac6450fb35578530636
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2142463243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095982a564f926ffd785368388022d0f792a5f393f83c25b2b334b3f0ee3c25f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Wed, 25 Mar 2026 18:28:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Mar 2026 18:29:47 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Mar 2026 18:29:48 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.1.zip
# Wed, 25 Mar 2026 18:30:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Mar 2026 18:30:11 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:30:12 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.windows-amd64.exe
# Wed, 25 Mar 2026 18:30:13 GMT
ENV DOCKER_BUILDX_SHA256=47d76e47acf3c7611dd594c4b0909fec680ae6406b6fa775f6077b195837e2b9
# Wed, 25 Mar 2026 18:30:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Mar 2026 18:30:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:30:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Wed, 25 Mar 2026 18:30:37 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Wed, 25 Mar 2026 18:30:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c48ff63fd51e54c1621e1ef191ba1ffb5babb91295c52763e73038877ddbcc0`  
		Last Modified: Wed, 25 Mar 2026 18:30:56 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05646e87bcc7eebcf75f1a96ca80aa255bd6868601cdf94768601c8078d9b4b7`  
		Last Modified: Wed, 25 Mar 2026 18:30:55 GMT  
		Size: 374.0 KB (373997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edba92fa22a5c1bc563c18f651db43bfdc9c0720c21fff8d046d759875e121d1`  
		Last Modified: Wed, 25 Mar 2026 18:30:54 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b934d13e109edc08e9a08ca989659aded111b61867e75aa39cc626586e14b6d`  
		Last Modified: Wed, 25 Mar 2026 18:30:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff304ba5506cff7b400064688c74084a2ff60a244b484160e1be812e7672e3d`  
		Last Modified: Wed, 25 Mar 2026 18:30:56 GMT  
		Size: 19.6 MB (19594910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47622b1e857ba4fe582334af32ea59c3b58783ab368030f1d2259ae216996aaa`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a676a9fc9cb7650a5a61aad602e864237a2410b300b3babac5f0cfb4c9f31bf9`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d698051d32bbd456b5de7801253c16270739faf8954ce78f45f3a7e95830067`  
		Last Modified: Wed, 25 Mar 2026 18:30:52 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b8f6f29800e2912ff8cd1d9696f47141cb71560b98c73b71157c6b39d77665`  
		Last Modified: Wed, 25 Mar 2026 18:31:04 GMT  
		Size: 29.6 MB (29639971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbee4f4914616df04e2f56d66e020a4ca506723690da654928872871a3d1130`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36549e61114f7f53657411a2bc956fd69c15ae2f08beb6f977143978b7447c7a`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111317c19214d92002469ac71ea269b2b838ae7163f090cf6796b17aeccea76d`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee1dd44d7e561101a0c094be20961ded0b2b663201441b16b06bbace8b589ab`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 11.6 MB (11646539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.3.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3.1-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:fdd48859b2b14b2fa4af458fcea153cfd95e8ce7429e66286229f28b47e507b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `docker:29.3.1-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:42419a818a06c8b0bdb32d28efe864c1965f849d4d58dac6450fb35578530636
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2142463243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095982a564f926ffd785368388022d0f792a5f393f83c25b2b334b3f0ee3c25f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Wed, 25 Mar 2026 18:28:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Mar 2026 18:29:47 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Mar 2026 18:29:48 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.1.zip
# Wed, 25 Mar 2026 18:30:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Mar 2026 18:30:11 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:30:12 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.windows-amd64.exe
# Wed, 25 Mar 2026 18:30:13 GMT
ENV DOCKER_BUILDX_SHA256=47d76e47acf3c7611dd594c4b0909fec680ae6406b6fa775f6077b195837e2b9
# Wed, 25 Mar 2026 18:30:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Mar 2026 18:30:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:30:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Wed, 25 Mar 2026 18:30:37 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Wed, 25 Mar 2026 18:30:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c48ff63fd51e54c1621e1ef191ba1ffb5babb91295c52763e73038877ddbcc0`  
		Last Modified: Wed, 25 Mar 2026 18:30:56 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05646e87bcc7eebcf75f1a96ca80aa255bd6868601cdf94768601c8078d9b4b7`  
		Last Modified: Wed, 25 Mar 2026 18:30:55 GMT  
		Size: 374.0 KB (373997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edba92fa22a5c1bc563c18f651db43bfdc9c0720c21fff8d046d759875e121d1`  
		Last Modified: Wed, 25 Mar 2026 18:30:54 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b934d13e109edc08e9a08ca989659aded111b61867e75aa39cc626586e14b6d`  
		Last Modified: Wed, 25 Mar 2026 18:30:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff304ba5506cff7b400064688c74084a2ff60a244b484160e1be812e7672e3d`  
		Last Modified: Wed, 25 Mar 2026 18:30:56 GMT  
		Size: 19.6 MB (19594910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47622b1e857ba4fe582334af32ea59c3b58783ab368030f1d2259ae216996aaa`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a676a9fc9cb7650a5a61aad602e864237a2410b300b3babac5f0cfb4c9f31bf9`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d698051d32bbd456b5de7801253c16270739faf8954ce78f45f3a7e95830067`  
		Last Modified: Wed, 25 Mar 2026 18:30:52 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b8f6f29800e2912ff8cd1d9696f47141cb71560b98c73b71157c6b39d77665`  
		Last Modified: Wed, 25 Mar 2026 18:31:04 GMT  
		Size: 29.6 MB (29639971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbee4f4914616df04e2f56d66e020a4ca506723690da654928872871a3d1130`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36549e61114f7f53657411a2bc956fd69c15ae2f08beb6f977143978b7447c7a`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111317c19214d92002469ac71ea269b2b838ae7163f090cf6796b17aeccea76d`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee1dd44d7e561101a0c094be20961ded0b2b663201441b16b06bbace8b589ab`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 11.6 MB (11646539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:70303ed0d265aee7bf4be0ddffe20b0b6e4f69ffa125e2a20cbb3718b99688db
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
$ docker pull docker@sha256:3459e4b0c6702acfdc23b2a48e4e8bdcfc51ef96bac2d0af3ea3edac4044192c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70660468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f34f75af30162c2d6b68fa089dac03a627ba7303e9758184d9d26dacb913ca7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:31:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:31:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:31:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:31:34 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:31:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:31:34 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:31:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:31:36 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:31:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:31:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:31:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f783f43bd0c479eca4a605cd057214fd4d32195579fd3858ea619042787418`  
		Last Modified: Wed, 25 Mar 2026 18:31:45 GMT  
		Size: 8.4 MB (8399805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dc00f58fe8675ce338442f1f3924e7575b889140324f529e6f7b7b552e6a8b`  
		Last Modified: Wed, 25 Mar 2026 18:31:44 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed7cc89d7e24509b5ecc2a876b68c336cc533fccd578553f96c40bd5977acaa`  
		Last Modified: Wed, 25 Mar 2026 18:31:45 GMT  
		Size: 18.9 MB (18925059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59f566876aae23a8d4ded9382841f58305b92c7453a48044734ac35241c5e5d`  
		Last Modified: Wed, 25 Mar 2026 18:31:46 GMT  
		Size: 28.5 MB (28516527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f27ff511c85a43e9a75a388dbd32088a24592f41c6987999fbcf0165672071d`  
		Last Modified: Wed, 25 Mar 2026 18:31:46 GMT  
		Size: 11.0 MB (10955101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac4601d8546b2a6477f79a9bff1a05ec9add30bf96dc48fcd27457170f39b07`  
		Last Modified: Wed, 25 Mar 2026 18:31:46 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b922537b6a3dd95fc487130c0ca4896eb541d70d4a9438dd39590ccb7b65943`  
		Last Modified: Wed, 25 Mar 2026 18:31:47 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62fa46a186b2dc7d1a25e70eb2c2653aa0431485adb908a7cf943d28c49cdf1`  
		Last Modified: Wed, 25 Mar 2026 18:31:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:827d9483e2a64b8c44523708ca54adaeec69e1ee40b1f275bb657e51828404f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587b7070e426c0932cb45f162874ea0917cc386aa52282a4e864f0aceeac21c5`

```dockerfile
```

-	Layers:
	-	`sha256:9c77ec231f2b5c72293c670da21cfc5dc7c509522268cc74c92f9098859cef6a`  
		Last Modified: Wed, 25 Mar 2026 18:31:44 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:ab088b3f5efe676c33f3339eeefbb2228b5e4b45cc6189a7ee8d717f98d47796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66741259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6299617540122589abca8da49bf316efc08ef3e0e4632b70f20e47121c8e7a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:20:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:20:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:20:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:20:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:20:55 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:20:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:20:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:20:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7327f5bd7b20a7c0c384c9bed111c54ed041e23650f2789ce160520bd54e7d64`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 8.3 MB (8300847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad441b201d110caa6bbae91773542ed3038e833916ab8fdbdee2efdd096951d`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a9b3570b577d5bd7b5702ea3b038bd6d6736da52c7e4cfa9204254b3ef6889`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 17.7 MB (17704832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687acedd268ebaa81d467b79f662cb296f999d5edc939573fc235718f10b3d5`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 26.8 MB (26774785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6738b4fa70496e709329c400187d16a1e6dcd9323aa0597219b36caeffbf73`  
		Last Modified: Wed, 25 Mar 2026 18:21:12 GMT  
		Size: 10.4 MB (10388825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0425cd14663ea2989a267ae635da01c39877aac17e1b4a26049c6e8584e9b7`  
		Last Modified: Wed, 25 Mar 2026 18:21:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7154483d9dd47aca8dda22548f6ac6381d6f297c1afcbda1c72dba31279d96f7`  
		Last Modified: Wed, 25 Mar 2026 18:21:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbfd7d41a6aa1e531936a17e36405a287262345307d1769bbf5e514f1f4955a`  
		Last Modified: Wed, 25 Mar 2026 18:21:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:4a04a0fb0422d24efcd71966c2ec778971b5a49ba8fb1934681a3c061a4f7bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8881255256c5bafe467ec0dffa5cdafa965971effe17aab0e66a451dbac7b198`

```dockerfile
```

-	Layers:
	-	`sha256:e6eb00c7bd1756168105295aa8a9f0546960e7bf78727f47d669e70e1096cc65`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:b4cf24daf2e960893a39d2f0a13a0b2b889e626725f5704295ff3c7a80e2ce56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65702900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e770b04316507e289fdbe463af8dd53873a490a5215e9664d3c38a2387b9b0bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:20:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:20:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:20:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:20:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:20:55 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:20:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:20:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:20:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9a25e5bfb326bc75a71b460d0544e0abe70b0c6c1498521b7fd245df901627`  
		Last Modified: Wed, 25 Mar 2026 18:21:05 GMT  
		Size: 7.6 MB (7597792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bd4d27cb3827cca3206705328c83ee80e164a78dc2aa97099d480bb1ded087`  
		Last Modified: Wed, 25 Mar 2026 18:21:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57192b9959272e69a74f1600a28d23141f96a9856eb275612e66d96aed4cb23`  
		Last Modified: Wed, 25 Mar 2026 18:21:05 GMT  
		Size: 17.7 MB (17694926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7afb84b0bb6525824e7b41a3eb6ca04fbd8a378336dace66c201e7f0a9fdfd`  
		Last Modified: Wed, 25 Mar 2026 18:21:06 GMT  
		Size: 26.8 MB (26754421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34cbd0d9bfc6a2fbae47c23f0d1c832eaf8aacf91c370cd7d44df319b6dcf32`  
		Last Modified: Wed, 25 Mar 2026 18:21:06 GMT  
		Size: 10.4 MB (10371888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92b6554d10f78775d85c869fd50243ef34c2f7fb06170e9bfd0f6cb1d8c722f`  
		Last Modified: Wed, 25 Mar 2026 18:21:06 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a550d751a72e95d6b192c5aa49bc54135cd12eaac778e2494033d746481e4e`  
		Last Modified: Wed, 25 Mar 2026 18:21:07 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbfd7d41a6aa1e531936a17e36405a287262345307d1769bbf5e514f1f4955a`  
		Last Modified: Wed, 25 Mar 2026 18:21:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:b36c22ea07bd32cf40c3233fe677b6cfd0b141b3c63f391124eed2843c5fe9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17c08feca64baed542d11807ef5bdc316ef9f6816d6d0e695109048771339bc`

```dockerfile
```

-	Layers:
	-	`sha256:d9a26fdeeceae1cd37f2b33208c330bcbaaa632331e7950fad92cdb05c62b6ea`  
		Last Modified: Wed, 25 Mar 2026 18:21:05 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:56cff04ad8dcf376a96423ddf5515c8bdcd171e683265335da57f17aa020ad1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65845112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee59cb9a3f85ae950ab85efdd43672abd503dbe5adcd1a55b95687f24e990ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:28:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:28:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:28:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:28:13 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:28:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:28:13 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:28:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:28:14 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:28:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:28:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:28:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7edc56943efc5fd8ceeeec0973e7862a22eef8479f31e4506aaa7683706598`  
		Last Modified: Wed, 25 Mar 2026 18:28:21 GMT  
		Size: 8.5 MB (8453635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d7bdfa7dc871c3af6f5b34ef1ef53c930b2fde5801879b794f1849da1dc4d`  
		Last Modified: Wed, 25 Mar 2026 18:28:20 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c366b69bd090a1557acbb6f1ebdab176751b61ca7e1c82af675fd5dd30436a`  
		Last Modified: Wed, 25 Mar 2026 18:28:21 GMT  
		Size: 17.5 MB (17476961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b74c99f62156a67a1a2f1edfa046c0c13825a6cdef351e68e41cbbffd8badb`  
		Last Modified: Wed, 25 Mar 2026 18:28:22 GMT  
		Size: 25.7 MB (25732670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fed48b65e655b617bf78f3b0c6df9994322561de4c1c4a706e621ec83f8fb84`  
		Last Modified: Wed, 25 Mar 2026 18:28:22 GMT  
		Size: 10.0 MB (9982606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318a3b2c176f6893caa80c95a652634492e38503c58e091a916b6d9c341a0648`  
		Last Modified: Wed, 25 Mar 2026 18:28:23 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c910ec30db0949d800f54bb9c1b3c4e2af20695bf5b14f43f4f9be42a0ecb2c`  
		Last Modified: Wed, 25 Mar 2026 18:28:23 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd0d057ad753e2ef837845dd9504265e602e0802dceee1b0083e05f00291b8c`  
		Last Modified: Wed, 25 Mar 2026 18:28:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:a3331dd737a9d4ad382fff64040bbad2660884a99286e44af8338a00851aec68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ed74d502ab8399d1e1a43c9de66bf070e1741c40c8a187c876aa031385bd08`

```dockerfile
```

-	Layers:
	-	`sha256:5de0f8302079e7f4909158e85e3fcabf6c532e1b84c2c25003b4bf3343ea0e94`  
		Last Modified: Wed, 25 Mar 2026 18:28:21 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:1ba18449911d01f477a3fc104123c85d677addc60701b14b3fcb5381f9c4a537
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
$ docker pull docker@sha256:e60900b4413a183173b0c12a7c34bfa7ba511fd074147a1b7974ebb296a0050b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144453044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5b3ee3882d4d0af9fc139d2545bf1d17e251c849e98b98da2fe418431e2ad8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:46:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:46:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:46:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:46:28 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:46:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:46:28 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:46:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:46:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:46:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:46:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:46:30 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:10:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:10:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:10:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:10:30 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f1c7a58cda4399b7be2fb8427c3b756917df1abb433e17a98888259aa70c83`  
		Last Modified: Thu, 05 Mar 2026 18:46:37 GMT  
		Size: 8.4 MB (8399691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba58ca1e42e5eeec21273f066c06e25afee78a5211c7d6deb38ba545b7d6240`  
		Last Modified: Thu, 05 Mar 2026 18:46:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f8c3243c30359f68ee8e1f96a24d246ca1357a82d8b30de9a33e9d282d93e1`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 18.9 MB (18919365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e9c4ffbcbf205284b573f955de57155f10b92234b491b2127720a57c90c1ce`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 28.5 MB (28516523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34962ed90623b311790e104f78a280cdc54a1ce559635328476148c6fc522888`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 11.0 MB (10953934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a9731c772a36b5ae18988bc0c1c69aff62cb86d597f2de367c5b330fb8d459`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a294ee3d24d1214f1944e57dadb6ef9c4b434a1a170e348838dafb16d31127`  
		Last Modified: Thu, 05 Mar 2026 18:46:39 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df03e33ed496925038509c0abcd9f087ab5ec4e4b917ed51730d71d63a87c91`  
		Last Modified: Thu, 05 Mar 2026 18:46:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fbd819f55b555293ac19eaaa17fd0ff75f9812f924da0a56610f334b1db8e6`  
		Last Modified: Thu, 05 Mar 2026 19:10:41 GMT  
		Size: 6.9 MB (6934736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524d6d9cccdc6fa4c04046756dada64359f4445d625ae2d4653714afad9044c`  
		Last Modified: Thu, 05 Mar 2026 19:10:40 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4da28e0bc44f1c47c50aab943753bc5626ab338c9dacd7cff96381acf13793`  
		Last Modified: Thu, 05 Mar 2026 19:10:41 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503f0e2071dd914a67c23aa1b570c3fccb863ebac670fa0d253ff15658adaf0a`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 66.8 MB (66766357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdcbaa55207a60126845f61a87ad8fbea9e87874674046ea2133cb2f3159d36`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bd5217468716f0f037bdb54d7c022dbf95c6896f29dc171a9677f86f621c25`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:51f66381d79e85e83914402852c9997eddc9b6c3b280e0aa86c37f2a4ba27738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8ef8f35ce741ad2c83d3a11a6b0eabe3616860c0a9fd2deba0d9b603978bf0`

```dockerfile
```

-	Layers:
	-	`sha256:9de809ee0c1e4804fb0ce3ce24f183e971a8f1020e5d25d1eba9202ecfb23554`  
		Last Modified: Thu, 05 Mar 2026 19:10:40 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:921ed9ba3b685e60ee0cdcd138b4aa718d396a4e4e1418de3348b766229448c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136262850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739701c78bbbb4755e7b5694d8e2032e7edaca1f5ab49ddc7c1bcef1e289abbe`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:45:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:45:36 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:45:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:45:39 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:45:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:45:39 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:45:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:45:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:45:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:45:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:45:43 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:08:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:08:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:08:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:08:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:08:49 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:08:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:08:49 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0593a5009b5f1611e29afa031add0caa8e17436567b91fa0cd2b29e51d22c89`  
		Last Modified: Thu, 05 Mar 2026 18:45:50 GMT  
		Size: 8.3 MB (8300931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aae9fbc3eb9720394677e4ecd6aab19d036b3e73b352fb74b67d6b3a2fc9fa6`  
		Last Modified: Thu, 05 Mar 2026 18:45:50 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d66dff73ca29a47e9b6b4c6c761a4d7aa8867dca97bc28872f55bf9f47e2c6`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 17.7 MB (17698879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2808c066fd3febfd5f5674816180176477b47da3158ad376e658eb6d8136fab1`  
		Last Modified: Thu, 05 Mar 2026 18:45:51 GMT  
		Size: 26.8 MB (26774787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663b0b4076c27408b2184d77a831c36817e8a8d8d4897cb92fce9cdd0165335a`  
		Last Modified: Thu, 05 Mar 2026 18:45:51 GMT  
		Size: 10.4 MB (10385429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3615b056b4ef975abfd3ae24796393abcb6cd5c819f1c8a6e68c1488f641f1a`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32f9cb2f283cf611fe753cefc9ac89c970b2a82e793b029047ec9a74dd88da4`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5dc68331a182d6047cc64dc01811876321654c40481e65df941bf21d1129ff`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281309e002e2014f85aa6e60f8f56d3a46cd826258710ea23f02ebd55fa56d86`  
		Last Modified: Thu, 05 Mar 2026 19:08:59 GMT  
		Size: 7.3 MB (7271697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d5638366f0629a45399b2da5bc12e7eaec99cd43a172c0e00a061cbad07fd9`  
		Last Modified: Thu, 05 Mar 2026 19:08:58 GMT  
		Size: 91.8 KB (91788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db525e8a11303b587a4637ce4f7e8cf2e27b87515229e415c66b907d6857c14`  
		Last Modified: Thu, 05 Mar 2026 19:08:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b41beca4d05ad9f4f8a0af06864a9b0bd92eb236aae78aec36d96eee3e972e7`  
		Last Modified: Thu, 05 Mar 2026 19:09:00 GMT  
		Size: 62.2 MB (62161362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c988857a21079067d802211bb65b801edbebcc1e6e21bd8e6e7eea98dc58fc`  
		Last Modified: Thu, 05 Mar 2026 19:09:00 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0de727742fa3feb2ba852cdaa770c212967433c39bb41ebfe1865a9ffcc78e`  
		Last Modified: Thu, 05 Mar 2026 19:09:00 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:01e39cec6c99783d318713cb96e9d665690e384f821039d02ecc3d40d501c51d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c18a85619e7433b908f936509e5dbd40bb98ace79929f60a844a1db3c93374`

```dockerfile
```

-	Layers:
	-	`sha256:d37d617810772a2c79e6330f2dbaf0e418ffcc3f2db333b8443afe97f45e219b`  
		Last Modified: Thu, 05 Mar 2026 19:08:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:74ea5cdbe2fe4518d73e3ac0241167a38c7616c3dd6be011cf48fc0a61189c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134355560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9d940d504e1f821c76a9e400c405dfbc51b3d58990d7abaae29dd773c08694`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:46:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:46:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:46:32 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:46:36 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:46:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:46:36 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:46:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:46:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:46:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:46:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:46:40 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:09:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:09:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:09:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:09:20 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:09:20 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:09:20 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:09:20 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95152b95c4ccfeb5059ced14a96c4f1c17872baa3e875c18056cb5bed1b56676`  
		Last Modified: Thu, 05 Mar 2026 18:46:46 GMT  
		Size: 7.6 MB (7597774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d532e57eb4774540148a1cccd311fc10645e4dc68e8512d6b4f5a07d77498e82`  
		Last Modified: Thu, 05 Mar 2026 18:46:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64983bc952c232855d431fc0da6e3080f4c4c64fc0dce721c1086cc916d3037`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 17.7 MB (17691333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0552f021a975b88c2f33fc3057737b716d29921dcf12fff1a7bd017272ee52bf`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 26.8 MB (26754433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe274cdce52e0d95eda23b7407fdd0cd8a861a2014d8a240bda6be387b22c74`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 10.4 MB (10369783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28feee09383ef1673e7a0cec5e45cf0ad41f8b64208682ad535da48f8de7e08e`  
		Last Modified: Thu, 05 Mar 2026 18:46:48 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c266b2e92e5c06c3362ac89279eac9742220da712ded40590f3312de938eb16a`  
		Last Modified: Thu, 05 Mar 2026 18:46:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b204129a9de694faa70c2c825548fbe88d190e24ecc2d949a3ea099c0ac40d3`  
		Last Modified: Thu, 05 Mar 2026 18:46:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6011a406c6080a98a187e060555bd77450686dc8a0a3a1bd21a8b635e7a7c7c5`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 6.6 MB (6573025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63255cd848e2b7900e0177b225137079a3c0e9bde16e58d50a40edba81e6b028`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 88.2 KB (88150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3758bf28f38de089029226cd958aeeb1d75194761390a5bd605206ae3d4092e3`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbec48042bff8bd1621f0f9cd3d2ec81bc03fdba86235b7e6586dec177d82907`  
		Last Modified: Thu, 05 Mar 2026 19:09:32 GMT  
		Size: 62.0 MB (61991183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f8030e199452b1b297f3a4acc28ce81ecd590b3b41343eb4dbb260d0a03684`  
		Last Modified: Thu, 05 Mar 2026 19:09:31 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a7939d77fae184c61e7cbceee2129945aff07b2c8ba46170605cd266cdee9f`  
		Last Modified: Thu, 05 Mar 2026 19:09:31 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:0d74abb912009d5524b2bc08d235dd65785a6a9c105843b2d5f2e38d9740c01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e7a73ef832c7e6998b93ef231c73a0f5a4b733dd27635018b7ccc4808f8859`

```dockerfile
```

-	Layers:
	-	`sha256:dfe982715ef650b1926988aa185ecef3d257673538c7392c6271f6a59a023df3`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 34.7 KB (34721 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1d1d67ba557d1ccedcd46d05ba832276e65260a518c240b087c71849cd6cbce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133716998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2468f972a259c78d9053fa37f4ca40d54c8071086fecff98d4e0f4829c120c36`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:44:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:44:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:44:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:44:32 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:44:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:44:32 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:44:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:44:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:44:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:44:34 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:10:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:10:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:10:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:10:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:10:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:10:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:10:13 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74f52f7948b98f731cc47a7da43a1a028f38396d447d93fa458cc7b1ee9ade0`  
		Last Modified: Thu, 05 Mar 2026 18:44:41 GMT  
		Size: 8.5 MB (8453572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50de1b9f6ee9b0bb47a9cb5e7877595782f60dc2d6c014088cfb72c4dca02106`  
		Last Modified: Thu, 05 Mar 2026 18:44:40 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8cd16e98d03b1081e8606a566c45e24d404e6738ce672011e2f5e3fe3b637b`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 17.5 MB (17472694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a548a65df6cf925e933ead68a3677913c3c9586d7115d161b6afd378cd8b1836`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 25.7 MB (25732665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09bdc4530b81e1aa74fe3d0322209932119b3cb64a72447d5442bd9c50cd4ed`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 10.0 MB (9974089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b96e65028eacc3700698877e774e4bfbca321b41420638481e753d07449225c`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faab51bb66faa3b0c0d737ebc09cfb486e94acbcdc20e883d8022102e4fc2fd`  
		Last Modified: Thu, 05 Mar 2026 18:44:43 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd02735b351188e3d18abc71b56816ddc7406e1d55c433166d34e8fd46aa5692`  
		Last Modified: Thu, 05 Mar 2026 18:44:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bd6c43d314f7ba1970375218d37bf189ee9e325f65b8a993a3846b8b081490`  
		Last Modified: Thu, 05 Mar 2026 19:10:23 GMT  
		Size: 7.2 MB (7213319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447b7408aabced1a21d26cecd53e54c14e75f0c7fa49a892e88b3faa8618791d`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 101.3 KB (101302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a4786ffc77dd17db34d4bd2edde2706bdb8bde49e2f5c532ffdb910ab16ee9`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce02e419a084f596f3e92c28731f67e0f113c3464b10ce77db5f722f7da9d1d`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 60.6 MB (60564110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf5b1f083f16666d8e3ef65369ed92093b78752eb5146941526e49b6d31965e`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720b8605e7f2e52dd9a65c8e463ab396a44abc68a0a689a3eda9a497503540fb`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:f842673f5ac13d592cac6534e468f00a1d0270c7b8b686dff5ede372d952ad2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aec29e8d6f9254e8a5488aabb8ce917d657467f43e13af6528879dc1f2bfe02`

```dockerfile
```

-	Layers:
	-	`sha256:d59a3392ae448d26d8ed94f620ba9496be18d97cce5dc57e5943d287b049c800`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:7b90623a6a8d610e766d0dda84f20c7fbafeefe68a83ba01ecb4d6921b777b49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:aeab8c8ba5bd982ecd69b6f302e87c02eb66dd2fa3db5a8c5e81366e35960cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165252061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089ebb0bf68cbe13e627bb94ebca07973c936be52099f607c90ededbd35a2a90`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:46:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:46:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:46:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:46:28 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:46:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:46:28 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:46:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:46:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:46:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:46:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:46:30 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:10:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:10:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:10:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:10:30 GMT
CMD []
# Thu, 05 Mar 2026 19:51:35 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 05 Mar 2026 19:51:35 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 05 Mar 2026 19:51:35 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:51:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 05 Mar 2026 19:51:36 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 05 Mar 2026 19:51:36 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 05 Mar 2026 19:51:36 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f1c7a58cda4399b7be2fb8427c3b756917df1abb433e17a98888259aa70c83`  
		Last Modified: Thu, 05 Mar 2026 18:46:37 GMT  
		Size: 8.4 MB (8399691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba58ca1e42e5eeec21273f066c06e25afee78a5211c7d6deb38ba545b7d6240`  
		Last Modified: Thu, 05 Mar 2026 18:46:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f8c3243c30359f68ee8e1f96a24d246ca1357a82d8b30de9a33e9d282d93e1`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 18.9 MB (18919365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e9c4ffbcbf205284b573f955de57155f10b92234b491b2127720a57c90c1ce`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 28.5 MB (28516523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34962ed90623b311790e104f78a280cdc54a1ce559635328476148c6fc522888`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 11.0 MB (10953934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a9731c772a36b5ae18988bc0c1c69aff62cb86d597f2de367c5b330fb8d459`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a294ee3d24d1214f1944e57dadb6ef9c4b434a1a170e348838dafb16d31127`  
		Last Modified: Thu, 05 Mar 2026 18:46:39 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df03e33ed496925038509c0abcd9f087ab5ec4e4b917ed51730d71d63a87c91`  
		Last Modified: Thu, 05 Mar 2026 18:46:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fbd819f55b555293ac19eaaa17fd0ff75f9812f924da0a56610f334b1db8e6`  
		Last Modified: Thu, 05 Mar 2026 19:10:41 GMT  
		Size: 6.9 MB (6934736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524d6d9cccdc6fa4c04046756dada64359f4445d625ae2d4653714afad9044c`  
		Last Modified: Thu, 05 Mar 2026 19:10:40 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4da28e0bc44f1c47c50aab943753bc5626ab338c9dacd7cff96381acf13793`  
		Last Modified: Thu, 05 Mar 2026 19:10:41 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503f0e2071dd914a67c23aa1b570c3fccb863ebac670fa0d253ff15658adaf0a`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 66.8 MB (66766357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdcbaa55207a60126845f61a87ad8fbea9e87874674046ea2133cb2f3159d36`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bd5217468716f0f037bdb54d7c022dbf95c6896f29dc171a9677f86f621c25`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624e0d70ccddab2837c7579988be593d7d2c14e98ecc0951b4b4b1d0159ea2e8`  
		Last Modified: Thu, 05 Mar 2026 19:51:42 GMT  
		Size: 3.4 MB (3419929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed14991c62b9a9ef3cfc532d6532e4fd5343461fd35c558d71b52fe601b961`  
		Last Modified: Thu, 05 Mar 2026 19:51:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ac276d93a270a03f1cf58e6899d6a02fad81464e22001619436513cbe7e0e8`  
		Last Modified: Thu, 05 Mar 2026 19:51:42 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0161c5d6b742bdaefd9ac5d339340963166794c14b9e069af0f39fac4010597a`  
		Last Modified: Thu, 05 Mar 2026 19:51:42 GMT  
		Size: 17.4 MB (17377747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cf600d07eddbd5c5e7f2c80032ccc565bdd549c0193703940b5508312e509a`  
		Last Modified: Thu, 05 Mar 2026 19:51:43 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c3581ae9fc196cbf20a722387b0d4f4395cdf30ea836abc781891c9019939fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b9e467c6ab22b4a83c306b278852334102b54e6919ef4adfeaf8977ad9641b`

```dockerfile
```

-	Layers:
	-	`sha256:4b084f57f37ad05ae58136fd5d64bd79f05ca02c03ff4358cb8c35475b49240e`  
		Last Modified: Thu, 05 Mar 2026 19:51:41 GMT  
		Size: 30.6 KB (30588 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:363611f480e6222f4c95e0fe9b92d68e16add9b4f390fc53d681084c4b60caee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154825064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05963d5fac11223eb3f65b15aa06ef12c1a799eeb4b5bb56d79bd428436e0cd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:44:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:44:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:44:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:44:32 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:44:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:44:32 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:44:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:44:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:44:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:44:34 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:10:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:10:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:10:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:10:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:10:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:10:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:10:13 GMT
CMD []
# Thu, 05 Mar 2026 19:52:11 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 05 Mar 2026 19:52:11 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 05 Mar 2026 19:52:11 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:52:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 05 Mar 2026 19:52:12 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 05 Mar 2026 19:52:12 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 05 Mar 2026 19:52:12 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74f52f7948b98f731cc47a7da43a1a028f38396d447d93fa458cc7b1ee9ade0`  
		Last Modified: Thu, 05 Mar 2026 18:44:41 GMT  
		Size: 8.5 MB (8453572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50de1b9f6ee9b0bb47a9cb5e7877595782f60dc2d6c014088cfb72c4dca02106`  
		Last Modified: Thu, 05 Mar 2026 18:44:40 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8cd16e98d03b1081e8606a566c45e24d404e6738ce672011e2f5e3fe3b637b`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 17.5 MB (17472694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a548a65df6cf925e933ead68a3677913c3c9586d7115d161b6afd378cd8b1836`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 25.7 MB (25732665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09bdc4530b81e1aa74fe3d0322209932119b3cb64a72447d5442bd9c50cd4ed`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 10.0 MB (9974089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b96e65028eacc3700698877e774e4bfbca321b41420638481e753d07449225c`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faab51bb66faa3b0c0d737ebc09cfb486e94acbcdc20e883d8022102e4fc2fd`  
		Last Modified: Thu, 05 Mar 2026 18:44:43 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd02735b351188e3d18abc71b56816ddc7406e1d55c433166d34e8fd46aa5692`  
		Last Modified: Thu, 05 Mar 2026 18:44:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bd6c43d314f7ba1970375218d37bf189ee9e325f65b8a993a3846b8b081490`  
		Last Modified: Thu, 05 Mar 2026 19:10:23 GMT  
		Size: 7.2 MB (7213319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447b7408aabced1a21d26cecd53e54c14e75f0c7fa49a892e88b3faa8618791d`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 101.3 KB (101302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a4786ffc77dd17db34d4bd2edde2706bdb8bde49e2f5c532ffdb910ab16ee9`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce02e419a084f596f3e92c28731f67e0f113c3464b10ce77db5f722f7da9d1d`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 60.6 MB (60564110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf5b1f083f16666d8e3ef65369ed92093b78752eb5146941526e49b6d31965e`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720b8605e7f2e52dd9a65c8e463ab396a44abc68a0a689a3eda9a497503540fb`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113a99610f0313cefac114163c823cc19536cc5ad728c999ce1c42a08df7b73e`  
		Last Modified: Thu, 05 Mar 2026 19:52:19 GMT  
		Size: 3.4 MB (3394381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f83f706c62205d1a7b78b43438268f91f5a1c97ce0aa6d9e895c6ccb93e6aaa`  
		Last Modified: Thu, 05 Mar 2026 19:52:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8ea4b65def4cea71f744e7c03f2bd0f14403430efba1dde697830900fd9220`  
		Last Modified: Thu, 05 Mar 2026 19:52:19 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d663f5f609d1ca281ed28345736bdf222b960707ccb29edd7d2fca31fffcce`  
		Last Modified: Thu, 05 Mar 2026 19:52:19 GMT  
		Size: 17.7 MB (17712346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fc8e3e13278240d699ba378e763c538e98fc43342e3c86b0625b503863f3f0`  
		Last Modified: Thu, 05 Mar 2026 19:52:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:419ad745bdc70ba4c204674efbc833c2b1eaff3596fbdf95c23b80444589037d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8693634da1b98934154ee830afbd8beb888c8ede561915c13c94c94ca449c750`

```dockerfile
```

-	Layers:
	-	`sha256:df3b03f6dd4be8fab2827638b57709b438a0bab274edac98ada56265237fec2c`  
		Last Modified: Thu, 05 Mar 2026 19:52:18 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:1ba18449911d01f477a3fc104123c85d677addc60701b14b3fcb5381f9c4a537
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
$ docker pull docker@sha256:e60900b4413a183173b0c12a7c34bfa7ba511fd074147a1b7974ebb296a0050b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144453044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5b3ee3882d4d0af9fc139d2545bf1d17e251c849e98b98da2fe418431e2ad8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:46:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:46:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:46:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:46:28 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:46:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:46:28 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:46:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:46:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:46:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:46:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:46:30 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:10:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:10:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:10:30 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:10:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:10:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:10:30 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f1c7a58cda4399b7be2fb8427c3b756917df1abb433e17a98888259aa70c83`  
		Last Modified: Thu, 05 Mar 2026 18:46:37 GMT  
		Size: 8.4 MB (8399691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba58ca1e42e5eeec21273f066c06e25afee78a5211c7d6deb38ba545b7d6240`  
		Last Modified: Thu, 05 Mar 2026 18:46:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f8c3243c30359f68ee8e1f96a24d246ca1357a82d8b30de9a33e9d282d93e1`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 18.9 MB (18919365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e9c4ffbcbf205284b573f955de57155f10b92234b491b2127720a57c90c1ce`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 28.5 MB (28516523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34962ed90623b311790e104f78a280cdc54a1ce559635328476148c6fc522888`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 11.0 MB (10953934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a9731c772a36b5ae18988bc0c1c69aff62cb86d597f2de367c5b330fb8d459`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a294ee3d24d1214f1944e57dadb6ef9c4b434a1a170e348838dafb16d31127`  
		Last Modified: Thu, 05 Mar 2026 18:46:39 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df03e33ed496925038509c0abcd9f087ab5ec4e4b917ed51730d71d63a87c91`  
		Last Modified: Thu, 05 Mar 2026 18:46:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fbd819f55b555293ac19eaaa17fd0ff75f9812f924da0a56610f334b1db8e6`  
		Last Modified: Thu, 05 Mar 2026 19:10:41 GMT  
		Size: 6.9 MB (6934736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524d6d9cccdc6fa4c04046756dada64359f4445d625ae2d4653714afad9044c`  
		Last Modified: Thu, 05 Mar 2026 19:10:40 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4da28e0bc44f1c47c50aab943753bc5626ab338c9dacd7cff96381acf13793`  
		Last Modified: Thu, 05 Mar 2026 19:10:41 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503f0e2071dd914a67c23aa1b570c3fccb863ebac670fa0d253ff15658adaf0a`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 66.8 MB (66766357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdcbaa55207a60126845f61a87ad8fbea9e87874674046ea2133cb2f3159d36`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bd5217468716f0f037bdb54d7c022dbf95c6896f29dc171a9677f86f621c25`  
		Last Modified: Thu, 05 Mar 2026 19:10:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:51f66381d79e85e83914402852c9997eddc9b6c3b280e0aa86c37f2a4ba27738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8ef8f35ce741ad2c83d3a11a6b0eabe3616860c0a9fd2deba0d9b603978bf0`

```dockerfile
```

-	Layers:
	-	`sha256:9de809ee0c1e4804fb0ce3ce24f183e971a8f1020e5d25d1eba9202ecfb23554`  
		Last Modified: Thu, 05 Mar 2026 19:10:40 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:921ed9ba3b685e60ee0cdcd138b4aa718d396a4e4e1418de3348b766229448c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136262850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739701c78bbbb4755e7b5694d8e2032e7edaca1f5ab49ddc7c1bcef1e289abbe`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:45:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:45:36 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:45:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:45:39 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:45:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:45:39 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:45:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:45:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:45:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:45:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:45:43 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:08:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:08:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:08:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:08:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:08:49 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:08:49 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:08:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:08:49 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0593a5009b5f1611e29afa031add0caa8e17436567b91fa0cd2b29e51d22c89`  
		Last Modified: Thu, 05 Mar 2026 18:45:50 GMT  
		Size: 8.3 MB (8300931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aae9fbc3eb9720394677e4ecd6aab19d036b3e73b352fb74b67d6b3a2fc9fa6`  
		Last Modified: Thu, 05 Mar 2026 18:45:50 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d66dff73ca29a47e9b6b4c6c761a4d7aa8867dca97bc28872f55bf9f47e2c6`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 17.7 MB (17698879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2808c066fd3febfd5f5674816180176477b47da3158ad376e658eb6d8136fab1`  
		Last Modified: Thu, 05 Mar 2026 18:45:51 GMT  
		Size: 26.8 MB (26774787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663b0b4076c27408b2184d77a831c36817e8a8d8d4897cb92fce9cdd0165335a`  
		Last Modified: Thu, 05 Mar 2026 18:45:51 GMT  
		Size: 10.4 MB (10385429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3615b056b4ef975abfd3ae24796393abcb6cd5c819f1c8a6e68c1488f641f1a`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32f9cb2f283cf611fe753cefc9ac89c970b2a82e793b029047ec9a74dd88da4`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5dc68331a182d6047cc64dc01811876321654c40481e65df941bf21d1129ff`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281309e002e2014f85aa6e60f8f56d3a46cd826258710ea23f02ebd55fa56d86`  
		Last Modified: Thu, 05 Mar 2026 19:08:59 GMT  
		Size: 7.3 MB (7271697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d5638366f0629a45399b2da5bc12e7eaec99cd43a172c0e00a061cbad07fd9`  
		Last Modified: Thu, 05 Mar 2026 19:08:58 GMT  
		Size: 91.8 KB (91788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db525e8a11303b587a4637ce4f7e8cf2e27b87515229e415c66b907d6857c14`  
		Last Modified: Thu, 05 Mar 2026 19:08:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b41beca4d05ad9f4f8a0af06864a9b0bd92eb236aae78aec36d96eee3e972e7`  
		Last Modified: Thu, 05 Mar 2026 19:09:00 GMT  
		Size: 62.2 MB (62161362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c988857a21079067d802211bb65b801edbebcc1e6e21bd8e6e7eea98dc58fc`  
		Last Modified: Thu, 05 Mar 2026 19:09:00 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0de727742fa3feb2ba852cdaa770c212967433c39bb41ebfe1865a9ffcc78e`  
		Last Modified: Thu, 05 Mar 2026 19:09:00 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:01e39cec6c99783d318713cb96e9d665690e384f821039d02ecc3d40d501c51d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c18a85619e7433b908f936509e5dbd40bb98ace79929f60a844a1db3c93374`

```dockerfile
```

-	Layers:
	-	`sha256:d37d617810772a2c79e6330f2dbaf0e418ffcc3f2db333b8443afe97f45e219b`  
		Last Modified: Thu, 05 Mar 2026 19:08:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:74ea5cdbe2fe4518d73e3ac0241167a38c7616c3dd6be011cf48fc0a61189c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134355560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9d940d504e1f821c76a9e400c405dfbc51b3d58990d7abaae29dd773c08694`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:46:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:46:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:46:32 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:46:36 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:46:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:46:36 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:46:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:46:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:46:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:46:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:46:40 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:09:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:09:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:09:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:09:20 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:09:20 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:09:20 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:09:20 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:09:20 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95152b95c4ccfeb5059ced14a96c4f1c17872baa3e875c18056cb5bed1b56676`  
		Last Modified: Thu, 05 Mar 2026 18:46:46 GMT  
		Size: 7.6 MB (7597774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d532e57eb4774540148a1cccd311fc10645e4dc68e8512d6b4f5a07d77498e82`  
		Last Modified: Thu, 05 Mar 2026 18:46:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64983bc952c232855d431fc0da6e3080f4c4c64fc0dce721c1086cc916d3037`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 17.7 MB (17691333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0552f021a975b88c2f33fc3057737b716d29921dcf12fff1a7bd017272ee52bf`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 26.8 MB (26754433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe274cdce52e0d95eda23b7407fdd0cd8a861a2014d8a240bda6be387b22c74`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 10.4 MB (10369783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28feee09383ef1673e7a0cec5e45cf0ad41f8b64208682ad535da48f8de7e08e`  
		Last Modified: Thu, 05 Mar 2026 18:46:48 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c266b2e92e5c06c3362ac89279eac9742220da712ded40590f3312de938eb16a`  
		Last Modified: Thu, 05 Mar 2026 18:46:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b204129a9de694faa70c2c825548fbe88d190e24ecc2d949a3ea099c0ac40d3`  
		Last Modified: Thu, 05 Mar 2026 18:46:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6011a406c6080a98a187e060555bd77450686dc8a0a3a1bd21a8b635e7a7c7c5`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 6.6 MB (6573025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63255cd848e2b7900e0177b225137079a3c0e9bde16e58d50a40edba81e6b028`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 88.2 KB (88150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3758bf28f38de089029226cd958aeeb1d75194761390a5bd605206ae3d4092e3`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbec48042bff8bd1621f0f9cd3d2ec81bc03fdba86235b7e6586dec177d82907`  
		Last Modified: Thu, 05 Mar 2026 19:09:32 GMT  
		Size: 62.0 MB (61991183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f8030e199452b1b297f3a4acc28ce81ecd590b3b41343eb4dbb260d0a03684`  
		Last Modified: Thu, 05 Mar 2026 19:09:31 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a7939d77fae184c61e7cbceee2129945aff07b2c8ba46170605cd266cdee9f`  
		Last Modified: Thu, 05 Mar 2026 19:09:31 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:0d74abb912009d5524b2bc08d235dd65785a6a9c105843b2d5f2e38d9740c01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e7a73ef832c7e6998b93ef231c73a0f5a4b733dd27635018b7ccc4808f8859`

```dockerfile
```

-	Layers:
	-	`sha256:dfe982715ef650b1926988aa185ecef3d257673538c7392c6271f6a59a023df3`  
		Last Modified: Thu, 05 Mar 2026 19:09:30 GMT  
		Size: 34.7 KB (34721 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1d1d67ba557d1ccedcd46d05ba832276e65260a518c240b087c71849cd6cbce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133716998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2468f972a259c78d9053fa37f4ca40d54c8071086fecff98d4e0f4829c120c36`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:44:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:44:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:44:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:44:32 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:44:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:44:32 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:44:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:44:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:44:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:44:34 GMT
CMD ["sh"]
# Thu, 05 Mar 2026 19:10:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Mar 2026 19:10:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Mar 2026 19:10:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Mar 2026 19:10:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 19:10:13 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Mar 2026 19:10:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Mar 2026 19:10:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Mar 2026 19:10:13 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74f52f7948b98f731cc47a7da43a1a028f38396d447d93fa458cc7b1ee9ade0`  
		Last Modified: Thu, 05 Mar 2026 18:44:41 GMT  
		Size: 8.5 MB (8453572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50de1b9f6ee9b0bb47a9cb5e7877595782f60dc2d6c014088cfb72c4dca02106`  
		Last Modified: Thu, 05 Mar 2026 18:44:40 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8cd16e98d03b1081e8606a566c45e24d404e6738ce672011e2f5e3fe3b637b`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 17.5 MB (17472694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a548a65df6cf925e933ead68a3677913c3c9586d7115d161b6afd378cd8b1836`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 25.7 MB (25732665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09bdc4530b81e1aa74fe3d0322209932119b3cb64a72447d5442bd9c50cd4ed`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 10.0 MB (9974089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b96e65028eacc3700698877e774e4bfbca321b41420638481e753d07449225c`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faab51bb66faa3b0c0d737ebc09cfb486e94acbcdc20e883d8022102e4fc2fd`  
		Last Modified: Thu, 05 Mar 2026 18:44:43 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd02735b351188e3d18abc71b56816ddc7406e1d55c433166d34e8fd46aa5692`  
		Last Modified: Thu, 05 Mar 2026 18:44:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bd6c43d314f7ba1970375218d37bf189ee9e325f65b8a993a3846b8b081490`  
		Last Modified: Thu, 05 Mar 2026 19:10:23 GMT  
		Size: 7.2 MB (7213319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447b7408aabced1a21d26cecd53e54c14e75f0c7fa49a892e88b3faa8618791d`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 101.3 KB (101302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a4786ffc77dd17db34d4bd2edde2706bdb8bde49e2f5c532ffdb910ab16ee9`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce02e419a084f596f3e92c28731f67e0f113c3464b10ce77db5f722f7da9d1d`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 60.6 MB (60564110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf5b1f083f16666d8e3ef65369ed92093b78752eb5146941526e49b6d31965e`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720b8605e7f2e52dd9a65c8e463ab396a44abc68a0a689a3eda9a497503540fb`  
		Last Modified: Thu, 05 Mar 2026 19:10:24 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:f842673f5ac13d592cac6534e468f00a1d0270c7b8b686dff5ede372d952ad2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aec29e8d6f9254e8a5488aabb8ce917d657467f43e13af6528879dc1f2bfe02`

```dockerfile
```

-	Layers:
	-	`sha256:d59a3392ae448d26d8ed94f620ba9496be18d97cce5dc57e5943d287b049c800`  
		Last Modified: Thu, 05 Mar 2026 19:10:22 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:fdd48859b2b14b2fa4af458fcea153cfd95e8ce7429e66286229f28b47e507b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `docker:windowsservercore` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:42419a818a06c8b0bdb32d28efe864c1965f849d4d58dac6450fb35578530636
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2142463243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095982a564f926ffd785368388022d0f792a5f393f83c25b2b334b3f0ee3c25f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Wed, 25 Mar 2026 18:28:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Mar 2026 18:29:47 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Mar 2026 18:29:48 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.1.zip
# Wed, 25 Mar 2026 18:30:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Mar 2026 18:30:11 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:30:12 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.windows-amd64.exe
# Wed, 25 Mar 2026 18:30:13 GMT
ENV DOCKER_BUILDX_SHA256=47d76e47acf3c7611dd594c4b0909fec680ae6406b6fa775f6077b195837e2b9
# Wed, 25 Mar 2026 18:30:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Mar 2026 18:30:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:30:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Wed, 25 Mar 2026 18:30:37 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Wed, 25 Mar 2026 18:30:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c48ff63fd51e54c1621e1ef191ba1ffb5babb91295c52763e73038877ddbcc0`  
		Last Modified: Wed, 25 Mar 2026 18:30:56 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05646e87bcc7eebcf75f1a96ca80aa255bd6868601cdf94768601c8078d9b4b7`  
		Last Modified: Wed, 25 Mar 2026 18:30:55 GMT  
		Size: 374.0 KB (373997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edba92fa22a5c1bc563c18f651db43bfdc9c0720c21fff8d046d759875e121d1`  
		Last Modified: Wed, 25 Mar 2026 18:30:54 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b934d13e109edc08e9a08ca989659aded111b61867e75aa39cc626586e14b6d`  
		Last Modified: Wed, 25 Mar 2026 18:30:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff304ba5506cff7b400064688c74084a2ff60a244b484160e1be812e7672e3d`  
		Last Modified: Wed, 25 Mar 2026 18:30:56 GMT  
		Size: 19.6 MB (19594910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47622b1e857ba4fe582334af32ea59c3b58783ab368030f1d2259ae216996aaa`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a676a9fc9cb7650a5a61aad602e864237a2410b300b3babac5f0cfb4c9f31bf9`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d698051d32bbd456b5de7801253c16270739faf8954ce78f45f3a7e95830067`  
		Last Modified: Wed, 25 Mar 2026 18:30:52 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b8f6f29800e2912ff8cd1d9696f47141cb71560b98c73b71157c6b39d77665`  
		Last Modified: Wed, 25 Mar 2026 18:31:04 GMT  
		Size: 29.6 MB (29639971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbee4f4914616df04e2f56d66e020a4ca506723690da654928872871a3d1130`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36549e61114f7f53657411a2bc956fd69c15ae2f08beb6f977143978b7447c7a`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111317c19214d92002469ac71ea269b2b838ae7163f090cf6796b17aeccea76d`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee1dd44d7e561101a0c094be20961ded0b2b663201441b16b06bbace8b589ab`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 11.6 MB (11646539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:9504c71617f036da76201851ee9ad86ea91a1f572837a6e9e49023ace0612bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull docker@sha256:7218b6c6fbe208207908f94f1ed696b4bd01423d2c443586c5f65031c5e0e93e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2043597626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378ba248bb85f2c6fe57c779e2da6f4c4498116174b27197870a8f9ee1d337d4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 21:55:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Mar 2026 21:55:45 GMT
ENV DOCKER_VERSION=29.3.0
# Tue, 10 Mar 2026 21:55:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.0.zip
# Tue, 10 Mar 2026 21:56:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 21:56:04 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Tue, 10 Mar 2026 21:56:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.windows-amd64.exe
# Tue, 10 Mar 2026 21:56:05 GMT
ENV DOCKER_BUILDX_SHA256=47d76e47acf3c7611dd594c4b0909fec680ae6406b6fa775f6077b195837e2b9
# Tue, 10 Mar 2026 21:56:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 21:56:22 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Tue, 10 Mar 2026 21:56:23 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-windows-x86_64.exe
# Tue, 10 Mar 2026 21:56:24 GMT
ENV DOCKER_COMPOSE_SHA256=ee84e42b93c501cb0aa2caa84d76b5f30ca6fb92f070e289fc37be7332c5822a
# Tue, 10 Mar 2026 21:56:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17a66011dcb9c38eedc922e2d718b0cff4e70ce31e167daaa8dfee148d9c195`  
		Last Modified: Tue, 10 Mar 2026 21:56:42 GMT  
		Size: 486.8 KB (486826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f159d4d5d7e56333bfd6e2e7b16344a0e872adf0b93acebefa53c4247fbc9396`  
		Last Modified: Tue, 10 Mar 2026 21:56:41 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccb66eda533f994dbbb9ff81d57c851758147e1a0630eea05e16a0716ff87ad`  
		Last Modified: Tue, 10 Mar 2026 21:56:41 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0cd965bfbb200c967e8ee796997bdd4cdb587a833c56d7a49317544aab06cc6`  
		Last Modified: Tue, 10 Mar 2026 21:56:44 GMT  
		Size: 19.6 MB (19571347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edc8f49358e8d56eb2e56b6ac13be2048a3a016717f24c53f49dc1fc9bde0f7`  
		Last Modified: Tue, 10 Mar 2026 21:56:40 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8ac62b592ebb8bae48e8d31dadb875c021f30a09defc65097fb06249ef2e6a`  
		Last Modified: Tue, 10 Mar 2026 21:56:40 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554c2edbde552817f409d72b85a719f3c34ddc1651c3a110b24b1d3aa4570cc3`  
		Last Modified: Tue, 10 Mar 2026 21:56:40 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90bad317fa3a54913b9758ee2e45f94e02a64cc9e4e0c693589b644de126d33`  
		Last Modified: Tue, 10 Mar 2026 21:56:46 GMT  
		Size: 29.6 MB (29623149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dbad83ed52d0db02d4f30b2e0a88e026dd56c68a61c0a3a99f4d64bc5b14d1`  
		Last Modified: Tue, 10 Mar 2026 21:56:38 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d05240889a0e152fce0f29182840145e329281d7d52b384e0251bb1a9abfa8`  
		Last Modified: Tue, 10 Mar 2026 21:56:38 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ac67609452a0105c993416f50fb486c0260df99ed76d920c31b1ab2aa344ab`  
		Last Modified: Tue, 10 Mar 2026 21:56:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3aff282c60575fe0964ee93b76dd77692c3ed1f6cbeeb91ecb807cfa30421b8`  
		Last Modified: Tue, 10 Mar 2026 21:56:40 GMT  
		Size: 11.6 MB (11623130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:fdd48859b2b14b2fa4af458fcea153cfd95e8ce7429e66286229f28b47e507b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:42419a818a06c8b0bdb32d28efe864c1965f849d4d58dac6450fb35578530636
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2142463243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095982a564f926ffd785368388022d0f792a5f393f83c25b2b334b3f0ee3c25f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Wed, 25 Mar 2026 18:28:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Mar 2026 18:29:47 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Mar 2026 18:29:48 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.1.zip
# Wed, 25 Mar 2026 18:30:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Mar 2026 18:30:11 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:30:12 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.windows-amd64.exe
# Wed, 25 Mar 2026 18:30:13 GMT
ENV DOCKER_BUILDX_SHA256=47d76e47acf3c7611dd594c4b0909fec680ae6406b6fa775f6077b195837e2b9
# Wed, 25 Mar 2026 18:30:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Mar 2026 18:30:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:30:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Wed, 25 Mar 2026 18:30:37 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Wed, 25 Mar 2026 18:30:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c48ff63fd51e54c1621e1ef191ba1ffb5babb91295c52763e73038877ddbcc0`  
		Last Modified: Wed, 25 Mar 2026 18:30:56 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05646e87bcc7eebcf75f1a96ca80aa255bd6868601cdf94768601c8078d9b4b7`  
		Last Modified: Wed, 25 Mar 2026 18:30:55 GMT  
		Size: 374.0 KB (373997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edba92fa22a5c1bc563c18f651db43bfdc9c0720c21fff8d046d759875e121d1`  
		Last Modified: Wed, 25 Mar 2026 18:30:54 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b934d13e109edc08e9a08ca989659aded111b61867e75aa39cc626586e14b6d`  
		Last Modified: Wed, 25 Mar 2026 18:30:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff304ba5506cff7b400064688c74084a2ff60a244b484160e1be812e7672e3d`  
		Last Modified: Wed, 25 Mar 2026 18:30:56 GMT  
		Size: 19.6 MB (19594910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47622b1e857ba4fe582334af32ea59c3b58783ab368030f1d2259ae216996aaa`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a676a9fc9cb7650a5a61aad602e864237a2410b300b3babac5f0cfb4c9f31bf9`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d698051d32bbd456b5de7801253c16270739faf8954ce78f45f3a7e95830067`  
		Last Modified: Wed, 25 Mar 2026 18:30:52 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b8f6f29800e2912ff8cd1d9696f47141cb71560b98c73b71157c6b39d77665`  
		Last Modified: Wed, 25 Mar 2026 18:31:04 GMT  
		Size: 29.6 MB (29639971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbee4f4914616df04e2f56d66e020a4ca506723690da654928872871a3d1130`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36549e61114f7f53657411a2bc956fd69c15ae2f08beb6f977143978b7447c7a`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111317c19214d92002469ac71ea269b2b838ae7163f090cf6796b17aeccea76d`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee1dd44d7e561101a0c094be20961ded0b2b663201441b16b06bbace8b589ab`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 11.6 MB (11646539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
