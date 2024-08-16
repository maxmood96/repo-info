<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:27`](#docker27)
-	[`docker:27-cli`](#docker27-cli)
-	[`docker:27-dind`](#docker27-dind)
-	[`docker:27-dind-rootless`](#docker27-dind-rootless)
-	[`docker:27-windowsservercore`](#docker27-windowsservercore)
-	[`docker:27-windowsservercore-1809`](#docker27-windowsservercore-1809)
-	[`docker:27-windowsservercore-ltsc2022`](#docker27-windowsservercore-ltsc2022)
-	[`docker:27.1`](#docker271)
-	[`docker:27.1-cli`](#docker271-cli)
-	[`docker:27.1-dind`](#docker271-dind)
-	[`docker:27.1-dind-rootless`](#docker271-dind-rootless)
-	[`docker:27.1-windowsservercore`](#docker271-windowsservercore)
-	[`docker:27.1-windowsservercore-1809`](#docker271-windowsservercore-1809)
-	[`docker:27.1-windowsservercore-ltsc2022`](#docker271-windowsservercore-ltsc2022)
-	[`docker:27.1.2`](#docker2712)
-	[`docker:27.1.2-alpine3.20`](#docker2712-alpine320)
-	[`docker:27.1.2-cli`](#docker2712-cli)
-	[`docker:27.1.2-cli-alpine3.20`](#docker2712-cli-alpine320)
-	[`docker:27.1.2-dind`](#docker2712-dind)
-	[`docker:27.1.2-dind-alpine3.20`](#docker2712-dind-alpine320)
-	[`docker:27.1.2-dind-rootless`](#docker2712-dind-rootless)
-	[`docker:27.1.2-windowsservercore`](#docker2712-windowsservercore)
-	[`docker:27.1.2-windowsservercore-1809`](#docker2712-windowsservercore-1809)
-	[`docker:27.1.2-windowsservercore-ltsc2022`](#docker2712-windowsservercore-ltsc2022)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)

## `docker:27`

```console
$ docker pull docker@sha256:6eb8bfb2c82d454c0248b5dd41b9607f1b76096c06acf985e862f2ea069db33e
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

### `docker:27` - linux; amd64

```console
$ docker pull docker@sha256:fc81f6680c575a7381f7a586aab4643cdbe79cf9f5af594d2c783a9eb0a0e1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130334773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb13d0c9247298368f97e0637bb60c105cf8159fd29364881b45b5c96c78d621`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97be572a9abc71e039fcf0e5c2cee826693d2e32b5aa28c52ee2e147f29f3ed2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 7.9 MB (7872256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d068c8136df4c77e60b80c6f269c341b11f27187ec77a9ce1a8519f4bdce441f`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3486b9b1692e5ae916e32c2133bb5e8f98a7f89b173cdb303b25d20094e8dee8`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.1 MB (18090913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1726802d7045e092159fdcac73e3c1461690d55c73403cdcdf031ac4145518e2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.4 MB (18404800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1774d2fed741a7a383f92d3969db43a321a4a02dcaad8a886967fb723954fa`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 18.8 MB (18818906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216e3a4876cf4f3c85c70bf9bed6dadfdc58ce83a5537dedb98ea42b20ff36c0`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5bd9a3f910707b7294207b927b3ade09f9d20b66525f2296ee65b90f7edb5`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425c20abf22d4da88ed53e7b1321b6515f33a887063e1f75e25530f7bf89723c`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5174f7db1d0f582b0c6e4a068cb27afd84b66c23716f5046592e2be1b5a225`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 6.7 MB (6657764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fcabf4da4d815f68d521020af7450dc776029613b976a0b4aa8d3429e7d18d`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 89.2 KB (89217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7096f07126cd3b58ec87699d558d9bf0b0b044533ada0f67254d85c94f0bc3b3`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8b74173c6813b97f6d02202faf9a563c7207e298b3204dd4340295344c8ede`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 56.8 MB (56770081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1647c2f9c8092fada70aa9758b7a69f1f3cd05a90891a0a532881cfd598c48`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c41c56a7d8896baa7e32b03546ff50a23492eb9543ed2089ab2fb66ede6ef`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:14ec78850163b4e599f6b88fe195725546c45bc30c37ed06f92bd2e7b2f5b392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33683cd4c1538f63f2751b42869d268ec779b0d5fe22d4765e60f56c75e84787`

```dockerfile
```

-	Layers:
	-	`sha256:76c6029aaa7435fba20177df1eb133a9c0a03d8b5c6fe48799e1fe75e360c69f`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v6

```console
$ docker pull docker@sha256:f027111d31885b0ed9642d1b92d7e62b7644b92089eebc5af8a32d7f8bebfc8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122569652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a41929651127c7fdf1f8cfa71354b837597836af87e070e112cbee135c1040`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749d51120dd4449c98cad5624e6a58aaf21f6b57355b1537b1262f69c27968e`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 7.8 MB (7807488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dee64c722233ea05fa0db7774bbb908ccb3860c76b492b90725b4a00faf74a`  
		Last Modified: Tue, 13 Aug 2024 20:03:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aa9bf3b5617e94aa7647537a116937dc7c6d223c96912c2ffc1302ccceab1b`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 16.4 MB (16362863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b4ff9c935b9bea7d6a6f982aab917c1a4fd29032db6ff2a2026ee7f77cc75`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.1 MB (17114711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31fe971362beacbc7fe1ce84a4f59817b327260334951577b2bdc1640d49164`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.8 MB (17776509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7dca5ea08fd6046c223c1378a8259479b60e2b7c9fe45d9ebc3394f237a3c`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 534.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffadf986c05f1d49184514bc67815f318456acc65c0abfd74b2cce1b6d86ecca`  
		Last Modified: Tue, 13 Aug 2024 20:03:15 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7edf55c16e9e482eb8124f38438564758d96aa113c06fd945bcb13988d3fba6`  
		Last Modified: Tue, 13 Aug 2024 20:03:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7dcf38e93a9b47e0f66795e256f2901c2c4bfc37556e81fea2a063cee12eed`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 7.0 MB (6984036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dc040353146061f1f9e8d56420bfefd970c9707a3834a5bcf02701bc7f87a6`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 88.4 KB (88407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af6ea4938ff0c08202d2f8e3f84e00a915d37297b863ed5032cc8f8fa5cd906`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a7459df9025cc27e33a8fecee41b7192346cf1721924cfabec6187dff5186`  
		Last Modified: Tue, 13 Aug 2024 20:57:37 GMT  
		Size: 53.1 MB (53062512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f07f1d6edcfeac2205add2fc7459ea84419349425810e89ef26b86733a587`  
		Last Modified: Tue, 13 Aug 2024 20:57:36 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40b0d4ce5c2e81228c159aa2dcd3e15ecf2f27ee8a41d175c78e599ca4af850`  
		Last Modified: Tue, 13 Aug 2024 20:57:36 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:6c057a6e1b62568c5bdee69c9c82240780e3862912fcaa566a3a3487a470fd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a96c343221bdcb48cb74979b02ab5c13b27dbff1a66a0ceb3780e97c736573f`

```dockerfile
```

-	Layers:
	-	`sha256:8cea367fa521297df7cfa3bc63f39bd2b776aa0f558f0427199bc08da2d719d2`  
		Last Modified: Tue, 13 Aug 2024 20:57:34 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v7

```console
$ docker pull docker@sha256:a4332a1e0f1aaa47f76bb148424557761569ddbaa01a4b0733831f22a7e2e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120929654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be199173f5a13331c5558376e7c160c53e51cc77a7f598bbe39233e723dade8b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81dc9168b7d20594a7b5afa567e1b9102c0d289d4b9956af1dd0553da38503f`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 7.1 MB (7143486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b63ca62b0868cd9cbb097a6c34d9eb3a8e551918380dd69db51fbe7459654`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff65173bbd98afd04b6c052172c858476533d0f4873c5b6a81bda0849b5792`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 16.4 MB (16353814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd7e108f551e071a490fb8213c13dccea238c6e5c6ed12be3eef86831d31eb`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 17.1 MB (17103032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b020a8e04eea5428d7645058058bdeea76775ad16c0c306557b00c9b3cce3707`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 17.8 MB (17771143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf51759e8c2b5bc311e671ddc5401fb8b470e266b8553c7d887176c8be0e673`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06151b2e48f60b43b5a3438902d125f5201b35d94f354ac3ac4351ed695565f`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf092fc62ad5de9ceea220ba585b82ea46d65253b23f11533d59f110184e5fe4`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a5e67d714baf4e953669b348ccf67b6156b080a6d6966dc09d0543f0c9be9e`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 6.3 MB (6308261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4b153923b2bef79dd19c29f9b88c045ce4e6e55242b154dbc462faed80d0db`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 84.5 KB (84499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ad462b285298ed7a2323c331255edc0ee999c93e0c8ae4a33c5ce454aeeff4`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67a0efc8d76bc7874505d46a4946de771e37c4eb62166bbec60dcd2a80e68e3`  
		Last Modified: Fri, 16 Aug 2024 21:57:37 GMT  
		Size: 53.1 MB (53062491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bba27c850d08471b57f0404d138486b2a1aed9dd9f3893b3b3def00f165ae25`  
		Last Modified: Fri, 16 Aug 2024 21:57:36 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a63b57aea184aabfabfd30d5a7c8567fe3d95a40b8f831ed764b2193d8bffe7`  
		Last Modified: Fri, 16 Aug 2024 21:57:36 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:10c4f8cecc7eb13f9d6d6dc54e1740ab90190e6d24c2e4eec6713b2931912225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a906609c1e200a6b10bedc63efea8af901e9897d1b8f31c4dcb5375222ba63f2`

```dockerfile
```

-	Layers:
	-	`sha256:3e420f6bc3bb35c7528c2f9e8ad122df634ff514d46807261853977ba0eb51f6`  
		Last Modified: Fri, 16 Aug 2024 21:57:34 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e739d640aea8812448d7dd39378e23771a2554a182f2099969410db56fa79917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122599486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d8b2b975dd95f7591d28783db8fc5752c99db0ffd5197320cecf290ce39c7f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eaa3c460d109197e8637b1a9599d7f18cccc546e66d1d62f6dd1508e2935dd`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 8.0 MB (7981761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9e960f5f951de003b26390946248f496a1eda867789ae06fd8b18055515450`  
		Last Modified: Tue, 13 Aug 2024 20:49:42 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99bff4ad6d3c4a0683cf02a74f06b61546be2a877da62aece45b0d3b9409871`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 17.0 MB (17049381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74376b78c4a6f5d12921d8dca6dcfa9e9f2bb0917ddeaa5991b98a8c6594581f`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 16.8 MB (16772960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c08f66b4f65a64aaad739c0ac5607c94142e38e67115632af35ef78cff1329c`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 17.2 MB (17182720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce67e83e18f9107f6bbf32d16c48a8f21c28e500a4212c8ebeca7b994936d7e`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c532de2c2cacfe1199219ef497170060946e3a593f771635c84f141b9a3b94c6`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7601c7d4e5af9ac7f6766b064bc79247c0912f3c5d6f3d02bfb58f49c9207`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194e0f500f2ba3365f850eac55a79e52a90ba4922806239f584025ccf347cea5`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 7.0 MB (7034963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9643f136f726def03ee1af9a52d6193e29fb13777be7e5dad5303f10ed36b68`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 98.7 KB (98659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8112d1aa134e43b2e075826bc7ea6a21adf3464ecd3aee260bf8f2947e9d5a50`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9dc9c485b7585bc344ca1a3c332c378d9ee340ecdb8aa344a75df81b017e1`  
		Last Modified: Tue, 13 Aug 2024 22:23:59 GMT  
		Size: 52.4 MB (52384159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7cbf878da555535371cabcf172c560243258cf73e8889885f96fbe66ded9c2`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97e744676fc32c335434d0c4e6890ce0f48ffb37aa99af9568bca483cbfca3f`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:f6be705e7230112840619e69b7e6322ce4fc67c5f11c95e929f9e841f1e8403c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43bac9495e2c3ff9a3596159acfb499a4e9f6688d7b379425baf358201b63a1`

```dockerfile
```

-	Layers:
	-	`sha256:9604ca831aeb0d74501b911f9a7b547356be1ae57280b751700fd1d324dfd1ad`  
		Last Modified: Tue, 13 Aug 2024 22:23:56 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-cli`

```console
$ docker pull docker@sha256:c8af17c2e98d13ce5c18d9d31d6e8df47c76d1ba504d2f1782980bb8673af4cb
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

### `docker:27-cli` - linux; amd64

```console
$ docker pull docker@sha256:444582958ec806c73d40f3702a8a8d84dc2e82feb0d9b44c738fca09ed2820ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66818343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe40c55ae60532fa0075302e6e93e7248c71837afcbd1c56e77b04e256552e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Aug 2024 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b830b3ce3f84ea7067567326d58a3c311c803b3e94cee51732c87abaf0b1644a`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 7.9 MB (7872313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f67cd05487ef47b2034f553790ea2efb816214bef9fd63d5d4f98254167b56e`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201b9999b9284e2bb11f5f0dc6cb35f9f890e8ef84edbd6edbd7f2ea82918c97`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 18.1 MB (18090908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0ed696b310c4d4cd09c07f7566ed6e2baa3f866160967ef06cf205d244859c`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 18.4 MB (18404798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d43008ea7ba356da560c03ab69f55df1d585a289fe0b9e4388f07ff04648932`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 18.8 MB (18825277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5e249d37736904735e2ce24e0bdea2329356683f6cdc14f3b8a7f1f5794c94`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75295f954e5cf281711fb0cb6e50cda9c6305918cc357d63e5347abf36cf48d`  
		Last Modified: Fri, 16 Aug 2024 20:55:55 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f64e86da193d3fea1e01efb5b7a81578e84d4e4593aee8279e9361b9e7e529`  
		Last Modified: Fri, 16 Aug 2024 20:55:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:bf1312c933add91f38029909c3177cd3b9f727efb4e56065fe297c6da6ffb91f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8336e1fddcafee01e26424a9f2c4608561aa729df648622918daaf2a3ef44053`

```dockerfile
```

-	Layers:
	-	`sha256:c16850f73bbeb2eb267302c311cadcadd55959d236b402c255acf9e6a760625f`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:ad97551c8ab5f60dc65827a43fb5bfc13375c4128efad7a326a9823e0be68d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62435713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468051ea9e870d4ee592d7253bae1b185cd265c4f3b54f8be9f8b1a820359d3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Aug 2024 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749d51120dd4449c98cad5624e6a58aaf21f6b57355b1537b1262f69c27968e`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 7.8 MB (7807488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dee64c722233ea05fa0db7774bbb908ccb3860c76b492b90725b4a00faf74a`  
		Last Modified: Tue, 13 Aug 2024 20:03:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aa9bf3b5617e94aa7647537a116937dc7c6d223c96912c2ffc1302ccceab1b`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 16.4 MB (16362863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b4ff9c935b9bea7d6a6f982aab917c1a4fd29032db6ff2a2026ee7f77cc75`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.1 MB (17114711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc83f1a40d0c658722d9af33f70561ec5dd29cadd86f625da7bcfa50022733b6`  
		Last Modified: Fri, 16 Aug 2024 20:55:46 GMT  
		Size: 17.8 MB (17783303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5f17b4f1f75fbc81e81b8c4714b51f7829480cd793423fdbe280b4a0e06cdc`  
		Last Modified: Fri, 16 Aug 2024 20:55:45 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d17e0519f279b5dc8f4f4d2233b55fa585e9d0f4e28b2ec38a893f46d415da`  
		Last Modified: Fri, 16 Aug 2024 20:55:45 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ddce9ce1633ca8261319074be47691ef0fa443df2b2fa759364895def2fb50`  
		Last Modified: Fri, 16 Aug 2024 20:55:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:72ac9cedabc23854d5804ef9acc704d8bc5672c4f2f7fa895f0536b433b53c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48dc65f2a968c7f37459c45a1f206fd483248e32a76f9d647ccd35c71bb1a66`

```dockerfile
```

-	Layers:
	-	`sha256:0f0379928ebdda35d5a3de2751c7fb8bf3f92b87ef1bc4445614cadfa4d0042b`  
		Last Modified: Fri, 16 Aug 2024 20:55:45 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:cc97a6244b7807809e92b3d720bc2b5f4748fe77f7b1d07f19d033559a0ad00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61468602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509b86a39961f355e5e37e9847693e175944080eae9ea5595e844a7932fe7c06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Aug 2024 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81dc9168b7d20594a7b5afa567e1b9102c0d289d4b9956af1dd0553da38503f`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 7.1 MB (7143486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b63ca62b0868cd9cbb097a6c34d9eb3a8e551918380dd69db51fbe7459654`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff65173bbd98afd04b6c052172c858476533d0f4873c5b6a81bda0849b5792`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 16.4 MB (16353814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd7e108f551e071a490fb8213c13dccea238c6e5c6ed12be3eef86831d31eb`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 17.1 MB (17103032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b020a8e04eea5428d7645058058bdeea76775ad16c0c306557b00c9b3cce3707`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 17.8 MB (17771143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf51759e8c2b5bc311e671ddc5401fb8b470e266b8553c7d887176c8be0e673`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06151b2e48f60b43b5a3438902d125f5201b35d94f354ac3ac4351ed695565f`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf092fc62ad5de9ceea220ba585b82ea46d65253b23f11533d59f110184e5fe4`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f183a263ab8d9b602944b555e29de9642d82e659e768b89ec39b5617024c4c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa7b9ac79beca13b0bc6894266285efc76f1e0853417a57b774ad69e6a882f5`

```dockerfile
```

-	Layers:
	-	`sha256:b2e8085a6ac1eeb458f441d28f5b14e745904be32fb62d75e214c3746c87091e`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:173d5a1620cd4c9838d8c6eeaff20a78fbcf08ee2e51c12449f832530e7edbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63080030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c697038997a5fe8ff64a0a9e3a2befe1ab1ffa2dbbce9a6d36ca94614c2e9207`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Aug 2024 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729161d0df240d9ed83f30e35c6fe471b1fae935500748d1ef7da84e664cdb8a`  
		Last Modified: Fri, 16 Aug 2024 20:55:42 GMT  
		Size: 8.0 MB (7981771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b9491762d2e0304f13e86117eb8d95e32f661c882e832b16bee6e8bb9098cb`  
		Last Modified: Fri, 16 Aug 2024 20:55:41 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fdb7ce0e7cf19d21a2bd7c9f95c09245271c0474a184066b1410007b8d4578`  
		Last Modified: Fri, 16 Aug 2024 20:55:42 GMT  
		Size: 17.0 MB (17049378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99813ceebaed11f6388e8ad3c4c1b371512de366ba5488d2f99200a424f074f`  
		Last Modified: Fri, 16 Aug 2024 20:55:42 GMT  
		Size: 16.8 MB (16772960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316a30f1c6a00f4fbfcba19ce9ccb4c2d5709b52e454b56144ec8f67d26208e2`  
		Last Modified: Fri, 16 Aug 2024 20:55:43 GMT  
		Size: 17.2 MB (17186835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0d611bb20624f74153d3ec09ce18870c07860b77939bdf1e019e0740de454a`  
		Last Modified: Fri, 16 Aug 2024 20:55:43 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9b0bb076214cf2f061a5937a293c9b2915ccf6dd121c501471f941589eab06`  
		Last Modified: Fri, 16 Aug 2024 20:55:43 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75f172f02f32a93ea69404964c9c459ce24e0f2cfe1585a6387e076ee96535d`  
		Last Modified: Fri, 16 Aug 2024 20:55:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9fe09d16bdc866f48ca5138929e946de2919fc7472dab2277a4690007a863f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4debb6c6f5e419a67a262e3c2d825765ae2e8b3f71720fbbd0843ead3c73e23`

```dockerfile
```

-	Layers:
	-	`sha256:ee581fd74c551286cbef0f11f61d4110c9e68a8323a697f9a454568d1603785a`  
		Last Modified: Fri, 16 Aug 2024 20:55:41 GMT  
		Size: 38.2 KB (38227 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind`

```console
$ docker pull docker@sha256:6eb8bfb2c82d454c0248b5dd41b9607f1b76096c06acf985e862f2ea069db33e
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

### `docker:27-dind` - linux; amd64

```console
$ docker pull docker@sha256:fc81f6680c575a7381f7a586aab4643cdbe79cf9f5af594d2c783a9eb0a0e1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130334773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb13d0c9247298368f97e0637bb60c105cf8159fd29364881b45b5c96c78d621`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97be572a9abc71e039fcf0e5c2cee826693d2e32b5aa28c52ee2e147f29f3ed2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 7.9 MB (7872256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d068c8136df4c77e60b80c6f269c341b11f27187ec77a9ce1a8519f4bdce441f`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3486b9b1692e5ae916e32c2133bb5e8f98a7f89b173cdb303b25d20094e8dee8`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.1 MB (18090913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1726802d7045e092159fdcac73e3c1461690d55c73403cdcdf031ac4145518e2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.4 MB (18404800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1774d2fed741a7a383f92d3969db43a321a4a02dcaad8a886967fb723954fa`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 18.8 MB (18818906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216e3a4876cf4f3c85c70bf9bed6dadfdc58ce83a5537dedb98ea42b20ff36c0`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5bd9a3f910707b7294207b927b3ade09f9d20b66525f2296ee65b90f7edb5`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425c20abf22d4da88ed53e7b1321b6515f33a887063e1f75e25530f7bf89723c`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5174f7db1d0f582b0c6e4a068cb27afd84b66c23716f5046592e2be1b5a225`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 6.7 MB (6657764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fcabf4da4d815f68d521020af7450dc776029613b976a0b4aa8d3429e7d18d`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 89.2 KB (89217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7096f07126cd3b58ec87699d558d9bf0b0b044533ada0f67254d85c94f0bc3b3`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8b74173c6813b97f6d02202faf9a563c7207e298b3204dd4340295344c8ede`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 56.8 MB (56770081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1647c2f9c8092fada70aa9758b7a69f1f3cd05a90891a0a532881cfd598c48`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c41c56a7d8896baa7e32b03546ff50a23492eb9543ed2089ab2fb66ede6ef`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:14ec78850163b4e599f6b88fe195725546c45bc30c37ed06f92bd2e7b2f5b392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33683cd4c1538f63f2751b42869d268ec779b0d5fe22d4765e60f56c75e84787`

```dockerfile
```

-	Layers:
	-	`sha256:76c6029aaa7435fba20177df1eb133a9c0a03d8b5c6fe48799e1fe75e360c69f`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:f027111d31885b0ed9642d1b92d7e62b7644b92089eebc5af8a32d7f8bebfc8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122569652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a41929651127c7fdf1f8cfa71354b837597836af87e070e112cbee135c1040`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749d51120dd4449c98cad5624e6a58aaf21f6b57355b1537b1262f69c27968e`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 7.8 MB (7807488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dee64c722233ea05fa0db7774bbb908ccb3860c76b492b90725b4a00faf74a`  
		Last Modified: Tue, 13 Aug 2024 20:03:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aa9bf3b5617e94aa7647537a116937dc7c6d223c96912c2ffc1302ccceab1b`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 16.4 MB (16362863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b4ff9c935b9bea7d6a6f982aab917c1a4fd29032db6ff2a2026ee7f77cc75`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.1 MB (17114711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31fe971362beacbc7fe1ce84a4f59817b327260334951577b2bdc1640d49164`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.8 MB (17776509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7dca5ea08fd6046c223c1378a8259479b60e2b7c9fe45d9ebc3394f237a3c`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 534.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffadf986c05f1d49184514bc67815f318456acc65c0abfd74b2cce1b6d86ecca`  
		Last Modified: Tue, 13 Aug 2024 20:03:15 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7edf55c16e9e482eb8124f38438564758d96aa113c06fd945bcb13988d3fba6`  
		Last Modified: Tue, 13 Aug 2024 20:03:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7dcf38e93a9b47e0f66795e256f2901c2c4bfc37556e81fea2a063cee12eed`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 7.0 MB (6984036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dc040353146061f1f9e8d56420bfefd970c9707a3834a5bcf02701bc7f87a6`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 88.4 KB (88407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af6ea4938ff0c08202d2f8e3f84e00a915d37297b863ed5032cc8f8fa5cd906`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a7459df9025cc27e33a8fecee41b7192346cf1721924cfabec6187dff5186`  
		Last Modified: Tue, 13 Aug 2024 20:57:37 GMT  
		Size: 53.1 MB (53062512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f07f1d6edcfeac2205add2fc7459ea84419349425810e89ef26b86733a587`  
		Last Modified: Tue, 13 Aug 2024 20:57:36 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40b0d4ce5c2e81228c159aa2dcd3e15ecf2f27ee8a41d175c78e599ca4af850`  
		Last Modified: Tue, 13 Aug 2024 20:57:36 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6c057a6e1b62568c5bdee69c9c82240780e3862912fcaa566a3a3487a470fd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a96c343221bdcb48cb74979b02ab5c13b27dbff1a66a0ceb3780e97c736573f`

```dockerfile
```

-	Layers:
	-	`sha256:8cea367fa521297df7cfa3bc63f39bd2b776aa0f558f0427199bc08da2d719d2`  
		Last Modified: Tue, 13 Aug 2024 20:57:34 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:a4332a1e0f1aaa47f76bb148424557761569ddbaa01a4b0733831f22a7e2e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120929654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be199173f5a13331c5558376e7c160c53e51cc77a7f598bbe39233e723dade8b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81dc9168b7d20594a7b5afa567e1b9102c0d289d4b9956af1dd0553da38503f`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 7.1 MB (7143486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b63ca62b0868cd9cbb097a6c34d9eb3a8e551918380dd69db51fbe7459654`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff65173bbd98afd04b6c052172c858476533d0f4873c5b6a81bda0849b5792`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 16.4 MB (16353814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd7e108f551e071a490fb8213c13dccea238c6e5c6ed12be3eef86831d31eb`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 17.1 MB (17103032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b020a8e04eea5428d7645058058bdeea76775ad16c0c306557b00c9b3cce3707`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 17.8 MB (17771143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf51759e8c2b5bc311e671ddc5401fb8b470e266b8553c7d887176c8be0e673`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06151b2e48f60b43b5a3438902d125f5201b35d94f354ac3ac4351ed695565f`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf092fc62ad5de9ceea220ba585b82ea46d65253b23f11533d59f110184e5fe4`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a5e67d714baf4e953669b348ccf67b6156b080a6d6966dc09d0543f0c9be9e`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 6.3 MB (6308261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4b153923b2bef79dd19c29f9b88c045ce4e6e55242b154dbc462faed80d0db`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 84.5 KB (84499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ad462b285298ed7a2323c331255edc0ee999c93e0c8ae4a33c5ce454aeeff4`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67a0efc8d76bc7874505d46a4946de771e37c4eb62166bbec60dcd2a80e68e3`  
		Last Modified: Fri, 16 Aug 2024 21:57:37 GMT  
		Size: 53.1 MB (53062491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bba27c850d08471b57f0404d138486b2a1aed9dd9f3893b3b3def00f165ae25`  
		Last Modified: Fri, 16 Aug 2024 21:57:36 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a63b57aea184aabfabfd30d5a7c8567fe3d95a40b8f831ed764b2193d8bffe7`  
		Last Modified: Fri, 16 Aug 2024 21:57:36 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:10c4f8cecc7eb13f9d6d6dc54e1740ab90190e6d24c2e4eec6713b2931912225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a906609c1e200a6b10bedc63efea8af901e9897d1b8f31c4dcb5375222ba63f2`

```dockerfile
```

-	Layers:
	-	`sha256:3e420f6bc3bb35c7528c2f9e8ad122df634ff514d46807261853977ba0eb51f6`  
		Last Modified: Fri, 16 Aug 2024 21:57:34 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e739d640aea8812448d7dd39378e23771a2554a182f2099969410db56fa79917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122599486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d8b2b975dd95f7591d28783db8fc5752c99db0ffd5197320cecf290ce39c7f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eaa3c460d109197e8637b1a9599d7f18cccc546e66d1d62f6dd1508e2935dd`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 8.0 MB (7981761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9e960f5f951de003b26390946248f496a1eda867789ae06fd8b18055515450`  
		Last Modified: Tue, 13 Aug 2024 20:49:42 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99bff4ad6d3c4a0683cf02a74f06b61546be2a877da62aece45b0d3b9409871`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 17.0 MB (17049381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74376b78c4a6f5d12921d8dca6dcfa9e9f2bb0917ddeaa5991b98a8c6594581f`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 16.8 MB (16772960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c08f66b4f65a64aaad739c0ac5607c94142e38e67115632af35ef78cff1329c`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 17.2 MB (17182720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce67e83e18f9107f6bbf32d16c48a8f21c28e500a4212c8ebeca7b994936d7e`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c532de2c2cacfe1199219ef497170060946e3a593f771635c84f141b9a3b94c6`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7601c7d4e5af9ac7f6766b064bc79247c0912f3c5d6f3d02bfb58f49c9207`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194e0f500f2ba3365f850eac55a79e52a90ba4922806239f584025ccf347cea5`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 7.0 MB (7034963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9643f136f726def03ee1af9a52d6193e29fb13777be7e5dad5303f10ed36b68`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 98.7 KB (98659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8112d1aa134e43b2e075826bc7ea6a21adf3464ecd3aee260bf8f2947e9d5a50`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9dc9c485b7585bc344ca1a3c332c378d9ee340ecdb8aa344a75df81b017e1`  
		Last Modified: Tue, 13 Aug 2024 22:23:59 GMT  
		Size: 52.4 MB (52384159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7cbf878da555535371cabcf172c560243258cf73e8889885f96fbe66ded9c2`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97e744676fc32c335434d0c4e6890ce0f48ffb37aa99af9568bca483cbfca3f`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f6be705e7230112840619e69b7e6322ce4fc67c5f11c95e929f9e841f1e8403c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43bac9495e2c3ff9a3596159acfb499a4e9f6688d7b379425baf358201b63a1`

```dockerfile
```

-	Layers:
	-	`sha256:9604ca831aeb0d74501b911f9a7b547356be1ae57280b751700fd1d324dfd1ad`  
		Last Modified: Tue, 13 Aug 2024 22:23:56 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:af47f6c5401fa4d78609555d2c4b9babfe237af534c7b07ff2b036a0d427a118
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:1c4b1d49cece4db7e2dcaebda47131381ee475d375613c0ad913dd384ee2cba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.3 MB (152296869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa93fbe161d9efbaa4c0e48ceab0e109620689af00487864f7130a6ec89b8a4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97be572a9abc71e039fcf0e5c2cee826693d2e32b5aa28c52ee2e147f29f3ed2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 7.9 MB (7872256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d068c8136df4c77e60b80c6f269c341b11f27187ec77a9ce1a8519f4bdce441f`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3486b9b1692e5ae916e32c2133bb5e8f98a7f89b173cdb303b25d20094e8dee8`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.1 MB (18090913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1726802d7045e092159fdcac73e3c1461690d55c73403cdcdf031ac4145518e2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.4 MB (18404800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1774d2fed741a7a383f92d3969db43a321a4a02dcaad8a886967fb723954fa`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 18.8 MB (18818906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216e3a4876cf4f3c85c70bf9bed6dadfdc58ce83a5537dedb98ea42b20ff36c0`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5bd9a3f910707b7294207b927b3ade09f9d20b66525f2296ee65b90f7edb5`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425c20abf22d4da88ed53e7b1321b6515f33a887063e1f75e25530f7bf89723c`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5174f7db1d0f582b0c6e4a068cb27afd84b66c23716f5046592e2be1b5a225`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 6.7 MB (6657764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fcabf4da4d815f68d521020af7450dc776029613b976a0b4aa8d3429e7d18d`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 89.2 KB (89217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7096f07126cd3b58ec87699d558d9bf0b0b044533ada0f67254d85c94f0bc3b3`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8b74173c6813b97f6d02202faf9a563c7207e298b3204dd4340295344c8ede`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 56.8 MB (56770081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1647c2f9c8092fada70aa9758b7a69f1f3cd05a90891a0a532881cfd598c48`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c41c56a7d8896baa7e32b03546ff50a23492eb9543ed2089ab2fb66ede6ef`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddff6840fdc9aeb42249c80b9c338fe603cc5f0b00252bf16b8bdf2a5fb2f8c`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 981.0 KB (980992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a02b3fadcd722d124529c5401debc307f981a90fc96d45d5d92b96f0dd7545`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c5873bde466cc998bafb56445a5cb01a1a2f54f4166b40ae385bea47531624`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fda618391a49e503c15787e90efea8390d3e23e0621ef57525f337c23de9b6`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 21.0 MB (20979748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08614a56f1a4c3bbf5ebad13045c832079e403dcebb54554e52d5abcdb3b436`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:e63fe7c3704aa2dcc99fb485a4c317a39cb9c1b4d21542ab08c4c4f80a9fc923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23246a0ef23fd48a00bdc4420f83bb303595779eef9540a6b307ca752627e8f3`

```dockerfile
```

-	Layers:
	-	`sha256:030786d4fe7aad28fd3146cfcd96aebaf0140ae35626e5c6bdb622099b291852`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 30.6 KB (30580 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:40aed2a21da30df0c9cc2f6c0094e5be75f4f063959f290d81137e463c1f4b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146459861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403f1c1202717e657a3afb32bea3613930169406534f89b7fc204a622540f610`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eaa3c460d109197e8637b1a9599d7f18cccc546e66d1d62f6dd1508e2935dd`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 8.0 MB (7981761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9e960f5f951de003b26390946248f496a1eda867789ae06fd8b18055515450`  
		Last Modified: Tue, 13 Aug 2024 20:49:42 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99bff4ad6d3c4a0683cf02a74f06b61546be2a877da62aece45b0d3b9409871`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 17.0 MB (17049381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74376b78c4a6f5d12921d8dca6dcfa9e9f2bb0917ddeaa5991b98a8c6594581f`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 16.8 MB (16772960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c08f66b4f65a64aaad739c0ac5607c94142e38e67115632af35ef78cff1329c`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 17.2 MB (17182720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce67e83e18f9107f6bbf32d16c48a8f21c28e500a4212c8ebeca7b994936d7e`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c532de2c2cacfe1199219ef497170060946e3a593f771635c84f141b9a3b94c6`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7601c7d4e5af9ac7f6766b064bc79247c0912f3c5d6f3d02bfb58f49c9207`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194e0f500f2ba3365f850eac55a79e52a90ba4922806239f584025ccf347cea5`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 7.0 MB (7034963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9643f136f726def03ee1af9a52d6193e29fb13777be7e5dad5303f10ed36b68`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 98.7 KB (98659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8112d1aa134e43b2e075826bc7ea6a21adf3464ecd3aee260bf8f2947e9d5a50`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9dc9c485b7585bc344ca1a3c332c378d9ee340ecdb8aa344a75df81b017e1`  
		Last Modified: Tue, 13 Aug 2024 22:23:59 GMT  
		Size: 52.4 MB (52384159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7cbf878da555535371cabcf172c560243258cf73e8889885f96fbe66ded9c2`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97e744676fc32c335434d0c4e6890ce0f48ffb37aa99af9568bca483cbfca3f`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4503187f1903453dfdd96e29f2843028e7ab3999269f4e94f7fba03b1754d3`  
		Last Modified: Tue, 13 Aug 2024 23:09:28 GMT  
		Size: 1.0 MB (1023136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e456d8b7e6c45005803d8726755e761e590e47c68a1fb8750c012f4bfb57ef5`  
		Last Modified: Tue, 13 Aug 2024 23:09:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c292ab69c00576a9f271ac96f8d010a8785c5572d03a5efc32e80f2208bbf67d`  
		Last Modified: Tue, 13 Aug 2024 23:09:28 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc26ac4f7d112ba3395f6d5d5b6bd5975e89bb3a1aeccbb6d382cbcbbc757ae`  
		Last Modified: Tue, 13 Aug 2024 23:09:29 GMT  
		Size: 22.8 MB (22835879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570ac36fe23a0443a0db74a04c915f8a2fa16a8185157707d6d94f88a2270973`  
		Last Modified: Tue, 13 Aug 2024 23:09:29 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:83b8fc3691f89e164a3848ca85d5afb6047d2b8c36ee8500361a705a4f238a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544dbc1f438dbe68196bbe42b384836b43013481026eb3482ea165adc58e0331`

```dockerfile
```

-	Layers:
	-	`sha256:fdc4f405dfa87c2c564b75159723ba929dc1a643febd173d3215221105b7936a`  
		Last Modified: Tue, 13 Aug 2024 23:09:27 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:e1ded4b3a2aaf5d101daaca1e22004a6c4002e37cdf0842705f51159f0df81ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:722e8fd401b84665b82e0666308e3852fb7e55ef623784849a0ad1a0fbbfcd28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199540785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57c9795d7276f4ddea53e5745bd047597db78375c979913534c8fdf874a086a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Fri, 16 Aug 2024 21:04:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 21:04:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Aug 2024 21:04:37 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 21:04:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.2.zip
# Fri, 16 Aug 2024 21:04:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:04:49 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 21:04:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Fri, 16 Aug 2024 21:04:50 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Fri, 16 Aug 2024 21:05:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:05:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 21:05:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Fri, 16 Aug 2024 21:05:02 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Fri, 16 Aug 2024 21:05:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e5e515bd55c81feeefd0785d8074f5be7923da2cce4b86409954eafb42a89d`  
		Last Modified: Fri, 16 Aug 2024 21:05:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4236dc1d150b9033a0c12635f2856623e96efcf383d48c97522085f757a77d`  
		Last Modified: Fri, 16 Aug 2024 21:05:21 GMT  
		Size: 374.9 KB (374907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab4df154260eea68dd35cc730282a87fb57915392903c11035c17f519a6c96e`  
		Last Modified: Fri, 16 Aug 2024 21:05:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3677549ffed405f5ae64e6403793e352ecfac2b219c9eedb5028ff32996da03`  
		Last Modified: Fri, 16 Aug 2024 21:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfc19c3fa98906bdc20e8a8400afe4f9b414a7340b21d265dccf34ed27ac257`  
		Last Modified: Fri, 16 Aug 2024 21:05:21 GMT  
		Size: 18.4 MB (18421675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82313e190eab60e8625450d2b286dea76021f5da19bfdebe577415fa461e5c9`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14377702006bc82ef23e61f2b8ed17e316e10b87ba0673db89ec95a79ee87a9`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b0c8b1a15fc09aae430ab9e6a6db5c6f206f1a740c3a1c1b480315148a7f7f`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200e06de81cfb77043b8271865cdff0194d0e6754f636fb258b8a95e941f3ccf`  
		Last Modified: Fri, 16 Aug 2024 21:05:18 GMT  
		Size: 19.3 MB (19265658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ee8b6441d22cc15446aee0d2f0675daead9c2e51dbac7d89edc47d99df8303`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e105068269a03cdc4679d19d4afb6c5a824ffb43ccfbc2430a18e0a80b35554`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c871e44afd26ad9c6e84da90afe24be797cc92c7e5862563a271f080b7d6dc`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a3de421425ac0e051642931e6459b4da6f2f3cd7022114cd5b7811b9eca88e`  
		Last Modified: Fri, 16 Aug 2024 21:05:18 GMT  
		Size: 19.7 MB (19701964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:6fc12e3169bfe0a9322c7740f4f4079f8f45dd1b79168c426a89a43ad0c6d9fb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303121283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd6dcd72864533d8de94060162775ef92bd31748712fbcd1f03469008647db8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Fri, 16 Aug 2024 20:59:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 21:00:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Aug 2024 21:00:13 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 21:00:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.2.zip
# Fri, 16 Aug 2024 21:00:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:00:35 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 21:00:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Fri, 16 Aug 2024 21:00:36 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Fri, 16 Aug 2024 21:00:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:00:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 21:00:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Fri, 16 Aug 2024 21:00:57 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Fri, 16 Aug 2024 21:01:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc681518e2d562ce97fc231963b0590c8a4578d640e9226ebc7e7a64072c1c57`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf861a9062e8367fea0bf7fd15b3a23566d429c8f7a698862ed56a6b30e5d08`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 502.8 KB (502826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a6eef9d04b51a84647684d5ac6acc5bbcf56cf1e9a1677f27f0a451d0dc191`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f7463ca73d8038d2384509adeb789ee442a132ab89bd9125fd0d865c0e957c`  
		Last Modified: Fri, 16 Aug 2024 21:01:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1096db739f2668906215c2b312cca48af870253ffbbc08f284d90e88e5d9afd0`  
		Last Modified: Fri, 16 Aug 2024 21:01:23 GMT  
		Size: 18.4 MB (18429168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ba54531e0b5e75e9c6afb0f70803c3f19b3297ba195a9a0f0ed65ac1ed6cbb`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf33926246d70e6dc5eb83affb3e85e5e70ba479cf02633542f105b7c0f9844c`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f26c7e8351ae5c2502dd7735392d69fa658ffb65cb5f1ca900319b9409cf63`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14de9ca87757d524465e1db5e32a8e157bd58a897ed38348289c0293a894bb21`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 19.3 MB (19271416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cca9a181e2403ef565744f377e65fbaeceec043ac17c57026563ab53faa0edc`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61b3946fd8e06fe43f43af8f8d64efafff325bd4e24525b4464c35e4247d30c`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d994d497e123945dca78f465e5d4c09bf3d99d78c717f359cf93b78ed69720e1`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0130b148c08f6100b5c93d2c5de1ddd3a4a69543356d1c729eb4e1f72bded8dd`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 19.7 MB (19702913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:89451243e7ee80b1dd7d6e13e80627c63f3775b02426c3284264932fd4002be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:6fc12e3169bfe0a9322c7740f4f4079f8f45dd1b79168c426a89a43ad0c6d9fb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303121283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd6dcd72864533d8de94060162775ef92bd31748712fbcd1f03469008647db8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Fri, 16 Aug 2024 20:59:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 21:00:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Aug 2024 21:00:13 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 21:00:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.2.zip
# Fri, 16 Aug 2024 21:00:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:00:35 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 21:00:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Fri, 16 Aug 2024 21:00:36 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Fri, 16 Aug 2024 21:00:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:00:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 21:00:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Fri, 16 Aug 2024 21:00:57 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Fri, 16 Aug 2024 21:01:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc681518e2d562ce97fc231963b0590c8a4578d640e9226ebc7e7a64072c1c57`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf861a9062e8367fea0bf7fd15b3a23566d429c8f7a698862ed56a6b30e5d08`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 502.8 KB (502826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a6eef9d04b51a84647684d5ac6acc5bbcf56cf1e9a1677f27f0a451d0dc191`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f7463ca73d8038d2384509adeb789ee442a132ab89bd9125fd0d865c0e957c`  
		Last Modified: Fri, 16 Aug 2024 21:01:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1096db739f2668906215c2b312cca48af870253ffbbc08f284d90e88e5d9afd0`  
		Last Modified: Fri, 16 Aug 2024 21:01:23 GMT  
		Size: 18.4 MB (18429168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ba54531e0b5e75e9c6afb0f70803c3f19b3297ba195a9a0f0ed65ac1ed6cbb`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf33926246d70e6dc5eb83affb3e85e5e70ba479cf02633542f105b7c0f9844c`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f26c7e8351ae5c2502dd7735392d69fa658ffb65cb5f1ca900319b9409cf63`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14de9ca87757d524465e1db5e32a8e157bd58a897ed38348289c0293a894bb21`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 19.3 MB (19271416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cca9a181e2403ef565744f377e65fbaeceec043ac17c57026563ab53faa0edc`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61b3946fd8e06fe43f43af8f8d64efafff325bd4e24525b4464c35e4247d30c`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d994d497e123945dca78f465e5d4c09bf3d99d78c717f359cf93b78ed69720e1`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0130b148c08f6100b5c93d2c5de1ddd3a4a69543356d1c729eb4e1f72bded8dd`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 19.7 MB (19702913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:87827cb0d8a93f2c55cd85a9bd673523c38715a87d0257cb18798505f0154212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:722e8fd401b84665b82e0666308e3852fb7e55ef623784849a0ad1a0fbbfcd28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199540785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57c9795d7276f4ddea53e5745bd047597db78375c979913534c8fdf874a086a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Fri, 16 Aug 2024 21:04:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 21:04:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Aug 2024 21:04:37 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 21:04:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.2.zip
# Fri, 16 Aug 2024 21:04:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:04:49 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 21:04:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Fri, 16 Aug 2024 21:04:50 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Fri, 16 Aug 2024 21:05:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:05:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 21:05:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Fri, 16 Aug 2024 21:05:02 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Fri, 16 Aug 2024 21:05:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e5e515bd55c81feeefd0785d8074f5be7923da2cce4b86409954eafb42a89d`  
		Last Modified: Fri, 16 Aug 2024 21:05:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4236dc1d150b9033a0c12635f2856623e96efcf383d48c97522085f757a77d`  
		Last Modified: Fri, 16 Aug 2024 21:05:21 GMT  
		Size: 374.9 KB (374907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab4df154260eea68dd35cc730282a87fb57915392903c11035c17f519a6c96e`  
		Last Modified: Fri, 16 Aug 2024 21:05:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3677549ffed405f5ae64e6403793e352ecfac2b219c9eedb5028ff32996da03`  
		Last Modified: Fri, 16 Aug 2024 21:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfc19c3fa98906bdc20e8a8400afe4f9b414a7340b21d265dccf34ed27ac257`  
		Last Modified: Fri, 16 Aug 2024 21:05:21 GMT  
		Size: 18.4 MB (18421675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82313e190eab60e8625450d2b286dea76021f5da19bfdebe577415fa461e5c9`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14377702006bc82ef23e61f2b8ed17e316e10b87ba0673db89ec95a79ee87a9`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b0c8b1a15fc09aae430ab9e6a6db5c6f206f1a740c3a1c1b480315148a7f7f`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200e06de81cfb77043b8271865cdff0194d0e6754f636fb258b8a95e941f3ccf`  
		Last Modified: Fri, 16 Aug 2024 21:05:18 GMT  
		Size: 19.3 MB (19265658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ee8b6441d22cc15446aee0d2f0675daead9c2e51dbac7d89edc47d99df8303`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e105068269a03cdc4679d19d4afb6c5a824ffb43ccfbc2430a18e0a80b35554`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c871e44afd26ad9c6e84da90afe24be797cc92c7e5862563a271f080b7d6dc`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a3de421425ac0e051642931e6459b4da6f2f3cd7022114cd5b7811b9eca88e`  
		Last Modified: Fri, 16 Aug 2024 21:05:18 GMT  
		Size: 19.7 MB (19701964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.1`

```console
$ docker pull docker@sha256:6eb8bfb2c82d454c0248b5dd41b9607f1b76096c06acf985e862f2ea069db33e
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

### `docker:27.1` - linux; amd64

```console
$ docker pull docker@sha256:fc81f6680c575a7381f7a586aab4643cdbe79cf9f5af594d2c783a9eb0a0e1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130334773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb13d0c9247298368f97e0637bb60c105cf8159fd29364881b45b5c96c78d621`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97be572a9abc71e039fcf0e5c2cee826693d2e32b5aa28c52ee2e147f29f3ed2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 7.9 MB (7872256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d068c8136df4c77e60b80c6f269c341b11f27187ec77a9ce1a8519f4bdce441f`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3486b9b1692e5ae916e32c2133bb5e8f98a7f89b173cdb303b25d20094e8dee8`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.1 MB (18090913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1726802d7045e092159fdcac73e3c1461690d55c73403cdcdf031ac4145518e2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.4 MB (18404800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1774d2fed741a7a383f92d3969db43a321a4a02dcaad8a886967fb723954fa`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 18.8 MB (18818906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216e3a4876cf4f3c85c70bf9bed6dadfdc58ce83a5537dedb98ea42b20ff36c0`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5bd9a3f910707b7294207b927b3ade09f9d20b66525f2296ee65b90f7edb5`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425c20abf22d4da88ed53e7b1321b6515f33a887063e1f75e25530f7bf89723c`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5174f7db1d0f582b0c6e4a068cb27afd84b66c23716f5046592e2be1b5a225`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 6.7 MB (6657764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fcabf4da4d815f68d521020af7450dc776029613b976a0b4aa8d3429e7d18d`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 89.2 KB (89217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7096f07126cd3b58ec87699d558d9bf0b0b044533ada0f67254d85c94f0bc3b3`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8b74173c6813b97f6d02202faf9a563c7207e298b3204dd4340295344c8ede`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 56.8 MB (56770081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1647c2f9c8092fada70aa9758b7a69f1f3cd05a90891a0a532881cfd598c48`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c41c56a7d8896baa7e32b03546ff50a23492eb9543ed2089ab2fb66ede6ef`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1` - unknown; unknown

```console
$ docker pull docker@sha256:14ec78850163b4e599f6b88fe195725546c45bc30c37ed06f92bd2e7b2f5b392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33683cd4c1538f63f2751b42869d268ec779b0d5fe22d4765e60f56c75e84787`

```dockerfile
```

-	Layers:
	-	`sha256:76c6029aaa7435fba20177df1eb133a9c0a03d8b5c6fe48799e1fe75e360c69f`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1` - linux; arm variant v6

```console
$ docker pull docker@sha256:f027111d31885b0ed9642d1b92d7e62b7644b92089eebc5af8a32d7f8bebfc8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122569652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a41929651127c7fdf1f8cfa71354b837597836af87e070e112cbee135c1040`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749d51120dd4449c98cad5624e6a58aaf21f6b57355b1537b1262f69c27968e`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 7.8 MB (7807488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dee64c722233ea05fa0db7774bbb908ccb3860c76b492b90725b4a00faf74a`  
		Last Modified: Tue, 13 Aug 2024 20:03:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aa9bf3b5617e94aa7647537a116937dc7c6d223c96912c2ffc1302ccceab1b`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 16.4 MB (16362863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b4ff9c935b9bea7d6a6f982aab917c1a4fd29032db6ff2a2026ee7f77cc75`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.1 MB (17114711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31fe971362beacbc7fe1ce84a4f59817b327260334951577b2bdc1640d49164`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.8 MB (17776509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7dca5ea08fd6046c223c1378a8259479b60e2b7c9fe45d9ebc3394f237a3c`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 534.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffadf986c05f1d49184514bc67815f318456acc65c0abfd74b2cce1b6d86ecca`  
		Last Modified: Tue, 13 Aug 2024 20:03:15 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7edf55c16e9e482eb8124f38438564758d96aa113c06fd945bcb13988d3fba6`  
		Last Modified: Tue, 13 Aug 2024 20:03:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7dcf38e93a9b47e0f66795e256f2901c2c4bfc37556e81fea2a063cee12eed`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 7.0 MB (6984036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dc040353146061f1f9e8d56420bfefd970c9707a3834a5bcf02701bc7f87a6`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 88.4 KB (88407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af6ea4938ff0c08202d2f8e3f84e00a915d37297b863ed5032cc8f8fa5cd906`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a7459df9025cc27e33a8fecee41b7192346cf1721924cfabec6187dff5186`  
		Last Modified: Tue, 13 Aug 2024 20:57:37 GMT  
		Size: 53.1 MB (53062512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f07f1d6edcfeac2205add2fc7459ea84419349425810e89ef26b86733a587`  
		Last Modified: Tue, 13 Aug 2024 20:57:36 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40b0d4ce5c2e81228c159aa2dcd3e15ecf2f27ee8a41d175c78e599ca4af850`  
		Last Modified: Tue, 13 Aug 2024 20:57:36 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1` - unknown; unknown

```console
$ docker pull docker@sha256:6c057a6e1b62568c5bdee69c9c82240780e3862912fcaa566a3a3487a470fd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a96c343221bdcb48cb74979b02ab5c13b27dbff1a66a0ceb3780e97c736573f`

```dockerfile
```

-	Layers:
	-	`sha256:8cea367fa521297df7cfa3bc63f39bd2b776aa0f558f0427199bc08da2d719d2`  
		Last Modified: Tue, 13 Aug 2024 20:57:34 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1` - linux; arm variant v7

```console
$ docker pull docker@sha256:a4332a1e0f1aaa47f76bb148424557761569ddbaa01a4b0733831f22a7e2e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120929654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be199173f5a13331c5558376e7c160c53e51cc77a7f598bbe39233e723dade8b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81dc9168b7d20594a7b5afa567e1b9102c0d289d4b9956af1dd0553da38503f`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 7.1 MB (7143486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b63ca62b0868cd9cbb097a6c34d9eb3a8e551918380dd69db51fbe7459654`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff65173bbd98afd04b6c052172c858476533d0f4873c5b6a81bda0849b5792`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 16.4 MB (16353814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd7e108f551e071a490fb8213c13dccea238c6e5c6ed12be3eef86831d31eb`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 17.1 MB (17103032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b020a8e04eea5428d7645058058bdeea76775ad16c0c306557b00c9b3cce3707`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 17.8 MB (17771143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf51759e8c2b5bc311e671ddc5401fb8b470e266b8553c7d887176c8be0e673`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06151b2e48f60b43b5a3438902d125f5201b35d94f354ac3ac4351ed695565f`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf092fc62ad5de9ceea220ba585b82ea46d65253b23f11533d59f110184e5fe4`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a5e67d714baf4e953669b348ccf67b6156b080a6d6966dc09d0543f0c9be9e`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 6.3 MB (6308261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4b153923b2bef79dd19c29f9b88c045ce4e6e55242b154dbc462faed80d0db`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 84.5 KB (84499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ad462b285298ed7a2323c331255edc0ee999c93e0c8ae4a33c5ce454aeeff4`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67a0efc8d76bc7874505d46a4946de771e37c4eb62166bbec60dcd2a80e68e3`  
		Last Modified: Fri, 16 Aug 2024 21:57:37 GMT  
		Size: 53.1 MB (53062491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bba27c850d08471b57f0404d138486b2a1aed9dd9f3893b3b3def00f165ae25`  
		Last Modified: Fri, 16 Aug 2024 21:57:36 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a63b57aea184aabfabfd30d5a7c8567fe3d95a40b8f831ed764b2193d8bffe7`  
		Last Modified: Fri, 16 Aug 2024 21:57:36 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1` - unknown; unknown

```console
$ docker pull docker@sha256:10c4f8cecc7eb13f9d6d6dc54e1740ab90190e6d24c2e4eec6713b2931912225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a906609c1e200a6b10bedc63efea8af901e9897d1b8f31c4dcb5375222ba63f2`

```dockerfile
```

-	Layers:
	-	`sha256:3e420f6bc3bb35c7528c2f9e8ad122df634ff514d46807261853977ba0eb51f6`  
		Last Modified: Fri, 16 Aug 2024 21:57:34 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e739d640aea8812448d7dd39378e23771a2554a182f2099969410db56fa79917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122599486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d8b2b975dd95f7591d28783db8fc5752c99db0ffd5197320cecf290ce39c7f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eaa3c460d109197e8637b1a9599d7f18cccc546e66d1d62f6dd1508e2935dd`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 8.0 MB (7981761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9e960f5f951de003b26390946248f496a1eda867789ae06fd8b18055515450`  
		Last Modified: Tue, 13 Aug 2024 20:49:42 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99bff4ad6d3c4a0683cf02a74f06b61546be2a877da62aece45b0d3b9409871`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 17.0 MB (17049381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74376b78c4a6f5d12921d8dca6dcfa9e9f2bb0917ddeaa5991b98a8c6594581f`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 16.8 MB (16772960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c08f66b4f65a64aaad739c0ac5607c94142e38e67115632af35ef78cff1329c`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 17.2 MB (17182720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce67e83e18f9107f6bbf32d16c48a8f21c28e500a4212c8ebeca7b994936d7e`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c532de2c2cacfe1199219ef497170060946e3a593f771635c84f141b9a3b94c6`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7601c7d4e5af9ac7f6766b064bc79247c0912f3c5d6f3d02bfb58f49c9207`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194e0f500f2ba3365f850eac55a79e52a90ba4922806239f584025ccf347cea5`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 7.0 MB (7034963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9643f136f726def03ee1af9a52d6193e29fb13777be7e5dad5303f10ed36b68`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 98.7 KB (98659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8112d1aa134e43b2e075826bc7ea6a21adf3464ecd3aee260bf8f2947e9d5a50`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9dc9c485b7585bc344ca1a3c332c378d9ee340ecdb8aa344a75df81b017e1`  
		Last Modified: Tue, 13 Aug 2024 22:23:59 GMT  
		Size: 52.4 MB (52384159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7cbf878da555535371cabcf172c560243258cf73e8889885f96fbe66ded9c2`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97e744676fc32c335434d0c4e6890ce0f48ffb37aa99af9568bca483cbfca3f`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1` - unknown; unknown

```console
$ docker pull docker@sha256:f6be705e7230112840619e69b7e6322ce4fc67c5f11c95e929f9e841f1e8403c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43bac9495e2c3ff9a3596159acfb499a4e9f6688d7b379425baf358201b63a1`

```dockerfile
```

-	Layers:
	-	`sha256:9604ca831aeb0d74501b911f9a7b547356be1ae57280b751700fd1d324dfd1ad`  
		Last Modified: Tue, 13 Aug 2024 22:23:56 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.1-cli`

```console
$ docker pull docker@sha256:c8af17c2e98d13ce5c18d9d31d6e8df47c76d1ba504d2f1782980bb8673af4cb
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

### `docker:27.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:444582958ec806c73d40f3702a8a8d84dc2e82feb0d9b44c738fca09ed2820ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66818343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe40c55ae60532fa0075302e6e93e7248c71837afcbd1c56e77b04e256552e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Aug 2024 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b830b3ce3f84ea7067567326d58a3c311c803b3e94cee51732c87abaf0b1644a`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 7.9 MB (7872313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f67cd05487ef47b2034f553790ea2efb816214bef9fd63d5d4f98254167b56e`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201b9999b9284e2bb11f5f0dc6cb35f9f890e8ef84edbd6edbd7f2ea82918c97`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 18.1 MB (18090908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0ed696b310c4d4cd09c07f7566ed6e2baa3f866160967ef06cf205d244859c`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 18.4 MB (18404798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d43008ea7ba356da560c03ab69f55df1d585a289fe0b9e4388f07ff04648932`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 18.8 MB (18825277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5e249d37736904735e2ce24e0bdea2329356683f6cdc14f3b8a7f1f5794c94`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75295f954e5cf281711fb0cb6e50cda9c6305918cc357d63e5347abf36cf48d`  
		Last Modified: Fri, 16 Aug 2024 20:55:55 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f64e86da193d3fea1e01efb5b7a81578e84d4e4593aee8279e9361b9e7e529`  
		Last Modified: Fri, 16 Aug 2024 20:55:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:bf1312c933add91f38029909c3177cd3b9f727efb4e56065fe297c6da6ffb91f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8336e1fddcafee01e26424a9f2c4608561aa729df648622918daaf2a3ef44053`

```dockerfile
```

-	Layers:
	-	`sha256:c16850f73bbeb2eb267302c311cadcadd55959d236b402c255acf9e6a760625f`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:ad97551c8ab5f60dc65827a43fb5bfc13375c4128efad7a326a9823e0be68d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62435713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468051ea9e870d4ee592d7253bae1b185cd265c4f3b54f8be9f8b1a820359d3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Aug 2024 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749d51120dd4449c98cad5624e6a58aaf21f6b57355b1537b1262f69c27968e`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 7.8 MB (7807488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dee64c722233ea05fa0db7774bbb908ccb3860c76b492b90725b4a00faf74a`  
		Last Modified: Tue, 13 Aug 2024 20:03:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aa9bf3b5617e94aa7647537a116937dc7c6d223c96912c2ffc1302ccceab1b`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 16.4 MB (16362863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b4ff9c935b9bea7d6a6f982aab917c1a4fd29032db6ff2a2026ee7f77cc75`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.1 MB (17114711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc83f1a40d0c658722d9af33f70561ec5dd29cadd86f625da7bcfa50022733b6`  
		Last Modified: Fri, 16 Aug 2024 20:55:46 GMT  
		Size: 17.8 MB (17783303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5f17b4f1f75fbc81e81b8c4714b51f7829480cd793423fdbe280b4a0e06cdc`  
		Last Modified: Fri, 16 Aug 2024 20:55:45 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d17e0519f279b5dc8f4f4d2233b55fa585e9d0f4e28b2ec38a893f46d415da`  
		Last Modified: Fri, 16 Aug 2024 20:55:45 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ddce9ce1633ca8261319074be47691ef0fa443df2b2fa759364895def2fb50`  
		Last Modified: Fri, 16 Aug 2024 20:55:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:72ac9cedabc23854d5804ef9acc704d8bc5672c4f2f7fa895f0536b433b53c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48dc65f2a968c7f37459c45a1f206fd483248e32a76f9d647ccd35c71bb1a66`

```dockerfile
```

-	Layers:
	-	`sha256:0f0379928ebdda35d5a3de2751c7fb8bf3f92b87ef1bc4445614cadfa4d0042b`  
		Last Modified: Fri, 16 Aug 2024 20:55:45 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:cc97a6244b7807809e92b3d720bc2b5f4748fe77f7b1d07f19d033559a0ad00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61468602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509b86a39961f355e5e37e9847693e175944080eae9ea5595e844a7932fe7c06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Aug 2024 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81dc9168b7d20594a7b5afa567e1b9102c0d289d4b9956af1dd0553da38503f`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 7.1 MB (7143486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b63ca62b0868cd9cbb097a6c34d9eb3a8e551918380dd69db51fbe7459654`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff65173bbd98afd04b6c052172c858476533d0f4873c5b6a81bda0849b5792`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 16.4 MB (16353814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd7e108f551e071a490fb8213c13dccea238c6e5c6ed12be3eef86831d31eb`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 17.1 MB (17103032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b020a8e04eea5428d7645058058bdeea76775ad16c0c306557b00c9b3cce3707`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 17.8 MB (17771143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf51759e8c2b5bc311e671ddc5401fb8b470e266b8553c7d887176c8be0e673`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06151b2e48f60b43b5a3438902d125f5201b35d94f354ac3ac4351ed695565f`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf092fc62ad5de9ceea220ba585b82ea46d65253b23f11533d59f110184e5fe4`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f183a263ab8d9b602944b555e29de9642d82e659e768b89ec39b5617024c4c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa7b9ac79beca13b0bc6894266285efc76f1e0853417a57b774ad69e6a882f5`

```dockerfile
```

-	Layers:
	-	`sha256:b2e8085a6ac1eeb458f441d28f5b14e745904be32fb62d75e214c3746c87091e`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:173d5a1620cd4c9838d8c6eeaff20a78fbcf08ee2e51c12449f832530e7edbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63080030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c697038997a5fe8ff64a0a9e3a2befe1ab1ffa2dbbce9a6d36ca94614c2e9207`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Aug 2024 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729161d0df240d9ed83f30e35c6fe471b1fae935500748d1ef7da84e664cdb8a`  
		Last Modified: Fri, 16 Aug 2024 20:55:42 GMT  
		Size: 8.0 MB (7981771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b9491762d2e0304f13e86117eb8d95e32f661c882e832b16bee6e8bb9098cb`  
		Last Modified: Fri, 16 Aug 2024 20:55:41 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fdb7ce0e7cf19d21a2bd7c9f95c09245271c0474a184066b1410007b8d4578`  
		Last Modified: Fri, 16 Aug 2024 20:55:42 GMT  
		Size: 17.0 MB (17049378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99813ceebaed11f6388e8ad3c4c1b371512de366ba5488d2f99200a424f074f`  
		Last Modified: Fri, 16 Aug 2024 20:55:42 GMT  
		Size: 16.8 MB (16772960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316a30f1c6a00f4fbfcba19ce9ccb4c2d5709b52e454b56144ec8f67d26208e2`  
		Last Modified: Fri, 16 Aug 2024 20:55:43 GMT  
		Size: 17.2 MB (17186835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0d611bb20624f74153d3ec09ce18870c07860b77939bdf1e019e0740de454a`  
		Last Modified: Fri, 16 Aug 2024 20:55:43 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9b0bb076214cf2f061a5937a293c9b2915ccf6dd121c501471f941589eab06`  
		Last Modified: Fri, 16 Aug 2024 20:55:43 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75f172f02f32a93ea69404964c9c459ce24e0f2cfe1585a6387e076ee96535d`  
		Last Modified: Fri, 16 Aug 2024 20:55:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9fe09d16bdc866f48ca5138929e946de2919fc7472dab2277a4690007a863f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4debb6c6f5e419a67a262e3c2d825765ae2e8b3f71720fbbd0843ead3c73e23`

```dockerfile
```

-	Layers:
	-	`sha256:ee581fd74c551286cbef0f11f61d4110c9e68a8323a697f9a454568d1603785a`  
		Last Modified: Fri, 16 Aug 2024 20:55:41 GMT  
		Size: 38.2 KB (38227 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.1-dind`

```console
$ docker pull docker@sha256:6eb8bfb2c82d454c0248b5dd41b9607f1b76096c06acf985e862f2ea069db33e
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

### `docker:27.1-dind` - linux; amd64

```console
$ docker pull docker@sha256:fc81f6680c575a7381f7a586aab4643cdbe79cf9f5af594d2c783a9eb0a0e1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130334773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb13d0c9247298368f97e0637bb60c105cf8159fd29364881b45b5c96c78d621`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97be572a9abc71e039fcf0e5c2cee826693d2e32b5aa28c52ee2e147f29f3ed2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 7.9 MB (7872256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d068c8136df4c77e60b80c6f269c341b11f27187ec77a9ce1a8519f4bdce441f`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3486b9b1692e5ae916e32c2133bb5e8f98a7f89b173cdb303b25d20094e8dee8`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.1 MB (18090913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1726802d7045e092159fdcac73e3c1461690d55c73403cdcdf031ac4145518e2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.4 MB (18404800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1774d2fed741a7a383f92d3969db43a321a4a02dcaad8a886967fb723954fa`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 18.8 MB (18818906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216e3a4876cf4f3c85c70bf9bed6dadfdc58ce83a5537dedb98ea42b20ff36c0`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5bd9a3f910707b7294207b927b3ade09f9d20b66525f2296ee65b90f7edb5`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425c20abf22d4da88ed53e7b1321b6515f33a887063e1f75e25530f7bf89723c`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5174f7db1d0f582b0c6e4a068cb27afd84b66c23716f5046592e2be1b5a225`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 6.7 MB (6657764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fcabf4da4d815f68d521020af7450dc776029613b976a0b4aa8d3429e7d18d`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 89.2 KB (89217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7096f07126cd3b58ec87699d558d9bf0b0b044533ada0f67254d85c94f0bc3b3`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8b74173c6813b97f6d02202faf9a563c7207e298b3204dd4340295344c8ede`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 56.8 MB (56770081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1647c2f9c8092fada70aa9758b7a69f1f3cd05a90891a0a532881cfd598c48`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c41c56a7d8896baa7e32b03546ff50a23492eb9543ed2089ab2fb66ede6ef`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:14ec78850163b4e599f6b88fe195725546c45bc30c37ed06f92bd2e7b2f5b392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33683cd4c1538f63f2751b42869d268ec779b0d5fe22d4765e60f56c75e84787`

```dockerfile
```

-	Layers:
	-	`sha256:76c6029aaa7435fba20177df1eb133a9c0a03d8b5c6fe48799e1fe75e360c69f`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:f027111d31885b0ed9642d1b92d7e62b7644b92089eebc5af8a32d7f8bebfc8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122569652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a41929651127c7fdf1f8cfa71354b837597836af87e070e112cbee135c1040`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749d51120dd4449c98cad5624e6a58aaf21f6b57355b1537b1262f69c27968e`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 7.8 MB (7807488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dee64c722233ea05fa0db7774bbb908ccb3860c76b492b90725b4a00faf74a`  
		Last Modified: Tue, 13 Aug 2024 20:03:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aa9bf3b5617e94aa7647537a116937dc7c6d223c96912c2ffc1302ccceab1b`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 16.4 MB (16362863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b4ff9c935b9bea7d6a6f982aab917c1a4fd29032db6ff2a2026ee7f77cc75`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.1 MB (17114711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31fe971362beacbc7fe1ce84a4f59817b327260334951577b2bdc1640d49164`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.8 MB (17776509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7dca5ea08fd6046c223c1378a8259479b60e2b7c9fe45d9ebc3394f237a3c`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 534.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffadf986c05f1d49184514bc67815f318456acc65c0abfd74b2cce1b6d86ecca`  
		Last Modified: Tue, 13 Aug 2024 20:03:15 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7edf55c16e9e482eb8124f38438564758d96aa113c06fd945bcb13988d3fba6`  
		Last Modified: Tue, 13 Aug 2024 20:03:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7dcf38e93a9b47e0f66795e256f2901c2c4bfc37556e81fea2a063cee12eed`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 7.0 MB (6984036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dc040353146061f1f9e8d56420bfefd970c9707a3834a5bcf02701bc7f87a6`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 88.4 KB (88407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af6ea4938ff0c08202d2f8e3f84e00a915d37297b863ed5032cc8f8fa5cd906`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a7459df9025cc27e33a8fecee41b7192346cf1721924cfabec6187dff5186`  
		Last Modified: Tue, 13 Aug 2024 20:57:37 GMT  
		Size: 53.1 MB (53062512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f07f1d6edcfeac2205add2fc7459ea84419349425810e89ef26b86733a587`  
		Last Modified: Tue, 13 Aug 2024 20:57:36 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40b0d4ce5c2e81228c159aa2dcd3e15ecf2f27ee8a41d175c78e599ca4af850`  
		Last Modified: Tue, 13 Aug 2024 20:57:36 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6c057a6e1b62568c5bdee69c9c82240780e3862912fcaa566a3a3487a470fd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a96c343221bdcb48cb74979b02ab5c13b27dbff1a66a0ceb3780e97c736573f`

```dockerfile
```

-	Layers:
	-	`sha256:8cea367fa521297df7cfa3bc63f39bd2b776aa0f558f0427199bc08da2d719d2`  
		Last Modified: Tue, 13 Aug 2024 20:57:34 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:a4332a1e0f1aaa47f76bb148424557761569ddbaa01a4b0733831f22a7e2e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120929654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be199173f5a13331c5558376e7c160c53e51cc77a7f598bbe39233e723dade8b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81dc9168b7d20594a7b5afa567e1b9102c0d289d4b9956af1dd0553da38503f`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 7.1 MB (7143486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b63ca62b0868cd9cbb097a6c34d9eb3a8e551918380dd69db51fbe7459654`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff65173bbd98afd04b6c052172c858476533d0f4873c5b6a81bda0849b5792`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 16.4 MB (16353814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd7e108f551e071a490fb8213c13dccea238c6e5c6ed12be3eef86831d31eb`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 17.1 MB (17103032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b020a8e04eea5428d7645058058bdeea76775ad16c0c306557b00c9b3cce3707`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 17.8 MB (17771143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf51759e8c2b5bc311e671ddc5401fb8b470e266b8553c7d887176c8be0e673`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06151b2e48f60b43b5a3438902d125f5201b35d94f354ac3ac4351ed695565f`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf092fc62ad5de9ceea220ba585b82ea46d65253b23f11533d59f110184e5fe4`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a5e67d714baf4e953669b348ccf67b6156b080a6d6966dc09d0543f0c9be9e`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 6.3 MB (6308261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4b153923b2bef79dd19c29f9b88c045ce4e6e55242b154dbc462faed80d0db`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 84.5 KB (84499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ad462b285298ed7a2323c331255edc0ee999c93e0c8ae4a33c5ce454aeeff4`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67a0efc8d76bc7874505d46a4946de771e37c4eb62166bbec60dcd2a80e68e3`  
		Last Modified: Fri, 16 Aug 2024 21:57:37 GMT  
		Size: 53.1 MB (53062491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bba27c850d08471b57f0404d138486b2a1aed9dd9f3893b3b3def00f165ae25`  
		Last Modified: Fri, 16 Aug 2024 21:57:36 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a63b57aea184aabfabfd30d5a7c8567fe3d95a40b8f831ed764b2193d8bffe7`  
		Last Modified: Fri, 16 Aug 2024 21:57:36 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:10c4f8cecc7eb13f9d6d6dc54e1740ab90190e6d24c2e4eec6713b2931912225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a906609c1e200a6b10bedc63efea8af901e9897d1b8f31c4dcb5375222ba63f2`

```dockerfile
```

-	Layers:
	-	`sha256:3e420f6bc3bb35c7528c2f9e8ad122df634ff514d46807261853977ba0eb51f6`  
		Last Modified: Fri, 16 Aug 2024 21:57:34 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e739d640aea8812448d7dd39378e23771a2554a182f2099969410db56fa79917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122599486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d8b2b975dd95f7591d28783db8fc5752c99db0ffd5197320cecf290ce39c7f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eaa3c460d109197e8637b1a9599d7f18cccc546e66d1d62f6dd1508e2935dd`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 8.0 MB (7981761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9e960f5f951de003b26390946248f496a1eda867789ae06fd8b18055515450`  
		Last Modified: Tue, 13 Aug 2024 20:49:42 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99bff4ad6d3c4a0683cf02a74f06b61546be2a877da62aece45b0d3b9409871`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 17.0 MB (17049381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74376b78c4a6f5d12921d8dca6dcfa9e9f2bb0917ddeaa5991b98a8c6594581f`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 16.8 MB (16772960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c08f66b4f65a64aaad739c0ac5607c94142e38e67115632af35ef78cff1329c`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 17.2 MB (17182720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce67e83e18f9107f6bbf32d16c48a8f21c28e500a4212c8ebeca7b994936d7e`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c532de2c2cacfe1199219ef497170060946e3a593f771635c84f141b9a3b94c6`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7601c7d4e5af9ac7f6766b064bc79247c0912f3c5d6f3d02bfb58f49c9207`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194e0f500f2ba3365f850eac55a79e52a90ba4922806239f584025ccf347cea5`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 7.0 MB (7034963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9643f136f726def03ee1af9a52d6193e29fb13777be7e5dad5303f10ed36b68`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 98.7 KB (98659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8112d1aa134e43b2e075826bc7ea6a21adf3464ecd3aee260bf8f2947e9d5a50`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9dc9c485b7585bc344ca1a3c332c378d9ee340ecdb8aa344a75df81b017e1`  
		Last Modified: Tue, 13 Aug 2024 22:23:59 GMT  
		Size: 52.4 MB (52384159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7cbf878da555535371cabcf172c560243258cf73e8889885f96fbe66ded9c2`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97e744676fc32c335434d0c4e6890ce0f48ffb37aa99af9568bca483cbfca3f`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f6be705e7230112840619e69b7e6322ce4fc67c5f11c95e929f9e841f1e8403c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43bac9495e2c3ff9a3596159acfb499a4e9f6688d7b379425baf358201b63a1`

```dockerfile
```

-	Layers:
	-	`sha256:9604ca831aeb0d74501b911f9a7b547356be1ae57280b751700fd1d324dfd1ad`  
		Last Modified: Tue, 13 Aug 2024 22:23:56 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.1-dind-rootless`

```console
$ docker pull docker@sha256:af47f6c5401fa4d78609555d2c4b9babfe237af534c7b07ff2b036a0d427a118
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.1-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:1c4b1d49cece4db7e2dcaebda47131381ee475d375613c0ad913dd384ee2cba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.3 MB (152296869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa93fbe161d9efbaa4c0e48ceab0e109620689af00487864f7130a6ec89b8a4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97be572a9abc71e039fcf0e5c2cee826693d2e32b5aa28c52ee2e147f29f3ed2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 7.9 MB (7872256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d068c8136df4c77e60b80c6f269c341b11f27187ec77a9ce1a8519f4bdce441f`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3486b9b1692e5ae916e32c2133bb5e8f98a7f89b173cdb303b25d20094e8dee8`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.1 MB (18090913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1726802d7045e092159fdcac73e3c1461690d55c73403cdcdf031ac4145518e2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.4 MB (18404800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1774d2fed741a7a383f92d3969db43a321a4a02dcaad8a886967fb723954fa`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 18.8 MB (18818906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216e3a4876cf4f3c85c70bf9bed6dadfdc58ce83a5537dedb98ea42b20ff36c0`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5bd9a3f910707b7294207b927b3ade09f9d20b66525f2296ee65b90f7edb5`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425c20abf22d4da88ed53e7b1321b6515f33a887063e1f75e25530f7bf89723c`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5174f7db1d0f582b0c6e4a068cb27afd84b66c23716f5046592e2be1b5a225`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 6.7 MB (6657764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fcabf4da4d815f68d521020af7450dc776029613b976a0b4aa8d3429e7d18d`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 89.2 KB (89217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7096f07126cd3b58ec87699d558d9bf0b0b044533ada0f67254d85c94f0bc3b3`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8b74173c6813b97f6d02202faf9a563c7207e298b3204dd4340295344c8ede`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 56.8 MB (56770081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1647c2f9c8092fada70aa9758b7a69f1f3cd05a90891a0a532881cfd598c48`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c41c56a7d8896baa7e32b03546ff50a23492eb9543ed2089ab2fb66ede6ef`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddff6840fdc9aeb42249c80b9c338fe603cc5f0b00252bf16b8bdf2a5fb2f8c`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 981.0 KB (980992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a02b3fadcd722d124529c5401debc307f981a90fc96d45d5d92b96f0dd7545`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c5873bde466cc998bafb56445a5cb01a1a2f54f4166b40ae385bea47531624`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fda618391a49e503c15787e90efea8390d3e23e0621ef57525f337c23de9b6`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 21.0 MB (20979748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08614a56f1a4c3bbf5ebad13045c832079e403dcebb54554e52d5abcdb3b436`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:e63fe7c3704aa2dcc99fb485a4c317a39cb9c1b4d21542ab08c4c4f80a9fc923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23246a0ef23fd48a00bdc4420f83bb303595779eef9540a6b307ca752627e8f3`

```dockerfile
```

-	Layers:
	-	`sha256:030786d4fe7aad28fd3146cfcd96aebaf0140ae35626e5c6bdb622099b291852`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 30.6 KB (30580 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:40aed2a21da30df0c9cc2f6c0094e5be75f4f063959f290d81137e463c1f4b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146459861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403f1c1202717e657a3afb32bea3613930169406534f89b7fc204a622540f610`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eaa3c460d109197e8637b1a9599d7f18cccc546e66d1d62f6dd1508e2935dd`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 8.0 MB (7981761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9e960f5f951de003b26390946248f496a1eda867789ae06fd8b18055515450`  
		Last Modified: Tue, 13 Aug 2024 20:49:42 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99bff4ad6d3c4a0683cf02a74f06b61546be2a877da62aece45b0d3b9409871`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 17.0 MB (17049381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74376b78c4a6f5d12921d8dca6dcfa9e9f2bb0917ddeaa5991b98a8c6594581f`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 16.8 MB (16772960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c08f66b4f65a64aaad739c0ac5607c94142e38e67115632af35ef78cff1329c`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 17.2 MB (17182720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce67e83e18f9107f6bbf32d16c48a8f21c28e500a4212c8ebeca7b994936d7e`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c532de2c2cacfe1199219ef497170060946e3a593f771635c84f141b9a3b94c6`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7601c7d4e5af9ac7f6766b064bc79247c0912f3c5d6f3d02bfb58f49c9207`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194e0f500f2ba3365f850eac55a79e52a90ba4922806239f584025ccf347cea5`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 7.0 MB (7034963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9643f136f726def03ee1af9a52d6193e29fb13777be7e5dad5303f10ed36b68`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 98.7 KB (98659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8112d1aa134e43b2e075826bc7ea6a21adf3464ecd3aee260bf8f2947e9d5a50`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9dc9c485b7585bc344ca1a3c332c378d9ee340ecdb8aa344a75df81b017e1`  
		Last Modified: Tue, 13 Aug 2024 22:23:59 GMT  
		Size: 52.4 MB (52384159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7cbf878da555535371cabcf172c560243258cf73e8889885f96fbe66ded9c2`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97e744676fc32c335434d0c4e6890ce0f48ffb37aa99af9568bca483cbfca3f`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4503187f1903453dfdd96e29f2843028e7ab3999269f4e94f7fba03b1754d3`  
		Last Modified: Tue, 13 Aug 2024 23:09:28 GMT  
		Size: 1.0 MB (1023136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e456d8b7e6c45005803d8726755e761e590e47c68a1fb8750c012f4bfb57ef5`  
		Last Modified: Tue, 13 Aug 2024 23:09:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c292ab69c00576a9f271ac96f8d010a8785c5572d03a5efc32e80f2208bbf67d`  
		Last Modified: Tue, 13 Aug 2024 23:09:28 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc26ac4f7d112ba3395f6d5d5b6bd5975e89bb3a1aeccbb6d382cbcbbc757ae`  
		Last Modified: Tue, 13 Aug 2024 23:09:29 GMT  
		Size: 22.8 MB (22835879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570ac36fe23a0443a0db74a04c915f8a2fa16a8185157707d6d94f88a2270973`  
		Last Modified: Tue, 13 Aug 2024 23:09:29 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:83b8fc3691f89e164a3848ca85d5afb6047d2b8c36ee8500361a705a4f238a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544dbc1f438dbe68196bbe42b384836b43013481026eb3482ea165adc58e0331`

```dockerfile
```

-	Layers:
	-	`sha256:fdc4f405dfa87c2c564b75159723ba929dc1a643febd173d3215221105b7936a`  
		Last Modified: Tue, 13 Aug 2024 23:09:27 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.1-windowsservercore`

```console
$ docker pull docker@sha256:e1ded4b3a2aaf5d101daaca1e22004a6c4002e37cdf0842705f51159f0df81ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `docker:27.1-windowsservercore` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:722e8fd401b84665b82e0666308e3852fb7e55ef623784849a0ad1a0fbbfcd28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199540785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57c9795d7276f4ddea53e5745bd047597db78375c979913534c8fdf874a086a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Fri, 16 Aug 2024 21:04:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 21:04:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Aug 2024 21:04:37 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 21:04:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.2.zip
# Fri, 16 Aug 2024 21:04:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:04:49 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 21:04:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Fri, 16 Aug 2024 21:04:50 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Fri, 16 Aug 2024 21:05:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:05:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 21:05:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Fri, 16 Aug 2024 21:05:02 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Fri, 16 Aug 2024 21:05:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e5e515bd55c81feeefd0785d8074f5be7923da2cce4b86409954eafb42a89d`  
		Last Modified: Fri, 16 Aug 2024 21:05:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4236dc1d150b9033a0c12635f2856623e96efcf383d48c97522085f757a77d`  
		Last Modified: Fri, 16 Aug 2024 21:05:21 GMT  
		Size: 374.9 KB (374907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab4df154260eea68dd35cc730282a87fb57915392903c11035c17f519a6c96e`  
		Last Modified: Fri, 16 Aug 2024 21:05:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3677549ffed405f5ae64e6403793e352ecfac2b219c9eedb5028ff32996da03`  
		Last Modified: Fri, 16 Aug 2024 21:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfc19c3fa98906bdc20e8a8400afe4f9b414a7340b21d265dccf34ed27ac257`  
		Last Modified: Fri, 16 Aug 2024 21:05:21 GMT  
		Size: 18.4 MB (18421675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82313e190eab60e8625450d2b286dea76021f5da19bfdebe577415fa461e5c9`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14377702006bc82ef23e61f2b8ed17e316e10b87ba0673db89ec95a79ee87a9`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b0c8b1a15fc09aae430ab9e6a6db5c6f206f1a740c3a1c1b480315148a7f7f`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200e06de81cfb77043b8271865cdff0194d0e6754f636fb258b8a95e941f3ccf`  
		Last Modified: Fri, 16 Aug 2024 21:05:18 GMT  
		Size: 19.3 MB (19265658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ee8b6441d22cc15446aee0d2f0675daead9c2e51dbac7d89edc47d99df8303`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e105068269a03cdc4679d19d4afb6c5a824ffb43ccfbc2430a18e0a80b35554`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c871e44afd26ad9c6e84da90afe24be797cc92c7e5862563a271f080b7d6dc`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a3de421425ac0e051642931e6459b4da6f2f3cd7022114cd5b7811b9eca88e`  
		Last Modified: Fri, 16 Aug 2024 21:05:18 GMT  
		Size: 19.7 MB (19701964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.1-windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:6fc12e3169bfe0a9322c7740f4f4079f8f45dd1b79168c426a89a43ad0c6d9fb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303121283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd6dcd72864533d8de94060162775ef92bd31748712fbcd1f03469008647db8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Fri, 16 Aug 2024 20:59:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 21:00:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Aug 2024 21:00:13 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 21:00:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.2.zip
# Fri, 16 Aug 2024 21:00:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:00:35 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 21:00:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Fri, 16 Aug 2024 21:00:36 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Fri, 16 Aug 2024 21:00:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:00:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 21:00:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Fri, 16 Aug 2024 21:00:57 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Fri, 16 Aug 2024 21:01:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc681518e2d562ce97fc231963b0590c8a4578d640e9226ebc7e7a64072c1c57`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf861a9062e8367fea0bf7fd15b3a23566d429c8f7a698862ed56a6b30e5d08`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 502.8 KB (502826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a6eef9d04b51a84647684d5ac6acc5bbcf56cf1e9a1677f27f0a451d0dc191`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f7463ca73d8038d2384509adeb789ee442a132ab89bd9125fd0d865c0e957c`  
		Last Modified: Fri, 16 Aug 2024 21:01:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1096db739f2668906215c2b312cca48af870253ffbbc08f284d90e88e5d9afd0`  
		Last Modified: Fri, 16 Aug 2024 21:01:23 GMT  
		Size: 18.4 MB (18429168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ba54531e0b5e75e9c6afb0f70803c3f19b3297ba195a9a0f0ed65ac1ed6cbb`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf33926246d70e6dc5eb83affb3e85e5e70ba479cf02633542f105b7c0f9844c`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f26c7e8351ae5c2502dd7735392d69fa658ffb65cb5f1ca900319b9409cf63`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14de9ca87757d524465e1db5e32a8e157bd58a897ed38348289c0293a894bb21`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 19.3 MB (19271416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cca9a181e2403ef565744f377e65fbaeceec043ac17c57026563ab53faa0edc`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61b3946fd8e06fe43f43af8f8d64efafff325bd4e24525b4464c35e4247d30c`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d994d497e123945dca78f465e5d4c09bf3d99d78c717f359cf93b78ed69720e1`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0130b148c08f6100b5c93d2c5de1ddd3a4a69543356d1c729eb4e1f72bded8dd`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 19.7 MB (19702913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.1-windowsservercore-1809`

```console
$ docker pull docker@sha256:89451243e7ee80b1dd7d6e13e80627c63f3775b02426c3284264932fd4002be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `docker:27.1-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:6fc12e3169bfe0a9322c7740f4f4079f8f45dd1b79168c426a89a43ad0c6d9fb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303121283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd6dcd72864533d8de94060162775ef92bd31748712fbcd1f03469008647db8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Fri, 16 Aug 2024 20:59:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 21:00:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Aug 2024 21:00:13 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 21:00:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.2.zip
# Fri, 16 Aug 2024 21:00:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:00:35 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 21:00:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Fri, 16 Aug 2024 21:00:36 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Fri, 16 Aug 2024 21:00:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:00:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 21:00:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Fri, 16 Aug 2024 21:00:57 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Fri, 16 Aug 2024 21:01:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc681518e2d562ce97fc231963b0590c8a4578d640e9226ebc7e7a64072c1c57`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf861a9062e8367fea0bf7fd15b3a23566d429c8f7a698862ed56a6b30e5d08`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 502.8 KB (502826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a6eef9d04b51a84647684d5ac6acc5bbcf56cf1e9a1677f27f0a451d0dc191`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f7463ca73d8038d2384509adeb789ee442a132ab89bd9125fd0d865c0e957c`  
		Last Modified: Fri, 16 Aug 2024 21:01:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1096db739f2668906215c2b312cca48af870253ffbbc08f284d90e88e5d9afd0`  
		Last Modified: Fri, 16 Aug 2024 21:01:23 GMT  
		Size: 18.4 MB (18429168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ba54531e0b5e75e9c6afb0f70803c3f19b3297ba195a9a0f0ed65ac1ed6cbb`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf33926246d70e6dc5eb83affb3e85e5e70ba479cf02633542f105b7c0f9844c`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f26c7e8351ae5c2502dd7735392d69fa658ffb65cb5f1ca900319b9409cf63`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14de9ca87757d524465e1db5e32a8e157bd58a897ed38348289c0293a894bb21`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 19.3 MB (19271416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cca9a181e2403ef565744f377e65fbaeceec043ac17c57026563ab53faa0edc`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61b3946fd8e06fe43f43af8f8d64efafff325bd4e24525b4464c35e4247d30c`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d994d497e123945dca78f465e5d4c09bf3d99d78c717f359cf93b78ed69720e1`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0130b148c08f6100b5c93d2c5de1ddd3a4a69543356d1c729eb4e1f72bded8dd`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 19.7 MB (19702913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:87827cb0d8a93f2c55cd85a9bd673523c38715a87d0257cb18798505f0154212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `docker:27.1-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:722e8fd401b84665b82e0666308e3852fb7e55ef623784849a0ad1a0fbbfcd28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199540785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57c9795d7276f4ddea53e5745bd047597db78375c979913534c8fdf874a086a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Fri, 16 Aug 2024 21:04:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 21:04:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Aug 2024 21:04:37 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 21:04:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.2.zip
# Fri, 16 Aug 2024 21:04:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:04:49 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 21:04:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Fri, 16 Aug 2024 21:04:50 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Fri, 16 Aug 2024 21:05:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:05:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 21:05:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Fri, 16 Aug 2024 21:05:02 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Fri, 16 Aug 2024 21:05:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e5e515bd55c81feeefd0785d8074f5be7923da2cce4b86409954eafb42a89d`  
		Last Modified: Fri, 16 Aug 2024 21:05:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4236dc1d150b9033a0c12635f2856623e96efcf383d48c97522085f757a77d`  
		Last Modified: Fri, 16 Aug 2024 21:05:21 GMT  
		Size: 374.9 KB (374907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab4df154260eea68dd35cc730282a87fb57915392903c11035c17f519a6c96e`  
		Last Modified: Fri, 16 Aug 2024 21:05:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3677549ffed405f5ae64e6403793e352ecfac2b219c9eedb5028ff32996da03`  
		Last Modified: Fri, 16 Aug 2024 21:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfc19c3fa98906bdc20e8a8400afe4f9b414a7340b21d265dccf34ed27ac257`  
		Last Modified: Fri, 16 Aug 2024 21:05:21 GMT  
		Size: 18.4 MB (18421675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82313e190eab60e8625450d2b286dea76021f5da19bfdebe577415fa461e5c9`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14377702006bc82ef23e61f2b8ed17e316e10b87ba0673db89ec95a79ee87a9`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b0c8b1a15fc09aae430ab9e6a6db5c6f206f1a740c3a1c1b480315148a7f7f`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200e06de81cfb77043b8271865cdff0194d0e6754f636fb258b8a95e941f3ccf`  
		Last Modified: Fri, 16 Aug 2024 21:05:18 GMT  
		Size: 19.3 MB (19265658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ee8b6441d22cc15446aee0d2f0675daead9c2e51dbac7d89edc47d99df8303`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e105068269a03cdc4679d19d4afb6c5a824ffb43ccfbc2430a18e0a80b35554`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c871e44afd26ad9c6e84da90afe24be797cc92c7e5862563a271f080b7d6dc`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a3de421425ac0e051642931e6459b4da6f2f3cd7022114cd5b7811b9eca88e`  
		Last Modified: Fri, 16 Aug 2024 21:05:18 GMT  
		Size: 19.7 MB (19701964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.1.2`

```console
$ docker pull docker@sha256:6eb8bfb2c82d454c0248b5dd41b9607f1b76096c06acf985e862f2ea069db33e
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

### `docker:27.1.2` - linux; amd64

```console
$ docker pull docker@sha256:fc81f6680c575a7381f7a586aab4643cdbe79cf9f5af594d2c783a9eb0a0e1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130334773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb13d0c9247298368f97e0637bb60c105cf8159fd29364881b45b5c96c78d621`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97be572a9abc71e039fcf0e5c2cee826693d2e32b5aa28c52ee2e147f29f3ed2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 7.9 MB (7872256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d068c8136df4c77e60b80c6f269c341b11f27187ec77a9ce1a8519f4bdce441f`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3486b9b1692e5ae916e32c2133bb5e8f98a7f89b173cdb303b25d20094e8dee8`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.1 MB (18090913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1726802d7045e092159fdcac73e3c1461690d55c73403cdcdf031ac4145518e2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.4 MB (18404800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1774d2fed741a7a383f92d3969db43a321a4a02dcaad8a886967fb723954fa`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 18.8 MB (18818906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216e3a4876cf4f3c85c70bf9bed6dadfdc58ce83a5537dedb98ea42b20ff36c0`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5bd9a3f910707b7294207b927b3ade09f9d20b66525f2296ee65b90f7edb5`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425c20abf22d4da88ed53e7b1321b6515f33a887063e1f75e25530f7bf89723c`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5174f7db1d0f582b0c6e4a068cb27afd84b66c23716f5046592e2be1b5a225`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 6.7 MB (6657764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fcabf4da4d815f68d521020af7450dc776029613b976a0b4aa8d3429e7d18d`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 89.2 KB (89217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7096f07126cd3b58ec87699d558d9bf0b0b044533ada0f67254d85c94f0bc3b3`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8b74173c6813b97f6d02202faf9a563c7207e298b3204dd4340295344c8ede`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 56.8 MB (56770081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1647c2f9c8092fada70aa9758b7a69f1f3cd05a90891a0a532881cfd598c48`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c41c56a7d8896baa7e32b03546ff50a23492eb9543ed2089ab2fb66ede6ef`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2` - unknown; unknown

```console
$ docker pull docker@sha256:14ec78850163b4e599f6b88fe195725546c45bc30c37ed06f92bd2e7b2f5b392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33683cd4c1538f63f2751b42869d268ec779b0d5fe22d4765e60f56c75e84787`

```dockerfile
```

-	Layers:
	-	`sha256:76c6029aaa7435fba20177df1eb133a9c0a03d8b5c6fe48799e1fe75e360c69f`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1.2` - linux; arm variant v6

```console
$ docker pull docker@sha256:f027111d31885b0ed9642d1b92d7e62b7644b92089eebc5af8a32d7f8bebfc8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122569652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a41929651127c7fdf1f8cfa71354b837597836af87e070e112cbee135c1040`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749d51120dd4449c98cad5624e6a58aaf21f6b57355b1537b1262f69c27968e`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 7.8 MB (7807488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dee64c722233ea05fa0db7774bbb908ccb3860c76b492b90725b4a00faf74a`  
		Last Modified: Tue, 13 Aug 2024 20:03:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aa9bf3b5617e94aa7647537a116937dc7c6d223c96912c2ffc1302ccceab1b`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 16.4 MB (16362863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b4ff9c935b9bea7d6a6f982aab917c1a4fd29032db6ff2a2026ee7f77cc75`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.1 MB (17114711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31fe971362beacbc7fe1ce84a4f59817b327260334951577b2bdc1640d49164`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.8 MB (17776509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7dca5ea08fd6046c223c1378a8259479b60e2b7c9fe45d9ebc3394f237a3c`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 534.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffadf986c05f1d49184514bc67815f318456acc65c0abfd74b2cce1b6d86ecca`  
		Last Modified: Tue, 13 Aug 2024 20:03:15 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7edf55c16e9e482eb8124f38438564758d96aa113c06fd945bcb13988d3fba6`  
		Last Modified: Tue, 13 Aug 2024 20:03:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7dcf38e93a9b47e0f66795e256f2901c2c4bfc37556e81fea2a063cee12eed`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 7.0 MB (6984036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dc040353146061f1f9e8d56420bfefd970c9707a3834a5bcf02701bc7f87a6`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 88.4 KB (88407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af6ea4938ff0c08202d2f8e3f84e00a915d37297b863ed5032cc8f8fa5cd906`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a7459df9025cc27e33a8fecee41b7192346cf1721924cfabec6187dff5186`  
		Last Modified: Tue, 13 Aug 2024 20:57:37 GMT  
		Size: 53.1 MB (53062512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f07f1d6edcfeac2205add2fc7459ea84419349425810e89ef26b86733a587`  
		Last Modified: Tue, 13 Aug 2024 20:57:36 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40b0d4ce5c2e81228c159aa2dcd3e15ecf2f27ee8a41d175c78e599ca4af850`  
		Last Modified: Tue, 13 Aug 2024 20:57:36 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2` - unknown; unknown

```console
$ docker pull docker@sha256:6c057a6e1b62568c5bdee69c9c82240780e3862912fcaa566a3a3487a470fd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a96c343221bdcb48cb74979b02ab5c13b27dbff1a66a0ceb3780e97c736573f`

```dockerfile
```

-	Layers:
	-	`sha256:8cea367fa521297df7cfa3bc63f39bd2b776aa0f558f0427199bc08da2d719d2`  
		Last Modified: Tue, 13 Aug 2024 20:57:34 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1.2` - linux; arm variant v7

```console
$ docker pull docker@sha256:a4332a1e0f1aaa47f76bb148424557761569ddbaa01a4b0733831f22a7e2e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120929654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be199173f5a13331c5558376e7c160c53e51cc77a7f598bbe39233e723dade8b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81dc9168b7d20594a7b5afa567e1b9102c0d289d4b9956af1dd0553da38503f`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 7.1 MB (7143486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b63ca62b0868cd9cbb097a6c34d9eb3a8e551918380dd69db51fbe7459654`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff65173bbd98afd04b6c052172c858476533d0f4873c5b6a81bda0849b5792`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 16.4 MB (16353814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd7e108f551e071a490fb8213c13dccea238c6e5c6ed12be3eef86831d31eb`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 17.1 MB (17103032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b020a8e04eea5428d7645058058bdeea76775ad16c0c306557b00c9b3cce3707`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 17.8 MB (17771143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf51759e8c2b5bc311e671ddc5401fb8b470e266b8553c7d887176c8be0e673`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06151b2e48f60b43b5a3438902d125f5201b35d94f354ac3ac4351ed695565f`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf092fc62ad5de9ceea220ba585b82ea46d65253b23f11533d59f110184e5fe4`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a5e67d714baf4e953669b348ccf67b6156b080a6d6966dc09d0543f0c9be9e`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 6.3 MB (6308261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4b153923b2bef79dd19c29f9b88c045ce4e6e55242b154dbc462faed80d0db`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 84.5 KB (84499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ad462b285298ed7a2323c331255edc0ee999c93e0c8ae4a33c5ce454aeeff4`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67a0efc8d76bc7874505d46a4946de771e37c4eb62166bbec60dcd2a80e68e3`  
		Last Modified: Fri, 16 Aug 2024 21:57:37 GMT  
		Size: 53.1 MB (53062491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bba27c850d08471b57f0404d138486b2a1aed9dd9f3893b3b3def00f165ae25`  
		Last Modified: Fri, 16 Aug 2024 21:57:36 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a63b57aea184aabfabfd30d5a7c8567fe3d95a40b8f831ed764b2193d8bffe7`  
		Last Modified: Fri, 16 Aug 2024 21:57:36 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2` - unknown; unknown

```console
$ docker pull docker@sha256:10c4f8cecc7eb13f9d6d6dc54e1740ab90190e6d24c2e4eec6713b2931912225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a906609c1e200a6b10bedc63efea8af901e9897d1b8f31c4dcb5375222ba63f2`

```dockerfile
```

-	Layers:
	-	`sha256:3e420f6bc3bb35c7528c2f9e8ad122df634ff514d46807261853977ba0eb51f6`  
		Last Modified: Fri, 16 Aug 2024 21:57:34 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1.2` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e739d640aea8812448d7dd39378e23771a2554a182f2099969410db56fa79917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122599486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d8b2b975dd95f7591d28783db8fc5752c99db0ffd5197320cecf290ce39c7f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eaa3c460d109197e8637b1a9599d7f18cccc546e66d1d62f6dd1508e2935dd`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 8.0 MB (7981761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9e960f5f951de003b26390946248f496a1eda867789ae06fd8b18055515450`  
		Last Modified: Tue, 13 Aug 2024 20:49:42 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99bff4ad6d3c4a0683cf02a74f06b61546be2a877da62aece45b0d3b9409871`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 17.0 MB (17049381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74376b78c4a6f5d12921d8dca6dcfa9e9f2bb0917ddeaa5991b98a8c6594581f`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 16.8 MB (16772960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c08f66b4f65a64aaad739c0ac5607c94142e38e67115632af35ef78cff1329c`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 17.2 MB (17182720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce67e83e18f9107f6bbf32d16c48a8f21c28e500a4212c8ebeca7b994936d7e`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c532de2c2cacfe1199219ef497170060946e3a593f771635c84f141b9a3b94c6`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7601c7d4e5af9ac7f6766b064bc79247c0912f3c5d6f3d02bfb58f49c9207`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194e0f500f2ba3365f850eac55a79e52a90ba4922806239f584025ccf347cea5`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 7.0 MB (7034963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9643f136f726def03ee1af9a52d6193e29fb13777be7e5dad5303f10ed36b68`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 98.7 KB (98659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8112d1aa134e43b2e075826bc7ea6a21adf3464ecd3aee260bf8f2947e9d5a50`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9dc9c485b7585bc344ca1a3c332c378d9ee340ecdb8aa344a75df81b017e1`  
		Last Modified: Tue, 13 Aug 2024 22:23:59 GMT  
		Size: 52.4 MB (52384159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7cbf878da555535371cabcf172c560243258cf73e8889885f96fbe66ded9c2`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97e744676fc32c335434d0c4e6890ce0f48ffb37aa99af9568bca483cbfca3f`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2` - unknown; unknown

```console
$ docker pull docker@sha256:f6be705e7230112840619e69b7e6322ce4fc67c5f11c95e929f9e841f1e8403c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43bac9495e2c3ff9a3596159acfb499a4e9f6688d7b379425baf358201b63a1`

```dockerfile
```

-	Layers:
	-	`sha256:9604ca831aeb0d74501b911f9a7b547356be1ae57280b751700fd1d324dfd1ad`  
		Last Modified: Tue, 13 Aug 2024 22:23:56 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.1.2-alpine3.20`

```console
$ docker pull docker@sha256:6eb8bfb2c82d454c0248b5dd41b9607f1b76096c06acf985e862f2ea069db33e
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

### `docker:27.1.2-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:fc81f6680c575a7381f7a586aab4643cdbe79cf9f5af594d2c783a9eb0a0e1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130334773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb13d0c9247298368f97e0637bb60c105cf8159fd29364881b45b5c96c78d621`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97be572a9abc71e039fcf0e5c2cee826693d2e32b5aa28c52ee2e147f29f3ed2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 7.9 MB (7872256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d068c8136df4c77e60b80c6f269c341b11f27187ec77a9ce1a8519f4bdce441f`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3486b9b1692e5ae916e32c2133bb5e8f98a7f89b173cdb303b25d20094e8dee8`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.1 MB (18090913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1726802d7045e092159fdcac73e3c1461690d55c73403cdcdf031ac4145518e2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.4 MB (18404800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1774d2fed741a7a383f92d3969db43a321a4a02dcaad8a886967fb723954fa`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 18.8 MB (18818906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216e3a4876cf4f3c85c70bf9bed6dadfdc58ce83a5537dedb98ea42b20ff36c0`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5bd9a3f910707b7294207b927b3ade09f9d20b66525f2296ee65b90f7edb5`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425c20abf22d4da88ed53e7b1321b6515f33a887063e1f75e25530f7bf89723c`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5174f7db1d0f582b0c6e4a068cb27afd84b66c23716f5046592e2be1b5a225`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 6.7 MB (6657764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fcabf4da4d815f68d521020af7450dc776029613b976a0b4aa8d3429e7d18d`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 89.2 KB (89217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7096f07126cd3b58ec87699d558d9bf0b0b044533ada0f67254d85c94f0bc3b3`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8b74173c6813b97f6d02202faf9a563c7207e298b3204dd4340295344c8ede`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 56.8 MB (56770081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1647c2f9c8092fada70aa9758b7a69f1f3cd05a90891a0a532881cfd598c48`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c41c56a7d8896baa7e32b03546ff50a23492eb9543ed2089ab2fb66ede6ef`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:14ec78850163b4e599f6b88fe195725546c45bc30c37ed06f92bd2e7b2f5b392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33683cd4c1538f63f2751b42869d268ec779b0d5fe22d4765e60f56c75e84787`

```dockerfile
```

-	Layers:
	-	`sha256:76c6029aaa7435fba20177df1eb133a9c0a03d8b5c6fe48799e1fe75e360c69f`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1.2-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:f027111d31885b0ed9642d1b92d7e62b7644b92089eebc5af8a32d7f8bebfc8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122569652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a41929651127c7fdf1f8cfa71354b837597836af87e070e112cbee135c1040`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749d51120dd4449c98cad5624e6a58aaf21f6b57355b1537b1262f69c27968e`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 7.8 MB (7807488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dee64c722233ea05fa0db7774bbb908ccb3860c76b492b90725b4a00faf74a`  
		Last Modified: Tue, 13 Aug 2024 20:03:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aa9bf3b5617e94aa7647537a116937dc7c6d223c96912c2ffc1302ccceab1b`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 16.4 MB (16362863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b4ff9c935b9bea7d6a6f982aab917c1a4fd29032db6ff2a2026ee7f77cc75`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.1 MB (17114711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31fe971362beacbc7fe1ce84a4f59817b327260334951577b2bdc1640d49164`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.8 MB (17776509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7dca5ea08fd6046c223c1378a8259479b60e2b7c9fe45d9ebc3394f237a3c`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 534.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffadf986c05f1d49184514bc67815f318456acc65c0abfd74b2cce1b6d86ecca`  
		Last Modified: Tue, 13 Aug 2024 20:03:15 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7edf55c16e9e482eb8124f38438564758d96aa113c06fd945bcb13988d3fba6`  
		Last Modified: Tue, 13 Aug 2024 20:03:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7dcf38e93a9b47e0f66795e256f2901c2c4bfc37556e81fea2a063cee12eed`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 7.0 MB (6984036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dc040353146061f1f9e8d56420bfefd970c9707a3834a5bcf02701bc7f87a6`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 88.4 KB (88407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af6ea4938ff0c08202d2f8e3f84e00a915d37297b863ed5032cc8f8fa5cd906`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a7459df9025cc27e33a8fecee41b7192346cf1721924cfabec6187dff5186`  
		Last Modified: Tue, 13 Aug 2024 20:57:37 GMT  
		Size: 53.1 MB (53062512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f07f1d6edcfeac2205add2fc7459ea84419349425810e89ef26b86733a587`  
		Last Modified: Tue, 13 Aug 2024 20:57:36 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40b0d4ce5c2e81228c159aa2dcd3e15ecf2f27ee8a41d175c78e599ca4af850`  
		Last Modified: Tue, 13 Aug 2024 20:57:36 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:6c057a6e1b62568c5bdee69c9c82240780e3862912fcaa566a3a3487a470fd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a96c343221bdcb48cb74979b02ab5c13b27dbff1a66a0ceb3780e97c736573f`

```dockerfile
```

-	Layers:
	-	`sha256:8cea367fa521297df7cfa3bc63f39bd2b776aa0f558f0427199bc08da2d719d2`  
		Last Modified: Tue, 13 Aug 2024 20:57:34 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1.2-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:a4332a1e0f1aaa47f76bb148424557761569ddbaa01a4b0733831f22a7e2e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120929654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be199173f5a13331c5558376e7c160c53e51cc77a7f598bbe39233e723dade8b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81dc9168b7d20594a7b5afa567e1b9102c0d289d4b9956af1dd0553da38503f`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 7.1 MB (7143486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b63ca62b0868cd9cbb097a6c34d9eb3a8e551918380dd69db51fbe7459654`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff65173bbd98afd04b6c052172c858476533d0f4873c5b6a81bda0849b5792`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 16.4 MB (16353814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd7e108f551e071a490fb8213c13dccea238c6e5c6ed12be3eef86831d31eb`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 17.1 MB (17103032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b020a8e04eea5428d7645058058bdeea76775ad16c0c306557b00c9b3cce3707`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 17.8 MB (17771143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf51759e8c2b5bc311e671ddc5401fb8b470e266b8553c7d887176c8be0e673`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06151b2e48f60b43b5a3438902d125f5201b35d94f354ac3ac4351ed695565f`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf092fc62ad5de9ceea220ba585b82ea46d65253b23f11533d59f110184e5fe4`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a5e67d714baf4e953669b348ccf67b6156b080a6d6966dc09d0543f0c9be9e`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 6.3 MB (6308261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4b153923b2bef79dd19c29f9b88c045ce4e6e55242b154dbc462faed80d0db`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 84.5 KB (84499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ad462b285298ed7a2323c331255edc0ee999c93e0c8ae4a33c5ce454aeeff4`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67a0efc8d76bc7874505d46a4946de771e37c4eb62166bbec60dcd2a80e68e3`  
		Last Modified: Fri, 16 Aug 2024 21:57:37 GMT  
		Size: 53.1 MB (53062491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bba27c850d08471b57f0404d138486b2a1aed9dd9f3893b3b3def00f165ae25`  
		Last Modified: Fri, 16 Aug 2024 21:57:36 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a63b57aea184aabfabfd30d5a7c8567fe3d95a40b8f831ed764b2193d8bffe7`  
		Last Modified: Fri, 16 Aug 2024 21:57:36 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:10c4f8cecc7eb13f9d6d6dc54e1740ab90190e6d24c2e4eec6713b2931912225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a906609c1e200a6b10bedc63efea8af901e9897d1b8f31c4dcb5375222ba63f2`

```dockerfile
```

-	Layers:
	-	`sha256:3e420f6bc3bb35c7528c2f9e8ad122df634ff514d46807261853977ba0eb51f6`  
		Last Modified: Fri, 16 Aug 2024 21:57:34 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1.2-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e739d640aea8812448d7dd39378e23771a2554a182f2099969410db56fa79917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122599486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d8b2b975dd95f7591d28783db8fc5752c99db0ffd5197320cecf290ce39c7f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eaa3c460d109197e8637b1a9599d7f18cccc546e66d1d62f6dd1508e2935dd`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 8.0 MB (7981761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9e960f5f951de003b26390946248f496a1eda867789ae06fd8b18055515450`  
		Last Modified: Tue, 13 Aug 2024 20:49:42 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99bff4ad6d3c4a0683cf02a74f06b61546be2a877da62aece45b0d3b9409871`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 17.0 MB (17049381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74376b78c4a6f5d12921d8dca6dcfa9e9f2bb0917ddeaa5991b98a8c6594581f`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 16.8 MB (16772960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c08f66b4f65a64aaad739c0ac5607c94142e38e67115632af35ef78cff1329c`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 17.2 MB (17182720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce67e83e18f9107f6bbf32d16c48a8f21c28e500a4212c8ebeca7b994936d7e`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c532de2c2cacfe1199219ef497170060946e3a593f771635c84f141b9a3b94c6`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7601c7d4e5af9ac7f6766b064bc79247c0912f3c5d6f3d02bfb58f49c9207`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194e0f500f2ba3365f850eac55a79e52a90ba4922806239f584025ccf347cea5`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 7.0 MB (7034963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9643f136f726def03ee1af9a52d6193e29fb13777be7e5dad5303f10ed36b68`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 98.7 KB (98659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8112d1aa134e43b2e075826bc7ea6a21adf3464ecd3aee260bf8f2947e9d5a50`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9dc9c485b7585bc344ca1a3c332c378d9ee340ecdb8aa344a75df81b017e1`  
		Last Modified: Tue, 13 Aug 2024 22:23:59 GMT  
		Size: 52.4 MB (52384159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7cbf878da555535371cabcf172c560243258cf73e8889885f96fbe66ded9c2`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97e744676fc32c335434d0c4e6890ce0f48ffb37aa99af9568bca483cbfca3f`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:f6be705e7230112840619e69b7e6322ce4fc67c5f11c95e929f9e841f1e8403c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43bac9495e2c3ff9a3596159acfb499a4e9f6688d7b379425baf358201b63a1`

```dockerfile
```

-	Layers:
	-	`sha256:9604ca831aeb0d74501b911f9a7b547356be1ae57280b751700fd1d324dfd1ad`  
		Last Modified: Tue, 13 Aug 2024 22:23:56 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.1.2-cli`

```console
$ docker pull docker@sha256:c8af17c2e98d13ce5c18d9d31d6e8df47c76d1ba504d2f1782980bb8673af4cb
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

### `docker:27.1.2-cli` - linux; amd64

```console
$ docker pull docker@sha256:444582958ec806c73d40f3702a8a8d84dc2e82feb0d9b44c738fca09ed2820ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66818343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe40c55ae60532fa0075302e6e93e7248c71837afcbd1c56e77b04e256552e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Aug 2024 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b830b3ce3f84ea7067567326d58a3c311c803b3e94cee51732c87abaf0b1644a`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 7.9 MB (7872313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f67cd05487ef47b2034f553790ea2efb816214bef9fd63d5d4f98254167b56e`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201b9999b9284e2bb11f5f0dc6cb35f9f890e8ef84edbd6edbd7f2ea82918c97`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 18.1 MB (18090908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0ed696b310c4d4cd09c07f7566ed6e2baa3f866160967ef06cf205d244859c`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 18.4 MB (18404798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d43008ea7ba356da560c03ab69f55df1d585a289fe0b9e4388f07ff04648932`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 18.8 MB (18825277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5e249d37736904735e2ce24e0bdea2329356683f6cdc14f3b8a7f1f5794c94`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75295f954e5cf281711fb0cb6e50cda9c6305918cc357d63e5347abf36cf48d`  
		Last Modified: Fri, 16 Aug 2024 20:55:55 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f64e86da193d3fea1e01efb5b7a81578e84d4e4593aee8279e9361b9e7e529`  
		Last Modified: Fri, 16 Aug 2024 20:55:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:bf1312c933add91f38029909c3177cd3b9f727efb4e56065fe297c6da6ffb91f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8336e1fddcafee01e26424a9f2c4608561aa729df648622918daaf2a3ef44053`

```dockerfile
```

-	Layers:
	-	`sha256:c16850f73bbeb2eb267302c311cadcadd55959d236b402c255acf9e6a760625f`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1.2-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:ad97551c8ab5f60dc65827a43fb5bfc13375c4128efad7a326a9823e0be68d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62435713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468051ea9e870d4ee592d7253bae1b185cd265c4f3b54f8be9f8b1a820359d3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Aug 2024 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749d51120dd4449c98cad5624e6a58aaf21f6b57355b1537b1262f69c27968e`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 7.8 MB (7807488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dee64c722233ea05fa0db7774bbb908ccb3860c76b492b90725b4a00faf74a`  
		Last Modified: Tue, 13 Aug 2024 20:03:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aa9bf3b5617e94aa7647537a116937dc7c6d223c96912c2ffc1302ccceab1b`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 16.4 MB (16362863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b4ff9c935b9bea7d6a6f982aab917c1a4fd29032db6ff2a2026ee7f77cc75`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.1 MB (17114711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc83f1a40d0c658722d9af33f70561ec5dd29cadd86f625da7bcfa50022733b6`  
		Last Modified: Fri, 16 Aug 2024 20:55:46 GMT  
		Size: 17.8 MB (17783303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5f17b4f1f75fbc81e81b8c4714b51f7829480cd793423fdbe280b4a0e06cdc`  
		Last Modified: Fri, 16 Aug 2024 20:55:45 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d17e0519f279b5dc8f4f4d2233b55fa585e9d0f4e28b2ec38a893f46d415da`  
		Last Modified: Fri, 16 Aug 2024 20:55:45 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ddce9ce1633ca8261319074be47691ef0fa443df2b2fa759364895def2fb50`  
		Last Modified: Fri, 16 Aug 2024 20:55:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:72ac9cedabc23854d5804ef9acc704d8bc5672c4f2f7fa895f0536b433b53c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48dc65f2a968c7f37459c45a1f206fd483248e32a76f9d647ccd35c71bb1a66`

```dockerfile
```

-	Layers:
	-	`sha256:0f0379928ebdda35d5a3de2751c7fb8bf3f92b87ef1bc4445614cadfa4d0042b`  
		Last Modified: Fri, 16 Aug 2024 20:55:45 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1.2-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:cc97a6244b7807809e92b3d720bc2b5f4748fe77f7b1d07f19d033559a0ad00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61468602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509b86a39961f355e5e37e9847693e175944080eae9ea5595e844a7932fe7c06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Aug 2024 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81dc9168b7d20594a7b5afa567e1b9102c0d289d4b9956af1dd0553da38503f`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 7.1 MB (7143486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b63ca62b0868cd9cbb097a6c34d9eb3a8e551918380dd69db51fbe7459654`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff65173bbd98afd04b6c052172c858476533d0f4873c5b6a81bda0849b5792`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 16.4 MB (16353814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd7e108f551e071a490fb8213c13dccea238c6e5c6ed12be3eef86831d31eb`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 17.1 MB (17103032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b020a8e04eea5428d7645058058bdeea76775ad16c0c306557b00c9b3cce3707`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 17.8 MB (17771143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf51759e8c2b5bc311e671ddc5401fb8b470e266b8553c7d887176c8be0e673`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06151b2e48f60b43b5a3438902d125f5201b35d94f354ac3ac4351ed695565f`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf092fc62ad5de9ceea220ba585b82ea46d65253b23f11533d59f110184e5fe4`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f183a263ab8d9b602944b555e29de9642d82e659e768b89ec39b5617024c4c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa7b9ac79beca13b0bc6894266285efc76f1e0853417a57b774ad69e6a882f5`

```dockerfile
```

-	Layers:
	-	`sha256:b2e8085a6ac1eeb458f441d28f5b14e745904be32fb62d75e214c3746c87091e`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1.2-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:173d5a1620cd4c9838d8c6eeaff20a78fbcf08ee2e51c12449f832530e7edbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63080030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c697038997a5fe8ff64a0a9e3a2befe1ab1ffa2dbbce9a6d36ca94614c2e9207`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Aug 2024 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729161d0df240d9ed83f30e35c6fe471b1fae935500748d1ef7da84e664cdb8a`  
		Last Modified: Fri, 16 Aug 2024 20:55:42 GMT  
		Size: 8.0 MB (7981771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b9491762d2e0304f13e86117eb8d95e32f661c882e832b16bee6e8bb9098cb`  
		Last Modified: Fri, 16 Aug 2024 20:55:41 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fdb7ce0e7cf19d21a2bd7c9f95c09245271c0474a184066b1410007b8d4578`  
		Last Modified: Fri, 16 Aug 2024 20:55:42 GMT  
		Size: 17.0 MB (17049378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99813ceebaed11f6388e8ad3c4c1b371512de366ba5488d2f99200a424f074f`  
		Last Modified: Fri, 16 Aug 2024 20:55:42 GMT  
		Size: 16.8 MB (16772960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316a30f1c6a00f4fbfcba19ce9ccb4c2d5709b52e454b56144ec8f67d26208e2`  
		Last Modified: Fri, 16 Aug 2024 20:55:43 GMT  
		Size: 17.2 MB (17186835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0d611bb20624f74153d3ec09ce18870c07860b77939bdf1e019e0740de454a`  
		Last Modified: Fri, 16 Aug 2024 20:55:43 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9b0bb076214cf2f061a5937a293c9b2915ccf6dd121c501471f941589eab06`  
		Last Modified: Fri, 16 Aug 2024 20:55:43 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75f172f02f32a93ea69404964c9c459ce24e0f2cfe1585a6387e076ee96535d`  
		Last Modified: Fri, 16 Aug 2024 20:55:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9fe09d16bdc866f48ca5138929e946de2919fc7472dab2277a4690007a863f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4debb6c6f5e419a67a262e3c2d825765ae2e8b3f71720fbbd0843ead3c73e23`

```dockerfile
```

-	Layers:
	-	`sha256:ee581fd74c551286cbef0f11f61d4110c9e68a8323a697f9a454568d1603785a`  
		Last Modified: Fri, 16 Aug 2024 20:55:41 GMT  
		Size: 38.2 KB (38227 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.1.2-cli-alpine3.20`

```console
$ docker pull docker@sha256:c8af17c2e98d13ce5c18d9d31d6e8df47c76d1ba504d2f1782980bb8673af4cb
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

### `docker:27.1.2-cli-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:444582958ec806c73d40f3702a8a8d84dc2e82feb0d9b44c738fca09ed2820ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66818343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe40c55ae60532fa0075302e6e93e7248c71837afcbd1c56e77b04e256552e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Aug 2024 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b830b3ce3f84ea7067567326d58a3c311c803b3e94cee51732c87abaf0b1644a`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 7.9 MB (7872313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f67cd05487ef47b2034f553790ea2efb816214bef9fd63d5d4f98254167b56e`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201b9999b9284e2bb11f5f0dc6cb35f9f890e8ef84edbd6edbd7f2ea82918c97`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 18.1 MB (18090908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0ed696b310c4d4cd09c07f7566ed6e2baa3f866160967ef06cf205d244859c`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 18.4 MB (18404798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d43008ea7ba356da560c03ab69f55df1d585a289fe0b9e4388f07ff04648932`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 18.8 MB (18825277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5e249d37736904735e2ce24e0bdea2329356683f6cdc14f3b8a7f1f5794c94`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75295f954e5cf281711fb0cb6e50cda9c6305918cc357d63e5347abf36cf48d`  
		Last Modified: Fri, 16 Aug 2024 20:55:55 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f64e86da193d3fea1e01efb5b7a81578e84d4e4593aee8279e9361b9e7e529`  
		Last Modified: Fri, 16 Aug 2024 20:55:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:bf1312c933add91f38029909c3177cd3b9f727efb4e56065fe297c6da6ffb91f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8336e1fddcafee01e26424a9f2c4608561aa729df648622918daaf2a3ef44053`

```dockerfile
```

-	Layers:
	-	`sha256:c16850f73bbeb2eb267302c311cadcadd55959d236b402c255acf9e6a760625f`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1.2-cli-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:ad97551c8ab5f60dc65827a43fb5bfc13375c4128efad7a326a9823e0be68d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62435713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468051ea9e870d4ee592d7253bae1b185cd265c4f3b54f8be9f8b1a820359d3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Aug 2024 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749d51120dd4449c98cad5624e6a58aaf21f6b57355b1537b1262f69c27968e`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 7.8 MB (7807488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dee64c722233ea05fa0db7774bbb908ccb3860c76b492b90725b4a00faf74a`  
		Last Modified: Tue, 13 Aug 2024 20:03:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aa9bf3b5617e94aa7647537a116937dc7c6d223c96912c2ffc1302ccceab1b`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 16.4 MB (16362863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b4ff9c935b9bea7d6a6f982aab917c1a4fd29032db6ff2a2026ee7f77cc75`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.1 MB (17114711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc83f1a40d0c658722d9af33f70561ec5dd29cadd86f625da7bcfa50022733b6`  
		Last Modified: Fri, 16 Aug 2024 20:55:46 GMT  
		Size: 17.8 MB (17783303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5f17b4f1f75fbc81e81b8c4714b51f7829480cd793423fdbe280b4a0e06cdc`  
		Last Modified: Fri, 16 Aug 2024 20:55:45 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d17e0519f279b5dc8f4f4d2233b55fa585e9d0f4e28b2ec38a893f46d415da`  
		Last Modified: Fri, 16 Aug 2024 20:55:45 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ddce9ce1633ca8261319074be47691ef0fa443df2b2fa759364895def2fb50`  
		Last Modified: Fri, 16 Aug 2024 20:55:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:72ac9cedabc23854d5804ef9acc704d8bc5672c4f2f7fa895f0536b433b53c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48dc65f2a968c7f37459c45a1f206fd483248e32a76f9d647ccd35c71bb1a66`

```dockerfile
```

-	Layers:
	-	`sha256:0f0379928ebdda35d5a3de2751c7fb8bf3f92b87ef1bc4445614cadfa4d0042b`  
		Last Modified: Fri, 16 Aug 2024 20:55:45 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1.2-cli-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:cc97a6244b7807809e92b3d720bc2b5f4748fe77f7b1d07f19d033559a0ad00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61468602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509b86a39961f355e5e37e9847693e175944080eae9ea5595e844a7932fe7c06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Aug 2024 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81dc9168b7d20594a7b5afa567e1b9102c0d289d4b9956af1dd0553da38503f`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 7.1 MB (7143486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b63ca62b0868cd9cbb097a6c34d9eb3a8e551918380dd69db51fbe7459654`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff65173bbd98afd04b6c052172c858476533d0f4873c5b6a81bda0849b5792`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 16.4 MB (16353814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd7e108f551e071a490fb8213c13dccea238c6e5c6ed12be3eef86831d31eb`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 17.1 MB (17103032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b020a8e04eea5428d7645058058bdeea76775ad16c0c306557b00c9b3cce3707`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 17.8 MB (17771143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf51759e8c2b5bc311e671ddc5401fb8b470e266b8553c7d887176c8be0e673`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06151b2e48f60b43b5a3438902d125f5201b35d94f354ac3ac4351ed695565f`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf092fc62ad5de9ceea220ba585b82ea46d65253b23f11533d59f110184e5fe4`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:f183a263ab8d9b602944b555e29de9642d82e659e768b89ec39b5617024c4c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa7b9ac79beca13b0bc6894266285efc76f1e0853417a57b774ad69e6a882f5`

```dockerfile
```

-	Layers:
	-	`sha256:b2e8085a6ac1eeb458f441d28f5b14e745904be32fb62d75e214c3746c87091e`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1.2-cli-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:173d5a1620cd4c9838d8c6eeaff20a78fbcf08ee2e51c12449f832530e7edbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63080030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c697038997a5fe8ff64a0a9e3a2befe1ab1ffa2dbbce9a6d36ca94614c2e9207`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Aug 2024 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729161d0df240d9ed83f30e35c6fe471b1fae935500748d1ef7da84e664cdb8a`  
		Last Modified: Fri, 16 Aug 2024 20:55:42 GMT  
		Size: 8.0 MB (7981771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b9491762d2e0304f13e86117eb8d95e32f661c882e832b16bee6e8bb9098cb`  
		Last Modified: Fri, 16 Aug 2024 20:55:41 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fdb7ce0e7cf19d21a2bd7c9f95c09245271c0474a184066b1410007b8d4578`  
		Last Modified: Fri, 16 Aug 2024 20:55:42 GMT  
		Size: 17.0 MB (17049378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99813ceebaed11f6388e8ad3c4c1b371512de366ba5488d2f99200a424f074f`  
		Last Modified: Fri, 16 Aug 2024 20:55:42 GMT  
		Size: 16.8 MB (16772960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316a30f1c6a00f4fbfcba19ce9ccb4c2d5709b52e454b56144ec8f67d26208e2`  
		Last Modified: Fri, 16 Aug 2024 20:55:43 GMT  
		Size: 17.2 MB (17186835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0d611bb20624f74153d3ec09ce18870c07860b77939bdf1e019e0740de454a`  
		Last Modified: Fri, 16 Aug 2024 20:55:43 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9b0bb076214cf2f061a5937a293c9b2915ccf6dd121c501471f941589eab06`  
		Last Modified: Fri, 16 Aug 2024 20:55:43 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75f172f02f32a93ea69404964c9c459ce24e0f2cfe1585a6387e076ee96535d`  
		Last Modified: Fri, 16 Aug 2024 20:55:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:9fe09d16bdc866f48ca5138929e946de2919fc7472dab2277a4690007a863f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4debb6c6f5e419a67a262e3c2d825765ae2e8b3f71720fbbd0843ead3c73e23`

```dockerfile
```

-	Layers:
	-	`sha256:ee581fd74c551286cbef0f11f61d4110c9e68a8323a697f9a454568d1603785a`  
		Last Modified: Fri, 16 Aug 2024 20:55:41 GMT  
		Size: 38.2 KB (38227 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.1.2-dind`

```console
$ docker pull docker@sha256:6eb8bfb2c82d454c0248b5dd41b9607f1b76096c06acf985e862f2ea069db33e
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

### `docker:27.1.2-dind` - linux; amd64

```console
$ docker pull docker@sha256:fc81f6680c575a7381f7a586aab4643cdbe79cf9f5af594d2c783a9eb0a0e1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130334773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb13d0c9247298368f97e0637bb60c105cf8159fd29364881b45b5c96c78d621`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97be572a9abc71e039fcf0e5c2cee826693d2e32b5aa28c52ee2e147f29f3ed2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 7.9 MB (7872256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d068c8136df4c77e60b80c6f269c341b11f27187ec77a9ce1a8519f4bdce441f`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3486b9b1692e5ae916e32c2133bb5e8f98a7f89b173cdb303b25d20094e8dee8`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.1 MB (18090913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1726802d7045e092159fdcac73e3c1461690d55c73403cdcdf031ac4145518e2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.4 MB (18404800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1774d2fed741a7a383f92d3969db43a321a4a02dcaad8a886967fb723954fa`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 18.8 MB (18818906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216e3a4876cf4f3c85c70bf9bed6dadfdc58ce83a5537dedb98ea42b20ff36c0`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5bd9a3f910707b7294207b927b3ade09f9d20b66525f2296ee65b90f7edb5`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425c20abf22d4da88ed53e7b1321b6515f33a887063e1f75e25530f7bf89723c`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5174f7db1d0f582b0c6e4a068cb27afd84b66c23716f5046592e2be1b5a225`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 6.7 MB (6657764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fcabf4da4d815f68d521020af7450dc776029613b976a0b4aa8d3429e7d18d`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 89.2 KB (89217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7096f07126cd3b58ec87699d558d9bf0b0b044533ada0f67254d85c94f0bc3b3`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8b74173c6813b97f6d02202faf9a563c7207e298b3204dd4340295344c8ede`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 56.8 MB (56770081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1647c2f9c8092fada70aa9758b7a69f1f3cd05a90891a0a532881cfd598c48`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c41c56a7d8896baa7e32b03546ff50a23492eb9543ed2089ab2fb66ede6ef`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:14ec78850163b4e599f6b88fe195725546c45bc30c37ed06f92bd2e7b2f5b392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33683cd4c1538f63f2751b42869d268ec779b0d5fe22d4765e60f56c75e84787`

```dockerfile
```

-	Layers:
	-	`sha256:76c6029aaa7435fba20177df1eb133a9c0a03d8b5c6fe48799e1fe75e360c69f`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1.2-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:f027111d31885b0ed9642d1b92d7e62b7644b92089eebc5af8a32d7f8bebfc8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122569652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a41929651127c7fdf1f8cfa71354b837597836af87e070e112cbee135c1040`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749d51120dd4449c98cad5624e6a58aaf21f6b57355b1537b1262f69c27968e`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 7.8 MB (7807488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dee64c722233ea05fa0db7774bbb908ccb3860c76b492b90725b4a00faf74a`  
		Last Modified: Tue, 13 Aug 2024 20:03:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aa9bf3b5617e94aa7647537a116937dc7c6d223c96912c2ffc1302ccceab1b`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 16.4 MB (16362863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b4ff9c935b9bea7d6a6f982aab917c1a4fd29032db6ff2a2026ee7f77cc75`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.1 MB (17114711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31fe971362beacbc7fe1ce84a4f59817b327260334951577b2bdc1640d49164`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.8 MB (17776509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7dca5ea08fd6046c223c1378a8259479b60e2b7c9fe45d9ebc3394f237a3c`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 534.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffadf986c05f1d49184514bc67815f318456acc65c0abfd74b2cce1b6d86ecca`  
		Last Modified: Tue, 13 Aug 2024 20:03:15 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7edf55c16e9e482eb8124f38438564758d96aa113c06fd945bcb13988d3fba6`  
		Last Modified: Tue, 13 Aug 2024 20:03:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7dcf38e93a9b47e0f66795e256f2901c2c4bfc37556e81fea2a063cee12eed`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 7.0 MB (6984036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dc040353146061f1f9e8d56420bfefd970c9707a3834a5bcf02701bc7f87a6`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 88.4 KB (88407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af6ea4938ff0c08202d2f8e3f84e00a915d37297b863ed5032cc8f8fa5cd906`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a7459df9025cc27e33a8fecee41b7192346cf1721924cfabec6187dff5186`  
		Last Modified: Tue, 13 Aug 2024 20:57:37 GMT  
		Size: 53.1 MB (53062512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f07f1d6edcfeac2205add2fc7459ea84419349425810e89ef26b86733a587`  
		Last Modified: Tue, 13 Aug 2024 20:57:36 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40b0d4ce5c2e81228c159aa2dcd3e15ecf2f27ee8a41d175c78e599ca4af850`  
		Last Modified: Tue, 13 Aug 2024 20:57:36 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6c057a6e1b62568c5bdee69c9c82240780e3862912fcaa566a3a3487a470fd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a96c343221bdcb48cb74979b02ab5c13b27dbff1a66a0ceb3780e97c736573f`

```dockerfile
```

-	Layers:
	-	`sha256:8cea367fa521297df7cfa3bc63f39bd2b776aa0f558f0427199bc08da2d719d2`  
		Last Modified: Tue, 13 Aug 2024 20:57:34 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1.2-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:a4332a1e0f1aaa47f76bb148424557761569ddbaa01a4b0733831f22a7e2e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120929654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be199173f5a13331c5558376e7c160c53e51cc77a7f598bbe39233e723dade8b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81dc9168b7d20594a7b5afa567e1b9102c0d289d4b9956af1dd0553da38503f`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 7.1 MB (7143486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b63ca62b0868cd9cbb097a6c34d9eb3a8e551918380dd69db51fbe7459654`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff65173bbd98afd04b6c052172c858476533d0f4873c5b6a81bda0849b5792`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 16.4 MB (16353814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd7e108f551e071a490fb8213c13dccea238c6e5c6ed12be3eef86831d31eb`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 17.1 MB (17103032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b020a8e04eea5428d7645058058bdeea76775ad16c0c306557b00c9b3cce3707`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 17.8 MB (17771143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf51759e8c2b5bc311e671ddc5401fb8b470e266b8553c7d887176c8be0e673`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06151b2e48f60b43b5a3438902d125f5201b35d94f354ac3ac4351ed695565f`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf092fc62ad5de9ceea220ba585b82ea46d65253b23f11533d59f110184e5fe4`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a5e67d714baf4e953669b348ccf67b6156b080a6d6966dc09d0543f0c9be9e`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 6.3 MB (6308261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4b153923b2bef79dd19c29f9b88c045ce4e6e55242b154dbc462faed80d0db`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 84.5 KB (84499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ad462b285298ed7a2323c331255edc0ee999c93e0c8ae4a33c5ce454aeeff4`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67a0efc8d76bc7874505d46a4946de771e37c4eb62166bbec60dcd2a80e68e3`  
		Last Modified: Fri, 16 Aug 2024 21:57:37 GMT  
		Size: 53.1 MB (53062491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bba27c850d08471b57f0404d138486b2a1aed9dd9f3893b3b3def00f165ae25`  
		Last Modified: Fri, 16 Aug 2024 21:57:36 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a63b57aea184aabfabfd30d5a7c8567fe3d95a40b8f831ed764b2193d8bffe7`  
		Last Modified: Fri, 16 Aug 2024 21:57:36 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:10c4f8cecc7eb13f9d6d6dc54e1740ab90190e6d24c2e4eec6713b2931912225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a906609c1e200a6b10bedc63efea8af901e9897d1b8f31c4dcb5375222ba63f2`

```dockerfile
```

-	Layers:
	-	`sha256:3e420f6bc3bb35c7528c2f9e8ad122df634ff514d46807261853977ba0eb51f6`  
		Last Modified: Fri, 16 Aug 2024 21:57:34 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1.2-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e739d640aea8812448d7dd39378e23771a2554a182f2099969410db56fa79917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122599486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d8b2b975dd95f7591d28783db8fc5752c99db0ffd5197320cecf290ce39c7f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eaa3c460d109197e8637b1a9599d7f18cccc546e66d1d62f6dd1508e2935dd`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 8.0 MB (7981761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9e960f5f951de003b26390946248f496a1eda867789ae06fd8b18055515450`  
		Last Modified: Tue, 13 Aug 2024 20:49:42 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99bff4ad6d3c4a0683cf02a74f06b61546be2a877da62aece45b0d3b9409871`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 17.0 MB (17049381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74376b78c4a6f5d12921d8dca6dcfa9e9f2bb0917ddeaa5991b98a8c6594581f`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 16.8 MB (16772960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c08f66b4f65a64aaad739c0ac5607c94142e38e67115632af35ef78cff1329c`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 17.2 MB (17182720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce67e83e18f9107f6bbf32d16c48a8f21c28e500a4212c8ebeca7b994936d7e`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c532de2c2cacfe1199219ef497170060946e3a593f771635c84f141b9a3b94c6`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7601c7d4e5af9ac7f6766b064bc79247c0912f3c5d6f3d02bfb58f49c9207`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194e0f500f2ba3365f850eac55a79e52a90ba4922806239f584025ccf347cea5`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 7.0 MB (7034963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9643f136f726def03ee1af9a52d6193e29fb13777be7e5dad5303f10ed36b68`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 98.7 KB (98659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8112d1aa134e43b2e075826bc7ea6a21adf3464ecd3aee260bf8f2947e9d5a50`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9dc9c485b7585bc344ca1a3c332c378d9ee340ecdb8aa344a75df81b017e1`  
		Last Modified: Tue, 13 Aug 2024 22:23:59 GMT  
		Size: 52.4 MB (52384159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7cbf878da555535371cabcf172c560243258cf73e8889885f96fbe66ded9c2`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97e744676fc32c335434d0c4e6890ce0f48ffb37aa99af9568bca483cbfca3f`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f6be705e7230112840619e69b7e6322ce4fc67c5f11c95e929f9e841f1e8403c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43bac9495e2c3ff9a3596159acfb499a4e9f6688d7b379425baf358201b63a1`

```dockerfile
```

-	Layers:
	-	`sha256:9604ca831aeb0d74501b911f9a7b547356be1ae57280b751700fd1d324dfd1ad`  
		Last Modified: Tue, 13 Aug 2024 22:23:56 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.1.2-dind-alpine3.20`

```console
$ docker pull docker@sha256:6eb8bfb2c82d454c0248b5dd41b9607f1b76096c06acf985e862f2ea069db33e
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

### `docker:27.1.2-dind-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:fc81f6680c575a7381f7a586aab4643cdbe79cf9f5af594d2c783a9eb0a0e1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130334773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb13d0c9247298368f97e0637bb60c105cf8159fd29364881b45b5c96c78d621`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97be572a9abc71e039fcf0e5c2cee826693d2e32b5aa28c52ee2e147f29f3ed2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 7.9 MB (7872256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d068c8136df4c77e60b80c6f269c341b11f27187ec77a9ce1a8519f4bdce441f`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3486b9b1692e5ae916e32c2133bb5e8f98a7f89b173cdb303b25d20094e8dee8`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.1 MB (18090913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1726802d7045e092159fdcac73e3c1461690d55c73403cdcdf031ac4145518e2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.4 MB (18404800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1774d2fed741a7a383f92d3969db43a321a4a02dcaad8a886967fb723954fa`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 18.8 MB (18818906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216e3a4876cf4f3c85c70bf9bed6dadfdc58ce83a5537dedb98ea42b20ff36c0`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5bd9a3f910707b7294207b927b3ade09f9d20b66525f2296ee65b90f7edb5`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425c20abf22d4da88ed53e7b1321b6515f33a887063e1f75e25530f7bf89723c`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5174f7db1d0f582b0c6e4a068cb27afd84b66c23716f5046592e2be1b5a225`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 6.7 MB (6657764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fcabf4da4d815f68d521020af7450dc776029613b976a0b4aa8d3429e7d18d`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 89.2 KB (89217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7096f07126cd3b58ec87699d558d9bf0b0b044533ada0f67254d85c94f0bc3b3`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8b74173c6813b97f6d02202faf9a563c7207e298b3204dd4340295344c8ede`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 56.8 MB (56770081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1647c2f9c8092fada70aa9758b7a69f1f3cd05a90891a0a532881cfd598c48`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c41c56a7d8896baa7e32b03546ff50a23492eb9543ed2089ab2fb66ede6ef`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:14ec78850163b4e599f6b88fe195725546c45bc30c37ed06f92bd2e7b2f5b392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33683cd4c1538f63f2751b42869d268ec779b0d5fe22d4765e60f56c75e84787`

```dockerfile
```

-	Layers:
	-	`sha256:76c6029aaa7435fba20177df1eb133a9c0a03d8b5c6fe48799e1fe75e360c69f`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1.2-dind-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:f027111d31885b0ed9642d1b92d7e62b7644b92089eebc5af8a32d7f8bebfc8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122569652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a41929651127c7fdf1f8cfa71354b837597836af87e070e112cbee135c1040`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749d51120dd4449c98cad5624e6a58aaf21f6b57355b1537b1262f69c27968e`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 7.8 MB (7807488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dee64c722233ea05fa0db7774bbb908ccb3860c76b492b90725b4a00faf74a`  
		Last Modified: Tue, 13 Aug 2024 20:03:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aa9bf3b5617e94aa7647537a116937dc7c6d223c96912c2ffc1302ccceab1b`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 16.4 MB (16362863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b4ff9c935b9bea7d6a6f982aab917c1a4fd29032db6ff2a2026ee7f77cc75`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.1 MB (17114711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31fe971362beacbc7fe1ce84a4f59817b327260334951577b2bdc1640d49164`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.8 MB (17776509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7dca5ea08fd6046c223c1378a8259479b60e2b7c9fe45d9ebc3394f237a3c`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 534.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffadf986c05f1d49184514bc67815f318456acc65c0abfd74b2cce1b6d86ecca`  
		Last Modified: Tue, 13 Aug 2024 20:03:15 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7edf55c16e9e482eb8124f38438564758d96aa113c06fd945bcb13988d3fba6`  
		Last Modified: Tue, 13 Aug 2024 20:03:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7dcf38e93a9b47e0f66795e256f2901c2c4bfc37556e81fea2a063cee12eed`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 7.0 MB (6984036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dc040353146061f1f9e8d56420bfefd970c9707a3834a5bcf02701bc7f87a6`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 88.4 KB (88407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af6ea4938ff0c08202d2f8e3f84e00a915d37297b863ed5032cc8f8fa5cd906`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a7459df9025cc27e33a8fecee41b7192346cf1721924cfabec6187dff5186`  
		Last Modified: Tue, 13 Aug 2024 20:57:37 GMT  
		Size: 53.1 MB (53062512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f07f1d6edcfeac2205add2fc7459ea84419349425810e89ef26b86733a587`  
		Last Modified: Tue, 13 Aug 2024 20:57:36 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40b0d4ce5c2e81228c159aa2dcd3e15ecf2f27ee8a41d175c78e599ca4af850`  
		Last Modified: Tue, 13 Aug 2024 20:57:36 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:6c057a6e1b62568c5bdee69c9c82240780e3862912fcaa566a3a3487a470fd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a96c343221bdcb48cb74979b02ab5c13b27dbff1a66a0ceb3780e97c736573f`

```dockerfile
```

-	Layers:
	-	`sha256:8cea367fa521297df7cfa3bc63f39bd2b776aa0f558f0427199bc08da2d719d2`  
		Last Modified: Tue, 13 Aug 2024 20:57:34 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1.2-dind-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:a4332a1e0f1aaa47f76bb148424557761569ddbaa01a4b0733831f22a7e2e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120929654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be199173f5a13331c5558376e7c160c53e51cc77a7f598bbe39233e723dade8b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81dc9168b7d20594a7b5afa567e1b9102c0d289d4b9956af1dd0553da38503f`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 7.1 MB (7143486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b63ca62b0868cd9cbb097a6c34d9eb3a8e551918380dd69db51fbe7459654`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff65173bbd98afd04b6c052172c858476533d0f4873c5b6a81bda0849b5792`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 16.4 MB (16353814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd7e108f551e071a490fb8213c13dccea238c6e5c6ed12be3eef86831d31eb`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 17.1 MB (17103032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b020a8e04eea5428d7645058058bdeea76775ad16c0c306557b00c9b3cce3707`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 17.8 MB (17771143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf51759e8c2b5bc311e671ddc5401fb8b470e266b8553c7d887176c8be0e673`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06151b2e48f60b43b5a3438902d125f5201b35d94f354ac3ac4351ed695565f`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf092fc62ad5de9ceea220ba585b82ea46d65253b23f11533d59f110184e5fe4`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a5e67d714baf4e953669b348ccf67b6156b080a6d6966dc09d0543f0c9be9e`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 6.3 MB (6308261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4b153923b2bef79dd19c29f9b88c045ce4e6e55242b154dbc462faed80d0db`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 84.5 KB (84499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ad462b285298ed7a2323c331255edc0ee999c93e0c8ae4a33c5ce454aeeff4`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67a0efc8d76bc7874505d46a4946de771e37c4eb62166bbec60dcd2a80e68e3`  
		Last Modified: Fri, 16 Aug 2024 21:57:37 GMT  
		Size: 53.1 MB (53062491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bba27c850d08471b57f0404d138486b2a1aed9dd9f3893b3b3def00f165ae25`  
		Last Modified: Fri, 16 Aug 2024 21:57:36 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a63b57aea184aabfabfd30d5a7c8567fe3d95a40b8f831ed764b2193d8bffe7`  
		Last Modified: Fri, 16 Aug 2024 21:57:36 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:10c4f8cecc7eb13f9d6d6dc54e1740ab90190e6d24c2e4eec6713b2931912225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a906609c1e200a6b10bedc63efea8af901e9897d1b8f31c4dcb5375222ba63f2`

```dockerfile
```

-	Layers:
	-	`sha256:3e420f6bc3bb35c7528c2f9e8ad122df634ff514d46807261853977ba0eb51f6`  
		Last Modified: Fri, 16 Aug 2024 21:57:34 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1.2-dind-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e739d640aea8812448d7dd39378e23771a2554a182f2099969410db56fa79917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122599486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d8b2b975dd95f7591d28783db8fc5752c99db0ffd5197320cecf290ce39c7f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eaa3c460d109197e8637b1a9599d7f18cccc546e66d1d62f6dd1508e2935dd`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 8.0 MB (7981761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9e960f5f951de003b26390946248f496a1eda867789ae06fd8b18055515450`  
		Last Modified: Tue, 13 Aug 2024 20:49:42 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99bff4ad6d3c4a0683cf02a74f06b61546be2a877da62aece45b0d3b9409871`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 17.0 MB (17049381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74376b78c4a6f5d12921d8dca6dcfa9e9f2bb0917ddeaa5991b98a8c6594581f`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 16.8 MB (16772960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c08f66b4f65a64aaad739c0ac5607c94142e38e67115632af35ef78cff1329c`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 17.2 MB (17182720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce67e83e18f9107f6bbf32d16c48a8f21c28e500a4212c8ebeca7b994936d7e`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c532de2c2cacfe1199219ef497170060946e3a593f771635c84f141b9a3b94c6`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7601c7d4e5af9ac7f6766b064bc79247c0912f3c5d6f3d02bfb58f49c9207`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194e0f500f2ba3365f850eac55a79e52a90ba4922806239f584025ccf347cea5`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 7.0 MB (7034963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9643f136f726def03ee1af9a52d6193e29fb13777be7e5dad5303f10ed36b68`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 98.7 KB (98659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8112d1aa134e43b2e075826bc7ea6a21adf3464ecd3aee260bf8f2947e9d5a50`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9dc9c485b7585bc344ca1a3c332c378d9ee340ecdb8aa344a75df81b017e1`  
		Last Modified: Tue, 13 Aug 2024 22:23:59 GMT  
		Size: 52.4 MB (52384159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7cbf878da555535371cabcf172c560243258cf73e8889885f96fbe66ded9c2`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97e744676fc32c335434d0c4e6890ce0f48ffb37aa99af9568bca483cbfca3f`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:f6be705e7230112840619e69b7e6322ce4fc67c5f11c95e929f9e841f1e8403c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43bac9495e2c3ff9a3596159acfb499a4e9f6688d7b379425baf358201b63a1`

```dockerfile
```

-	Layers:
	-	`sha256:9604ca831aeb0d74501b911f9a7b547356be1ae57280b751700fd1d324dfd1ad`  
		Last Modified: Tue, 13 Aug 2024 22:23:56 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.1.2-dind-rootless`

```console
$ docker pull docker@sha256:af47f6c5401fa4d78609555d2c4b9babfe237af534c7b07ff2b036a0d427a118
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.1.2-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:1c4b1d49cece4db7e2dcaebda47131381ee475d375613c0ad913dd384ee2cba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.3 MB (152296869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa93fbe161d9efbaa4c0e48ceab0e109620689af00487864f7130a6ec89b8a4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97be572a9abc71e039fcf0e5c2cee826693d2e32b5aa28c52ee2e147f29f3ed2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 7.9 MB (7872256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d068c8136df4c77e60b80c6f269c341b11f27187ec77a9ce1a8519f4bdce441f`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3486b9b1692e5ae916e32c2133bb5e8f98a7f89b173cdb303b25d20094e8dee8`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.1 MB (18090913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1726802d7045e092159fdcac73e3c1461690d55c73403cdcdf031ac4145518e2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.4 MB (18404800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1774d2fed741a7a383f92d3969db43a321a4a02dcaad8a886967fb723954fa`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 18.8 MB (18818906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216e3a4876cf4f3c85c70bf9bed6dadfdc58ce83a5537dedb98ea42b20ff36c0`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5bd9a3f910707b7294207b927b3ade09f9d20b66525f2296ee65b90f7edb5`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425c20abf22d4da88ed53e7b1321b6515f33a887063e1f75e25530f7bf89723c`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5174f7db1d0f582b0c6e4a068cb27afd84b66c23716f5046592e2be1b5a225`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 6.7 MB (6657764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fcabf4da4d815f68d521020af7450dc776029613b976a0b4aa8d3429e7d18d`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 89.2 KB (89217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7096f07126cd3b58ec87699d558d9bf0b0b044533ada0f67254d85c94f0bc3b3`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8b74173c6813b97f6d02202faf9a563c7207e298b3204dd4340295344c8ede`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 56.8 MB (56770081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1647c2f9c8092fada70aa9758b7a69f1f3cd05a90891a0a532881cfd598c48`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c41c56a7d8896baa7e32b03546ff50a23492eb9543ed2089ab2fb66ede6ef`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddff6840fdc9aeb42249c80b9c338fe603cc5f0b00252bf16b8bdf2a5fb2f8c`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 981.0 KB (980992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a02b3fadcd722d124529c5401debc307f981a90fc96d45d5d92b96f0dd7545`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c5873bde466cc998bafb56445a5cb01a1a2f54f4166b40ae385bea47531624`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fda618391a49e503c15787e90efea8390d3e23e0621ef57525f337c23de9b6`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 21.0 MB (20979748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08614a56f1a4c3bbf5ebad13045c832079e403dcebb54554e52d5abcdb3b436`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:e63fe7c3704aa2dcc99fb485a4c317a39cb9c1b4d21542ab08c4c4f80a9fc923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23246a0ef23fd48a00bdc4420f83bb303595779eef9540a6b307ca752627e8f3`

```dockerfile
```

-	Layers:
	-	`sha256:030786d4fe7aad28fd3146cfcd96aebaf0140ae35626e5c6bdb622099b291852`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 30.6 KB (30580 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.1.2-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:40aed2a21da30df0c9cc2f6c0094e5be75f4f063959f290d81137e463c1f4b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146459861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403f1c1202717e657a3afb32bea3613930169406534f89b7fc204a622540f610`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eaa3c460d109197e8637b1a9599d7f18cccc546e66d1d62f6dd1508e2935dd`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 8.0 MB (7981761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9e960f5f951de003b26390946248f496a1eda867789ae06fd8b18055515450`  
		Last Modified: Tue, 13 Aug 2024 20:49:42 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99bff4ad6d3c4a0683cf02a74f06b61546be2a877da62aece45b0d3b9409871`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 17.0 MB (17049381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74376b78c4a6f5d12921d8dca6dcfa9e9f2bb0917ddeaa5991b98a8c6594581f`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 16.8 MB (16772960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c08f66b4f65a64aaad739c0ac5607c94142e38e67115632af35ef78cff1329c`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 17.2 MB (17182720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce67e83e18f9107f6bbf32d16c48a8f21c28e500a4212c8ebeca7b994936d7e`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c532de2c2cacfe1199219ef497170060946e3a593f771635c84f141b9a3b94c6`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7601c7d4e5af9ac7f6766b064bc79247c0912f3c5d6f3d02bfb58f49c9207`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194e0f500f2ba3365f850eac55a79e52a90ba4922806239f584025ccf347cea5`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 7.0 MB (7034963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9643f136f726def03ee1af9a52d6193e29fb13777be7e5dad5303f10ed36b68`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 98.7 KB (98659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8112d1aa134e43b2e075826bc7ea6a21adf3464ecd3aee260bf8f2947e9d5a50`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9dc9c485b7585bc344ca1a3c332c378d9ee340ecdb8aa344a75df81b017e1`  
		Last Modified: Tue, 13 Aug 2024 22:23:59 GMT  
		Size: 52.4 MB (52384159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7cbf878da555535371cabcf172c560243258cf73e8889885f96fbe66ded9c2`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97e744676fc32c335434d0c4e6890ce0f48ffb37aa99af9568bca483cbfca3f`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4503187f1903453dfdd96e29f2843028e7ab3999269f4e94f7fba03b1754d3`  
		Last Modified: Tue, 13 Aug 2024 23:09:28 GMT  
		Size: 1.0 MB (1023136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e456d8b7e6c45005803d8726755e761e590e47c68a1fb8750c012f4bfb57ef5`  
		Last Modified: Tue, 13 Aug 2024 23:09:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c292ab69c00576a9f271ac96f8d010a8785c5572d03a5efc32e80f2208bbf67d`  
		Last Modified: Tue, 13 Aug 2024 23:09:28 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc26ac4f7d112ba3395f6d5d5b6bd5975e89bb3a1aeccbb6d382cbcbbc757ae`  
		Last Modified: Tue, 13 Aug 2024 23:09:29 GMT  
		Size: 22.8 MB (22835879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570ac36fe23a0443a0db74a04c915f8a2fa16a8185157707d6d94f88a2270973`  
		Last Modified: Tue, 13 Aug 2024 23:09:29 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.1.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:83b8fc3691f89e164a3848ca85d5afb6047d2b8c36ee8500361a705a4f238a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544dbc1f438dbe68196bbe42b384836b43013481026eb3482ea165adc58e0331`

```dockerfile
```

-	Layers:
	-	`sha256:fdc4f405dfa87c2c564b75159723ba929dc1a643febd173d3215221105b7936a`  
		Last Modified: Tue, 13 Aug 2024 23:09:27 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.1.2-windowsservercore`

```console
$ docker pull docker@sha256:e1ded4b3a2aaf5d101daaca1e22004a6c4002e37cdf0842705f51159f0df81ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `docker:27.1.2-windowsservercore` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:722e8fd401b84665b82e0666308e3852fb7e55ef623784849a0ad1a0fbbfcd28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199540785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57c9795d7276f4ddea53e5745bd047597db78375c979913534c8fdf874a086a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Fri, 16 Aug 2024 21:04:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 21:04:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Aug 2024 21:04:37 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 21:04:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.2.zip
# Fri, 16 Aug 2024 21:04:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:04:49 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 21:04:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Fri, 16 Aug 2024 21:04:50 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Fri, 16 Aug 2024 21:05:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:05:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 21:05:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Fri, 16 Aug 2024 21:05:02 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Fri, 16 Aug 2024 21:05:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e5e515bd55c81feeefd0785d8074f5be7923da2cce4b86409954eafb42a89d`  
		Last Modified: Fri, 16 Aug 2024 21:05:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4236dc1d150b9033a0c12635f2856623e96efcf383d48c97522085f757a77d`  
		Last Modified: Fri, 16 Aug 2024 21:05:21 GMT  
		Size: 374.9 KB (374907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab4df154260eea68dd35cc730282a87fb57915392903c11035c17f519a6c96e`  
		Last Modified: Fri, 16 Aug 2024 21:05:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3677549ffed405f5ae64e6403793e352ecfac2b219c9eedb5028ff32996da03`  
		Last Modified: Fri, 16 Aug 2024 21:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfc19c3fa98906bdc20e8a8400afe4f9b414a7340b21d265dccf34ed27ac257`  
		Last Modified: Fri, 16 Aug 2024 21:05:21 GMT  
		Size: 18.4 MB (18421675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82313e190eab60e8625450d2b286dea76021f5da19bfdebe577415fa461e5c9`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14377702006bc82ef23e61f2b8ed17e316e10b87ba0673db89ec95a79ee87a9`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b0c8b1a15fc09aae430ab9e6a6db5c6f206f1a740c3a1c1b480315148a7f7f`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200e06de81cfb77043b8271865cdff0194d0e6754f636fb258b8a95e941f3ccf`  
		Last Modified: Fri, 16 Aug 2024 21:05:18 GMT  
		Size: 19.3 MB (19265658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ee8b6441d22cc15446aee0d2f0675daead9c2e51dbac7d89edc47d99df8303`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e105068269a03cdc4679d19d4afb6c5a824ffb43ccfbc2430a18e0a80b35554`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c871e44afd26ad9c6e84da90afe24be797cc92c7e5862563a271f080b7d6dc`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a3de421425ac0e051642931e6459b4da6f2f3cd7022114cd5b7811b9eca88e`  
		Last Modified: Fri, 16 Aug 2024 21:05:18 GMT  
		Size: 19.7 MB (19701964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.1.2-windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:6fc12e3169bfe0a9322c7740f4f4079f8f45dd1b79168c426a89a43ad0c6d9fb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303121283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd6dcd72864533d8de94060162775ef92bd31748712fbcd1f03469008647db8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Fri, 16 Aug 2024 20:59:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 21:00:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Aug 2024 21:00:13 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 21:00:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.2.zip
# Fri, 16 Aug 2024 21:00:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:00:35 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 21:00:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Fri, 16 Aug 2024 21:00:36 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Fri, 16 Aug 2024 21:00:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:00:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 21:00:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Fri, 16 Aug 2024 21:00:57 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Fri, 16 Aug 2024 21:01:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc681518e2d562ce97fc231963b0590c8a4578d640e9226ebc7e7a64072c1c57`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf861a9062e8367fea0bf7fd15b3a23566d429c8f7a698862ed56a6b30e5d08`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 502.8 KB (502826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a6eef9d04b51a84647684d5ac6acc5bbcf56cf1e9a1677f27f0a451d0dc191`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f7463ca73d8038d2384509adeb789ee442a132ab89bd9125fd0d865c0e957c`  
		Last Modified: Fri, 16 Aug 2024 21:01:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1096db739f2668906215c2b312cca48af870253ffbbc08f284d90e88e5d9afd0`  
		Last Modified: Fri, 16 Aug 2024 21:01:23 GMT  
		Size: 18.4 MB (18429168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ba54531e0b5e75e9c6afb0f70803c3f19b3297ba195a9a0f0ed65ac1ed6cbb`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf33926246d70e6dc5eb83affb3e85e5e70ba479cf02633542f105b7c0f9844c`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f26c7e8351ae5c2502dd7735392d69fa658ffb65cb5f1ca900319b9409cf63`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14de9ca87757d524465e1db5e32a8e157bd58a897ed38348289c0293a894bb21`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 19.3 MB (19271416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cca9a181e2403ef565744f377e65fbaeceec043ac17c57026563ab53faa0edc`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61b3946fd8e06fe43f43af8f8d64efafff325bd4e24525b4464c35e4247d30c`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d994d497e123945dca78f465e5d4c09bf3d99d78c717f359cf93b78ed69720e1`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0130b148c08f6100b5c93d2c5de1ddd3a4a69543356d1c729eb4e1f72bded8dd`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 19.7 MB (19702913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.1.2-windowsservercore-1809`

```console
$ docker pull docker@sha256:89451243e7ee80b1dd7d6e13e80627c63f3775b02426c3284264932fd4002be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `docker:27.1.2-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:6fc12e3169bfe0a9322c7740f4f4079f8f45dd1b79168c426a89a43ad0c6d9fb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303121283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd6dcd72864533d8de94060162775ef92bd31748712fbcd1f03469008647db8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Fri, 16 Aug 2024 20:59:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 21:00:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Aug 2024 21:00:13 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 21:00:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.2.zip
# Fri, 16 Aug 2024 21:00:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:00:35 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 21:00:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Fri, 16 Aug 2024 21:00:36 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Fri, 16 Aug 2024 21:00:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:00:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 21:00:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Fri, 16 Aug 2024 21:00:57 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Fri, 16 Aug 2024 21:01:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc681518e2d562ce97fc231963b0590c8a4578d640e9226ebc7e7a64072c1c57`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf861a9062e8367fea0bf7fd15b3a23566d429c8f7a698862ed56a6b30e5d08`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 502.8 KB (502826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a6eef9d04b51a84647684d5ac6acc5bbcf56cf1e9a1677f27f0a451d0dc191`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f7463ca73d8038d2384509adeb789ee442a132ab89bd9125fd0d865c0e957c`  
		Last Modified: Fri, 16 Aug 2024 21:01:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1096db739f2668906215c2b312cca48af870253ffbbc08f284d90e88e5d9afd0`  
		Last Modified: Fri, 16 Aug 2024 21:01:23 GMT  
		Size: 18.4 MB (18429168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ba54531e0b5e75e9c6afb0f70803c3f19b3297ba195a9a0f0ed65ac1ed6cbb`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf33926246d70e6dc5eb83affb3e85e5e70ba479cf02633542f105b7c0f9844c`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f26c7e8351ae5c2502dd7735392d69fa658ffb65cb5f1ca900319b9409cf63`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14de9ca87757d524465e1db5e32a8e157bd58a897ed38348289c0293a894bb21`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 19.3 MB (19271416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cca9a181e2403ef565744f377e65fbaeceec043ac17c57026563ab53faa0edc`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61b3946fd8e06fe43f43af8f8d64efafff325bd4e24525b4464c35e4247d30c`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d994d497e123945dca78f465e5d4c09bf3d99d78c717f359cf93b78ed69720e1`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0130b148c08f6100b5c93d2c5de1ddd3a4a69543356d1c729eb4e1f72bded8dd`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 19.7 MB (19702913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.1.2-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:87827cb0d8a93f2c55cd85a9bd673523c38715a87d0257cb18798505f0154212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `docker:27.1.2-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:722e8fd401b84665b82e0666308e3852fb7e55ef623784849a0ad1a0fbbfcd28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199540785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57c9795d7276f4ddea53e5745bd047597db78375c979913534c8fdf874a086a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Fri, 16 Aug 2024 21:04:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 21:04:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Aug 2024 21:04:37 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 21:04:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.2.zip
# Fri, 16 Aug 2024 21:04:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:04:49 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 21:04:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Fri, 16 Aug 2024 21:04:50 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Fri, 16 Aug 2024 21:05:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:05:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 21:05:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Fri, 16 Aug 2024 21:05:02 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Fri, 16 Aug 2024 21:05:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e5e515bd55c81feeefd0785d8074f5be7923da2cce4b86409954eafb42a89d`  
		Last Modified: Fri, 16 Aug 2024 21:05:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4236dc1d150b9033a0c12635f2856623e96efcf383d48c97522085f757a77d`  
		Last Modified: Fri, 16 Aug 2024 21:05:21 GMT  
		Size: 374.9 KB (374907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab4df154260eea68dd35cc730282a87fb57915392903c11035c17f519a6c96e`  
		Last Modified: Fri, 16 Aug 2024 21:05:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3677549ffed405f5ae64e6403793e352ecfac2b219c9eedb5028ff32996da03`  
		Last Modified: Fri, 16 Aug 2024 21:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfc19c3fa98906bdc20e8a8400afe4f9b414a7340b21d265dccf34ed27ac257`  
		Last Modified: Fri, 16 Aug 2024 21:05:21 GMT  
		Size: 18.4 MB (18421675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82313e190eab60e8625450d2b286dea76021f5da19bfdebe577415fa461e5c9`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14377702006bc82ef23e61f2b8ed17e316e10b87ba0673db89ec95a79ee87a9`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b0c8b1a15fc09aae430ab9e6a6db5c6f206f1a740c3a1c1b480315148a7f7f`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200e06de81cfb77043b8271865cdff0194d0e6754f636fb258b8a95e941f3ccf`  
		Last Modified: Fri, 16 Aug 2024 21:05:18 GMT  
		Size: 19.3 MB (19265658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ee8b6441d22cc15446aee0d2f0675daead9c2e51dbac7d89edc47d99df8303`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e105068269a03cdc4679d19d4afb6c5a824ffb43ccfbc2430a18e0a80b35554`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c871e44afd26ad9c6e84da90afe24be797cc92c7e5862563a271f080b7d6dc`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a3de421425ac0e051642931e6459b4da6f2f3cd7022114cd5b7811b9eca88e`  
		Last Modified: Fri, 16 Aug 2024 21:05:18 GMT  
		Size: 19.7 MB (19701964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:c8af17c2e98d13ce5c18d9d31d6e8df47c76d1ba504d2f1782980bb8673af4cb
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
$ docker pull docker@sha256:444582958ec806c73d40f3702a8a8d84dc2e82feb0d9b44c738fca09ed2820ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66818343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe40c55ae60532fa0075302e6e93e7248c71837afcbd1c56e77b04e256552e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Aug 2024 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b830b3ce3f84ea7067567326d58a3c311c803b3e94cee51732c87abaf0b1644a`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 7.9 MB (7872313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f67cd05487ef47b2034f553790ea2efb816214bef9fd63d5d4f98254167b56e`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201b9999b9284e2bb11f5f0dc6cb35f9f890e8ef84edbd6edbd7f2ea82918c97`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 18.1 MB (18090908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0ed696b310c4d4cd09c07f7566ed6e2baa3f866160967ef06cf205d244859c`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 18.4 MB (18404798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d43008ea7ba356da560c03ab69f55df1d585a289fe0b9e4388f07ff04648932`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 18.8 MB (18825277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5e249d37736904735e2ce24e0bdea2329356683f6cdc14f3b8a7f1f5794c94`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75295f954e5cf281711fb0cb6e50cda9c6305918cc357d63e5347abf36cf48d`  
		Last Modified: Fri, 16 Aug 2024 20:55:55 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f64e86da193d3fea1e01efb5b7a81578e84d4e4593aee8279e9361b9e7e529`  
		Last Modified: Fri, 16 Aug 2024 20:55:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:bf1312c933add91f38029909c3177cd3b9f727efb4e56065fe297c6da6ffb91f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8336e1fddcafee01e26424a9f2c4608561aa729df648622918daaf2a3ef44053`

```dockerfile
```

-	Layers:
	-	`sha256:c16850f73bbeb2eb267302c311cadcadd55959d236b402c255acf9e6a760625f`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:ad97551c8ab5f60dc65827a43fb5bfc13375c4128efad7a326a9823e0be68d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62435713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468051ea9e870d4ee592d7253bae1b185cd265c4f3b54f8be9f8b1a820359d3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Aug 2024 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749d51120dd4449c98cad5624e6a58aaf21f6b57355b1537b1262f69c27968e`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 7.8 MB (7807488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dee64c722233ea05fa0db7774bbb908ccb3860c76b492b90725b4a00faf74a`  
		Last Modified: Tue, 13 Aug 2024 20:03:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aa9bf3b5617e94aa7647537a116937dc7c6d223c96912c2ffc1302ccceab1b`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 16.4 MB (16362863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b4ff9c935b9bea7d6a6f982aab917c1a4fd29032db6ff2a2026ee7f77cc75`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.1 MB (17114711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc83f1a40d0c658722d9af33f70561ec5dd29cadd86f625da7bcfa50022733b6`  
		Last Modified: Fri, 16 Aug 2024 20:55:46 GMT  
		Size: 17.8 MB (17783303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5f17b4f1f75fbc81e81b8c4714b51f7829480cd793423fdbe280b4a0e06cdc`  
		Last Modified: Fri, 16 Aug 2024 20:55:45 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d17e0519f279b5dc8f4f4d2233b55fa585e9d0f4e28b2ec38a893f46d415da`  
		Last Modified: Fri, 16 Aug 2024 20:55:45 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ddce9ce1633ca8261319074be47691ef0fa443df2b2fa759364895def2fb50`  
		Last Modified: Fri, 16 Aug 2024 20:55:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:72ac9cedabc23854d5804ef9acc704d8bc5672c4f2f7fa895f0536b433b53c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48dc65f2a968c7f37459c45a1f206fd483248e32a76f9d647ccd35c71bb1a66`

```dockerfile
```

-	Layers:
	-	`sha256:0f0379928ebdda35d5a3de2751c7fb8bf3f92b87ef1bc4445614cadfa4d0042b`  
		Last Modified: Fri, 16 Aug 2024 20:55:45 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:cc97a6244b7807809e92b3d720bc2b5f4748fe77f7b1d07f19d033559a0ad00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61468602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509b86a39961f355e5e37e9847693e175944080eae9ea5595e844a7932fe7c06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Aug 2024 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81dc9168b7d20594a7b5afa567e1b9102c0d289d4b9956af1dd0553da38503f`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 7.1 MB (7143486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b63ca62b0868cd9cbb097a6c34d9eb3a8e551918380dd69db51fbe7459654`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff65173bbd98afd04b6c052172c858476533d0f4873c5b6a81bda0849b5792`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 16.4 MB (16353814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd7e108f551e071a490fb8213c13dccea238c6e5c6ed12be3eef86831d31eb`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 17.1 MB (17103032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b020a8e04eea5428d7645058058bdeea76775ad16c0c306557b00c9b3cce3707`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 17.8 MB (17771143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf51759e8c2b5bc311e671ddc5401fb8b470e266b8553c7d887176c8be0e673`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06151b2e48f60b43b5a3438902d125f5201b35d94f354ac3ac4351ed695565f`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf092fc62ad5de9ceea220ba585b82ea46d65253b23f11533d59f110184e5fe4`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:f183a263ab8d9b602944b555e29de9642d82e659e768b89ec39b5617024c4c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa7b9ac79beca13b0bc6894266285efc76f1e0853417a57b774ad69e6a882f5`

```dockerfile
```

-	Layers:
	-	`sha256:b2e8085a6ac1eeb458f441d28f5b14e745904be32fb62d75e214c3746c87091e`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:173d5a1620cd4c9838d8c6eeaff20a78fbcf08ee2e51c12449f832530e7edbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63080030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c697038997a5fe8ff64a0a9e3a2befe1ab1ffa2dbbce9a6d36ca94614c2e9207`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Aug 2024 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Aug 2024 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Aug 2024 11:04:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729161d0df240d9ed83f30e35c6fe471b1fae935500748d1ef7da84e664cdb8a`  
		Last Modified: Fri, 16 Aug 2024 20:55:42 GMT  
		Size: 8.0 MB (7981771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b9491762d2e0304f13e86117eb8d95e32f661c882e832b16bee6e8bb9098cb`  
		Last Modified: Fri, 16 Aug 2024 20:55:41 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fdb7ce0e7cf19d21a2bd7c9f95c09245271c0474a184066b1410007b8d4578`  
		Last Modified: Fri, 16 Aug 2024 20:55:42 GMT  
		Size: 17.0 MB (17049378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99813ceebaed11f6388e8ad3c4c1b371512de366ba5488d2f99200a424f074f`  
		Last Modified: Fri, 16 Aug 2024 20:55:42 GMT  
		Size: 16.8 MB (16772960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316a30f1c6a00f4fbfcba19ce9ccb4c2d5709b52e454b56144ec8f67d26208e2`  
		Last Modified: Fri, 16 Aug 2024 20:55:43 GMT  
		Size: 17.2 MB (17186835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0d611bb20624f74153d3ec09ce18870c07860b77939bdf1e019e0740de454a`  
		Last Modified: Fri, 16 Aug 2024 20:55:43 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9b0bb076214cf2f061a5937a293c9b2915ccf6dd121c501471f941589eab06`  
		Last Modified: Fri, 16 Aug 2024 20:55:43 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75f172f02f32a93ea69404964c9c459ce24e0f2cfe1585a6387e076ee96535d`  
		Last Modified: Fri, 16 Aug 2024 20:55:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:9fe09d16bdc866f48ca5138929e946de2919fc7472dab2277a4690007a863f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4debb6c6f5e419a67a262e3c2d825765ae2e8b3f71720fbbd0843ead3c73e23`

```dockerfile
```

-	Layers:
	-	`sha256:ee581fd74c551286cbef0f11f61d4110c9e68a8323a697f9a454568d1603785a`  
		Last Modified: Fri, 16 Aug 2024 20:55:41 GMT  
		Size: 38.2 KB (38227 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:6eb8bfb2c82d454c0248b5dd41b9607f1b76096c06acf985e862f2ea069db33e
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
$ docker pull docker@sha256:fc81f6680c575a7381f7a586aab4643cdbe79cf9f5af594d2c783a9eb0a0e1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130334773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb13d0c9247298368f97e0637bb60c105cf8159fd29364881b45b5c96c78d621`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97be572a9abc71e039fcf0e5c2cee826693d2e32b5aa28c52ee2e147f29f3ed2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 7.9 MB (7872256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d068c8136df4c77e60b80c6f269c341b11f27187ec77a9ce1a8519f4bdce441f`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3486b9b1692e5ae916e32c2133bb5e8f98a7f89b173cdb303b25d20094e8dee8`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.1 MB (18090913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1726802d7045e092159fdcac73e3c1461690d55c73403cdcdf031ac4145518e2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.4 MB (18404800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1774d2fed741a7a383f92d3969db43a321a4a02dcaad8a886967fb723954fa`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 18.8 MB (18818906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216e3a4876cf4f3c85c70bf9bed6dadfdc58ce83a5537dedb98ea42b20ff36c0`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5bd9a3f910707b7294207b927b3ade09f9d20b66525f2296ee65b90f7edb5`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425c20abf22d4da88ed53e7b1321b6515f33a887063e1f75e25530f7bf89723c`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5174f7db1d0f582b0c6e4a068cb27afd84b66c23716f5046592e2be1b5a225`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 6.7 MB (6657764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fcabf4da4d815f68d521020af7450dc776029613b976a0b4aa8d3429e7d18d`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 89.2 KB (89217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7096f07126cd3b58ec87699d558d9bf0b0b044533ada0f67254d85c94f0bc3b3`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8b74173c6813b97f6d02202faf9a563c7207e298b3204dd4340295344c8ede`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 56.8 MB (56770081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1647c2f9c8092fada70aa9758b7a69f1f3cd05a90891a0a532881cfd598c48`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c41c56a7d8896baa7e32b03546ff50a23492eb9543ed2089ab2fb66ede6ef`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:14ec78850163b4e599f6b88fe195725546c45bc30c37ed06f92bd2e7b2f5b392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33683cd4c1538f63f2751b42869d268ec779b0d5fe22d4765e60f56c75e84787`

```dockerfile
```

-	Layers:
	-	`sha256:76c6029aaa7435fba20177df1eb133a9c0a03d8b5c6fe48799e1fe75e360c69f`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:f027111d31885b0ed9642d1b92d7e62b7644b92089eebc5af8a32d7f8bebfc8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122569652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a41929651127c7fdf1f8cfa71354b837597836af87e070e112cbee135c1040`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749d51120dd4449c98cad5624e6a58aaf21f6b57355b1537b1262f69c27968e`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 7.8 MB (7807488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dee64c722233ea05fa0db7774bbb908ccb3860c76b492b90725b4a00faf74a`  
		Last Modified: Tue, 13 Aug 2024 20:03:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aa9bf3b5617e94aa7647537a116937dc7c6d223c96912c2ffc1302ccceab1b`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 16.4 MB (16362863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b4ff9c935b9bea7d6a6f982aab917c1a4fd29032db6ff2a2026ee7f77cc75`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.1 MB (17114711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31fe971362beacbc7fe1ce84a4f59817b327260334951577b2bdc1640d49164`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.8 MB (17776509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7dca5ea08fd6046c223c1378a8259479b60e2b7c9fe45d9ebc3394f237a3c`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 534.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffadf986c05f1d49184514bc67815f318456acc65c0abfd74b2cce1b6d86ecca`  
		Last Modified: Tue, 13 Aug 2024 20:03:15 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7edf55c16e9e482eb8124f38438564758d96aa113c06fd945bcb13988d3fba6`  
		Last Modified: Tue, 13 Aug 2024 20:03:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7dcf38e93a9b47e0f66795e256f2901c2c4bfc37556e81fea2a063cee12eed`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 7.0 MB (6984036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dc040353146061f1f9e8d56420bfefd970c9707a3834a5bcf02701bc7f87a6`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 88.4 KB (88407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af6ea4938ff0c08202d2f8e3f84e00a915d37297b863ed5032cc8f8fa5cd906`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a7459df9025cc27e33a8fecee41b7192346cf1721924cfabec6187dff5186`  
		Last Modified: Tue, 13 Aug 2024 20:57:37 GMT  
		Size: 53.1 MB (53062512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f07f1d6edcfeac2205add2fc7459ea84419349425810e89ef26b86733a587`  
		Last Modified: Tue, 13 Aug 2024 20:57:36 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40b0d4ce5c2e81228c159aa2dcd3e15ecf2f27ee8a41d175c78e599ca4af850`  
		Last Modified: Tue, 13 Aug 2024 20:57:36 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:6c057a6e1b62568c5bdee69c9c82240780e3862912fcaa566a3a3487a470fd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a96c343221bdcb48cb74979b02ab5c13b27dbff1a66a0ceb3780e97c736573f`

```dockerfile
```

-	Layers:
	-	`sha256:8cea367fa521297df7cfa3bc63f39bd2b776aa0f558f0427199bc08da2d719d2`  
		Last Modified: Tue, 13 Aug 2024 20:57:34 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:a4332a1e0f1aaa47f76bb148424557761569ddbaa01a4b0733831f22a7e2e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120929654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be199173f5a13331c5558376e7c160c53e51cc77a7f598bbe39233e723dade8b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81dc9168b7d20594a7b5afa567e1b9102c0d289d4b9956af1dd0553da38503f`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 7.1 MB (7143486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b63ca62b0868cd9cbb097a6c34d9eb3a8e551918380dd69db51fbe7459654`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff65173bbd98afd04b6c052172c858476533d0f4873c5b6a81bda0849b5792`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 16.4 MB (16353814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd7e108f551e071a490fb8213c13dccea238c6e5c6ed12be3eef86831d31eb`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 17.1 MB (17103032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b020a8e04eea5428d7645058058bdeea76775ad16c0c306557b00c9b3cce3707`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 17.8 MB (17771143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf51759e8c2b5bc311e671ddc5401fb8b470e266b8553c7d887176c8be0e673`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06151b2e48f60b43b5a3438902d125f5201b35d94f354ac3ac4351ed695565f`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf092fc62ad5de9ceea220ba585b82ea46d65253b23f11533d59f110184e5fe4`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a5e67d714baf4e953669b348ccf67b6156b080a6d6966dc09d0543f0c9be9e`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 6.3 MB (6308261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4b153923b2bef79dd19c29f9b88c045ce4e6e55242b154dbc462faed80d0db`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 84.5 KB (84499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ad462b285298ed7a2323c331255edc0ee999c93e0c8ae4a33c5ce454aeeff4`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67a0efc8d76bc7874505d46a4946de771e37c4eb62166bbec60dcd2a80e68e3`  
		Last Modified: Fri, 16 Aug 2024 21:57:37 GMT  
		Size: 53.1 MB (53062491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bba27c850d08471b57f0404d138486b2a1aed9dd9f3893b3b3def00f165ae25`  
		Last Modified: Fri, 16 Aug 2024 21:57:36 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a63b57aea184aabfabfd30d5a7c8567fe3d95a40b8f831ed764b2193d8bffe7`  
		Last Modified: Fri, 16 Aug 2024 21:57:36 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:10c4f8cecc7eb13f9d6d6dc54e1740ab90190e6d24c2e4eec6713b2931912225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a906609c1e200a6b10bedc63efea8af901e9897d1b8f31c4dcb5375222ba63f2`

```dockerfile
```

-	Layers:
	-	`sha256:3e420f6bc3bb35c7528c2f9e8ad122df634ff514d46807261853977ba0eb51f6`  
		Last Modified: Fri, 16 Aug 2024 21:57:34 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e739d640aea8812448d7dd39378e23771a2554a182f2099969410db56fa79917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122599486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d8b2b975dd95f7591d28783db8fc5752c99db0ffd5197320cecf290ce39c7f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eaa3c460d109197e8637b1a9599d7f18cccc546e66d1d62f6dd1508e2935dd`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 8.0 MB (7981761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9e960f5f951de003b26390946248f496a1eda867789ae06fd8b18055515450`  
		Last Modified: Tue, 13 Aug 2024 20:49:42 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99bff4ad6d3c4a0683cf02a74f06b61546be2a877da62aece45b0d3b9409871`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 17.0 MB (17049381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74376b78c4a6f5d12921d8dca6dcfa9e9f2bb0917ddeaa5991b98a8c6594581f`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 16.8 MB (16772960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c08f66b4f65a64aaad739c0ac5607c94142e38e67115632af35ef78cff1329c`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 17.2 MB (17182720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce67e83e18f9107f6bbf32d16c48a8f21c28e500a4212c8ebeca7b994936d7e`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c532de2c2cacfe1199219ef497170060946e3a593f771635c84f141b9a3b94c6`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7601c7d4e5af9ac7f6766b064bc79247c0912f3c5d6f3d02bfb58f49c9207`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194e0f500f2ba3365f850eac55a79e52a90ba4922806239f584025ccf347cea5`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 7.0 MB (7034963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9643f136f726def03ee1af9a52d6193e29fb13777be7e5dad5303f10ed36b68`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 98.7 KB (98659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8112d1aa134e43b2e075826bc7ea6a21adf3464ecd3aee260bf8f2947e9d5a50`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9dc9c485b7585bc344ca1a3c332c378d9ee340ecdb8aa344a75df81b017e1`  
		Last Modified: Tue, 13 Aug 2024 22:23:59 GMT  
		Size: 52.4 MB (52384159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7cbf878da555535371cabcf172c560243258cf73e8889885f96fbe66ded9c2`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97e744676fc32c335434d0c4e6890ce0f48ffb37aa99af9568bca483cbfca3f`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:f6be705e7230112840619e69b7e6322ce4fc67c5f11c95e929f9e841f1e8403c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43bac9495e2c3ff9a3596159acfb499a4e9f6688d7b379425baf358201b63a1`

```dockerfile
```

-	Layers:
	-	`sha256:9604ca831aeb0d74501b911f9a7b547356be1ae57280b751700fd1d324dfd1ad`  
		Last Modified: Tue, 13 Aug 2024 22:23:56 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:af47f6c5401fa4d78609555d2c4b9babfe237af534c7b07ff2b036a0d427a118
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:1c4b1d49cece4db7e2dcaebda47131381ee475d375613c0ad913dd384ee2cba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.3 MB (152296869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa93fbe161d9efbaa4c0e48ceab0e109620689af00487864f7130a6ec89b8a4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97be572a9abc71e039fcf0e5c2cee826693d2e32b5aa28c52ee2e147f29f3ed2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 7.9 MB (7872256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d068c8136df4c77e60b80c6f269c341b11f27187ec77a9ce1a8519f4bdce441f`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3486b9b1692e5ae916e32c2133bb5e8f98a7f89b173cdb303b25d20094e8dee8`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.1 MB (18090913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1726802d7045e092159fdcac73e3c1461690d55c73403cdcdf031ac4145518e2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.4 MB (18404800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1774d2fed741a7a383f92d3969db43a321a4a02dcaad8a886967fb723954fa`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 18.8 MB (18818906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216e3a4876cf4f3c85c70bf9bed6dadfdc58ce83a5537dedb98ea42b20ff36c0`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5bd9a3f910707b7294207b927b3ade09f9d20b66525f2296ee65b90f7edb5`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425c20abf22d4da88ed53e7b1321b6515f33a887063e1f75e25530f7bf89723c`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5174f7db1d0f582b0c6e4a068cb27afd84b66c23716f5046592e2be1b5a225`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 6.7 MB (6657764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fcabf4da4d815f68d521020af7450dc776029613b976a0b4aa8d3429e7d18d`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 89.2 KB (89217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7096f07126cd3b58ec87699d558d9bf0b0b044533ada0f67254d85c94f0bc3b3`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8b74173c6813b97f6d02202faf9a563c7207e298b3204dd4340295344c8ede`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 56.8 MB (56770081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1647c2f9c8092fada70aa9758b7a69f1f3cd05a90891a0a532881cfd598c48`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c41c56a7d8896baa7e32b03546ff50a23492eb9543ed2089ab2fb66ede6ef`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddff6840fdc9aeb42249c80b9c338fe603cc5f0b00252bf16b8bdf2a5fb2f8c`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 981.0 KB (980992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a02b3fadcd722d124529c5401debc307f981a90fc96d45d5d92b96f0dd7545`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c5873bde466cc998bafb56445a5cb01a1a2f54f4166b40ae385bea47531624`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fda618391a49e503c15787e90efea8390d3e23e0621ef57525f337c23de9b6`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 21.0 MB (20979748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08614a56f1a4c3bbf5ebad13045c832079e403dcebb54554e52d5abcdb3b436`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:e63fe7c3704aa2dcc99fb485a4c317a39cb9c1b4d21542ab08c4c4f80a9fc923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23246a0ef23fd48a00bdc4420f83bb303595779eef9540a6b307ca752627e8f3`

```dockerfile
```

-	Layers:
	-	`sha256:030786d4fe7aad28fd3146cfcd96aebaf0140ae35626e5c6bdb622099b291852`  
		Last Modified: Tue, 13 Aug 2024 21:56:06 GMT  
		Size: 30.6 KB (30580 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:40aed2a21da30df0c9cc2f6c0094e5be75f4f063959f290d81137e463c1f4b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146459861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403f1c1202717e657a3afb32bea3613930169406534f89b7fc204a622540f610`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eaa3c460d109197e8637b1a9599d7f18cccc546e66d1d62f6dd1508e2935dd`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 8.0 MB (7981761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9e960f5f951de003b26390946248f496a1eda867789ae06fd8b18055515450`  
		Last Modified: Tue, 13 Aug 2024 20:49:42 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99bff4ad6d3c4a0683cf02a74f06b61546be2a877da62aece45b0d3b9409871`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 17.0 MB (17049381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74376b78c4a6f5d12921d8dca6dcfa9e9f2bb0917ddeaa5991b98a8c6594581f`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 16.8 MB (16772960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c08f66b4f65a64aaad739c0ac5607c94142e38e67115632af35ef78cff1329c`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 17.2 MB (17182720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce67e83e18f9107f6bbf32d16c48a8f21c28e500a4212c8ebeca7b994936d7e`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c532de2c2cacfe1199219ef497170060946e3a593f771635c84f141b9a3b94c6`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7601c7d4e5af9ac7f6766b064bc79247c0912f3c5d6f3d02bfb58f49c9207`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194e0f500f2ba3365f850eac55a79e52a90ba4922806239f584025ccf347cea5`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 7.0 MB (7034963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9643f136f726def03ee1af9a52d6193e29fb13777be7e5dad5303f10ed36b68`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 98.7 KB (98659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8112d1aa134e43b2e075826bc7ea6a21adf3464ecd3aee260bf8f2947e9d5a50`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9dc9c485b7585bc344ca1a3c332c378d9ee340ecdb8aa344a75df81b017e1`  
		Last Modified: Tue, 13 Aug 2024 22:23:59 GMT  
		Size: 52.4 MB (52384159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7cbf878da555535371cabcf172c560243258cf73e8889885f96fbe66ded9c2`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97e744676fc32c335434d0c4e6890ce0f48ffb37aa99af9568bca483cbfca3f`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4503187f1903453dfdd96e29f2843028e7ab3999269f4e94f7fba03b1754d3`  
		Last Modified: Tue, 13 Aug 2024 23:09:28 GMT  
		Size: 1.0 MB (1023136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e456d8b7e6c45005803d8726755e761e590e47c68a1fb8750c012f4bfb57ef5`  
		Last Modified: Tue, 13 Aug 2024 23:09:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c292ab69c00576a9f271ac96f8d010a8785c5572d03a5efc32e80f2208bbf67d`  
		Last Modified: Tue, 13 Aug 2024 23:09:28 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc26ac4f7d112ba3395f6d5d5b6bd5975e89bb3a1aeccbb6d382cbcbbc757ae`  
		Last Modified: Tue, 13 Aug 2024 23:09:29 GMT  
		Size: 22.8 MB (22835879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570ac36fe23a0443a0db74a04c915f8a2fa16a8185157707d6d94f88a2270973`  
		Last Modified: Tue, 13 Aug 2024 23:09:29 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:83b8fc3691f89e164a3848ca85d5afb6047d2b8c36ee8500361a705a4f238a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544dbc1f438dbe68196bbe42b384836b43013481026eb3482ea165adc58e0331`

```dockerfile
```

-	Layers:
	-	`sha256:fdc4f405dfa87c2c564b75159723ba929dc1a643febd173d3215221105b7936a`  
		Last Modified: Tue, 13 Aug 2024 23:09:27 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:6eb8bfb2c82d454c0248b5dd41b9607f1b76096c06acf985e862f2ea069db33e
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
$ docker pull docker@sha256:fc81f6680c575a7381f7a586aab4643cdbe79cf9f5af594d2c783a9eb0a0e1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130334773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb13d0c9247298368f97e0637bb60c105cf8159fd29364881b45b5c96c78d621`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97be572a9abc71e039fcf0e5c2cee826693d2e32b5aa28c52ee2e147f29f3ed2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 7.9 MB (7872256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d068c8136df4c77e60b80c6f269c341b11f27187ec77a9ce1a8519f4bdce441f`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3486b9b1692e5ae916e32c2133bb5e8f98a7f89b173cdb303b25d20094e8dee8`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.1 MB (18090913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1726802d7045e092159fdcac73e3c1461690d55c73403cdcdf031ac4145518e2`  
		Last Modified: Tue, 13 Aug 2024 20:01:51 GMT  
		Size: 18.4 MB (18404800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1774d2fed741a7a383f92d3969db43a321a4a02dcaad8a886967fb723954fa`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 18.8 MB (18818906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216e3a4876cf4f3c85c70bf9bed6dadfdc58ce83a5537dedb98ea42b20ff36c0`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5bd9a3f910707b7294207b927b3ade09f9d20b66525f2296ee65b90f7edb5`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425c20abf22d4da88ed53e7b1321b6515f33a887063e1f75e25530f7bf89723c`  
		Last Modified: Tue, 13 Aug 2024 20:01:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5174f7db1d0f582b0c6e4a068cb27afd84b66c23716f5046592e2be1b5a225`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 6.7 MB (6657764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fcabf4da4d815f68d521020af7450dc776029613b976a0b4aa8d3429e7d18d`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 89.2 KB (89217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7096f07126cd3b58ec87699d558d9bf0b0b044533ada0f67254d85c94f0bc3b3`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8b74173c6813b97f6d02202faf9a563c7207e298b3204dd4340295344c8ede`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 56.8 MB (56770081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1647c2f9c8092fada70aa9758b7a69f1f3cd05a90891a0a532881cfd598c48`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c41c56a7d8896baa7e32b03546ff50a23492eb9543ed2089ab2fb66ede6ef`  
		Last Modified: Tue, 13 Aug 2024 20:57:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:14ec78850163b4e599f6b88fe195725546c45bc30c37ed06f92bd2e7b2f5b392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33683cd4c1538f63f2751b42869d268ec779b0d5fe22d4765e60f56c75e84787`

```dockerfile
```

-	Layers:
	-	`sha256:76c6029aaa7435fba20177df1eb133a9c0a03d8b5c6fe48799e1fe75e360c69f`  
		Last Modified: Tue, 13 Aug 2024 20:57:30 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:f027111d31885b0ed9642d1b92d7e62b7644b92089eebc5af8a32d7f8bebfc8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122569652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a41929651127c7fdf1f8cfa71354b837597836af87e070e112cbee135c1040`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749d51120dd4449c98cad5624e6a58aaf21f6b57355b1537b1262f69c27968e`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 7.8 MB (7807488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dee64c722233ea05fa0db7774bbb908ccb3860c76b492b90725b4a00faf74a`  
		Last Modified: Tue, 13 Aug 2024 20:03:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aa9bf3b5617e94aa7647537a116937dc7c6d223c96912c2ffc1302ccceab1b`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 16.4 MB (16362863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b4ff9c935b9bea7d6a6f982aab917c1a4fd29032db6ff2a2026ee7f77cc75`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.1 MB (17114711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31fe971362beacbc7fe1ce84a4f59817b327260334951577b2bdc1640d49164`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 17.8 MB (17776509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7dca5ea08fd6046c223c1378a8259479b60e2b7c9fe45d9ebc3394f237a3c`  
		Last Modified: Tue, 13 Aug 2024 20:03:14 GMT  
		Size: 534.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffadf986c05f1d49184514bc67815f318456acc65c0abfd74b2cce1b6d86ecca`  
		Last Modified: Tue, 13 Aug 2024 20:03:15 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7edf55c16e9e482eb8124f38438564758d96aa113c06fd945bcb13988d3fba6`  
		Last Modified: Tue, 13 Aug 2024 20:03:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7dcf38e93a9b47e0f66795e256f2901c2c4bfc37556e81fea2a063cee12eed`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 7.0 MB (6984036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dc040353146061f1f9e8d56420bfefd970c9707a3834a5bcf02701bc7f87a6`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 88.4 KB (88407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af6ea4938ff0c08202d2f8e3f84e00a915d37297b863ed5032cc8f8fa5cd906`  
		Last Modified: Tue, 13 Aug 2024 20:57:35 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a7459df9025cc27e33a8fecee41b7192346cf1721924cfabec6187dff5186`  
		Last Modified: Tue, 13 Aug 2024 20:57:37 GMT  
		Size: 53.1 MB (53062512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f07f1d6edcfeac2205add2fc7459ea84419349425810e89ef26b86733a587`  
		Last Modified: Tue, 13 Aug 2024 20:57:36 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40b0d4ce5c2e81228c159aa2dcd3e15ecf2f27ee8a41d175c78e599ca4af850`  
		Last Modified: Tue, 13 Aug 2024 20:57:36 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:6c057a6e1b62568c5bdee69c9c82240780e3862912fcaa566a3a3487a470fd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a96c343221bdcb48cb74979b02ab5c13b27dbff1a66a0ceb3780e97c736573f`

```dockerfile
```

-	Layers:
	-	`sha256:8cea367fa521297df7cfa3bc63f39bd2b776aa0f558f0427199bc08da2d719d2`  
		Last Modified: Tue, 13 Aug 2024 20:57:34 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:a4332a1e0f1aaa47f76bb148424557761569ddbaa01a4b0733831f22a7e2e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120929654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be199173f5a13331c5558376e7c160c53e51cc77a7f598bbe39233e723dade8b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81dc9168b7d20594a7b5afa567e1b9102c0d289d4b9956af1dd0553da38503f`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 7.1 MB (7143486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b63ca62b0868cd9cbb097a6c34d9eb3a8e551918380dd69db51fbe7459654`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff65173bbd98afd04b6c052172c858476533d0f4873c5b6a81bda0849b5792`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 16.4 MB (16353814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd7e108f551e071a490fb8213c13dccea238c6e5c6ed12be3eef86831d31eb`  
		Last Modified: Wed, 14 Aug 2024 00:34:11 GMT  
		Size: 17.1 MB (17103032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b020a8e04eea5428d7645058058bdeea76775ad16c0c306557b00c9b3cce3707`  
		Last Modified: Fri, 16 Aug 2024 20:55:54 GMT  
		Size: 17.8 MB (17771143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf51759e8c2b5bc311e671ddc5401fb8b470e266b8553c7d887176c8be0e673`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06151b2e48f60b43b5a3438902d125f5201b35d94f354ac3ac4351ed695565f`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf092fc62ad5de9ceea220ba585b82ea46d65253b23f11533d59f110184e5fe4`  
		Last Modified: Fri, 16 Aug 2024 20:55:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a5e67d714baf4e953669b348ccf67b6156b080a6d6966dc09d0543f0c9be9e`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 6.3 MB (6308261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4b153923b2bef79dd19c29f9b88c045ce4e6e55242b154dbc462faed80d0db`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 84.5 KB (84499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ad462b285298ed7a2323c331255edc0ee999c93e0c8ae4a33c5ce454aeeff4`  
		Last Modified: Fri, 16 Aug 2024 21:57:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67a0efc8d76bc7874505d46a4946de771e37c4eb62166bbec60dcd2a80e68e3`  
		Last Modified: Fri, 16 Aug 2024 21:57:37 GMT  
		Size: 53.1 MB (53062491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bba27c850d08471b57f0404d138486b2a1aed9dd9f3893b3b3def00f165ae25`  
		Last Modified: Fri, 16 Aug 2024 21:57:36 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a63b57aea184aabfabfd30d5a7c8567fe3d95a40b8f831ed764b2193d8bffe7`  
		Last Modified: Fri, 16 Aug 2024 21:57:36 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:10c4f8cecc7eb13f9d6d6dc54e1740ab90190e6d24c2e4eec6713b2931912225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a906609c1e200a6b10bedc63efea8af901e9897d1b8f31c4dcb5375222ba63f2`

```dockerfile
```

-	Layers:
	-	`sha256:3e420f6bc3bb35c7528c2f9e8ad122df634ff514d46807261853977ba0eb51f6`  
		Last Modified: Fri, 16 Aug 2024 21:57:34 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e739d640aea8812448d7dd39378e23771a2554a182f2099969410db56fa79917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122599486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d8b2b975dd95f7591d28783db8fc5752c99db0ffd5197320cecf290ce39c7f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Aug 2024 16:47:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD ["sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 13 Aug 2024 16:47:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 16:47:50 GMT
VOLUME [/var/lib/docker]
# Tue, 13 Aug 2024 16:47:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 13 Aug 2024 16:47:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 13 Aug 2024 16:47:50 GMT
CMD []
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eaa3c460d109197e8637b1a9599d7f18cccc546e66d1d62f6dd1508e2935dd`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 8.0 MB (7981761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9e960f5f951de003b26390946248f496a1eda867789ae06fd8b18055515450`  
		Last Modified: Tue, 13 Aug 2024 20:49:42 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99bff4ad6d3c4a0683cf02a74f06b61546be2a877da62aece45b0d3b9409871`  
		Last Modified: Tue, 13 Aug 2024 20:49:43 GMT  
		Size: 17.0 MB (17049381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74376b78c4a6f5d12921d8dca6dcfa9e9f2bb0917ddeaa5991b98a8c6594581f`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 16.8 MB (16772960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c08f66b4f65a64aaad739c0ac5607c94142e38e67115632af35ef78cff1329c`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 17.2 MB (17182720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce67e83e18f9107f6bbf32d16c48a8f21c28e500a4212c8ebeca7b994936d7e`  
		Last Modified: Tue, 13 Aug 2024 20:49:44 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c532de2c2cacfe1199219ef497170060946e3a593f771635c84f141b9a3b94c6`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7601c7d4e5af9ac7f6766b064bc79247c0912f3c5d6f3d02bfb58f49c9207`  
		Last Modified: Tue, 13 Aug 2024 20:49:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194e0f500f2ba3365f850eac55a79e52a90ba4922806239f584025ccf347cea5`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 7.0 MB (7034963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9643f136f726def03ee1af9a52d6193e29fb13777be7e5dad5303f10ed36b68`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 98.7 KB (98659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8112d1aa134e43b2e075826bc7ea6a21adf3464ecd3aee260bf8f2947e9d5a50`  
		Last Modified: Tue, 13 Aug 2024 22:23:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9dc9c485b7585bc344ca1a3c332c378d9ee340ecdb8aa344a75df81b017e1`  
		Last Modified: Tue, 13 Aug 2024 22:23:59 GMT  
		Size: 52.4 MB (52384159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7cbf878da555535371cabcf172c560243258cf73e8889885f96fbe66ded9c2`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97e744676fc32c335434d0c4e6890ce0f48ffb37aa99af9568bca483cbfca3f`  
		Last Modified: Tue, 13 Aug 2024 22:23:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:f6be705e7230112840619e69b7e6322ce4fc67c5f11c95e929f9e841f1e8403c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43bac9495e2c3ff9a3596159acfb499a4e9f6688d7b379425baf358201b63a1`

```dockerfile
```

-	Layers:
	-	`sha256:9604ca831aeb0d74501b911f9a7b547356be1ae57280b751700fd1d324dfd1ad`  
		Last Modified: Tue, 13 Aug 2024 22:23:56 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:e1ded4b3a2aaf5d101daaca1e22004a6c4002e37cdf0842705f51159f0df81ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:722e8fd401b84665b82e0666308e3852fb7e55ef623784849a0ad1a0fbbfcd28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199540785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57c9795d7276f4ddea53e5745bd047597db78375c979913534c8fdf874a086a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Fri, 16 Aug 2024 21:04:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 21:04:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Aug 2024 21:04:37 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 21:04:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.2.zip
# Fri, 16 Aug 2024 21:04:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:04:49 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 21:04:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Fri, 16 Aug 2024 21:04:50 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Fri, 16 Aug 2024 21:05:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:05:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 21:05:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Fri, 16 Aug 2024 21:05:02 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Fri, 16 Aug 2024 21:05:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e5e515bd55c81feeefd0785d8074f5be7923da2cce4b86409954eafb42a89d`  
		Last Modified: Fri, 16 Aug 2024 21:05:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4236dc1d150b9033a0c12635f2856623e96efcf383d48c97522085f757a77d`  
		Last Modified: Fri, 16 Aug 2024 21:05:21 GMT  
		Size: 374.9 KB (374907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab4df154260eea68dd35cc730282a87fb57915392903c11035c17f519a6c96e`  
		Last Modified: Fri, 16 Aug 2024 21:05:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3677549ffed405f5ae64e6403793e352ecfac2b219c9eedb5028ff32996da03`  
		Last Modified: Fri, 16 Aug 2024 21:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfc19c3fa98906bdc20e8a8400afe4f9b414a7340b21d265dccf34ed27ac257`  
		Last Modified: Fri, 16 Aug 2024 21:05:21 GMT  
		Size: 18.4 MB (18421675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82313e190eab60e8625450d2b286dea76021f5da19bfdebe577415fa461e5c9`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14377702006bc82ef23e61f2b8ed17e316e10b87ba0673db89ec95a79ee87a9`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b0c8b1a15fc09aae430ab9e6a6db5c6f206f1a740c3a1c1b480315148a7f7f`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200e06de81cfb77043b8271865cdff0194d0e6754f636fb258b8a95e941f3ccf`  
		Last Modified: Fri, 16 Aug 2024 21:05:18 GMT  
		Size: 19.3 MB (19265658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ee8b6441d22cc15446aee0d2f0675daead9c2e51dbac7d89edc47d99df8303`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e105068269a03cdc4679d19d4afb6c5a824ffb43ccfbc2430a18e0a80b35554`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c871e44afd26ad9c6e84da90afe24be797cc92c7e5862563a271f080b7d6dc`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a3de421425ac0e051642931e6459b4da6f2f3cd7022114cd5b7811b9eca88e`  
		Last Modified: Fri, 16 Aug 2024 21:05:18 GMT  
		Size: 19.7 MB (19701964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:6fc12e3169bfe0a9322c7740f4f4079f8f45dd1b79168c426a89a43ad0c6d9fb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303121283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd6dcd72864533d8de94060162775ef92bd31748712fbcd1f03469008647db8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Fri, 16 Aug 2024 20:59:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 21:00:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Aug 2024 21:00:13 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 21:00:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.2.zip
# Fri, 16 Aug 2024 21:00:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:00:35 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 21:00:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Fri, 16 Aug 2024 21:00:36 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Fri, 16 Aug 2024 21:00:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:00:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 21:00:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Fri, 16 Aug 2024 21:00:57 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Fri, 16 Aug 2024 21:01:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc681518e2d562ce97fc231963b0590c8a4578d640e9226ebc7e7a64072c1c57`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf861a9062e8367fea0bf7fd15b3a23566d429c8f7a698862ed56a6b30e5d08`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 502.8 KB (502826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a6eef9d04b51a84647684d5ac6acc5bbcf56cf1e9a1677f27f0a451d0dc191`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f7463ca73d8038d2384509adeb789ee442a132ab89bd9125fd0d865c0e957c`  
		Last Modified: Fri, 16 Aug 2024 21:01:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1096db739f2668906215c2b312cca48af870253ffbbc08f284d90e88e5d9afd0`  
		Last Modified: Fri, 16 Aug 2024 21:01:23 GMT  
		Size: 18.4 MB (18429168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ba54531e0b5e75e9c6afb0f70803c3f19b3297ba195a9a0f0ed65ac1ed6cbb`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf33926246d70e6dc5eb83affb3e85e5e70ba479cf02633542f105b7c0f9844c`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f26c7e8351ae5c2502dd7735392d69fa658ffb65cb5f1ca900319b9409cf63`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14de9ca87757d524465e1db5e32a8e157bd58a897ed38348289c0293a894bb21`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 19.3 MB (19271416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cca9a181e2403ef565744f377e65fbaeceec043ac17c57026563ab53faa0edc`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61b3946fd8e06fe43f43af8f8d64efafff325bd4e24525b4464c35e4247d30c`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d994d497e123945dca78f465e5d4c09bf3d99d78c717f359cf93b78ed69720e1`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0130b148c08f6100b5c93d2c5de1ddd3a4a69543356d1c729eb4e1f72bded8dd`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 19.7 MB (19702913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:89451243e7ee80b1dd7d6e13e80627c63f3775b02426c3284264932fd4002be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:6fc12e3169bfe0a9322c7740f4f4079f8f45dd1b79168c426a89a43ad0c6d9fb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303121283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd6dcd72864533d8de94060162775ef92bd31748712fbcd1f03469008647db8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Fri, 16 Aug 2024 20:59:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 21:00:12 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Aug 2024 21:00:13 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 21:00:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.2.zip
# Fri, 16 Aug 2024 21:00:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:00:35 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 21:00:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Fri, 16 Aug 2024 21:00:36 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Fri, 16 Aug 2024 21:00:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:00:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 21:00:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Fri, 16 Aug 2024 21:00:57 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Fri, 16 Aug 2024 21:01:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc681518e2d562ce97fc231963b0590c8a4578d640e9226ebc7e7a64072c1c57`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf861a9062e8367fea0bf7fd15b3a23566d429c8f7a698862ed56a6b30e5d08`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 502.8 KB (502826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a6eef9d04b51a84647684d5ac6acc5bbcf56cf1e9a1677f27f0a451d0dc191`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f7463ca73d8038d2384509adeb789ee442a132ab89bd9125fd0d865c0e957c`  
		Last Modified: Fri, 16 Aug 2024 21:01:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1096db739f2668906215c2b312cca48af870253ffbbc08f284d90e88e5d9afd0`  
		Last Modified: Fri, 16 Aug 2024 21:01:23 GMT  
		Size: 18.4 MB (18429168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ba54531e0b5e75e9c6afb0f70803c3f19b3297ba195a9a0f0ed65ac1ed6cbb`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf33926246d70e6dc5eb83affb3e85e5e70ba479cf02633542f105b7c0f9844c`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f26c7e8351ae5c2502dd7735392d69fa658ffb65cb5f1ca900319b9409cf63`  
		Last Modified: Fri, 16 Aug 2024 21:01:20 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14de9ca87757d524465e1db5e32a8e157bd58a897ed38348289c0293a894bb21`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 19.3 MB (19271416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cca9a181e2403ef565744f377e65fbaeceec043ac17c57026563ab53faa0edc`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61b3946fd8e06fe43f43af8f8d64efafff325bd4e24525b4464c35e4247d30c`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d994d497e123945dca78f465e5d4c09bf3d99d78c717f359cf93b78ed69720e1`  
		Last Modified: Fri, 16 Aug 2024 21:01:19 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0130b148c08f6100b5c93d2c5de1ddd3a4a69543356d1c729eb4e1f72bded8dd`  
		Last Modified: Fri, 16 Aug 2024 21:01:22 GMT  
		Size: 19.7 MB (19702913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:87827cb0d8a93f2c55cd85a9bd673523c38715a87d0257cb18798505f0154212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:722e8fd401b84665b82e0666308e3852fb7e55ef623784849a0ad1a0fbbfcd28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199540785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57c9795d7276f4ddea53e5745bd047597db78375c979913534c8fdf874a086a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Fri, 16 Aug 2024 21:04:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 21:04:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 16 Aug 2024 21:04:37 GMT
ENV DOCKER_VERSION=27.1.2
# Fri, 16 Aug 2024 21:04:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.2.zip
# Fri, 16 Aug 2024 21:04:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:04:49 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Fri, 16 Aug 2024 21:04:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Fri, 16 Aug 2024 21:04:50 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Fri, 16 Aug 2024 21:05:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 16 Aug 2024 21:05:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Fri, 16 Aug 2024 21:05:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Fri, 16 Aug 2024 21:05:02 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Fri, 16 Aug 2024 21:05:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e5e515bd55c81feeefd0785d8074f5be7923da2cce4b86409954eafb42a89d`  
		Last Modified: Fri, 16 Aug 2024 21:05:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4236dc1d150b9033a0c12635f2856623e96efcf383d48c97522085f757a77d`  
		Last Modified: Fri, 16 Aug 2024 21:05:21 GMT  
		Size: 374.9 KB (374907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab4df154260eea68dd35cc730282a87fb57915392903c11035c17f519a6c96e`  
		Last Modified: Fri, 16 Aug 2024 21:05:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3677549ffed405f5ae64e6403793e352ecfac2b219c9eedb5028ff32996da03`  
		Last Modified: Fri, 16 Aug 2024 21:05:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfc19c3fa98906bdc20e8a8400afe4f9b414a7340b21d265dccf34ed27ac257`  
		Last Modified: Fri, 16 Aug 2024 21:05:21 GMT  
		Size: 18.4 MB (18421675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82313e190eab60e8625450d2b286dea76021f5da19bfdebe577415fa461e5c9`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14377702006bc82ef23e61f2b8ed17e316e10b87ba0673db89ec95a79ee87a9`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b0c8b1a15fc09aae430ab9e6a6db5c6f206f1a740c3a1c1b480315148a7f7f`  
		Last Modified: Fri, 16 Aug 2024 21:05:17 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200e06de81cfb77043b8271865cdff0194d0e6754f636fb258b8a95e941f3ccf`  
		Last Modified: Fri, 16 Aug 2024 21:05:18 GMT  
		Size: 19.3 MB (19265658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ee8b6441d22cc15446aee0d2f0675daead9c2e51dbac7d89edc47d99df8303`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e105068269a03cdc4679d19d4afb6c5a824ffb43ccfbc2430a18e0a80b35554`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c871e44afd26ad9c6e84da90afe24be797cc92c7e5862563a271f080b7d6dc`  
		Last Modified: Fri, 16 Aug 2024 21:05:15 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a3de421425ac0e051642931e6459b4da6f2f3cd7022114cd5b7811b9eca88e`  
		Last Modified: Fri, 16 Aug 2024 21:05:18 GMT  
		Size: 19.7 MB (19701964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
