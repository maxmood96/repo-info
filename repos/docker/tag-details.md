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
-	[`docker:29.3.0`](#docker2930)
-	[`docker:29.3.0-alpine3.23`](#docker2930-alpine323)
-	[`docker:29.3.0-cli`](#docker2930-cli)
-	[`docker:29.3.0-cli-alpine3.23`](#docker2930-cli-alpine323)
-	[`docker:29.3.0-dind`](#docker2930-dind)
-	[`docker:29.3.0-dind-alpine3.23`](#docker2930-dind-alpine323)
-	[`docker:29.3.0-dind-rootless`](#docker2930-dind-rootless)
-	[`docker:29.3.0-windowsservercore`](#docker2930-windowsservercore)
-	[`docker:29.3.0-windowsservercore-ltsc2022`](#docker2930-windowsservercore-ltsc2022)
-	[`docker:29.3.0-windowsservercore-ltsc2025`](#docker2930-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:29`

```console
$ docker pull docker@sha256:68f6d9ab84623d1116c5432a3b924a07ee09960e6129ca1cb03ef14010588cb4
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
$ docker pull docker@sha256:81fcfefed70c7154045d23dec3523719e7564ad2605c1a8a29fdd13ae9e1c710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143960556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c643ed57132b58411e32edf0540e88a41d1fbc98199d74f6565bc1777e73d688`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:32:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:32:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:32:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:05 GMT
CMD ["sh"]
# Sat, 28 Feb 2026 01:10:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 28 Feb 2026 01:10:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 28 Feb 2026 01:10:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 28 Feb 2026 01:10:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
VOLUME [/var/lib/docker]
# Sat, 28 Feb 2026 01:10:57 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 28 Feb 2026 01:10:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 28 Feb 2026 01:10:57 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ad56decde40eed4b884568f98b02d946417493176196dc029ab5e17c16b8eb`  
		Last Modified: Sat, 28 Feb 2026 00:33:12 GMT  
		Size: 8.4 MB (8399669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342aaf2cc08446a08f0c3201e79521412a27ec651d43233e7591635ba001c7df`  
		Last Modified: Sat, 28 Feb 2026 00:33:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9632763a5f6e5657586d42acd7aab8f7b50c5a9c42bc6c925c7cc1c4690cbd`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 18.8 MB (18773125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273ed7fc2746040170324eb790dc34cf0f4e212546ea29a395b7efefd95385d0`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eae5b0ffe938ee3f0cdd909657ca40f0528831b03d3d3ec32d88bf2a889cca`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 11.0 MB (10953930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed25dc6106a64ddaa30940a80175eddee65e79eac95d515a7c9fa35d9d93a22`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048c355ee240ae4713fa8e796335e4a6ea52fc7b34f42881992fb2954dd1ac2e`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f3f6dd36e1c7b333ba1f09b0987ea030d3d2750f5033170f2e746227cff7e6`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaa4baf3866b503b2f32ce744935a68b0df9d10607680ef5682126f09b9360`  
		Last Modified: Sat, 28 Feb 2026 01:11:08 GMT  
		Size: 6.9 MB (6934691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec2ed410cea5bc307ea8e2227c83b433957ceb6c916efe3e747edc437445f4e`  
		Last Modified: Sat, 28 Feb 2026 01:11:07 GMT  
		Size: 92.5 KB (92468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5521b863247b8ec145bb965e69f88121a5d4658dc8c98d3053ff3c005d4b3b48`  
		Last Modified: Sat, 28 Feb 2026 01:11:08 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27c5afc8cc77a003520d64522134adc6469902a7ec92500709691b1dc4e5200`  
		Last Modified: Sat, 28 Feb 2026 01:11:09 GMT  
		Size: 66.6 MB (66625155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e365fc1dcf7059372ca577d494d424d53e29c1b9e1f879006992d060f5a02d37`  
		Last Modified: Sat, 28 Feb 2026 01:11:09 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d3092c518457079ad29ae8aaa4a44167a207e5b03ea70bd7587232b7855368`  
		Last Modified: Sat, 28 Feb 2026 01:11:09 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:a267e8d9da86afb00b8c97e7c1c023b2d8758a8df73b3b5755f1f1ae99745efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04cb494266b4fc82300382c99c4b78a744ac87a5a3d60f921dac122209436850`

```dockerfile
```

-	Layers:
	-	`sha256:bca36398fa62499981389ef963ec3e8732477fd3189e49d5b0a19962f021e882`  
		Last Modified: Sat, 28 Feb 2026 01:11:07 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v6

```console
$ docker pull docker@sha256:a36a708ef4ab20c051d7182ae2f16870c654ce36c041a883f4b3045498542416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135811601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c805d64686b3d65ef3dd20aa06d17d5c4074716241083750c4ce663fc641fd77`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:33:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:33:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:33:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:36 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:36 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:39 GMT
CMD ["sh"]
# Sat, 28 Feb 2026 01:08:57 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 28 Feb 2026 01:08:58 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 28 Feb 2026 01:08:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 01:09:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 28 Feb 2026 01:09:03 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 28 Feb 2026 01:09:03 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 28 Feb 2026 01:09:03 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:09:03 GMT
VOLUME [/var/lib/docker]
# Sat, 28 Feb 2026 01:09:03 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 28 Feb 2026 01:09:03 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 28 Feb 2026 01:09:03 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b2c1188f77d466b63114530c948db4a2b72f6432015051eb4c6fc5ed17a318`  
		Last Modified: Sat, 28 Feb 2026 00:33:47 GMT  
		Size: 8.3 MB (8300892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d069c0ddccdd129439f3fc19b3beb0deb0ea53ebe0d54791b223081c0bfd09`  
		Last Modified: Sat, 28 Feb 2026 00:33:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84f79f2e027c27c1420192bbb6269e4133d62301076e5f92f52a21a7c341822`  
		Last Modified: Sat, 28 Feb 2026 00:33:47 GMT  
		Size: 17.6 MB (17574992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d9822253e2de58052e59355a3ee3a3e3219482e8ff9da6021bba9c31169a73`  
		Last Modified: Sat, 28 Feb 2026 00:33:47 GMT  
		Size: 26.6 MB (26574514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977fe3e040234fe198164a9728011f9bdf228d76a92669ba3aa98acbf91cd8d1`  
		Last Modified: Sat, 28 Feb 2026 00:33:48 GMT  
		Size: 10.4 MB (10385436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9b5078999b461db61885ae27aefeaad4cd7679c996ee4dc106c5481deb7172`  
		Last Modified: Sat, 28 Feb 2026 00:33:48 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcf453e2e7207817cd2f1cafcd2c26502a7cec3072cb5a8b8c1e49e7720eef6`  
		Last Modified: Sat, 28 Feb 2026 00:33:48 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3831f33bbdf7e0cd2a3ba77cc3d9b6dea4ffd87f09eb7a18d0df5ac6354dae`  
		Last Modified: Sat, 28 Feb 2026 00:33:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b7b97efb6c96c9626c6452c6d35907116fd44e9d8dd4a730e3de085fdfcb87`  
		Last Modified: Sat, 28 Feb 2026 01:09:14 GMT  
		Size: 7.3 MB (7271699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb28f43f383cd367845812769677219708f450192b0bce32ea6ae1323cbbf12c`  
		Last Modified: Sat, 28 Feb 2026 01:09:13 GMT  
		Size: 91.8 KB (91779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1143b390d4eb69eec28024598bde4e9a359c89c6219eb10475930689486123`  
		Last Modified: Sat, 28 Feb 2026 01:09:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288371601350ba56b1dc5d245271aeda8acc45db516a7cf1ca4edee711d7349b`  
		Last Modified: Sat, 28 Feb 2026 01:09:15 GMT  
		Size: 62.0 MB (62034312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8aa70bb05db86bf9265162619f611758dbcaa8ab0f06e5712909b80a97e6472`  
		Last Modified: Sat, 28 Feb 2026 01:09:13 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c3984a3e460e2c4cf1824f452f5e8a3472cd095ca0044b172ccf33ba31b4c5`  
		Last Modified: Sat, 28 Feb 2026 01:09:14 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:0ada12f8e5ddea957492c54b4028272b319b90df66b2ec6482a748996caef3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a15c8c9d8910fa3b67e64a0b4c5ff0a3a043b468f787a3193101971707f19ad`

```dockerfile
```

-	Layers:
	-	`sha256:d8679db966c7defd214d55efd0fc6a1f698492ad859d9708372af6e6bae01e35`  
		Last Modified: Sat, 28 Feb 2026 01:09:13 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v7

```console
$ docker pull docker@sha256:c1e28a4f3b227ee7db14d82c37324957af6fc4efbc0521fff59f00ea6ecce2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133894570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e0c6071fac97999a74b349e820fdabef122b6e9bf5555a22afcce2432cf2f8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:32:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:32:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:32:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:32:34 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:32:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:32:34 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:32:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:32:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:32:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:32:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:32:39 GMT
CMD ["sh"]
# Sat, 28 Feb 2026 01:09:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 28 Feb 2026 01:09:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 28 Feb 2026 01:09:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 01:09:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 28 Feb 2026 01:09:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 28 Feb 2026 01:09:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 28 Feb 2026 01:09:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:09:13 GMT
VOLUME [/var/lib/docker]
# Sat, 28 Feb 2026 01:09:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 28 Feb 2026 01:09:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 28 Feb 2026 01:09:13 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282f6e2b7c9718d720ce426672429335541cf1c919bf9c845984c433c879cdc4`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 7.6 MB (7597811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354b5b8fd3a086ebaa1f824553d2d81811f9bc34aa15f16251dd1149b040957f`  
		Last Modified: Sat, 28 Feb 2026 00:32:46 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c343ba8124dc1173c2441732470ac81040c16fa72ca600062307c2150db08efd`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 17.6 MB (17566420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3c55e011e6f401320580bc9559a8eec2bd1121139952f1d621befd1557f233`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 26.5 MB (26546113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01b5cad9fc8f11ff6eceb574bedcff79a5acd3f04a71d09030e0b337df68f7b`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 10.4 MB (10369780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41923b1f427db13299befcd38419467285b2ca66ad0a4b33f483296df5b5f467`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440d27ed514452926e359f9aeccb369ab42162dc457ef0cb90a9aa6684666b0c`  
		Last Modified: Sat, 28 Feb 2026 00:32:48 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47078bcf7b70f7b4c214ba0d20f1c8e10e7347e12a105ca35addd773811b04c1`  
		Last Modified: Sat, 28 Feb 2026 00:32:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4646932f3e91cb6ab7dbc864b4e08445a66ec41cd374fbe49ec1896ed88a982`  
		Last Modified: Sat, 28 Feb 2026 01:09:24 GMT  
		Size: 6.6 MB (6573022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19c564899e9b5a6c19f0cdc29230499311e905a2b3da9955c8d458746d5e905`  
		Last Modified: Sat, 28 Feb 2026 01:09:23 GMT  
		Size: 88.2 KB (88156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01f4e2cf953a2d6d9a9f3a1443b3b8ef98280b66a90e8d007394fcd607f0f91`  
		Last Modified: Sat, 28 Feb 2026 01:09:23 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1686d5a17066d20b94ebba8ea4ad36abb7e768dac3ff5094d9f899ac1212beac`  
		Last Modified: Sat, 28 Feb 2026 01:09:25 GMT  
		Size: 61.9 MB (61863393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829040129e131eff6b7babe59601d0efda9023e17990e656b9947f091da2c036`  
		Last Modified: Sat, 28 Feb 2026 01:09:25 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d5f9cb70da8c12cf982ed75d5dd9eb4c800c749ac416383fac30c4dc2dd3dd`  
		Last Modified: Sat, 28 Feb 2026 01:09:24 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:4f94ebe1fabec8df89f1b602cc9af7f71be9db93d156dbd2c7070c36533ea9dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac1cbf9bbda4bc07b7c4a7ece169ab46ee3ee85ceab6511396586e6419b2fbe`

```dockerfile
```

-	Layers:
	-	`sha256:e5a96ba22363c34a75191791ae68225d552c1f1627d115e575d9c76c6589fe71`  
		Last Modified: Sat, 28 Feb 2026 01:09:23 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4ca8506088c30f906cdfad8f863b9f2c41eef5b159e4b752a6c8d1c07fca74f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133273459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8ecd5b1d17216fcea5159b6dcf8aeffebfae9306de065fe5ddfb98aae43fa6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:33:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:07 GMT
CMD ["sh"]
# Sat, 28 Feb 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 28 Feb 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 28 Feb 2026 01:10:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 28 Feb 2026 01:10:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
VOLUME [/var/lib/docker]
# Sat, 28 Feb 2026 01:10:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 28 Feb 2026 01:10:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 28 Feb 2026 01:10:24 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60904be95e049500c5894c6d214007956f1035c22b15ff77ca522ac2f628513`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 8.5 MB (8453564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b0b4b880f947788126e86f12bf4ec6c59bfedb59205ec90c5344b9e9a39861`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1f471b1d5b369a49fb05baa23cedb1b9fa1b9015ee6f27e2b9c5a34b10767e`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 17.3 MB (17349112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662c4f142eb7ddca6437ee0959e5b89824fbe97fa5d1a9d1613c79eb52d0840`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 25.5 MB (25540813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8e4f342d8afaf59c1558d78cd1f5c1e1d074b96b11c5c794918cd74ec7353b`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 10.0 MB (9974085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1186c16de0a9a9c9cc0c496c6164690809b3defab752f3b709727f48df7745fb`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf3a986bcd21c6233dd627338e709a488f1f34ce5a97c2756ff6b05b51a3113`  
		Last Modified: Sat, 28 Feb 2026 00:33:16 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44fcf3aa39e6d6b37daecf7b8046a614dbf9488aaca5bf8eefed943801df648`  
		Last Modified: Sat, 28 Feb 2026 00:33:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbf4035e1f4acb2bd237e1645b2bc3e70a443d5a1848f4882c09901a0a220d8`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 7.2 MB (7213295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad674e6263a8a736b9a1ced02582b966ce06e5c7fc7c2fc21b3714e9a0507831`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 101.3 KB (101286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc08837f92210ce965fca88a82162045be6c2eefb791a36ecbff458a61290501`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c647a3ee71654578d02cac37d0b50bd38b344b814c0b00b5b71988b287163d5`  
		Last Modified: Sat, 28 Feb 2026 01:10:36 GMT  
		Size: 60.4 MB (60436054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7282f0ceaef0633b111139db8bf324c0c4d3045254de20c95b0c6e181195d759`  
		Last Modified: Sat, 28 Feb 2026 01:10:35 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ef9d8eaefdd9ca91eaa763fcfb13a8ada246f317f40c6c60f74d8b8066c975`  
		Last Modified: Sat, 28 Feb 2026 01:10:35 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:2748df42f6df2e6f3e87566ec113dba1c9c6c94d8463cfc0fbcc2d64ab4f9733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42e0ddb0a8b1512b11247ffdb0d8af1f53634b4d9b91e61ac1fe42684abdfa8`

```dockerfile
```

-	Layers:
	-	`sha256:85137676ef3e7b9bd815bd4c1e81e8f915dd5665b890b53565ff08c370b3d55c`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:cab69e2d0a1a2ea9a1ce1060252f439e83483ae41ec09317aecb33b08a0656a5
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
$ docker pull docker@sha256:61eaf318a33c0d37231cfcb496ad6e4c547e609a992c43ba456be9eefa4223cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70302244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4660288b9b1871838afdbb93297d9606cd0cecb9108d84c5725428e810e2f60e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:32:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:32:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:32:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ad56decde40eed4b884568f98b02d946417493176196dc029ab5e17c16b8eb`  
		Last Modified: Sat, 28 Feb 2026 00:33:12 GMT  
		Size: 8.4 MB (8399669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342aaf2cc08446a08f0c3201e79521412a27ec651d43233e7591635ba001c7df`  
		Last Modified: Sat, 28 Feb 2026 00:33:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9632763a5f6e5657586d42acd7aab8f7b50c5a9c42bc6c925c7cc1c4690cbd`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 18.8 MB (18773125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273ed7fc2746040170324eb790dc34cf0f4e212546ea29a395b7efefd95385d0`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eae5b0ffe938ee3f0cdd909657ca40f0528831b03d3d3ec32d88bf2a889cca`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 11.0 MB (10953930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed25dc6106a64ddaa30940a80175eddee65e79eac95d515a7c9fa35d9d93a22`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048c355ee240ae4713fa8e796335e4a6ea52fc7b34f42881992fb2954dd1ac2e`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f3f6dd36e1c7b333ba1f09b0987ea030d3d2750f5033170f2e746227cff7e6`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:b0475bfdf9f0ff004e8adccde3b3e701c17ff24f1bac9068eda9e1a232629c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43f6533aace4da9151c80022d3054ae46ee57571d31964300d821b26e5465eb`

```dockerfile
```

-	Layers:
	-	`sha256:ffef58d7d564c693206df20dfa8398493c3bd2a9e4e5126a12d67213dd509e0b`  
		Last Modified: Sat, 28 Feb 2026 00:33:12 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:51c7cd8fd48d2bb76401b87baa09a14b170fe52ca356c0c99fd7e168d80153d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66407812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4456f4155a1327a286d3fc189e230eb06aacf818b2a72b293e164ec5c0320e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:33:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:33:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:33:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:36 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:36 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b2c1188f77d466b63114530c948db4a2b72f6432015051eb4c6fc5ed17a318`  
		Last Modified: Sat, 28 Feb 2026 00:33:47 GMT  
		Size: 8.3 MB (8300892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d069c0ddccdd129439f3fc19b3beb0deb0ea53ebe0d54791b223081c0bfd09`  
		Last Modified: Sat, 28 Feb 2026 00:33:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84f79f2e027c27c1420192bbb6269e4133d62301076e5f92f52a21a7c341822`  
		Last Modified: Sat, 28 Feb 2026 00:33:47 GMT  
		Size: 17.6 MB (17574992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d9822253e2de58052e59355a3ee3a3e3219482e8ff9da6021bba9c31169a73`  
		Last Modified: Sat, 28 Feb 2026 00:33:47 GMT  
		Size: 26.6 MB (26574514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977fe3e040234fe198164a9728011f9bdf228d76a92669ba3aa98acbf91cd8d1`  
		Last Modified: Sat, 28 Feb 2026 00:33:48 GMT  
		Size: 10.4 MB (10385436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9b5078999b461db61885ae27aefeaad4cd7679c996ee4dc106c5481deb7172`  
		Last Modified: Sat, 28 Feb 2026 00:33:48 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcf453e2e7207817cd2f1cafcd2c26502a7cec3072cb5a8b8c1e49e7720eef6`  
		Last Modified: Sat, 28 Feb 2026 00:33:48 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3831f33bbdf7e0cd2a3ba77cc3d9b6dea4ffd87f09eb7a18d0df5ac6354dae`  
		Last Modified: Sat, 28 Feb 2026 00:33:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9d7716df1aede936adaf0fe3deb36addd057a35780b0186f4f1f7d1955c41b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af00649395af49edb0bbd0a19fd0cc1db7af9915ebd70cafa59ebee4f311b60`

```dockerfile
```

-	Layers:
	-	`sha256:e6b2249d10157cab657330d395f90242fae24ca9c9a12ee8b328a621f2e0ecfc`  
		Last Modified: Sat, 28 Feb 2026 00:33:46 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:381de97367b51842200da5a791fb997b3b5c9149900d68064288e6b190f7e89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65364001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d397b31096240e447d64f1431afc291561f750ea87a68322c9ce5eda7848952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:32:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:32:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:32:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:32:34 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:32:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:32:34 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:32:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:32:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:32:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:32:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:32:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282f6e2b7c9718d720ce426672429335541cf1c919bf9c845984c433c879cdc4`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 7.6 MB (7597811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354b5b8fd3a086ebaa1f824553d2d81811f9bc34aa15f16251dd1149b040957f`  
		Last Modified: Sat, 28 Feb 2026 00:32:46 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c343ba8124dc1173c2441732470ac81040c16fa72ca600062307c2150db08efd`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 17.6 MB (17566420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3c55e011e6f401320580bc9559a8eec2bd1121139952f1d621befd1557f233`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 26.5 MB (26546113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01b5cad9fc8f11ff6eceb574bedcff79a5acd3f04a71d09030e0b337df68f7b`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 10.4 MB (10369780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41923b1f427db13299befcd38419467285b2ca66ad0a4b33f483296df5b5f467`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440d27ed514452926e359f9aeccb369ab42162dc457ef0cb90a9aa6684666b0c`  
		Last Modified: Sat, 28 Feb 2026 00:32:48 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47078bcf7b70f7b4c214ba0d20f1c8e10e7347e12a105ca35addd773811b04c1`  
		Last Modified: Sat, 28 Feb 2026 00:32:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e5807ae87b8e7066b82da385443764ab7e4f21308b4181eb58c88975d7c167cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528510c893d8b8f034b3bbc17275f034345c8c9d3852c827b5e357d6798d5b1d`

```dockerfile
```

-	Layers:
	-	`sha256:bb1422430bd5e44adbb541518e3a9e79c78ad25d05c8aa6b1b29d2934d4762a3`  
		Last Modified: Sat, 28 Feb 2026 00:32:46 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b419ff204d51c59cf7e3e01c4277dad148fc5f300f172c2f65700a1cac93e7c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65516823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b618349b315d48d95f60e08d9377bd62bdfd24403eeb09069be71e5e564326e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:33:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60904be95e049500c5894c6d214007956f1035c22b15ff77ca522ac2f628513`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 8.5 MB (8453564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b0b4b880f947788126e86f12bf4ec6c59bfedb59205ec90c5344b9e9a39861`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1f471b1d5b369a49fb05baa23cedb1b9fa1b9015ee6f27e2b9c5a34b10767e`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 17.3 MB (17349112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662c4f142eb7ddca6437ee0959e5b89824fbe97fa5d1a9d1613c79eb52d0840`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 25.5 MB (25540813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8e4f342d8afaf59c1558d78cd1f5c1e1d074b96b11c5c794918cd74ec7353b`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 10.0 MB (9974085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1186c16de0a9a9c9cc0c496c6164690809b3defab752f3b709727f48df7745fb`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf3a986bcd21c6233dd627338e709a488f1f34ce5a97c2756ff6b05b51a3113`  
		Last Modified: Sat, 28 Feb 2026 00:33:16 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44fcf3aa39e6d6b37daecf7b8046a614dbf9488aaca5bf8eefed943801df648`  
		Last Modified: Sat, 28 Feb 2026 00:33:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e9de5b8217500a0ec096e0b8bb9a8789c7a9724c61ccc6ac5cd2f4a7e3280d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f4db5f2e930b8e32deee8f1ae4ac490c44829280a680b77e4907438dae3400`

```dockerfile
```

-	Layers:
	-	`sha256:0433045c024921198fd8eb3b1df4aba3072436207276e52a0670d152f6b1446b`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind`

```console
$ docker pull docker@sha256:68f6d9ab84623d1116c5432a3b924a07ee09960e6129ca1cb03ef14010588cb4
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
$ docker pull docker@sha256:81fcfefed70c7154045d23dec3523719e7564ad2605c1a8a29fdd13ae9e1c710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143960556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c643ed57132b58411e32edf0540e88a41d1fbc98199d74f6565bc1777e73d688`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:32:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:32:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:32:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:05 GMT
CMD ["sh"]
# Sat, 28 Feb 2026 01:10:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 28 Feb 2026 01:10:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 28 Feb 2026 01:10:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 28 Feb 2026 01:10:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
VOLUME [/var/lib/docker]
# Sat, 28 Feb 2026 01:10:57 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 28 Feb 2026 01:10:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 28 Feb 2026 01:10:57 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ad56decde40eed4b884568f98b02d946417493176196dc029ab5e17c16b8eb`  
		Last Modified: Sat, 28 Feb 2026 00:33:12 GMT  
		Size: 8.4 MB (8399669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342aaf2cc08446a08f0c3201e79521412a27ec651d43233e7591635ba001c7df`  
		Last Modified: Sat, 28 Feb 2026 00:33:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9632763a5f6e5657586d42acd7aab8f7b50c5a9c42bc6c925c7cc1c4690cbd`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 18.8 MB (18773125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273ed7fc2746040170324eb790dc34cf0f4e212546ea29a395b7efefd95385d0`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eae5b0ffe938ee3f0cdd909657ca40f0528831b03d3d3ec32d88bf2a889cca`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 11.0 MB (10953930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed25dc6106a64ddaa30940a80175eddee65e79eac95d515a7c9fa35d9d93a22`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048c355ee240ae4713fa8e796335e4a6ea52fc7b34f42881992fb2954dd1ac2e`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f3f6dd36e1c7b333ba1f09b0987ea030d3d2750f5033170f2e746227cff7e6`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaa4baf3866b503b2f32ce744935a68b0df9d10607680ef5682126f09b9360`  
		Last Modified: Sat, 28 Feb 2026 01:11:08 GMT  
		Size: 6.9 MB (6934691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec2ed410cea5bc307ea8e2227c83b433957ceb6c916efe3e747edc437445f4e`  
		Last Modified: Sat, 28 Feb 2026 01:11:07 GMT  
		Size: 92.5 KB (92468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5521b863247b8ec145bb965e69f88121a5d4658dc8c98d3053ff3c005d4b3b48`  
		Last Modified: Sat, 28 Feb 2026 01:11:08 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27c5afc8cc77a003520d64522134adc6469902a7ec92500709691b1dc4e5200`  
		Last Modified: Sat, 28 Feb 2026 01:11:09 GMT  
		Size: 66.6 MB (66625155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e365fc1dcf7059372ca577d494d424d53e29c1b9e1f879006992d060f5a02d37`  
		Last Modified: Sat, 28 Feb 2026 01:11:09 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d3092c518457079ad29ae8aaa4a44167a207e5b03ea70bd7587232b7855368`  
		Last Modified: Sat, 28 Feb 2026 01:11:09 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a267e8d9da86afb00b8c97e7c1c023b2d8758a8df73b3b5755f1f1ae99745efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04cb494266b4fc82300382c99c4b78a744ac87a5a3d60f921dac122209436850`

```dockerfile
```

-	Layers:
	-	`sha256:bca36398fa62499981389ef963ec3e8732477fd3189e49d5b0a19962f021e882`  
		Last Modified: Sat, 28 Feb 2026 01:11:07 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:a36a708ef4ab20c051d7182ae2f16870c654ce36c041a883f4b3045498542416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135811601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c805d64686b3d65ef3dd20aa06d17d5c4074716241083750c4ce663fc641fd77`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:33:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:33:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:33:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:36 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:36 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:39 GMT
CMD ["sh"]
# Sat, 28 Feb 2026 01:08:57 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 28 Feb 2026 01:08:58 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 28 Feb 2026 01:08:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 01:09:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 28 Feb 2026 01:09:03 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 28 Feb 2026 01:09:03 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 28 Feb 2026 01:09:03 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:09:03 GMT
VOLUME [/var/lib/docker]
# Sat, 28 Feb 2026 01:09:03 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 28 Feb 2026 01:09:03 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 28 Feb 2026 01:09:03 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b2c1188f77d466b63114530c948db4a2b72f6432015051eb4c6fc5ed17a318`  
		Last Modified: Sat, 28 Feb 2026 00:33:47 GMT  
		Size: 8.3 MB (8300892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d069c0ddccdd129439f3fc19b3beb0deb0ea53ebe0d54791b223081c0bfd09`  
		Last Modified: Sat, 28 Feb 2026 00:33:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84f79f2e027c27c1420192bbb6269e4133d62301076e5f92f52a21a7c341822`  
		Last Modified: Sat, 28 Feb 2026 00:33:47 GMT  
		Size: 17.6 MB (17574992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d9822253e2de58052e59355a3ee3a3e3219482e8ff9da6021bba9c31169a73`  
		Last Modified: Sat, 28 Feb 2026 00:33:47 GMT  
		Size: 26.6 MB (26574514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977fe3e040234fe198164a9728011f9bdf228d76a92669ba3aa98acbf91cd8d1`  
		Last Modified: Sat, 28 Feb 2026 00:33:48 GMT  
		Size: 10.4 MB (10385436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9b5078999b461db61885ae27aefeaad4cd7679c996ee4dc106c5481deb7172`  
		Last Modified: Sat, 28 Feb 2026 00:33:48 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcf453e2e7207817cd2f1cafcd2c26502a7cec3072cb5a8b8c1e49e7720eef6`  
		Last Modified: Sat, 28 Feb 2026 00:33:48 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3831f33bbdf7e0cd2a3ba77cc3d9b6dea4ffd87f09eb7a18d0df5ac6354dae`  
		Last Modified: Sat, 28 Feb 2026 00:33:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b7b97efb6c96c9626c6452c6d35907116fd44e9d8dd4a730e3de085fdfcb87`  
		Last Modified: Sat, 28 Feb 2026 01:09:14 GMT  
		Size: 7.3 MB (7271699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb28f43f383cd367845812769677219708f450192b0bce32ea6ae1323cbbf12c`  
		Last Modified: Sat, 28 Feb 2026 01:09:13 GMT  
		Size: 91.8 KB (91779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1143b390d4eb69eec28024598bde4e9a359c89c6219eb10475930689486123`  
		Last Modified: Sat, 28 Feb 2026 01:09:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288371601350ba56b1dc5d245271aeda8acc45db516a7cf1ca4edee711d7349b`  
		Last Modified: Sat, 28 Feb 2026 01:09:15 GMT  
		Size: 62.0 MB (62034312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8aa70bb05db86bf9265162619f611758dbcaa8ab0f06e5712909b80a97e6472`  
		Last Modified: Sat, 28 Feb 2026 01:09:13 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c3984a3e460e2c4cf1824f452f5e8a3472cd095ca0044b172ccf33ba31b4c5`  
		Last Modified: Sat, 28 Feb 2026 01:09:14 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:0ada12f8e5ddea957492c54b4028272b319b90df66b2ec6482a748996caef3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a15c8c9d8910fa3b67e64a0b4c5ff0a3a043b468f787a3193101971707f19ad`

```dockerfile
```

-	Layers:
	-	`sha256:d8679db966c7defd214d55efd0fc6a1f698492ad859d9708372af6e6bae01e35`  
		Last Modified: Sat, 28 Feb 2026 01:09:13 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:c1e28a4f3b227ee7db14d82c37324957af6fc4efbc0521fff59f00ea6ecce2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133894570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e0c6071fac97999a74b349e820fdabef122b6e9bf5555a22afcce2432cf2f8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:32:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:32:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:32:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:32:34 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:32:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:32:34 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:32:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:32:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:32:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:32:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:32:39 GMT
CMD ["sh"]
# Sat, 28 Feb 2026 01:09:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 28 Feb 2026 01:09:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 28 Feb 2026 01:09:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 01:09:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 28 Feb 2026 01:09:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 28 Feb 2026 01:09:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 28 Feb 2026 01:09:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:09:13 GMT
VOLUME [/var/lib/docker]
# Sat, 28 Feb 2026 01:09:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 28 Feb 2026 01:09:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 28 Feb 2026 01:09:13 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282f6e2b7c9718d720ce426672429335541cf1c919bf9c845984c433c879cdc4`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 7.6 MB (7597811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354b5b8fd3a086ebaa1f824553d2d81811f9bc34aa15f16251dd1149b040957f`  
		Last Modified: Sat, 28 Feb 2026 00:32:46 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c343ba8124dc1173c2441732470ac81040c16fa72ca600062307c2150db08efd`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 17.6 MB (17566420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3c55e011e6f401320580bc9559a8eec2bd1121139952f1d621befd1557f233`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 26.5 MB (26546113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01b5cad9fc8f11ff6eceb574bedcff79a5acd3f04a71d09030e0b337df68f7b`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 10.4 MB (10369780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41923b1f427db13299befcd38419467285b2ca66ad0a4b33f483296df5b5f467`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440d27ed514452926e359f9aeccb369ab42162dc457ef0cb90a9aa6684666b0c`  
		Last Modified: Sat, 28 Feb 2026 00:32:48 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47078bcf7b70f7b4c214ba0d20f1c8e10e7347e12a105ca35addd773811b04c1`  
		Last Modified: Sat, 28 Feb 2026 00:32:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4646932f3e91cb6ab7dbc864b4e08445a66ec41cd374fbe49ec1896ed88a982`  
		Last Modified: Sat, 28 Feb 2026 01:09:24 GMT  
		Size: 6.6 MB (6573022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19c564899e9b5a6c19f0cdc29230499311e905a2b3da9955c8d458746d5e905`  
		Last Modified: Sat, 28 Feb 2026 01:09:23 GMT  
		Size: 88.2 KB (88156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01f4e2cf953a2d6d9a9f3a1443b3b8ef98280b66a90e8d007394fcd607f0f91`  
		Last Modified: Sat, 28 Feb 2026 01:09:23 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1686d5a17066d20b94ebba8ea4ad36abb7e768dac3ff5094d9f899ac1212beac`  
		Last Modified: Sat, 28 Feb 2026 01:09:25 GMT  
		Size: 61.9 MB (61863393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829040129e131eff6b7babe59601d0efda9023e17990e656b9947f091da2c036`  
		Last Modified: Sat, 28 Feb 2026 01:09:25 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d5f9cb70da8c12cf982ed75d5dd9eb4c800c749ac416383fac30c4dc2dd3dd`  
		Last Modified: Sat, 28 Feb 2026 01:09:24 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4f94ebe1fabec8df89f1b602cc9af7f71be9db93d156dbd2c7070c36533ea9dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac1cbf9bbda4bc07b7c4a7ece169ab46ee3ee85ceab6511396586e6419b2fbe`

```dockerfile
```

-	Layers:
	-	`sha256:e5a96ba22363c34a75191791ae68225d552c1f1627d115e575d9c76c6589fe71`  
		Last Modified: Sat, 28 Feb 2026 01:09:23 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4ca8506088c30f906cdfad8f863b9f2c41eef5b159e4b752a6c8d1c07fca74f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133273459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8ecd5b1d17216fcea5159b6dcf8aeffebfae9306de065fe5ddfb98aae43fa6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:33:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:07 GMT
CMD ["sh"]
# Sat, 28 Feb 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 28 Feb 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 28 Feb 2026 01:10:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 28 Feb 2026 01:10:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
VOLUME [/var/lib/docker]
# Sat, 28 Feb 2026 01:10:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 28 Feb 2026 01:10:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 28 Feb 2026 01:10:24 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60904be95e049500c5894c6d214007956f1035c22b15ff77ca522ac2f628513`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 8.5 MB (8453564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b0b4b880f947788126e86f12bf4ec6c59bfedb59205ec90c5344b9e9a39861`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1f471b1d5b369a49fb05baa23cedb1b9fa1b9015ee6f27e2b9c5a34b10767e`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 17.3 MB (17349112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662c4f142eb7ddca6437ee0959e5b89824fbe97fa5d1a9d1613c79eb52d0840`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 25.5 MB (25540813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8e4f342d8afaf59c1558d78cd1f5c1e1d074b96b11c5c794918cd74ec7353b`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 10.0 MB (9974085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1186c16de0a9a9c9cc0c496c6164690809b3defab752f3b709727f48df7745fb`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf3a986bcd21c6233dd627338e709a488f1f34ce5a97c2756ff6b05b51a3113`  
		Last Modified: Sat, 28 Feb 2026 00:33:16 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44fcf3aa39e6d6b37daecf7b8046a614dbf9488aaca5bf8eefed943801df648`  
		Last Modified: Sat, 28 Feb 2026 00:33:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbf4035e1f4acb2bd237e1645b2bc3e70a443d5a1848f4882c09901a0a220d8`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 7.2 MB (7213295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad674e6263a8a736b9a1ced02582b966ce06e5c7fc7c2fc21b3714e9a0507831`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 101.3 KB (101286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc08837f92210ce965fca88a82162045be6c2eefb791a36ecbff458a61290501`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c647a3ee71654578d02cac37d0b50bd38b344b814c0b00b5b71988b287163d5`  
		Last Modified: Sat, 28 Feb 2026 01:10:36 GMT  
		Size: 60.4 MB (60436054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7282f0ceaef0633b111139db8bf324c0c4d3045254de20c95b0c6e181195d759`  
		Last Modified: Sat, 28 Feb 2026 01:10:35 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ef9d8eaefdd9ca91eaa763fcfb13a8ada246f317f40c6c60f74d8b8066c975`  
		Last Modified: Sat, 28 Feb 2026 01:10:35 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:2748df42f6df2e6f3e87566ec113dba1c9c6c94d8463cfc0fbcc2d64ab4f9733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42e0ddb0a8b1512b11247ffdb0d8af1f53634b4d9b91e61ac1fe42684abdfa8`

```dockerfile
```

-	Layers:
	-	`sha256:85137676ef3e7b9bd815bd4c1e81e8f915dd5665b890b53565ff08c370b3d55c`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:67c4114553192e9072969fc347426048cfe4192385dc762d8eb449c05e904255
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:0a0ac6f82505da7dca92525bc232f36d9e2094c325a98e387afa70736334b435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164757707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e095376b1219c57b174714bd2cb2119f6fbb53eed15b522810c059b24393a183`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:32:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:32:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:32:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:05 GMT
CMD ["sh"]
# Sat, 28 Feb 2026 01:10:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 28 Feb 2026 01:10:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 28 Feb 2026 01:10:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 28 Feb 2026 01:10:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
VOLUME [/var/lib/docker]
# Sat, 28 Feb 2026 01:10:57 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 28 Feb 2026 01:10:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 28 Feb 2026 01:10:57 GMT
CMD []
# Sat, 28 Feb 2026 02:10:17 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 28 Feb 2026 02:10:17 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 28 Feb 2026 02:10:17 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 02:10:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Sat, 28 Feb 2026 02:10:18 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 28 Feb 2026 02:10:18 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 28 Feb 2026 02:10:18 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ad56decde40eed4b884568f98b02d946417493176196dc029ab5e17c16b8eb`  
		Last Modified: Sat, 28 Feb 2026 00:33:12 GMT  
		Size: 8.4 MB (8399669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342aaf2cc08446a08f0c3201e79521412a27ec651d43233e7591635ba001c7df`  
		Last Modified: Sat, 28 Feb 2026 00:33:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9632763a5f6e5657586d42acd7aab8f7b50c5a9c42bc6c925c7cc1c4690cbd`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 18.8 MB (18773125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273ed7fc2746040170324eb790dc34cf0f4e212546ea29a395b7efefd95385d0`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eae5b0ffe938ee3f0cdd909657ca40f0528831b03d3d3ec32d88bf2a889cca`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 11.0 MB (10953930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed25dc6106a64ddaa30940a80175eddee65e79eac95d515a7c9fa35d9d93a22`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048c355ee240ae4713fa8e796335e4a6ea52fc7b34f42881992fb2954dd1ac2e`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f3f6dd36e1c7b333ba1f09b0987ea030d3d2750f5033170f2e746227cff7e6`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaa4baf3866b503b2f32ce744935a68b0df9d10607680ef5682126f09b9360`  
		Last Modified: Sat, 28 Feb 2026 01:11:08 GMT  
		Size: 6.9 MB (6934691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec2ed410cea5bc307ea8e2227c83b433957ceb6c916efe3e747edc437445f4e`  
		Last Modified: Sat, 28 Feb 2026 01:11:07 GMT  
		Size: 92.5 KB (92468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5521b863247b8ec145bb965e69f88121a5d4658dc8c98d3053ff3c005d4b3b48`  
		Last Modified: Sat, 28 Feb 2026 01:11:08 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27c5afc8cc77a003520d64522134adc6469902a7ec92500709691b1dc4e5200`  
		Last Modified: Sat, 28 Feb 2026 01:11:09 GMT  
		Size: 66.6 MB (66625155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e365fc1dcf7059372ca577d494d424d53e29c1b9e1f879006992d060f5a02d37`  
		Last Modified: Sat, 28 Feb 2026 01:11:09 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d3092c518457079ad29ae8aaa4a44167a207e5b03ea70bd7587232b7855368`  
		Last Modified: Sat, 28 Feb 2026 01:11:09 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea07fdbeac58fa5ae031f5103513199224ee197d3b9bfb78c98973f4ede3458d`  
		Last Modified: Sat, 28 Feb 2026 02:10:25 GMT  
		Size: 3.4 MB (3419937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e10d1e31052868d4af4e84137fda7c4f274275f7bd7d6a9a2df484e50de31a6`  
		Last Modified: Sat, 28 Feb 2026 02:10:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67197dde0e559538fa7a586f62607fda4178740a90483898e06d2ddaede7cbb`  
		Last Modified: Sat, 28 Feb 2026 02:10:24 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc44efd4f6477d59afc0cfbe2194410af581e707b80f126feb0cd74f9bf7a09a`  
		Last Modified: Sat, 28 Feb 2026 02:10:25 GMT  
		Size: 17.4 MB (17375873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c9d74ba037e2288d688503e060d60473f8de614acf3ae3187fa65e92dbc02a`  
		Last Modified: Sat, 28 Feb 2026 02:10:25 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:229a145b3e0ee40451bed6f5b2a89526281abd795f7f7ea854d4d1d4799e2ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072b82deb7ac10413157846247beaa2874b8d88e217bd14d2b9e51c1daa5e24f`

```dockerfile
```

-	Layers:
	-	`sha256:11f2492afc85739c79961fff3e4a958268c98f2f61a2c248b16707052603eb19`  
		Last Modified: Sat, 28 Feb 2026 02:10:24 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:00153161cea80697b9f8e986d1377f02cbb48eb8367f05eaf8b95139f587ed3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154379691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ceeb4d02aa025a92d5ed84ba0be884ee7c436ea01d7c0b9120b4e65fd2e022`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:33:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:07 GMT
CMD ["sh"]
# Sat, 28 Feb 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 28 Feb 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 28 Feb 2026 01:10:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 28 Feb 2026 01:10:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
VOLUME [/var/lib/docker]
# Sat, 28 Feb 2026 01:10:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 28 Feb 2026 01:10:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 28 Feb 2026 01:10:24 GMT
CMD []
# Sat, 28 Feb 2026 02:10:20 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 28 Feb 2026 02:10:21 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 28 Feb 2026 02:10:21 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 02:10:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Sat, 28 Feb 2026 02:10:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 28 Feb 2026 02:10:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 28 Feb 2026 02:10:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60904be95e049500c5894c6d214007956f1035c22b15ff77ca522ac2f628513`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 8.5 MB (8453564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b0b4b880f947788126e86f12bf4ec6c59bfedb59205ec90c5344b9e9a39861`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1f471b1d5b369a49fb05baa23cedb1b9fa1b9015ee6f27e2b9c5a34b10767e`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 17.3 MB (17349112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662c4f142eb7ddca6437ee0959e5b89824fbe97fa5d1a9d1613c79eb52d0840`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 25.5 MB (25540813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8e4f342d8afaf59c1558d78cd1f5c1e1d074b96b11c5c794918cd74ec7353b`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 10.0 MB (9974085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1186c16de0a9a9c9cc0c496c6164690809b3defab752f3b709727f48df7745fb`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf3a986bcd21c6233dd627338e709a488f1f34ce5a97c2756ff6b05b51a3113`  
		Last Modified: Sat, 28 Feb 2026 00:33:16 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44fcf3aa39e6d6b37daecf7b8046a614dbf9488aaca5bf8eefed943801df648`  
		Last Modified: Sat, 28 Feb 2026 00:33:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbf4035e1f4acb2bd237e1645b2bc3e70a443d5a1848f4882c09901a0a220d8`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 7.2 MB (7213295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad674e6263a8a736b9a1ced02582b966ce06e5c7fc7c2fc21b3714e9a0507831`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 101.3 KB (101286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc08837f92210ce965fca88a82162045be6c2eefb791a36ecbff458a61290501`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c647a3ee71654578d02cac37d0b50bd38b344b814c0b00b5b71988b287163d5`  
		Last Modified: Sat, 28 Feb 2026 01:10:36 GMT  
		Size: 60.4 MB (60436054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7282f0ceaef0633b111139db8bf324c0c4d3045254de20c95b0c6e181195d759`  
		Last Modified: Sat, 28 Feb 2026 01:10:35 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ef9d8eaefdd9ca91eaa763fcfb13a8ada246f317f40c6c60f74d8b8066c975`  
		Last Modified: Sat, 28 Feb 2026 01:10:35 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a0c9b4874456dfa79b0384f80f09bb12d3cf669771248572d23e8dbda772d4`  
		Last Modified: Sat, 28 Feb 2026 02:10:28 GMT  
		Size: 3.4 MB (3394366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a03a35f96f25b1f7b3127fe0aa2bdea3a8744ee63afe40f8b3352ac4f4a1d7f`  
		Last Modified: Sat, 28 Feb 2026 02:10:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750090f3fc9d5fbc8cb9b86df94971408ed314506ff15f2bb5511088fcb09807`  
		Last Modified: Sat, 28 Feb 2026 02:10:28 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f14efc01a4517e185beefc7fc22d0b505da441097201f92af24a940fe91481`  
		Last Modified: Sat, 28 Feb 2026 02:10:29 GMT  
		Size: 17.7 MB (17710528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6cba83eb4ac84187acbc616a27f2d40659212a6046b18fe59bcadc89eb8278`  
		Last Modified: Sat, 28 Feb 2026 02:10:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:5de8e40bc106e0b6e4f2bdc97967ecae0332471ca888034f109e8ffbe0398196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b631622527a2d8bff580b1249ebaace56672581dbe2027d217c30b418d12c5f`

```dockerfile
```

-	Layers:
	-	`sha256:dbbce98df8c42a1eeb8c5a65b56f35f70e73f9fd2e64d5369b69509df7885fcd`  
		Last Modified: Sat, 28 Feb 2026 02:10:28 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:cca5f5b2b62a74f88c0c7aa6dd14ad0e2e4b903a79d818967c8c092057d26985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32370; amd64

```console
$ docker pull docker@sha256:8adc1ea2a335bacb49fd01b1cac0cf3288b6241ce54744a6f1cb58f27720c443
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2025646567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f960ce56780111af6819315df734df0ac835f351417abb824f38888e95b16e9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Sat, 28 Feb 2026 00:42:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 28 Feb 2026 00:44:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 28 Feb 2026 00:44:02 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:44:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Sat, 28 Feb 2026 00:44:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 28 Feb 2026 00:44:18 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:44:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Sat, 28 Feb 2026 00:44:19 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Sat, 28 Feb 2026 00:44:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 28 Feb 2026 00:44:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:44:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-windows-x86_64.exe
# Sat, 28 Feb 2026 00:44:30 GMT
ENV DOCKER_COMPOSE_SHA256=ee84e42b93c501cb0aa2caa84d76b5f30ca6fb92f070e289fc37be7332c5822a
# Sat, 28 Feb 2026 00:44:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8fecd8861c56fefbd35822e522c756a164aa3d37dd262f98ad438a95f8db81`  
		Last Modified: Sat, 28 Feb 2026 00:44:47 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f7b071c2faeaa8569fda83bb88fba9ed73846631970b3b0d14721fc48a8559`  
		Last Modified: Sat, 28 Feb 2026 00:44:46 GMT  
		Size: 369.0 KB (369040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e349d48567f1c6c7903eb5d37de6df665046e21340c38e0a4a5979d7eb05bca0`  
		Last Modified: Sat, 28 Feb 2026 00:44:45 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ef673a03e21f60cb7a2f30229fc9fa4f379cb921aef1b72951239cfdac5594`  
		Last Modified: Sat, 28 Feb 2026 00:44:45 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e190b3d2972d3201fbae0ac07c094428f7a732d8e416908d03315315aaefa`  
		Last Modified: Sat, 28 Feb 2026 00:44:47 GMT  
		Size: 19.4 MB (19445004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a369575b922e845d939ad940aa1ea82e9cd08f06e346a0001ea7483ae5cb2c9d`  
		Last Modified: Sat, 28 Feb 2026 00:44:44 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1522ec443e28a83261bf5734712b4c9e11aec045f70d11b79269e263ce14e8a`  
		Last Modified: Sat, 28 Feb 2026 00:44:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c077c7089ab69c4846f6326bfc8b115c5d20413f8c10b6a513721c8c295a3c3`  
		Last Modified: Sat, 28 Feb 2026 00:44:44 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfd81c02864aa131850545bb63bf55804e738732881a931669f9a619979c074`  
		Last Modified: Sat, 28 Feb 2026 00:44:46 GMT  
		Size: 29.4 MB (29419828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b640fd9bf971384c0ef0f4d964b6d311ee0a0d66729df8dd2ca97af1ccaba502`  
		Last Modified: Sat, 28 Feb 2026 00:44:42 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff016c0dfe5242b2a2a90ceaad29581fdacfef972a2f8709b33f8e7ee17fc0bb`  
		Last Modified: Sat, 28 Feb 2026 00:44:42 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b503dbc573993dbb1567403db5b6765a54d2def3ede2df5271ed13b54484aee`  
		Last Modified: Sat, 28 Feb 2026 00:44:42 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37151df22c07f87a0463edda2aac3d9ee8578d7e747212faa48f66fd04767c54`  
		Last Modified: Sat, 28 Feb 2026 00:44:44 GMT  
		Size: 11.6 MB (11641004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.4773; amd64

```console
$ docker pull docker@sha256:a8b9761529846487729828118bc9d1ce96302a873180a668fdf5cdd9d0b9d4f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1923675549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a7a4f75a27e4ef61863bcc67443ad3281dd982210ff24610cd05e931586ccd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Sat, 28 Feb 2026 00:37:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 28 Feb 2026 00:38:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 28 Feb 2026 00:38:01 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:38:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Sat, 28 Feb 2026 00:38:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 28 Feb 2026 00:38:28 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:38:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Sat, 28 Feb 2026 00:38:30 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Sat, 28 Feb 2026 00:38:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 28 Feb 2026 00:38:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:38:49 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-windows-x86_64.exe
# Sat, 28 Feb 2026 00:38:50 GMT
ENV DOCKER_COMPOSE_SHA256=ee84e42b93c501cb0aa2caa84d76b5f30ca6fb92f070e289fc37be7332c5822a
# Sat, 28 Feb 2026 00:39:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be4d1183e15fd05c6d783c5878ff791e038c48438ca1ba670f3613c106d08d2`  
		Last Modified: Sat, 28 Feb 2026 00:39:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bb9a9714c637901616444e50e2cda139f123a430725359b304d803afc9c9c7`  
		Last Modified: Sat, 28 Feb 2026 00:39:10 GMT  
		Size: 501.8 KB (501824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b98f479028ad7847b57cb613806e29a2c97c5a2a7dffd6d5ce1ce66178b7c68`  
		Last Modified: Sat, 28 Feb 2026 00:39:10 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269a765ecda9d069746e9c2da6e04fba00d1136c12b0cc4061e0a2775869f007`  
		Last Modified: Sat, 28 Feb 2026 00:39:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c78c7d5fa55df50d672144746fcd4e331fc02b195fe3f0701261fd6addf833f`  
		Last Modified: Sat, 28 Feb 2026 00:39:12 GMT  
		Size: 19.4 MB (19440746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9625ce298bdcd094c4964086c9b8611453b7eb30975573133e75884f2915daac`  
		Last Modified: Sat, 28 Feb 2026 00:39:08 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9066580973f92a7516a5f09efd8e0d21d02071fe417c30a60153425ed108ca06`  
		Last Modified: Sat, 28 Feb 2026 00:39:08 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd2225bdb0312a4122abb278e88e0900611dbe800a6b424e65afbd9983abb99`  
		Last Modified: Sat, 28 Feb 2026 00:39:08 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783a739d2dd01ce6b5bb8a724064c3dd2d8feaed38aace83203bef0d8c9045e0`  
		Last Modified: Sat, 28 Feb 2026 00:39:28 GMT  
		Size: 29.4 MB (29424520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b773ca8de4854b1075f7b0efe657b60f19fd158cab220de986164e02b762b82`  
		Last Modified: Sat, 28 Feb 2026 00:39:06 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a37f5c008907b0eba192b39c2a2c6c101e4bcbc45872308cebce66db1cedef8`  
		Last Modified: Sat, 28 Feb 2026 00:39:06 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822095fd913199d892689f8637438d94605d8bc8de9646cfa1ccdd0532473da1`  
		Last Modified: Sat, 28 Feb 2026 00:39:06 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc64c3da6990cf40fafd08e9c67fae552b8d46c42cf5185a2ec0e446b567817`  
		Last Modified: Sat, 28 Feb 2026 00:39:08 GMT  
		Size: 11.6 MB (11639433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:246e353702cde321874dc9ddcaa2d8bf00330f188c1107008646ae6f1dbd9903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull docker@sha256:a8b9761529846487729828118bc9d1ce96302a873180a668fdf5cdd9d0b9d4f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1923675549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a7a4f75a27e4ef61863bcc67443ad3281dd982210ff24610cd05e931586ccd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Sat, 28 Feb 2026 00:37:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 28 Feb 2026 00:38:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 28 Feb 2026 00:38:01 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:38:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Sat, 28 Feb 2026 00:38:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 28 Feb 2026 00:38:28 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:38:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Sat, 28 Feb 2026 00:38:30 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Sat, 28 Feb 2026 00:38:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 28 Feb 2026 00:38:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:38:49 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-windows-x86_64.exe
# Sat, 28 Feb 2026 00:38:50 GMT
ENV DOCKER_COMPOSE_SHA256=ee84e42b93c501cb0aa2caa84d76b5f30ca6fb92f070e289fc37be7332c5822a
# Sat, 28 Feb 2026 00:39:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be4d1183e15fd05c6d783c5878ff791e038c48438ca1ba670f3613c106d08d2`  
		Last Modified: Sat, 28 Feb 2026 00:39:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bb9a9714c637901616444e50e2cda139f123a430725359b304d803afc9c9c7`  
		Last Modified: Sat, 28 Feb 2026 00:39:10 GMT  
		Size: 501.8 KB (501824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b98f479028ad7847b57cb613806e29a2c97c5a2a7dffd6d5ce1ce66178b7c68`  
		Last Modified: Sat, 28 Feb 2026 00:39:10 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269a765ecda9d069746e9c2da6e04fba00d1136c12b0cc4061e0a2775869f007`  
		Last Modified: Sat, 28 Feb 2026 00:39:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c78c7d5fa55df50d672144746fcd4e331fc02b195fe3f0701261fd6addf833f`  
		Last Modified: Sat, 28 Feb 2026 00:39:12 GMT  
		Size: 19.4 MB (19440746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9625ce298bdcd094c4964086c9b8611453b7eb30975573133e75884f2915daac`  
		Last Modified: Sat, 28 Feb 2026 00:39:08 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9066580973f92a7516a5f09efd8e0d21d02071fe417c30a60153425ed108ca06`  
		Last Modified: Sat, 28 Feb 2026 00:39:08 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd2225bdb0312a4122abb278e88e0900611dbe800a6b424e65afbd9983abb99`  
		Last Modified: Sat, 28 Feb 2026 00:39:08 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783a739d2dd01ce6b5bb8a724064c3dd2d8feaed38aace83203bef0d8c9045e0`  
		Last Modified: Sat, 28 Feb 2026 00:39:28 GMT  
		Size: 29.4 MB (29424520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b773ca8de4854b1075f7b0efe657b60f19fd158cab220de986164e02b762b82`  
		Last Modified: Sat, 28 Feb 2026 00:39:06 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a37f5c008907b0eba192b39c2a2c6c101e4bcbc45872308cebce66db1cedef8`  
		Last Modified: Sat, 28 Feb 2026 00:39:06 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822095fd913199d892689f8637438d94605d8bc8de9646cfa1ccdd0532473da1`  
		Last Modified: Sat, 28 Feb 2026 00:39:06 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc64c3da6990cf40fafd08e9c67fae552b8d46c42cf5185a2ec0e446b567817`  
		Last Modified: Sat, 28 Feb 2026 00:39:08 GMT  
		Size: 11.6 MB (11639433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a86a7f53fd5f28509c601a3bee5223705f9e2da2d13c6aa49559db7ecb7fa913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull docker@sha256:8adc1ea2a335bacb49fd01b1cac0cf3288b6241ce54744a6f1cb58f27720c443
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2025646567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f960ce56780111af6819315df734df0ac835f351417abb824f38888e95b16e9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Sat, 28 Feb 2026 00:42:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 28 Feb 2026 00:44:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 28 Feb 2026 00:44:02 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:44:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Sat, 28 Feb 2026 00:44:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 28 Feb 2026 00:44:18 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:44:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Sat, 28 Feb 2026 00:44:19 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Sat, 28 Feb 2026 00:44:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 28 Feb 2026 00:44:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:44:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-windows-x86_64.exe
# Sat, 28 Feb 2026 00:44:30 GMT
ENV DOCKER_COMPOSE_SHA256=ee84e42b93c501cb0aa2caa84d76b5f30ca6fb92f070e289fc37be7332c5822a
# Sat, 28 Feb 2026 00:44:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8fecd8861c56fefbd35822e522c756a164aa3d37dd262f98ad438a95f8db81`  
		Last Modified: Sat, 28 Feb 2026 00:44:47 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f7b071c2faeaa8569fda83bb88fba9ed73846631970b3b0d14721fc48a8559`  
		Last Modified: Sat, 28 Feb 2026 00:44:46 GMT  
		Size: 369.0 KB (369040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e349d48567f1c6c7903eb5d37de6df665046e21340c38e0a4a5979d7eb05bca0`  
		Last Modified: Sat, 28 Feb 2026 00:44:45 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ef673a03e21f60cb7a2f30229fc9fa4f379cb921aef1b72951239cfdac5594`  
		Last Modified: Sat, 28 Feb 2026 00:44:45 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e190b3d2972d3201fbae0ac07c094428f7a732d8e416908d03315315aaefa`  
		Last Modified: Sat, 28 Feb 2026 00:44:47 GMT  
		Size: 19.4 MB (19445004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a369575b922e845d939ad940aa1ea82e9cd08f06e346a0001ea7483ae5cb2c9d`  
		Last Modified: Sat, 28 Feb 2026 00:44:44 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1522ec443e28a83261bf5734712b4c9e11aec045f70d11b79269e263ce14e8a`  
		Last Modified: Sat, 28 Feb 2026 00:44:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c077c7089ab69c4846f6326bfc8b115c5d20413f8c10b6a513721c8c295a3c3`  
		Last Modified: Sat, 28 Feb 2026 00:44:44 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfd81c02864aa131850545bb63bf55804e738732881a931669f9a619979c074`  
		Last Modified: Sat, 28 Feb 2026 00:44:46 GMT  
		Size: 29.4 MB (29419828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b640fd9bf971384c0ef0f4d964b6d311ee0a0d66729df8dd2ca97af1ccaba502`  
		Last Modified: Sat, 28 Feb 2026 00:44:42 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff016c0dfe5242b2a2a90ceaad29581fdacfef972a2f8709b33f8e7ee17fc0bb`  
		Last Modified: Sat, 28 Feb 2026 00:44:42 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b503dbc573993dbb1567403db5b6765a54d2def3ede2df5271ed13b54484aee`  
		Last Modified: Sat, 28 Feb 2026 00:44:42 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37151df22c07f87a0463edda2aac3d9ee8578d7e747212faa48f66fd04767c54`  
		Last Modified: Sat, 28 Feb 2026 00:44:44 GMT  
		Size: 11.6 MB (11641004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.3`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3-cli`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3-dind`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3-dind-rootless`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3-windowsservercore`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3.0`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3.0-alpine3.23`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3.0-cli`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3.0-cli-alpine3.23`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3.0-dind`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3.0-dind-alpine3.23`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3.0-dind-rootless`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3.0-windowsservercore`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.3.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:cli`

```console
$ docker pull docker@sha256:cab69e2d0a1a2ea9a1ce1060252f439e83483ae41ec09317aecb33b08a0656a5
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
$ docker pull docker@sha256:61eaf318a33c0d37231cfcb496ad6e4c547e609a992c43ba456be9eefa4223cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70302244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4660288b9b1871838afdbb93297d9606cd0cecb9108d84c5725428e810e2f60e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:32:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:32:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:32:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ad56decde40eed4b884568f98b02d946417493176196dc029ab5e17c16b8eb`  
		Last Modified: Sat, 28 Feb 2026 00:33:12 GMT  
		Size: 8.4 MB (8399669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342aaf2cc08446a08f0c3201e79521412a27ec651d43233e7591635ba001c7df`  
		Last Modified: Sat, 28 Feb 2026 00:33:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9632763a5f6e5657586d42acd7aab8f7b50c5a9c42bc6c925c7cc1c4690cbd`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 18.8 MB (18773125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273ed7fc2746040170324eb790dc34cf0f4e212546ea29a395b7efefd95385d0`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eae5b0ffe938ee3f0cdd909657ca40f0528831b03d3d3ec32d88bf2a889cca`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 11.0 MB (10953930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed25dc6106a64ddaa30940a80175eddee65e79eac95d515a7c9fa35d9d93a22`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048c355ee240ae4713fa8e796335e4a6ea52fc7b34f42881992fb2954dd1ac2e`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f3f6dd36e1c7b333ba1f09b0987ea030d3d2750f5033170f2e746227cff7e6`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:b0475bfdf9f0ff004e8adccde3b3e701c17ff24f1bac9068eda9e1a232629c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43f6533aace4da9151c80022d3054ae46ee57571d31964300d821b26e5465eb`

```dockerfile
```

-	Layers:
	-	`sha256:ffef58d7d564c693206df20dfa8398493c3bd2a9e4e5126a12d67213dd509e0b`  
		Last Modified: Sat, 28 Feb 2026 00:33:12 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:51c7cd8fd48d2bb76401b87baa09a14b170fe52ca356c0c99fd7e168d80153d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66407812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4456f4155a1327a286d3fc189e230eb06aacf818b2a72b293e164ec5c0320e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:33:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:33:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:33:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:36 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:36 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b2c1188f77d466b63114530c948db4a2b72f6432015051eb4c6fc5ed17a318`  
		Last Modified: Sat, 28 Feb 2026 00:33:47 GMT  
		Size: 8.3 MB (8300892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d069c0ddccdd129439f3fc19b3beb0deb0ea53ebe0d54791b223081c0bfd09`  
		Last Modified: Sat, 28 Feb 2026 00:33:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84f79f2e027c27c1420192bbb6269e4133d62301076e5f92f52a21a7c341822`  
		Last Modified: Sat, 28 Feb 2026 00:33:47 GMT  
		Size: 17.6 MB (17574992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d9822253e2de58052e59355a3ee3a3e3219482e8ff9da6021bba9c31169a73`  
		Last Modified: Sat, 28 Feb 2026 00:33:47 GMT  
		Size: 26.6 MB (26574514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977fe3e040234fe198164a9728011f9bdf228d76a92669ba3aa98acbf91cd8d1`  
		Last Modified: Sat, 28 Feb 2026 00:33:48 GMT  
		Size: 10.4 MB (10385436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9b5078999b461db61885ae27aefeaad4cd7679c996ee4dc106c5481deb7172`  
		Last Modified: Sat, 28 Feb 2026 00:33:48 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcf453e2e7207817cd2f1cafcd2c26502a7cec3072cb5a8b8c1e49e7720eef6`  
		Last Modified: Sat, 28 Feb 2026 00:33:48 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3831f33bbdf7e0cd2a3ba77cc3d9b6dea4ffd87f09eb7a18d0df5ac6354dae`  
		Last Modified: Sat, 28 Feb 2026 00:33:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:9d7716df1aede936adaf0fe3deb36addd057a35780b0186f4f1f7d1955c41b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af00649395af49edb0bbd0a19fd0cc1db7af9915ebd70cafa59ebee4f311b60`

```dockerfile
```

-	Layers:
	-	`sha256:e6b2249d10157cab657330d395f90242fae24ca9c9a12ee8b328a621f2e0ecfc`  
		Last Modified: Sat, 28 Feb 2026 00:33:46 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:381de97367b51842200da5a791fb997b3b5c9149900d68064288e6b190f7e89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65364001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d397b31096240e447d64f1431afc291561f750ea87a68322c9ce5eda7848952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:32:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:32:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:32:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:32:34 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:32:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:32:34 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:32:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:32:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:32:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:32:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:32:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282f6e2b7c9718d720ce426672429335541cf1c919bf9c845984c433c879cdc4`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 7.6 MB (7597811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354b5b8fd3a086ebaa1f824553d2d81811f9bc34aa15f16251dd1149b040957f`  
		Last Modified: Sat, 28 Feb 2026 00:32:46 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c343ba8124dc1173c2441732470ac81040c16fa72ca600062307c2150db08efd`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 17.6 MB (17566420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3c55e011e6f401320580bc9559a8eec2bd1121139952f1d621befd1557f233`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 26.5 MB (26546113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01b5cad9fc8f11ff6eceb574bedcff79a5acd3f04a71d09030e0b337df68f7b`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 10.4 MB (10369780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41923b1f427db13299befcd38419467285b2ca66ad0a4b33f483296df5b5f467`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440d27ed514452926e359f9aeccb369ab42162dc457ef0cb90a9aa6684666b0c`  
		Last Modified: Sat, 28 Feb 2026 00:32:48 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47078bcf7b70f7b4c214ba0d20f1c8e10e7347e12a105ca35addd773811b04c1`  
		Last Modified: Sat, 28 Feb 2026 00:32:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:e5807ae87b8e7066b82da385443764ab7e4f21308b4181eb58c88975d7c167cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528510c893d8b8f034b3bbc17275f034345c8c9d3852c827b5e357d6798d5b1d`

```dockerfile
```

-	Layers:
	-	`sha256:bb1422430bd5e44adbb541518e3a9e79c78ad25d05c8aa6b1b29d2934d4762a3`  
		Last Modified: Sat, 28 Feb 2026 00:32:46 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b419ff204d51c59cf7e3e01c4277dad148fc5f300f172c2f65700a1cac93e7c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65516823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b618349b315d48d95f60e08d9377bd62bdfd24403eeb09069be71e5e564326e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:33:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60904be95e049500c5894c6d214007956f1035c22b15ff77ca522ac2f628513`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 8.5 MB (8453564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b0b4b880f947788126e86f12bf4ec6c59bfedb59205ec90c5344b9e9a39861`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1f471b1d5b369a49fb05baa23cedb1b9fa1b9015ee6f27e2b9c5a34b10767e`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 17.3 MB (17349112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662c4f142eb7ddca6437ee0959e5b89824fbe97fa5d1a9d1613c79eb52d0840`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 25.5 MB (25540813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8e4f342d8afaf59c1558d78cd1f5c1e1d074b96b11c5c794918cd74ec7353b`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 10.0 MB (9974085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1186c16de0a9a9c9cc0c496c6164690809b3defab752f3b709727f48df7745fb`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf3a986bcd21c6233dd627338e709a488f1f34ce5a97c2756ff6b05b51a3113`  
		Last Modified: Sat, 28 Feb 2026 00:33:16 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44fcf3aa39e6d6b37daecf7b8046a614dbf9488aaca5bf8eefed943801df648`  
		Last Modified: Sat, 28 Feb 2026 00:33:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:e9de5b8217500a0ec096e0b8bb9a8789c7a9724c61ccc6ac5cd2f4a7e3280d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f4db5f2e930b8e32deee8f1ae4ac490c44829280a680b77e4907438dae3400`

```dockerfile
```

-	Layers:
	-	`sha256:0433045c024921198fd8eb3b1df4aba3072436207276e52a0670d152f6b1446b`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:68f6d9ab84623d1116c5432a3b924a07ee09960e6129ca1cb03ef14010588cb4
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
$ docker pull docker@sha256:81fcfefed70c7154045d23dec3523719e7564ad2605c1a8a29fdd13ae9e1c710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143960556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c643ed57132b58411e32edf0540e88a41d1fbc98199d74f6565bc1777e73d688`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:32:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:32:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:32:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:05 GMT
CMD ["sh"]
# Sat, 28 Feb 2026 01:10:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 28 Feb 2026 01:10:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 28 Feb 2026 01:10:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 28 Feb 2026 01:10:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
VOLUME [/var/lib/docker]
# Sat, 28 Feb 2026 01:10:57 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 28 Feb 2026 01:10:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 28 Feb 2026 01:10:57 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ad56decde40eed4b884568f98b02d946417493176196dc029ab5e17c16b8eb`  
		Last Modified: Sat, 28 Feb 2026 00:33:12 GMT  
		Size: 8.4 MB (8399669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342aaf2cc08446a08f0c3201e79521412a27ec651d43233e7591635ba001c7df`  
		Last Modified: Sat, 28 Feb 2026 00:33:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9632763a5f6e5657586d42acd7aab8f7b50c5a9c42bc6c925c7cc1c4690cbd`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 18.8 MB (18773125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273ed7fc2746040170324eb790dc34cf0f4e212546ea29a395b7efefd95385d0`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eae5b0ffe938ee3f0cdd909657ca40f0528831b03d3d3ec32d88bf2a889cca`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 11.0 MB (10953930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed25dc6106a64ddaa30940a80175eddee65e79eac95d515a7c9fa35d9d93a22`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048c355ee240ae4713fa8e796335e4a6ea52fc7b34f42881992fb2954dd1ac2e`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f3f6dd36e1c7b333ba1f09b0987ea030d3d2750f5033170f2e746227cff7e6`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaa4baf3866b503b2f32ce744935a68b0df9d10607680ef5682126f09b9360`  
		Last Modified: Sat, 28 Feb 2026 01:11:08 GMT  
		Size: 6.9 MB (6934691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec2ed410cea5bc307ea8e2227c83b433957ceb6c916efe3e747edc437445f4e`  
		Last Modified: Sat, 28 Feb 2026 01:11:07 GMT  
		Size: 92.5 KB (92468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5521b863247b8ec145bb965e69f88121a5d4658dc8c98d3053ff3c005d4b3b48`  
		Last Modified: Sat, 28 Feb 2026 01:11:08 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27c5afc8cc77a003520d64522134adc6469902a7ec92500709691b1dc4e5200`  
		Last Modified: Sat, 28 Feb 2026 01:11:09 GMT  
		Size: 66.6 MB (66625155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e365fc1dcf7059372ca577d494d424d53e29c1b9e1f879006992d060f5a02d37`  
		Last Modified: Sat, 28 Feb 2026 01:11:09 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d3092c518457079ad29ae8aaa4a44167a207e5b03ea70bd7587232b7855368`  
		Last Modified: Sat, 28 Feb 2026 01:11:09 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:a267e8d9da86afb00b8c97e7c1c023b2d8758a8df73b3b5755f1f1ae99745efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04cb494266b4fc82300382c99c4b78a744ac87a5a3d60f921dac122209436850`

```dockerfile
```

-	Layers:
	-	`sha256:bca36398fa62499981389ef963ec3e8732477fd3189e49d5b0a19962f021e882`  
		Last Modified: Sat, 28 Feb 2026 01:11:07 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:a36a708ef4ab20c051d7182ae2f16870c654ce36c041a883f4b3045498542416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135811601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c805d64686b3d65ef3dd20aa06d17d5c4074716241083750c4ce663fc641fd77`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:33:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:33:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:33:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:36 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:36 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:39 GMT
CMD ["sh"]
# Sat, 28 Feb 2026 01:08:57 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 28 Feb 2026 01:08:58 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 28 Feb 2026 01:08:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 01:09:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 28 Feb 2026 01:09:03 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 28 Feb 2026 01:09:03 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 28 Feb 2026 01:09:03 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:09:03 GMT
VOLUME [/var/lib/docker]
# Sat, 28 Feb 2026 01:09:03 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 28 Feb 2026 01:09:03 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 28 Feb 2026 01:09:03 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b2c1188f77d466b63114530c948db4a2b72f6432015051eb4c6fc5ed17a318`  
		Last Modified: Sat, 28 Feb 2026 00:33:47 GMT  
		Size: 8.3 MB (8300892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d069c0ddccdd129439f3fc19b3beb0deb0ea53ebe0d54791b223081c0bfd09`  
		Last Modified: Sat, 28 Feb 2026 00:33:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84f79f2e027c27c1420192bbb6269e4133d62301076e5f92f52a21a7c341822`  
		Last Modified: Sat, 28 Feb 2026 00:33:47 GMT  
		Size: 17.6 MB (17574992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d9822253e2de58052e59355a3ee3a3e3219482e8ff9da6021bba9c31169a73`  
		Last Modified: Sat, 28 Feb 2026 00:33:47 GMT  
		Size: 26.6 MB (26574514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977fe3e040234fe198164a9728011f9bdf228d76a92669ba3aa98acbf91cd8d1`  
		Last Modified: Sat, 28 Feb 2026 00:33:48 GMT  
		Size: 10.4 MB (10385436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9b5078999b461db61885ae27aefeaad4cd7679c996ee4dc106c5481deb7172`  
		Last Modified: Sat, 28 Feb 2026 00:33:48 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcf453e2e7207817cd2f1cafcd2c26502a7cec3072cb5a8b8c1e49e7720eef6`  
		Last Modified: Sat, 28 Feb 2026 00:33:48 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3831f33bbdf7e0cd2a3ba77cc3d9b6dea4ffd87f09eb7a18d0df5ac6354dae`  
		Last Modified: Sat, 28 Feb 2026 00:33:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b7b97efb6c96c9626c6452c6d35907116fd44e9d8dd4a730e3de085fdfcb87`  
		Last Modified: Sat, 28 Feb 2026 01:09:14 GMT  
		Size: 7.3 MB (7271699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb28f43f383cd367845812769677219708f450192b0bce32ea6ae1323cbbf12c`  
		Last Modified: Sat, 28 Feb 2026 01:09:13 GMT  
		Size: 91.8 KB (91779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1143b390d4eb69eec28024598bde4e9a359c89c6219eb10475930689486123`  
		Last Modified: Sat, 28 Feb 2026 01:09:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288371601350ba56b1dc5d245271aeda8acc45db516a7cf1ca4edee711d7349b`  
		Last Modified: Sat, 28 Feb 2026 01:09:15 GMT  
		Size: 62.0 MB (62034312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8aa70bb05db86bf9265162619f611758dbcaa8ab0f06e5712909b80a97e6472`  
		Last Modified: Sat, 28 Feb 2026 01:09:13 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c3984a3e460e2c4cf1824f452f5e8a3472cd095ca0044b172ccf33ba31b4c5`  
		Last Modified: Sat, 28 Feb 2026 01:09:14 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:0ada12f8e5ddea957492c54b4028272b319b90df66b2ec6482a748996caef3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a15c8c9d8910fa3b67e64a0b4c5ff0a3a043b468f787a3193101971707f19ad`

```dockerfile
```

-	Layers:
	-	`sha256:d8679db966c7defd214d55efd0fc6a1f698492ad859d9708372af6e6bae01e35`  
		Last Modified: Sat, 28 Feb 2026 01:09:13 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:c1e28a4f3b227ee7db14d82c37324957af6fc4efbc0521fff59f00ea6ecce2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133894570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e0c6071fac97999a74b349e820fdabef122b6e9bf5555a22afcce2432cf2f8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:32:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:32:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:32:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:32:34 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:32:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:32:34 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:32:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:32:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:32:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:32:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:32:39 GMT
CMD ["sh"]
# Sat, 28 Feb 2026 01:09:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 28 Feb 2026 01:09:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 28 Feb 2026 01:09:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 01:09:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 28 Feb 2026 01:09:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 28 Feb 2026 01:09:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 28 Feb 2026 01:09:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:09:13 GMT
VOLUME [/var/lib/docker]
# Sat, 28 Feb 2026 01:09:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 28 Feb 2026 01:09:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 28 Feb 2026 01:09:13 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282f6e2b7c9718d720ce426672429335541cf1c919bf9c845984c433c879cdc4`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 7.6 MB (7597811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354b5b8fd3a086ebaa1f824553d2d81811f9bc34aa15f16251dd1149b040957f`  
		Last Modified: Sat, 28 Feb 2026 00:32:46 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c343ba8124dc1173c2441732470ac81040c16fa72ca600062307c2150db08efd`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 17.6 MB (17566420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3c55e011e6f401320580bc9559a8eec2bd1121139952f1d621befd1557f233`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 26.5 MB (26546113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01b5cad9fc8f11ff6eceb574bedcff79a5acd3f04a71d09030e0b337df68f7b`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 10.4 MB (10369780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41923b1f427db13299befcd38419467285b2ca66ad0a4b33f483296df5b5f467`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440d27ed514452926e359f9aeccb369ab42162dc457ef0cb90a9aa6684666b0c`  
		Last Modified: Sat, 28 Feb 2026 00:32:48 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47078bcf7b70f7b4c214ba0d20f1c8e10e7347e12a105ca35addd773811b04c1`  
		Last Modified: Sat, 28 Feb 2026 00:32:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4646932f3e91cb6ab7dbc864b4e08445a66ec41cd374fbe49ec1896ed88a982`  
		Last Modified: Sat, 28 Feb 2026 01:09:24 GMT  
		Size: 6.6 MB (6573022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19c564899e9b5a6c19f0cdc29230499311e905a2b3da9955c8d458746d5e905`  
		Last Modified: Sat, 28 Feb 2026 01:09:23 GMT  
		Size: 88.2 KB (88156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01f4e2cf953a2d6d9a9f3a1443b3b8ef98280b66a90e8d007394fcd607f0f91`  
		Last Modified: Sat, 28 Feb 2026 01:09:23 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1686d5a17066d20b94ebba8ea4ad36abb7e768dac3ff5094d9f899ac1212beac`  
		Last Modified: Sat, 28 Feb 2026 01:09:25 GMT  
		Size: 61.9 MB (61863393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829040129e131eff6b7babe59601d0efda9023e17990e656b9947f091da2c036`  
		Last Modified: Sat, 28 Feb 2026 01:09:25 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d5f9cb70da8c12cf982ed75d5dd9eb4c800c749ac416383fac30c4dc2dd3dd`  
		Last Modified: Sat, 28 Feb 2026 01:09:24 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:4f94ebe1fabec8df89f1b602cc9af7f71be9db93d156dbd2c7070c36533ea9dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac1cbf9bbda4bc07b7c4a7ece169ab46ee3ee85ceab6511396586e6419b2fbe`

```dockerfile
```

-	Layers:
	-	`sha256:e5a96ba22363c34a75191791ae68225d552c1f1627d115e575d9c76c6589fe71`  
		Last Modified: Sat, 28 Feb 2026 01:09:23 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4ca8506088c30f906cdfad8f863b9f2c41eef5b159e4b752a6c8d1c07fca74f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133273459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8ecd5b1d17216fcea5159b6dcf8aeffebfae9306de065fe5ddfb98aae43fa6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:33:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:07 GMT
CMD ["sh"]
# Sat, 28 Feb 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 28 Feb 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 28 Feb 2026 01:10:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 28 Feb 2026 01:10:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
VOLUME [/var/lib/docker]
# Sat, 28 Feb 2026 01:10:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 28 Feb 2026 01:10:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 28 Feb 2026 01:10:24 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60904be95e049500c5894c6d214007956f1035c22b15ff77ca522ac2f628513`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 8.5 MB (8453564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b0b4b880f947788126e86f12bf4ec6c59bfedb59205ec90c5344b9e9a39861`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1f471b1d5b369a49fb05baa23cedb1b9fa1b9015ee6f27e2b9c5a34b10767e`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 17.3 MB (17349112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662c4f142eb7ddca6437ee0959e5b89824fbe97fa5d1a9d1613c79eb52d0840`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 25.5 MB (25540813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8e4f342d8afaf59c1558d78cd1f5c1e1d074b96b11c5c794918cd74ec7353b`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 10.0 MB (9974085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1186c16de0a9a9c9cc0c496c6164690809b3defab752f3b709727f48df7745fb`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf3a986bcd21c6233dd627338e709a488f1f34ce5a97c2756ff6b05b51a3113`  
		Last Modified: Sat, 28 Feb 2026 00:33:16 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44fcf3aa39e6d6b37daecf7b8046a614dbf9488aaca5bf8eefed943801df648`  
		Last Modified: Sat, 28 Feb 2026 00:33:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbf4035e1f4acb2bd237e1645b2bc3e70a443d5a1848f4882c09901a0a220d8`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 7.2 MB (7213295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad674e6263a8a736b9a1ced02582b966ce06e5c7fc7c2fc21b3714e9a0507831`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 101.3 KB (101286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc08837f92210ce965fca88a82162045be6c2eefb791a36ecbff458a61290501`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c647a3ee71654578d02cac37d0b50bd38b344b814c0b00b5b71988b287163d5`  
		Last Modified: Sat, 28 Feb 2026 01:10:36 GMT  
		Size: 60.4 MB (60436054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7282f0ceaef0633b111139db8bf324c0c4d3045254de20c95b0c6e181195d759`  
		Last Modified: Sat, 28 Feb 2026 01:10:35 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ef9d8eaefdd9ca91eaa763fcfb13a8ada246f317f40c6c60f74d8b8066c975`  
		Last Modified: Sat, 28 Feb 2026 01:10:35 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:2748df42f6df2e6f3e87566ec113dba1c9c6c94d8463cfc0fbcc2d64ab4f9733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42e0ddb0a8b1512b11247ffdb0d8af1f53634b4d9b91e61ac1fe42684abdfa8`

```dockerfile
```

-	Layers:
	-	`sha256:85137676ef3e7b9bd815bd4c1e81e8f915dd5665b890b53565ff08c370b3d55c`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:67c4114553192e9072969fc347426048cfe4192385dc762d8eb449c05e904255
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:0a0ac6f82505da7dca92525bc232f36d9e2094c325a98e387afa70736334b435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164757707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e095376b1219c57b174714bd2cb2119f6fbb53eed15b522810c059b24393a183`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:32:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:32:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:32:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:05 GMT
CMD ["sh"]
# Sat, 28 Feb 2026 01:10:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 28 Feb 2026 01:10:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 28 Feb 2026 01:10:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 28 Feb 2026 01:10:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
VOLUME [/var/lib/docker]
# Sat, 28 Feb 2026 01:10:57 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 28 Feb 2026 01:10:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 28 Feb 2026 01:10:57 GMT
CMD []
# Sat, 28 Feb 2026 02:10:17 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 28 Feb 2026 02:10:17 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 28 Feb 2026 02:10:17 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 02:10:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Sat, 28 Feb 2026 02:10:18 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 28 Feb 2026 02:10:18 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 28 Feb 2026 02:10:18 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ad56decde40eed4b884568f98b02d946417493176196dc029ab5e17c16b8eb`  
		Last Modified: Sat, 28 Feb 2026 00:33:12 GMT  
		Size: 8.4 MB (8399669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342aaf2cc08446a08f0c3201e79521412a27ec651d43233e7591635ba001c7df`  
		Last Modified: Sat, 28 Feb 2026 00:33:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9632763a5f6e5657586d42acd7aab8f7b50c5a9c42bc6c925c7cc1c4690cbd`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 18.8 MB (18773125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273ed7fc2746040170324eb790dc34cf0f4e212546ea29a395b7efefd95385d0`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eae5b0ffe938ee3f0cdd909657ca40f0528831b03d3d3ec32d88bf2a889cca`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 11.0 MB (10953930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed25dc6106a64ddaa30940a80175eddee65e79eac95d515a7c9fa35d9d93a22`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048c355ee240ae4713fa8e796335e4a6ea52fc7b34f42881992fb2954dd1ac2e`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f3f6dd36e1c7b333ba1f09b0987ea030d3d2750f5033170f2e746227cff7e6`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaa4baf3866b503b2f32ce744935a68b0df9d10607680ef5682126f09b9360`  
		Last Modified: Sat, 28 Feb 2026 01:11:08 GMT  
		Size: 6.9 MB (6934691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec2ed410cea5bc307ea8e2227c83b433957ceb6c916efe3e747edc437445f4e`  
		Last Modified: Sat, 28 Feb 2026 01:11:07 GMT  
		Size: 92.5 KB (92468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5521b863247b8ec145bb965e69f88121a5d4658dc8c98d3053ff3c005d4b3b48`  
		Last Modified: Sat, 28 Feb 2026 01:11:08 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27c5afc8cc77a003520d64522134adc6469902a7ec92500709691b1dc4e5200`  
		Last Modified: Sat, 28 Feb 2026 01:11:09 GMT  
		Size: 66.6 MB (66625155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e365fc1dcf7059372ca577d494d424d53e29c1b9e1f879006992d060f5a02d37`  
		Last Modified: Sat, 28 Feb 2026 01:11:09 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d3092c518457079ad29ae8aaa4a44167a207e5b03ea70bd7587232b7855368`  
		Last Modified: Sat, 28 Feb 2026 01:11:09 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea07fdbeac58fa5ae031f5103513199224ee197d3b9bfb78c98973f4ede3458d`  
		Last Modified: Sat, 28 Feb 2026 02:10:25 GMT  
		Size: 3.4 MB (3419937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e10d1e31052868d4af4e84137fda7c4f274275f7bd7d6a9a2df484e50de31a6`  
		Last Modified: Sat, 28 Feb 2026 02:10:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67197dde0e559538fa7a586f62607fda4178740a90483898e06d2ddaede7cbb`  
		Last Modified: Sat, 28 Feb 2026 02:10:24 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc44efd4f6477d59afc0cfbe2194410af581e707b80f126feb0cd74f9bf7a09a`  
		Last Modified: Sat, 28 Feb 2026 02:10:25 GMT  
		Size: 17.4 MB (17375873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c9d74ba037e2288d688503e060d60473f8de614acf3ae3187fa65e92dbc02a`  
		Last Modified: Sat, 28 Feb 2026 02:10:25 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:229a145b3e0ee40451bed6f5b2a89526281abd795f7f7ea854d4d1d4799e2ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072b82deb7ac10413157846247beaa2874b8d88e217bd14d2b9e51c1daa5e24f`

```dockerfile
```

-	Layers:
	-	`sha256:11f2492afc85739c79961fff3e4a958268c98f2f61a2c248b16707052603eb19`  
		Last Modified: Sat, 28 Feb 2026 02:10:24 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:00153161cea80697b9f8e986d1377f02cbb48eb8367f05eaf8b95139f587ed3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154379691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ceeb4d02aa025a92d5ed84ba0be884ee7c436ea01d7c0b9120b4e65fd2e022`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:33:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:07 GMT
CMD ["sh"]
# Sat, 28 Feb 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 28 Feb 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 28 Feb 2026 01:10:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 28 Feb 2026 01:10:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
VOLUME [/var/lib/docker]
# Sat, 28 Feb 2026 01:10:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 28 Feb 2026 01:10:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 28 Feb 2026 01:10:24 GMT
CMD []
# Sat, 28 Feb 2026 02:10:20 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 28 Feb 2026 02:10:21 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 28 Feb 2026 02:10:21 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 02:10:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Sat, 28 Feb 2026 02:10:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 28 Feb 2026 02:10:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 28 Feb 2026 02:10:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60904be95e049500c5894c6d214007956f1035c22b15ff77ca522ac2f628513`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 8.5 MB (8453564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b0b4b880f947788126e86f12bf4ec6c59bfedb59205ec90c5344b9e9a39861`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1f471b1d5b369a49fb05baa23cedb1b9fa1b9015ee6f27e2b9c5a34b10767e`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 17.3 MB (17349112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662c4f142eb7ddca6437ee0959e5b89824fbe97fa5d1a9d1613c79eb52d0840`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 25.5 MB (25540813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8e4f342d8afaf59c1558d78cd1f5c1e1d074b96b11c5c794918cd74ec7353b`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 10.0 MB (9974085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1186c16de0a9a9c9cc0c496c6164690809b3defab752f3b709727f48df7745fb`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf3a986bcd21c6233dd627338e709a488f1f34ce5a97c2756ff6b05b51a3113`  
		Last Modified: Sat, 28 Feb 2026 00:33:16 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44fcf3aa39e6d6b37daecf7b8046a614dbf9488aaca5bf8eefed943801df648`  
		Last Modified: Sat, 28 Feb 2026 00:33:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbf4035e1f4acb2bd237e1645b2bc3e70a443d5a1848f4882c09901a0a220d8`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 7.2 MB (7213295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad674e6263a8a736b9a1ced02582b966ce06e5c7fc7c2fc21b3714e9a0507831`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 101.3 KB (101286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc08837f92210ce965fca88a82162045be6c2eefb791a36ecbff458a61290501`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c647a3ee71654578d02cac37d0b50bd38b344b814c0b00b5b71988b287163d5`  
		Last Modified: Sat, 28 Feb 2026 01:10:36 GMT  
		Size: 60.4 MB (60436054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7282f0ceaef0633b111139db8bf324c0c4d3045254de20c95b0c6e181195d759`  
		Last Modified: Sat, 28 Feb 2026 01:10:35 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ef9d8eaefdd9ca91eaa763fcfb13a8ada246f317f40c6c60f74d8b8066c975`  
		Last Modified: Sat, 28 Feb 2026 01:10:35 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a0c9b4874456dfa79b0384f80f09bb12d3cf669771248572d23e8dbda772d4`  
		Last Modified: Sat, 28 Feb 2026 02:10:28 GMT  
		Size: 3.4 MB (3394366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a03a35f96f25b1f7b3127fe0aa2bdea3a8744ee63afe40f8b3352ac4f4a1d7f`  
		Last Modified: Sat, 28 Feb 2026 02:10:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750090f3fc9d5fbc8cb9b86df94971408ed314506ff15f2bb5511088fcb09807`  
		Last Modified: Sat, 28 Feb 2026 02:10:28 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f14efc01a4517e185beefc7fc22d0b505da441097201f92af24a940fe91481`  
		Last Modified: Sat, 28 Feb 2026 02:10:29 GMT  
		Size: 17.7 MB (17710528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6cba83eb4ac84187acbc616a27f2d40659212a6046b18fe59bcadc89eb8278`  
		Last Modified: Sat, 28 Feb 2026 02:10:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:5de8e40bc106e0b6e4f2bdc97967ecae0332471ca888034f109e8ffbe0398196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b631622527a2d8bff580b1249ebaace56672581dbe2027d217c30b418d12c5f`

```dockerfile
```

-	Layers:
	-	`sha256:dbbce98df8c42a1eeb8c5a65b56f35f70e73f9fd2e64d5369b69509df7885fcd`  
		Last Modified: Sat, 28 Feb 2026 02:10:28 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:68f6d9ab84623d1116c5432a3b924a07ee09960e6129ca1cb03ef14010588cb4
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
$ docker pull docker@sha256:81fcfefed70c7154045d23dec3523719e7564ad2605c1a8a29fdd13ae9e1c710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143960556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c643ed57132b58411e32edf0540e88a41d1fbc98199d74f6565bc1777e73d688`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:32:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:32:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:32:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:05 GMT
CMD ["sh"]
# Sat, 28 Feb 2026 01:10:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 28 Feb 2026 01:10:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 28 Feb 2026 01:10:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 28 Feb 2026 01:10:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:10:57 GMT
VOLUME [/var/lib/docker]
# Sat, 28 Feb 2026 01:10:57 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 28 Feb 2026 01:10:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 28 Feb 2026 01:10:57 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ad56decde40eed4b884568f98b02d946417493176196dc029ab5e17c16b8eb`  
		Last Modified: Sat, 28 Feb 2026 00:33:12 GMT  
		Size: 8.4 MB (8399669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342aaf2cc08446a08f0c3201e79521412a27ec651d43233e7591635ba001c7df`  
		Last Modified: Sat, 28 Feb 2026 00:33:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9632763a5f6e5657586d42acd7aab8f7b50c5a9c42bc6c925c7cc1c4690cbd`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 18.8 MB (18773125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273ed7fc2746040170324eb790dc34cf0f4e212546ea29a395b7efefd95385d0`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eae5b0ffe938ee3f0cdd909657ca40f0528831b03d3d3ec32d88bf2a889cca`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 11.0 MB (10953930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed25dc6106a64ddaa30940a80175eddee65e79eac95d515a7c9fa35d9d93a22`  
		Last Modified: Sat, 28 Feb 2026 00:33:13 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048c355ee240ae4713fa8e796335e4a6ea52fc7b34f42881992fb2954dd1ac2e`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f3f6dd36e1c7b333ba1f09b0987ea030d3d2750f5033170f2e746227cff7e6`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaa4baf3866b503b2f32ce744935a68b0df9d10607680ef5682126f09b9360`  
		Last Modified: Sat, 28 Feb 2026 01:11:08 GMT  
		Size: 6.9 MB (6934691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec2ed410cea5bc307ea8e2227c83b433957ceb6c916efe3e747edc437445f4e`  
		Last Modified: Sat, 28 Feb 2026 01:11:07 GMT  
		Size: 92.5 KB (92468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5521b863247b8ec145bb965e69f88121a5d4658dc8c98d3053ff3c005d4b3b48`  
		Last Modified: Sat, 28 Feb 2026 01:11:08 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27c5afc8cc77a003520d64522134adc6469902a7ec92500709691b1dc4e5200`  
		Last Modified: Sat, 28 Feb 2026 01:11:09 GMT  
		Size: 66.6 MB (66625155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e365fc1dcf7059372ca577d494d424d53e29c1b9e1f879006992d060f5a02d37`  
		Last Modified: Sat, 28 Feb 2026 01:11:09 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d3092c518457079ad29ae8aaa4a44167a207e5b03ea70bd7587232b7855368`  
		Last Modified: Sat, 28 Feb 2026 01:11:09 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:a267e8d9da86afb00b8c97e7c1c023b2d8758a8df73b3b5755f1f1ae99745efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04cb494266b4fc82300382c99c4b78a744ac87a5a3d60f921dac122209436850`

```dockerfile
```

-	Layers:
	-	`sha256:bca36398fa62499981389ef963ec3e8732477fd3189e49d5b0a19962f021e882`  
		Last Modified: Sat, 28 Feb 2026 01:11:07 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:a36a708ef4ab20c051d7182ae2f16870c654ce36c041a883f4b3045498542416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135811601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c805d64686b3d65ef3dd20aa06d17d5c4074716241083750c4ce663fc641fd77`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:33:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:33:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:33:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:36 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:36 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:39 GMT
CMD ["sh"]
# Sat, 28 Feb 2026 01:08:57 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 28 Feb 2026 01:08:58 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 28 Feb 2026 01:08:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 01:09:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 28 Feb 2026 01:09:03 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 28 Feb 2026 01:09:03 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 28 Feb 2026 01:09:03 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:09:03 GMT
VOLUME [/var/lib/docker]
# Sat, 28 Feb 2026 01:09:03 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 28 Feb 2026 01:09:03 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 28 Feb 2026 01:09:03 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b2c1188f77d466b63114530c948db4a2b72f6432015051eb4c6fc5ed17a318`  
		Last Modified: Sat, 28 Feb 2026 00:33:47 GMT  
		Size: 8.3 MB (8300892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d069c0ddccdd129439f3fc19b3beb0deb0ea53ebe0d54791b223081c0bfd09`  
		Last Modified: Sat, 28 Feb 2026 00:33:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84f79f2e027c27c1420192bbb6269e4133d62301076e5f92f52a21a7c341822`  
		Last Modified: Sat, 28 Feb 2026 00:33:47 GMT  
		Size: 17.6 MB (17574992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d9822253e2de58052e59355a3ee3a3e3219482e8ff9da6021bba9c31169a73`  
		Last Modified: Sat, 28 Feb 2026 00:33:47 GMT  
		Size: 26.6 MB (26574514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977fe3e040234fe198164a9728011f9bdf228d76a92669ba3aa98acbf91cd8d1`  
		Last Modified: Sat, 28 Feb 2026 00:33:48 GMT  
		Size: 10.4 MB (10385436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9b5078999b461db61885ae27aefeaad4cd7679c996ee4dc106c5481deb7172`  
		Last Modified: Sat, 28 Feb 2026 00:33:48 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcf453e2e7207817cd2f1cafcd2c26502a7cec3072cb5a8b8c1e49e7720eef6`  
		Last Modified: Sat, 28 Feb 2026 00:33:48 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3831f33bbdf7e0cd2a3ba77cc3d9b6dea4ffd87f09eb7a18d0df5ac6354dae`  
		Last Modified: Sat, 28 Feb 2026 00:33:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b7b97efb6c96c9626c6452c6d35907116fd44e9d8dd4a730e3de085fdfcb87`  
		Last Modified: Sat, 28 Feb 2026 01:09:14 GMT  
		Size: 7.3 MB (7271699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb28f43f383cd367845812769677219708f450192b0bce32ea6ae1323cbbf12c`  
		Last Modified: Sat, 28 Feb 2026 01:09:13 GMT  
		Size: 91.8 KB (91779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1143b390d4eb69eec28024598bde4e9a359c89c6219eb10475930689486123`  
		Last Modified: Sat, 28 Feb 2026 01:09:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288371601350ba56b1dc5d245271aeda8acc45db516a7cf1ca4edee711d7349b`  
		Last Modified: Sat, 28 Feb 2026 01:09:15 GMT  
		Size: 62.0 MB (62034312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8aa70bb05db86bf9265162619f611758dbcaa8ab0f06e5712909b80a97e6472`  
		Last Modified: Sat, 28 Feb 2026 01:09:13 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c3984a3e460e2c4cf1824f452f5e8a3472cd095ca0044b172ccf33ba31b4c5`  
		Last Modified: Sat, 28 Feb 2026 01:09:14 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:0ada12f8e5ddea957492c54b4028272b319b90df66b2ec6482a748996caef3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a15c8c9d8910fa3b67e64a0b4c5ff0a3a043b468f787a3193101971707f19ad`

```dockerfile
```

-	Layers:
	-	`sha256:d8679db966c7defd214d55efd0fc6a1f698492ad859d9708372af6e6bae01e35`  
		Last Modified: Sat, 28 Feb 2026 01:09:13 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:c1e28a4f3b227ee7db14d82c37324957af6fc4efbc0521fff59f00ea6ecce2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133894570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e0c6071fac97999a74b349e820fdabef122b6e9bf5555a22afcce2432cf2f8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:32:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:32:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:32:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:32:34 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:32:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:32:34 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:32:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:32:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:32:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:32:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:32:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:32:39 GMT
CMD ["sh"]
# Sat, 28 Feb 2026 01:09:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 28 Feb 2026 01:09:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 28 Feb 2026 01:09:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 01:09:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 28 Feb 2026 01:09:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 28 Feb 2026 01:09:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 28 Feb 2026 01:09:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:09:13 GMT
VOLUME [/var/lib/docker]
# Sat, 28 Feb 2026 01:09:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 28 Feb 2026 01:09:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 28 Feb 2026 01:09:13 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282f6e2b7c9718d720ce426672429335541cf1c919bf9c845984c433c879cdc4`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 7.6 MB (7597811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354b5b8fd3a086ebaa1f824553d2d81811f9bc34aa15f16251dd1149b040957f`  
		Last Modified: Sat, 28 Feb 2026 00:32:46 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c343ba8124dc1173c2441732470ac81040c16fa72ca600062307c2150db08efd`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 17.6 MB (17566420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3c55e011e6f401320580bc9559a8eec2bd1121139952f1d621befd1557f233`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 26.5 MB (26546113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01b5cad9fc8f11ff6eceb574bedcff79a5acd3f04a71d09030e0b337df68f7b`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 10.4 MB (10369780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41923b1f427db13299befcd38419467285b2ca66ad0a4b33f483296df5b5f467`  
		Last Modified: Sat, 28 Feb 2026 00:32:47 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440d27ed514452926e359f9aeccb369ab42162dc457ef0cb90a9aa6684666b0c`  
		Last Modified: Sat, 28 Feb 2026 00:32:48 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47078bcf7b70f7b4c214ba0d20f1c8e10e7347e12a105ca35addd773811b04c1`  
		Last Modified: Sat, 28 Feb 2026 00:32:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4646932f3e91cb6ab7dbc864b4e08445a66ec41cd374fbe49ec1896ed88a982`  
		Last Modified: Sat, 28 Feb 2026 01:09:24 GMT  
		Size: 6.6 MB (6573022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19c564899e9b5a6c19f0cdc29230499311e905a2b3da9955c8d458746d5e905`  
		Last Modified: Sat, 28 Feb 2026 01:09:23 GMT  
		Size: 88.2 KB (88156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01f4e2cf953a2d6d9a9f3a1443b3b8ef98280b66a90e8d007394fcd607f0f91`  
		Last Modified: Sat, 28 Feb 2026 01:09:23 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1686d5a17066d20b94ebba8ea4ad36abb7e768dac3ff5094d9f899ac1212beac`  
		Last Modified: Sat, 28 Feb 2026 01:09:25 GMT  
		Size: 61.9 MB (61863393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829040129e131eff6b7babe59601d0efda9023e17990e656b9947f091da2c036`  
		Last Modified: Sat, 28 Feb 2026 01:09:25 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d5f9cb70da8c12cf982ed75d5dd9eb4c800c749ac416383fac30c4dc2dd3dd`  
		Last Modified: Sat, 28 Feb 2026 01:09:24 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:4f94ebe1fabec8df89f1b602cc9af7f71be9db93d156dbd2c7070c36533ea9dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac1cbf9bbda4bc07b7c4a7ece169ab46ee3ee85ceab6511396586e6419b2fbe`

```dockerfile
```

-	Layers:
	-	`sha256:e5a96ba22363c34a75191791ae68225d552c1f1627d115e575d9c76c6589fe71`  
		Last Modified: Sat, 28 Feb 2026 01:09:23 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4ca8506088c30f906cdfad8f863b9f2c41eef5b159e4b752a6c8d1c07fca74f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133273459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8ecd5b1d17216fcea5159b6dcf8aeffebfae9306de065fe5ddfb98aae43fa6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Sat, 28 Feb 2026 00:33:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 28 Feb 2026 00:33:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:33:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 28 Feb 2026 00:33:05 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:33:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 28 Feb 2026 00:33:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:33:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 28 Feb 2026 00:33:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 28 Feb 2026 00:33:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 00:33:07 GMT
CMD ["sh"]
# Sat, 28 Feb 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 28 Feb 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 28 Feb 2026 01:10:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 28 Feb 2026 01:10:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:10:24 GMT
VOLUME [/var/lib/docker]
# Sat, 28 Feb 2026 01:10:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 28 Feb 2026 01:10:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 28 Feb 2026 01:10:24 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60904be95e049500c5894c6d214007956f1035c22b15ff77ca522ac2f628513`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 8.5 MB (8453564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b0b4b880f947788126e86f12bf4ec6c59bfedb59205ec90c5344b9e9a39861`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1f471b1d5b369a49fb05baa23cedb1b9fa1b9015ee6f27e2b9c5a34b10767e`  
		Last Modified: Sat, 28 Feb 2026 00:33:14 GMT  
		Size: 17.3 MB (17349112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662c4f142eb7ddca6437ee0959e5b89824fbe97fa5d1a9d1613c79eb52d0840`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 25.5 MB (25540813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8e4f342d8afaf59c1558d78cd1f5c1e1d074b96b11c5c794918cd74ec7353b`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 10.0 MB (9974085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1186c16de0a9a9c9cc0c496c6164690809b3defab752f3b709727f48df7745fb`  
		Last Modified: Sat, 28 Feb 2026 00:33:15 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf3a986bcd21c6233dd627338e709a488f1f34ce5a97c2756ff6b05b51a3113`  
		Last Modified: Sat, 28 Feb 2026 00:33:16 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44fcf3aa39e6d6b37daecf7b8046a614dbf9488aaca5bf8eefed943801df648`  
		Last Modified: Sat, 28 Feb 2026 00:33:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbf4035e1f4acb2bd237e1645b2bc3e70a443d5a1848f4882c09901a0a220d8`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 7.2 MB (7213295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad674e6263a8a736b9a1ced02582b966ce06e5c7fc7c2fc21b3714e9a0507831`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 101.3 KB (101286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc08837f92210ce965fca88a82162045be6c2eefb791a36ecbff458a61290501`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c647a3ee71654578d02cac37d0b50bd38b344b814c0b00b5b71988b287163d5`  
		Last Modified: Sat, 28 Feb 2026 01:10:36 GMT  
		Size: 60.4 MB (60436054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7282f0ceaef0633b111139db8bf324c0c4d3045254de20c95b0c6e181195d759`  
		Last Modified: Sat, 28 Feb 2026 01:10:35 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ef9d8eaefdd9ca91eaa763fcfb13a8ada246f317f40c6c60f74d8b8066c975`  
		Last Modified: Sat, 28 Feb 2026 01:10:35 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:2748df42f6df2e6f3e87566ec113dba1c9c6c94d8463cfc0fbcc2d64ab4f9733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42e0ddb0a8b1512b11247ffdb0d8af1f53634b4d9b91e61ac1fe42684abdfa8`

```dockerfile
```

-	Layers:
	-	`sha256:85137676ef3e7b9bd815bd4c1e81e8f915dd5665b890b53565ff08c370b3d55c`  
		Last Modified: Sat, 28 Feb 2026 01:10:34 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:cca5f5b2b62a74f88c0c7aa6dd14ad0e2e4b903a79d818967c8c092057d26985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `docker:windowsservercore` - windows version 10.0.26100.32370; amd64

```console
$ docker pull docker@sha256:8adc1ea2a335bacb49fd01b1cac0cf3288b6241ce54744a6f1cb58f27720c443
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2025646567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f960ce56780111af6819315df734df0ac835f351417abb824f38888e95b16e9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Sat, 28 Feb 2026 00:42:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 28 Feb 2026 00:44:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 28 Feb 2026 00:44:02 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:44:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Sat, 28 Feb 2026 00:44:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 28 Feb 2026 00:44:18 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:44:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Sat, 28 Feb 2026 00:44:19 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Sat, 28 Feb 2026 00:44:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 28 Feb 2026 00:44:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:44:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-windows-x86_64.exe
# Sat, 28 Feb 2026 00:44:30 GMT
ENV DOCKER_COMPOSE_SHA256=ee84e42b93c501cb0aa2caa84d76b5f30ca6fb92f070e289fc37be7332c5822a
# Sat, 28 Feb 2026 00:44:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8fecd8861c56fefbd35822e522c756a164aa3d37dd262f98ad438a95f8db81`  
		Last Modified: Sat, 28 Feb 2026 00:44:47 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f7b071c2faeaa8569fda83bb88fba9ed73846631970b3b0d14721fc48a8559`  
		Last Modified: Sat, 28 Feb 2026 00:44:46 GMT  
		Size: 369.0 KB (369040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e349d48567f1c6c7903eb5d37de6df665046e21340c38e0a4a5979d7eb05bca0`  
		Last Modified: Sat, 28 Feb 2026 00:44:45 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ef673a03e21f60cb7a2f30229fc9fa4f379cb921aef1b72951239cfdac5594`  
		Last Modified: Sat, 28 Feb 2026 00:44:45 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e190b3d2972d3201fbae0ac07c094428f7a732d8e416908d03315315aaefa`  
		Last Modified: Sat, 28 Feb 2026 00:44:47 GMT  
		Size: 19.4 MB (19445004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a369575b922e845d939ad940aa1ea82e9cd08f06e346a0001ea7483ae5cb2c9d`  
		Last Modified: Sat, 28 Feb 2026 00:44:44 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1522ec443e28a83261bf5734712b4c9e11aec045f70d11b79269e263ce14e8a`  
		Last Modified: Sat, 28 Feb 2026 00:44:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c077c7089ab69c4846f6326bfc8b115c5d20413f8c10b6a513721c8c295a3c3`  
		Last Modified: Sat, 28 Feb 2026 00:44:44 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfd81c02864aa131850545bb63bf55804e738732881a931669f9a619979c074`  
		Last Modified: Sat, 28 Feb 2026 00:44:46 GMT  
		Size: 29.4 MB (29419828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b640fd9bf971384c0ef0f4d964b6d311ee0a0d66729df8dd2ca97af1ccaba502`  
		Last Modified: Sat, 28 Feb 2026 00:44:42 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff016c0dfe5242b2a2a90ceaad29581fdacfef972a2f8709b33f8e7ee17fc0bb`  
		Last Modified: Sat, 28 Feb 2026 00:44:42 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b503dbc573993dbb1567403db5b6765a54d2def3ede2df5271ed13b54484aee`  
		Last Modified: Sat, 28 Feb 2026 00:44:42 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37151df22c07f87a0463edda2aac3d9ee8578d7e747212faa48f66fd04767c54`  
		Last Modified: Sat, 28 Feb 2026 00:44:44 GMT  
		Size: 11.6 MB (11641004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4773; amd64

```console
$ docker pull docker@sha256:a8b9761529846487729828118bc9d1ce96302a873180a668fdf5cdd9d0b9d4f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1923675549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a7a4f75a27e4ef61863bcc67443ad3281dd982210ff24610cd05e931586ccd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Sat, 28 Feb 2026 00:37:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 28 Feb 2026 00:38:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 28 Feb 2026 00:38:01 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:38:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Sat, 28 Feb 2026 00:38:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 28 Feb 2026 00:38:28 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:38:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Sat, 28 Feb 2026 00:38:30 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Sat, 28 Feb 2026 00:38:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 28 Feb 2026 00:38:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:38:49 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-windows-x86_64.exe
# Sat, 28 Feb 2026 00:38:50 GMT
ENV DOCKER_COMPOSE_SHA256=ee84e42b93c501cb0aa2caa84d76b5f30ca6fb92f070e289fc37be7332c5822a
# Sat, 28 Feb 2026 00:39:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be4d1183e15fd05c6d783c5878ff791e038c48438ca1ba670f3613c106d08d2`  
		Last Modified: Sat, 28 Feb 2026 00:39:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bb9a9714c637901616444e50e2cda139f123a430725359b304d803afc9c9c7`  
		Last Modified: Sat, 28 Feb 2026 00:39:10 GMT  
		Size: 501.8 KB (501824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b98f479028ad7847b57cb613806e29a2c97c5a2a7dffd6d5ce1ce66178b7c68`  
		Last Modified: Sat, 28 Feb 2026 00:39:10 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269a765ecda9d069746e9c2da6e04fba00d1136c12b0cc4061e0a2775869f007`  
		Last Modified: Sat, 28 Feb 2026 00:39:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c78c7d5fa55df50d672144746fcd4e331fc02b195fe3f0701261fd6addf833f`  
		Last Modified: Sat, 28 Feb 2026 00:39:12 GMT  
		Size: 19.4 MB (19440746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9625ce298bdcd094c4964086c9b8611453b7eb30975573133e75884f2915daac`  
		Last Modified: Sat, 28 Feb 2026 00:39:08 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9066580973f92a7516a5f09efd8e0d21d02071fe417c30a60153425ed108ca06`  
		Last Modified: Sat, 28 Feb 2026 00:39:08 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd2225bdb0312a4122abb278e88e0900611dbe800a6b424e65afbd9983abb99`  
		Last Modified: Sat, 28 Feb 2026 00:39:08 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783a739d2dd01ce6b5bb8a724064c3dd2d8feaed38aace83203bef0d8c9045e0`  
		Last Modified: Sat, 28 Feb 2026 00:39:28 GMT  
		Size: 29.4 MB (29424520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b773ca8de4854b1075f7b0efe657b60f19fd158cab220de986164e02b762b82`  
		Last Modified: Sat, 28 Feb 2026 00:39:06 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a37f5c008907b0eba192b39c2a2c6c101e4bcbc45872308cebce66db1cedef8`  
		Last Modified: Sat, 28 Feb 2026 00:39:06 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822095fd913199d892689f8637438d94605d8bc8de9646cfa1ccdd0532473da1`  
		Last Modified: Sat, 28 Feb 2026 00:39:06 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc64c3da6990cf40fafd08e9c67fae552b8d46c42cf5185a2ec0e446b567817`  
		Last Modified: Sat, 28 Feb 2026 00:39:08 GMT  
		Size: 11.6 MB (11639433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:246e353702cde321874dc9ddcaa2d8bf00330f188c1107008646ae6f1dbd9903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull docker@sha256:a8b9761529846487729828118bc9d1ce96302a873180a668fdf5cdd9d0b9d4f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1923675549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a7a4f75a27e4ef61863bcc67443ad3281dd982210ff24610cd05e931586ccd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Sat, 28 Feb 2026 00:37:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 28 Feb 2026 00:38:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 28 Feb 2026 00:38:01 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:38:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Sat, 28 Feb 2026 00:38:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 28 Feb 2026 00:38:28 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:38:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Sat, 28 Feb 2026 00:38:30 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Sat, 28 Feb 2026 00:38:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 28 Feb 2026 00:38:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:38:49 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-windows-x86_64.exe
# Sat, 28 Feb 2026 00:38:50 GMT
ENV DOCKER_COMPOSE_SHA256=ee84e42b93c501cb0aa2caa84d76b5f30ca6fb92f070e289fc37be7332c5822a
# Sat, 28 Feb 2026 00:39:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be4d1183e15fd05c6d783c5878ff791e038c48438ca1ba670f3613c106d08d2`  
		Last Modified: Sat, 28 Feb 2026 00:39:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bb9a9714c637901616444e50e2cda139f123a430725359b304d803afc9c9c7`  
		Last Modified: Sat, 28 Feb 2026 00:39:10 GMT  
		Size: 501.8 KB (501824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b98f479028ad7847b57cb613806e29a2c97c5a2a7dffd6d5ce1ce66178b7c68`  
		Last Modified: Sat, 28 Feb 2026 00:39:10 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269a765ecda9d069746e9c2da6e04fba00d1136c12b0cc4061e0a2775869f007`  
		Last Modified: Sat, 28 Feb 2026 00:39:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c78c7d5fa55df50d672144746fcd4e331fc02b195fe3f0701261fd6addf833f`  
		Last Modified: Sat, 28 Feb 2026 00:39:12 GMT  
		Size: 19.4 MB (19440746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9625ce298bdcd094c4964086c9b8611453b7eb30975573133e75884f2915daac`  
		Last Modified: Sat, 28 Feb 2026 00:39:08 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9066580973f92a7516a5f09efd8e0d21d02071fe417c30a60153425ed108ca06`  
		Last Modified: Sat, 28 Feb 2026 00:39:08 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd2225bdb0312a4122abb278e88e0900611dbe800a6b424e65afbd9983abb99`  
		Last Modified: Sat, 28 Feb 2026 00:39:08 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783a739d2dd01ce6b5bb8a724064c3dd2d8feaed38aace83203bef0d8c9045e0`  
		Last Modified: Sat, 28 Feb 2026 00:39:28 GMT  
		Size: 29.4 MB (29424520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b773ca8de4854b1075f7b0efe657b60f19fd158cab220de986164e02b762b82`  
		Last Modified: Sat, 28 Feb 2026 00:39:06 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a37f5c008907b0eba192b39c2a2c6c101e4bcbc45872308cebce66db1cedef8`  
		Last Modified: Sat, 28 Feb 2026 00:39:06 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822095fd913199d892689f8637438d94605d8bc8de9646cfa1ccdd0532473da1`  
		Last Modified: Sat, 28 Feb 2026 00:39:06 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc64c3da6990cf40fafd08e9c67fae552b8d46c42cf5185a2ec0e446b567817`  
		Last Modified: Sat, 28 Feb 2026 00:39:08 GMT  
		Size: 11.6 MB (11639433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a86a7f53fd5f28509c601a3bee5223705f9e2da2d13c6aa49559db7ecb7fa913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull docker@sha256:8adc1ea2a335bacb49fd01b1cac0cf3288b6241ce54744a6f1cb58f27720c443
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2025646567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f960ce56780111af6819315df734df0ac835f351417abb824f38888e95b16e9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Sat, 28 Feb 2026 00:42:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 28 Feb 2026 00:44:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 28 Feb 2026 00:44:02 GMT
ENV DOCKER_VERSION=29.2.1
# Sat, 28 Feb 2026 00:44:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Sat, 28 Feb 2026 00:44:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 28 Feb 2026 00:44:18 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Sat, 28 Feb 2026 00:44:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Sat, 28 Feb 2026 00:44:19 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Sat, 28 Feb 2026 00:44:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 28 Feb 2026 00:44:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Sat, 28 Feb 2026 00:44:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-windows-x86_64.exe
# Sat, 28 Feb 2026 00:44:30 GMT
ENV DOCKER_COMPOSE_SHA256=ee84e42b93c501cb0aa2caa84d76b5f30ca6fb92f070e289fc37be7332c5822a
# Sat, 28 Feb 2026 00:44:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8fecd8861c56fefbd35822e522c756a164aa3d37dd262f98ad438a95f8db81`  
		Last Modified: Sat, 28 Feb 2026 00:44:47 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f7b071c2faeaa8569fda83bb88fba9ed73846631970b3b0d14721fc48a8559`  
		Last Modified: Sat, 28 Feb 2026 00:44:46 GMT  
		Size: 369.0 KB (369040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e349d48567f1c6c7903eb5d37de6df665046e21340c38e0a4a5979d7eb05bca0`  
		Last Modified: Sat, 28 Feb 2026 00:44:45 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ef673a03e21f60cb7a2f30229fc9fa4f379cb921aef1b72951239cfdac5594`  
		Last Modified: Sat, 28 Feb 2026 00:44:45 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e190b3d2972d3201fbae0ac07c094428f7a732d8e416908d03315315aaefa`  
		Last Modified: Sat, 28 Feb 2026 00:44:47 GMT  
		Size: 19.4 MB (19445004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a369575b922e845d939ad940aa1ea82e9cd08f06e346a0001ea7483ae5cb2c9d`  
		Last Modified: Sat, 28 Feb 2026 00:44:44 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1522ec443e28a83261bf5734712b4c9e11aec045f70d11b79269e263ce14e8a`  
		Last Modified: Sat, 28 Feb 2026 00:44:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c077c7089ab69c4846f6326bfc8b115c5d20413f8c10b6a513721c8c295a3c3`  
		Last Modified: Sat, 28 Feb 2026 00:44:44 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfd81c02864aa131850545bb63bf55804e738732881a931669f9a619979c074`  
		Last Modified: Sat, 28 Feb 2026 00:44:46 GMT  
		Size: 29.4 MB (29419828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b640fd9bf971384c0ef0f4d964b6d311ee0a0d66729df8dd2ca97af1ccaba502`  
		Last Modified: Sat, 28 Feb 2026 00:44:42 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff016c0dfe5242b2a2a90ceaad29581fdacfef972a2f8709b33f8e7ee17fc0bb`  
		Last Modified: Sat, 28 Feb 2026 00:44:42 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b503dbc573993dbb1567403db5b6765a54d2def3ede2df5271ed13b54484aee`  
		Last Modified: Sat, 28 Feb 2026 00:44:42 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37151df22c07f87a0463edda2aac3d9ee8578d7e747212faa48f66fd04767c54`  
		Last Modified: Sat, 28 Feb 2026 00:44:44 GMT  
		Size: 11.6 MB (11641004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
