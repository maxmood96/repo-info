<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:27`](#docker27)
-	[`docker:27-cli`](#docker27-cli)
-	[`docker:27-dind`](#docker27-dind)
-	[`docker:27-dind-rootless`](#docker27-dind-rootless)
-	[`docker:27-windowsservercore`](#docker27-windowsservercore)
-	[`docker:27-windowsservercore-1809`](#docker27-windowsservercore-1809)
-	[`docker:27-windowsservercore-ltsc2022`](#docker27-windowsservercore-ltsc2022)
-	[`docker:27.2`](#docker272)
-	[`docker:27.2-cli`](#docker272-cli)
-	[`docker:27.2-dind`](#docker272-dind)
-	[`docker:27.2-dind-rootless`](#docker272-dind-rootless)
-	[`docker:27.2-windowsservercore`](#docker272-windowsservercore)
-	[`docker:27.2-windowsservercore-1809`](#docker272-windowsservercore-1809)
-	[`docker:27.2-windowsservercore-ltsc2022`](#docker272-windowsservercore-ltsc2022)
-	[`docker:27.2.1`](#docker2721)
-	[`docker:27.2.1-alpine3.20`](#docker2721-alpine320)
-	[`docker:27.2.1-cli`](#docker2721-cli)
-	[`docker:27.2.1-cli-alpine3.20`](#docker2721-cli-alpine320)
-	[`docker:27.2.1-dind`](#docker2721-dind)
-	[`docker:27.2.1-dind-alpine3.20`](#docker2721-dind-alpine320)
-	[`docker:27.2.1-dind-rootless`](#docker2721-dind-rootless)
-	[`docker:27.2.1-windowsservercore`](#docker2721-windowsservercore)
-	[`docker:27.2.1-windowsservercore-1809`](#docker2721-windowsservercore-1809)
-	[`docker:27.2.1-windowsservercore-ltsc2022`](#docker2721-windowsservercore-ltsc2022)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)

## `docker:27`

```console
$ docker pull docker@sha256:294f99b7749b47d3bfac8535c231a6c47cd0f28be8205af83928b2dde18abda7
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
$ docker pull docker@sha256:9218d2dc6ab909992500f116eb49948376fb23f5cd9ccf427dd62b3d865ea49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131884120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371f9f35b2da407e86e3d81ea7a4efc0594697c3abb6b47bac15bbfa0533f293`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db09d90694836eab5370b7d5f552b34f5772781701b00fd4e7c3950519ee72`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 7.9 MB (7872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538dd9aacd297989031c915937096bfdd889838bf150c05212223a9b3507070`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfaa9e1957304899a8d16f9cf6fca1ddbf8debde833e6b68831a81b50ee6fc2`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616c0277b4c4b06061b57f23022504d07faea54188b3a5b0d5b51dfa4e990b9`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.4 MB (18432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692e2842ca25a9bf245905f6e29b66a65bbdc85f1873aae896b69370566a5f9`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cd67bc2f21b34aeca4c5627b6b4b5dbede9b76ea404dd4079e77464166d0b`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966ec96386506904d07991e403853675dc204da54a5e1fd0c1abd1e6da10197`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1d01552a20f6313745d5d6563fc8a44c75d0010cb7cd94399a1487838380`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c62cf5a0b55f78c6952456f627b45a4927bcd20a476a84feebb376a2e5afac`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 6.7 MB (6657921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3592c908208e8a16c99d3263902c97301ed446b46205bfcbb8d9ee8611123fa`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 89.2 KB (89218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd4c1986daa1bdd24f3621084f644cff84734eeb7aff037024fdf56f6aae3c1`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f41134be18ef5373326b3114ba85c9698be27a64dc12f0f60a1f5e6d0eac9`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 57.8 MB (57773398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaea47f5e1a31cc71bc565396dc93187e844d7f4ad7885746889e44dc40a4b`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a6f212eac3af392a8a5097e434764cff04c4e70ff2a9c1d4809c5c2e18d9e3`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:797fd1c255c0affbf4ea21c2af94c6f9904c76f433cacfb5aa44a15260ed50de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad921b63e93d9459a50c321f18aa4cad7866107facd5e54d1497bd0a6c86c6fd`

```dockerfile
```

-	Layers:
	-	`sha256:c9f2b5ad322c5b5af063de9a0bf790828d7771944a1fcec170e83a363c84a90c`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v6

```console
$ docker pull docker@sha256:0d871bea6fe47e7bf76b382ee2d4b128fe292b8fdb9082b21345c7d54cfdccae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123320023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cc1cb94b0e714568ec3d9021c42c78f629e704609cfc06069a093ad4a9fea0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1aa033c3dd6f9dcabf3e5db8b0d23e75bacc18083a9fc5fc3bf8dd32b531c9`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 17.1 MB (17141620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1075e78e61225557a73cb4df8bdb388a4e0a3a54d78fb029b95995467ee104`  
		Last Modified: Wed, 11 Sep 2024 02:01:31 GMT  
		Size: 17.8 MB (17783313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e371b1027e98e0af0c4a206108df3590c4135af5dd5c95267415707045a1884`  
		Last Modified: Wed, 11 Sep 2024 02:01:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226c034025ceb5a5072018428121e6627a7adea704c15385680801a1fd204fb`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dc19fcc1171071ce37cd5bee8802261a02276f6819a1116bba48770ae075f`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bf43051f6d401906c8b54ab26747cdead0e1b75ebec9c87fc12bf84d6dc5ed`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 7.0 MB (6984307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da17202765e315d32b089e1c25d097f8e0085fbb39264f5438693657418417`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 88.4 KB (88398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e960455cee8307842cd7579d74c83c6cb33ed93689bc96725f8ed7ebaf5d59b`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bbbc69f2a31b558cb399de570b4197e2b9834a828760b430ff42c27749a5b4`  
		Last Modified: Wed, 11 Sep 2024 02:50:52 GMT  
		Size: 53.5 MB (53494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103acb18844ccc79264ef2a516bb06bd5a0fecb9f01c581d3382253bdfa4423d`  
		Last Modified: Wed, 11 Sep 2024 02:50:51 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0f859154c8a30c4a41eb85bdfb5bafdd1617a0787c82c879a8a0575b531ac`  
		Last Modified: Wed, 11 Sep 2024 02:50:51 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:5c5a017a1a9973a3ee57ddf3ddb4efd0e946b7da75bf289ba07ff8a9143ba0a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ce3bf47c18b13d056ef62e3576f93da7e2113326d337a31b0e4d5e835a21de`

```dockerfile
```

-	Layers:
	-	`sha256:1dbc2fbc5d04bf6005bd82413353aa41ed322750380a145666a8789b6900915b`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v7

```console
$ docker pull docker@sha256:68d52b1f8e3a30d5c9ebe8531f1ceb2b14389dc70dc7f73fc640cc2612b0cb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121668199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28baeefb60bbf0c1f288b4ba28c02be3975f6866a625e2122122b2366329bc7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cf2b1859f16ea4a3efc3ebdcff929c005fc44c05d7202ce69bbd5258d6989a`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 17.1 MB (17129209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e839e120983d5ca2057bee14103b0d822031e067c63b69d5f7e1d0845a446`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 17.8 MB (17771142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29362d9881a8e2c6fd23dac747f90a311fd37d78cbe5bfe2bc93d137ca3f7b93`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b72324b3582fd670d40a641281f441939c93b3eec0c1a40744ce9f42d416aef`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20947c69fcf36566adb6594921006179ce40d22530bd7d0a5c2f9b50e15639`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3903b8a5e83aa88438bc00e6a21cbfb21f98d72bf4a90554fbbc9a67c624287`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 6.3 MB (6308115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a08d98b7b8a40124cdff9c9cfb28790278fd87f375c88ea1239edb53b70aedb`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 84.5 KB (84482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c31665ca29d651d05ff3ca3fdc61f6a67ce69e291415b2651008e20b66e92dc`  
		Last Modified: Wed, 11 Sep 2024 02:50:55 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdde100f6de66fb3973ccfa58803d39516f505beacbffa025f887a7a952e3af9`  
		Last Modified: Wed, 11 Sep 2024 02:50:57 GMT  
		Size: 53.5 MB (53494122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131ea12518408d5c3f587e5ce4fe43d86e73f90603ed92f2ae54b2d321e2d47a`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f824312e672e112fdb8abcca34a0ae94e522859b14b6ba6b92d991d2e996ba7`  
		Last Modified: Wed, 11 Sep 2024 02:50:57 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:4f69fea1e0e9bf4868790f90d7c7db9943225d34949695ace47f8784e814be93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db4c9ab2f89bb268cc28bcab911d9b7fc0a33b4e3b11b6b9baab0265727e3ae`

```dockerfile
```

-	Layers:
	-	`sha256:96e05737fa765bceaa6840ea6423d151ae12256c0d7a05d01ade85d7a178e388`  
		Last Modified: Wed, 11 Sep 2024 02:50:55 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e5140f28e7e82d172f34d88dfbd7a1bacbd4cbd3f24abdcaf1b0be485b916dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124152073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a7e2ef80ce4b0a550c648ddfb69a1953cdb927ca159fe704bf937bc8979d77`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eada7f8d96edf35fbf9cccdfe2a31683f121351212c1d270f7a73b2e1f530e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.2 MB (17186842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b544e07d92af2d47cc10db55727317ca8ccc95a899db6ce41cdd41cb820c0`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ca207ff0f9c918c07b12825084dba82e9f8c9d490f1ffcf33fe0c7b45fab2`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c5493b785a7581afc20e1db4ba86a79bd5e5e8ef3dfa1ad64620028e196eb`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e5be9720db99d659c53b6a67a1dd2ba6e958b7622248ab8dfc91c58d5c0f1d`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 7.0 MB (7034910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320bcabad1025e90ed07d105bd2724f1565672227ec5927061b082183adc6b11`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 98.7 KB (98650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9235e7f34f8cc28423dac4653e318c60d54cff3b0544a5e924074efdf31578`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9d4c07d55e9442550b66fb78c2d91de8856309dcc6875aa4c34aaa96f85316`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 53.4 MB (53398203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df4284aea7cda8255fd5026391b9b8b9db9af96da9875fe9db8f0185ac0ccd`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c51f22e855b132e7146b336aac0310cbe52e537cd77af861d9f27629b425ea6`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:fff328b2549d85866f264e626fb1fca2080ff3b685aa527410f3ea8ce95f38ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fd23934d6432c356a3df01ffbcf3ffbe9940918ffb9408d76137da20e3a2af`

```dockerfile
```

-	Layers:
	-	`sha256:23b22cd0119f1928542bdacdaf4016a4fa50c2fe26aa68aac38149f329c2acfd`  
		Last Modified: Wed, 11 Sep 2024 02:50:47 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-cli`

```console
$ docker pull docker@sha256:f1e76d61b9ea8cb8eb44e93ea88091e16b4654658e883daae5f384de8f2e85b9
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
$ docker pull docker@sha256:01d856527b7e1b20d8e45a5c1cef71b5286d8a28460aac196a2239e549e9579f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67357792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d932cd3128d241bc878402ddc81dadfd0a412580aa8762a4e83e90499b3e893e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 10 Sep 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db09d90694836eab5370b7d5f552b34f5772781701b00fd4e7c3950519ee72`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 7.9 MB (7872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538dd9aacd297989031c915937096bfdd889838bf150c05212223a9b3507070`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfaa9e1957304899a8d16f9cf6fca1ddbf8debde833e6b68831a81b50ee6fc2`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616c0277b4c4b06061b57f23022504d07faea54188b3a5b0d5b51dfa4e990b9`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.4 MB (18432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692e2842ca25a9bf245905f6e29b66a65bbdc85f1873aae896b69370566a5f9`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cd67bc2f21b34aeca4c5627b6b4b5dbede9b76ea404dd4079e77464166d0b`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966ec96386506904d07991e403853675dc204da54a5e1fd0c1abd1e6da10197`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1d01552a20f6313745d5d6563fc8a44c75d0010cb7cd94399a1487838380`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:fd0e8c17c33bd8f8f44ac7cb928ac835388efce409ab36d6352961a00445c13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6137457032a6de0c065094e8eae103fd4499ace40937c93c7f7eedc1e32b6c3f`

```dockerfile
```

-	Layers:
	-	`sha256:2c4ce9d43b4d0578cd2db40ddc93a6d28f57ac5b491b4124ce0f14ed8e0909e4`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:f952f57a5301422a4807829a5d3ea4eea7243bfdf5e6e2e2f388ab208c50d08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62747370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c27f5a2b9894d0f6743db7cae0f3d726b24995bb7b584c07e36b319e7fe4bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 10 Sep 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1aa033c3dd6f9dcabf3e5db8b0d23e75bacc18083a9fc5fc3bf8dd32b531c9`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 17.1 MB (17141620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1075e78e61225557a73cb4df8bdb388a4e0a3a54d78fb029b95995467ee104`  
		Last Modified: Wed, 11 Sep 2024 02:01:31 GMT  
		Size: 17.8 MB (17783313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e371b1027e98e0af0c4a206108df3590c4135af5dd5c95267415707045a1884`  
		Last Modified: Wed, 11 Sep 2024 02:01:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226c034025ceb5a5072018428121e6627a7adea704c15385680801a1fd204fb`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dc19fcc1171071ce37cd5bee8802261a02276f6819a1116bba48770ae075f`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8c67ecfc62f1593fe9a21212a907a7475fb54a41741a093fe89f9a559fb989d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b29b3ddf761b15badc7ae0959d6005bbaf8b7b2f47dbb8de4b121a4ac60a45`

```dockerfile
```

-	Layers:
	-	`sha256:0955ae0eec0014c0f03bdaaf6a297e846d68da79d1e207c148f9ee0c3c7949cf`  
		Last Modified: Wed, 11 Sep 2024 02:01:29 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:26f4d2199b7ce26c7da298d81fdef751b09bf06c28ee8accc6981d27136233e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61775678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19294d0006d84ceec939bc3ceea2f87f956a91d6308cf3ba3e5646ca19bb4f51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 10 Sep 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cf2b1859f16ea4a3efc3ebdcff929c005fc44c05d7202ce69bbd5258d6989a`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 17.1 MB (17129209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e839e120983d5ca2057bee14103b0d822031e067c63b69d5f7e1d0845a446`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 17.8 MB (17771142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29362d9881a8e2c6fd23dac747f90a311fd37d78cbe5bfe2bc93d137ca3f7b93`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b72324b3582fd670d40a641281f441939c93b3eec0c1a40744ce9f42d416aef`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20947c69fcf36566adb6594921006179ce40d22530bd7d0a5c2f9b50e15639`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f773840574922d6e659b29fbcf461f41a91b4cadf462640657a42112be60bbcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0f8ab3b7a66d0459e31f704adf548456f24de05d66c5e8d00b312bf3b16046`

```dockerfile
```

-	Layers:
	-	`sha256:df52a7f089450cdc3de9670fb900382743ef2eed9fb8fa3771a370f4474f5d87`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5b06e0f5c7cb040b54f682062dec862502064a0b33a4c28099101a752f032188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63614518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b0eae91923bc21d58136d51ddacd96eaecc82b912f73aa585eee9cbccb015a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 10 Sep 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eada7f8d96edf35fbf9cccdfe2a31683f121351212c1d270f7a73b2e1f530e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.2 MB (17186842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b544e07d92af2d47cc10db55727317ca8ccc95a899db6ce41cdd41cb820c0`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ca207ff0f9c918c07b12825084dba82e9f8c9d490f1ffcf33fe0c7b45fab2`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c5493b785a7581afc20e1db4ba86a79bd5e5e8ef3dfa1ad64620028e196eb`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:49c13ed1077c9288d6731d1c032a854f6a56f59b9976404a639ce592ccb36ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9c5ae3da4b9ff13cf06b615700faf98c4d2d79d0b0552d105de12373e85149`

```dockerfile
```

-	Layers:
	-	`sha256:83d1c6b075d68f8bb4649dcdf1ca85edc3489dfbcaf519c18a61e94f8220b96e`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 38.2 KB (38227 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind`

```console
$ docker pull docker@sha256:294f99b7749b47d3bfac8535c231a6c47cd0f28be8205af83928b2dde18abda7
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
$ docker pull docker@sha256:9218d2dc6ab909992500f116eb49948376fb23f5cd9ccf427dd62b3d865ea49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131884120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371f9f35b2da407e86e3d81ea7a4efc0594697c3abb6b47bac15bbfa0533f293`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db09d90694836eab5370b7d5f552b34f5772781701b00fd4e7c3950519ee72`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 7.9 MB (7872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538dd9aacd297989031c915937096bfdd889838bf150c05212223a9b3507070`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfaa9e1957304899a8d16f9cf6fca1ddbf8debde833e6b68831a81b50ee6fc2`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616c0277b4c4b06061b57f23022504d07faea54188b3a5b0d5b51dfa4e990b9`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.4 MB (18432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692e2842ca25a9bf245905f6e29b66a65bbdc85f1873aae896b69370566a5f9`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cd67bc2f21b34aeca4c5627b6b4b5dbede9b76ea404dd4079e77464166d0b`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966ec96386506904d07991e403853675dc204da54a5e1fd0c1abd1e6da10197`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1d01552a20f6313745d5d6563fc8a44c75d0010cb7cd94399a1487838380`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c62cf5a0b55f78c6952456f627b45a4927bcd20a476a84feebb376a2e5afac`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 6.7 MB (6657921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3592c908208e8a16c99d3263902c97301ed446b46205bfcbb8d9ee8611123fa`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 89.2 KB (89218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd4c1986daa1bdd24f3621084f644cff84734eeb7aff037024fdf56f6aae3c1`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f41134be18ef5373326b3114ba85c9698be27a64dc12f0f60a1f5e6d0eac9`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 57.8 MB (57773398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaea47f5e1a31cc71bc565396dc93187e844d7f4ad7885746889e44dc40a4b`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a6f212eac3af392a8a5097e434764cff04c4e70ff2a9c1d4809c5c2e18d9e3`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:797fd1c255c0affbf4ea21c2af94c6f9904c76f433cacfb5aa44a15260ed50de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad921b63e93d9459a50c321f18aa4cad7866107facd5e54d1497bd0a6c86c6fd`

```dockerfile
```

-	Layers:
	-	`sha256:c9f2b5ad322c5b5af063de9a0bf790828d7771944a1fcec170e83a363c84a90c`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:0d871bea6fe47e7bf76b382ee2d4b128fe292b8fdb9082b21345c7d54cfdccae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123320023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cc1cb94b0e714568ec3d9021c42c78f629e704609cfc06069a093ad4a9fea0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1aa033c3dd6f9dcabf3e5db8b0d23e75bacc18083a9fc5fc3bf8dd32b531c9`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 17.1 MB (17141620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1075e78e61225557a73cb4df8bdb388a4e0a3a54d78fb029b95995467ee104`  
		Last Modified: Wed, 11 Sep 2024 02:01:31 GMT  
		Size: 17.8 MB (17783313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e371b1027e98e0af0c4a206108df3590c4135af5dd5c95267415707045a1884`  
		Last Modified: Wed, 11 Sep 2024 02:01:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226c034025ceb5a5072018428121e6627a7adea704c15385680801a1fd204fb`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dc19fcc1171071ce37cd5bee8802261a02276f6819a1116bba48770ae075f`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bf43051f6d401906c8b54ab26747cdead0e1b75ebec9c87fc12bf84d6dc5ed`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 7.0 MB (6984307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da17202765e315d32b089e1c25d097f8e0085fbb39264f5438693657418417`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 88.4 KB (88398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e960455cee8307842cd7579d74c83c6cb33ed93689bc96725f8ed7ebaf5d59b`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bbbc69f2a31b558cb399de570b4197e2b9834a828760b430ff42c27749a5b4`  
		Last Modified: Wed, 11 Sep 2024 02:50:52 GMT  
		Size: 53.5 MB (53494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103acb18844ccc79264ef2a516bb06bd5a0fecb9f01c581d3382253bdfa4423d`  
		Last Modified: Wed, 11 Sep 2024 02:50:51 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0f859154c8a30c4a41eb85bdfb5bafdd1617a0787c82c879a8a0575b531ac`  
		Last Modified: Wed, 11 Sep 2024 02:50:51 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5c5a017a1a9973a3ee57ddf3ddb4efd0e946b7da75bf289ba07ff8a9143ba0a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ce3bf47c18b13d056ef62e3576f93da7e2113326d337a31b0e4d5e835a21de`

```dockerfile
```

-	Layers:
	-	`sha256:1dbc2fbc5d04bf6005bd82413353aa41ed322750380a145666a8789b6900915b`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:68d52b1f8e3a30d5c9ebe8531f1ceb2b14389dc70dc7f73fc640cc2612b0cb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121668199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28baeefb60bbf0c1f288b4ba28c02be3975f6866a625e2122122b2366329bc7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cf2b1859f16ea4a3efc3ebdcff929c005fc44c05d7202ce69bbd5258d6989a`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 17.1 MB (17129209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e839e120983d5ca2057bee14103b0d822031e067c63b69d5f7e1d0845a446`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 17.8 MB (17771142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29362d9881a8e2c6fd23dac747f90a311fd37d78cbe5bfe2bc93d137ca3f7b93`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b72324b3582fd670d40a641281f441939c93b3eec0c1a40744ce9f42d416aef`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20947c69fcf36566adb6594921006179ce40d22530bd7d0a5c2f9b50e15639`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3903b8a5e83aa88438bc00e6a21cbfb21f98d72bf4a90554fbbc9a67c624287`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 6.3 MB (6308115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a08d98b7b8a40124cdff9c9cfb28790278fd87f375c88ea1239edb53b70aedb`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 84.5 KB (84482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c31665ca29d651d05ff3ca3fdc61f6a67ce69e291415b2651008e20b66e92dc`  
		Last Modified: Wed, 11 Sep 2024 02:50:55 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdde100f6de66fb3973ccfa58803d39516f505beacbffa025f887a7a952e3af9`  
		Last Modified: Wed, 11 Sep 2024 02:50:57 GMT  
		Size: 53.5 MB (53494122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131ea12518408d5c3f587e5ce4fe43d86e73f90603ed92f2ae54b2d321e2d47a`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f824312e672e112fdb8abcca34a0ae94e522859b14b6ba6b92d991d2e996ba7`  
		Last Modified: Wed, 11 Sep 2024 02:50:57 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4f69fea1e0e9bf4868790f90d7c7db9943225d34949695ace47f8784e814be93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db4c9ab2f89bb268cc28bcab911d9b7fc0a33b4e3b11b6b9baab0265727e3ae`

```dockerfile
```

-	Layers:
	-	`sha256:96e05737fa765bceaa6840ea6423d151ae12256c0d7a05d01ade85d7a178e388`  
		Last Modified: Wed, 11 Sep 2024 02:50:55 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e5140f28e7e82d172f34d88dfbd7a1bacbd4cbd3f24abdcaf1b0be485b916dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124152073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a7e2ef80ce4b0a550c648ddfb69a1953cdb927ca159fe704bf937bc8979d77`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eada7f8d96edf35fbf9cccdfe2a31683f121351212c1d270f7a73b2e1f530e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.2 MB (17186842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b544e07d92af2d47cc10db55727317ca8ccc95a899db6ce41cdd41cb820c0`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ca207ff0f9c918c07b12825084dba82e9f8c9d490f1ffcf33fe0c7b45fab2`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c5493b785a7581afc20e1db4ba86a79bd5e5e8ef3dfa1ad64620028e196eb`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e5be9720db99d659c53b6a67a1dd2ba6e958b7622248ab8dfc91c58d5c0f1d`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 7.0 MB (7034910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320bcabad1025e90ed07d105bd2724f1565672227ec5927061b082183adc6b11`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 98.7 KB (98650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9235e7f34f8cc28423dac4653e318c60d54cff3b0544a5e924074efdf31578`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9d4c07d55e9442550b66fb78c2d91de8856309dcc6875aa4c34aaa96f85316`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 53.4 MB (53398203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df4284aea7cda8255fd5026391b9b8b9db9af96da9875fe9db8f0185ac0ccd`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c51f22e855b132e7146b336aac0310cbe52e537cd77af861d9f27629b425ea6`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:fff328b2549d85866f264e626fb1fca2080ff3b685aa527410f3ea8ce95f38ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fd23934d6432c356a3df01ffbcf3ffbe9940918ffb9408d76137da20e3a2af`

```dockerfile
```

-	Layers:
	-	`sha256:23b22cd0119f1928542bdacdaf4016a4fa50c2fe26aa68aac38149f329c2acfd`  
		Last Modified: Wed, 11 Sep 2024 02:50:47 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:a85bf1d09cf0c684d7de3268d4c54b8bb152b79b53c1efa324cc8df94da42b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:5b34a2411903326499d2f67470d83ce97dc0183ca802e6fcf91ca1b564bf01bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154153776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e83a23dba859599f0adfa4a4b7996f23a41de2f5621f047074a9da77c6274f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db09d90694836eab5370b7d5f552b34f5772781701b00fd4e7c3950519ee72`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 7.9 MB (7872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538dd9aacd297989031c915937096bfdd889838bf150c05212223a9b3507070`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfaa9e1957304899a8d16f9cf6fca1ddbf8debde833e6b68831a81b50ee6fc2`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616c0277b4c4b06061b57f23022504d07faea54188b3a5b0d5b51dfa4e990b9`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.4 MB (18432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692e2842ca25a9bf245905f6e29b66a65bbdc85f1873aae896b69370566a5f9`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cd67bc2f21b34aeca4c5627b6b4b5dbede9b76ea404dd4079e77464166d0b`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966ec96386506904d07991e403853675dc204da54a5e1fd0c1abd1e6da10197`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1d01552a20f6313745d5d6563fc8a44c75d0010cb7cd94399a1487838380`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c62cf5a0b55f78c6952456f627b45a4927bcd20a476a84feebb376a2e5afac`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 6.7 MB (6657921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3592c908208e8a16c99d3263902c97301ed446b46205bfcbb8d9ee8611123fa`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 89.2 KB (89218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd4c1986daa1bdd24f3621084f644cff84734eeb7aff037024fdf56f6aae3c1`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f41134be18ef5373326b3114ba85c9698be27a64dc12f0f60a1f5e6d0eac9`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 57.8 MB (57773398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaea47f5e1a31cc71bc565396dc93187e844d7f4ad7885746889e44dc40a4b`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a6f212eac3af392a8a5097e434764cff04c4e70ff2a9c1d4809c5c2e18d9e3`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b065473b42eefb9a792eb005311c212c14df916c2575869263ae2fc25bd862`  
		Last Modified: Wed, 11 Sep 2024 03:48:49 GMT  
		Size: 981.0 KB (980986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852d28940731d27787147baf692114c5a57e84af5870515a9cf826785e61c97e`  
		Last Modified: Wed, 11 Sep 2024 03:48:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2754af7f7c8de794edb28a5c9f9ba8c90bdf84c274b9f556a39c0ea3240f1ab`  
		Last Modified: Wed, 11 Sep 2024 03:48:49 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636b57c4498bf4e949f7e09044a06c834e167dc3facda3697e3e1fff4b1739e8`  
		Last Modified: Wed, 11 Sep 2024 03:48:50 GMT  
		Size: 21.3 MB (21287315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f993cc096d161b79e4c922715fa6fe0c3d065ffa32abe11cf805a5937def91`  
		Last Modified: Wed, 11 Sep 2024 03:48:50 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c3fb49a3f69e9f44f3a3f159a35777da8859fb3530256aa2e196c953dfb4f8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7759138f227c5ac9b927aa368e0931f67ea0cd6196dfc9785aa8c3d4a23bacd`

```dockerfile
```

-	Layers:
	-	`sha256:7fc1f180c7e9851ada027667060ef9f9afc83a449caaccc1e42e3f58de86ba7d`  
		Last Modified: Wed, 11 Sep 2024 03:48:49 GMT  
		Size: 30.6 KB (30580 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bcedcdbefd4c0a8026ca435140dd2260a8b8de76d7f7ca5aa88030b661852828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148310987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d21859101d6a92e4bdb3cd0fc0396aab45b56110d1c29617704bda32774c45`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eada7f8d96edf35fbf9cccdfe2a31683f121351212c1d270f7a73b2e1f530e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.2 MB (17186842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b544e07d92af2d47cc10db55727317ca8ccc95a899db6ce41cdd41cb820c0`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ca207ff0f9c918c07b12825084dba82e9f8c9d490f1ffcf33fe0c7b45fab2`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c5493b785a7581afc20e1db4ba86a79bd5e5e8ef3dfa1ad64620028e196eb`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e5be9720db99d659c53b6a67a1dd2ba6e958b7622248ab8dfc91c58d5c0f1d`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 7.0 MB (7034910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320bcabad1025e90ed07d105bd2724f1565672227ec5927061b082183adc6b11`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 98.7 KB (98650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9235e7f34f8cc28423dac4653e318c60d54cff3b0544a5e924074efdf31578`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9d4c07d55e9442550b66fb78c2d91de8856309dcc6875aa4c34aaa96f85316`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 53.4 MB (53398203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df4284aea7cda8255fd5026391b9b8b9db9af96da9875fe9db8f0185ac0ccd`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c51f22e855b132e7146b336aac0310cbe52e537cd77af861d9f27629b425ea6`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61abcef331c5400bd552a2b6a5ecc6d03ecee4f12e9cf72c4a866ec26c4e2fe7`  
		Last Modified: Wed, 11 Sep 2024 03:48:43 GMT  
		Size: 1.0 MB (1023119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0a2f42af77b9a719e519573af0f3e531e92847a4b6f6095d42ffb21b48ae44`  
		Last Modified: Wed, 11 Sep 2024 03:48:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d713d1485ac825869be3a208d8d2699337d7ce096e81e2eeab4f7fc83fd0cc`  
		Last Modified: Wed, 11 Sep 2024 03:48:43 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c70f1919f2604484b0212c929c9881df57425101e48ec186fc604ca7b74c92e`  
		Last Modified: Wed, 11 Sep 2024 03:48:44 GMT  
		Size: 23.1 MB (23134441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab61b3f82263bbf4714ce5dc1a9816f6c16b3a159cd8e8cf873a94ce857aaeb1`  
		Last Modified: Wed, 11 Sep 2024 03:48:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0cdb6cb36b46b803fec1343b539275b39b36043f1df4e6fd6c3dc696980ca15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4a5c6803fcd314f69e271e0c35c18f4c05e2f48eaf0c977c298dcc6a732c71`

```dockerfile
```

-	Layers:
	-	`sha256:e6bc659420a6a66c2ebcb45c47ea7e01bff903c946a478d6fe5246ea077cdc54`  
		Last Modified: Wed, 11 Sep 2024 03:48:42 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:27ba43da317d5f4e4a2de77459eaf2e80d335f279f539e96243b98c45a9d504e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:a82aa3fe951a62771fff8170c24096425b50bc9e264286388152fa9b81712f5f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520410181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d257b03e5fade898fde7ea9c893f1a592471ad97e4ed6492b7b212b24c1ce0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 02:06:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 02:06:38 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 02:06:38 GMT
ENV DOCKER_VERSION=27.2.1
# Wed, 11 Sep 2024 02:06:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Wed, 11 Sep 2024 02:06:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:06:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Wed, 11 Sep 2024 02:06:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.windows-amd64.exe
# Wed, 11 Sep 2024 02:06:51 GMT
ENV DOCKER_BUILDX_SHA256=2bee3541fd1ed077d5f59141085f59345d0d0380d5749724e7088a3f02a113ca
# Wed, 11 Sep 2024 02:07:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:07:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 11 Sep 2024 02:07:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 11 Sep 2024 02:07:11 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 11 Sep 2024 02:07:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e2f86d5d1b2a5b865a052fc16b9166a550aed670add96ae7a6548a82b5b722`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8981ca84e679b362967aa517438bf611399eb20ea708bf9471e8f84100dfa7`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 342.6 KB (342630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0c9302154e848dc4bb0463644b87c8fae31baa96db751b75bc3a5d8195cbbe`  
		Last Modified: Wed, 11 Sep 2024 02:07:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41a22741d542661237a8d8e85456308c1cbd52d9498dfa0dfcbb566e1cc355a`  
		Last Modified: Wed, 11 Sep 2024 02:07:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6c4124d41c5d00b862e39fbfb5816f520bd94f02a0b82f582598effce81572`  
		Last Modified: Wed, 11 Sep 2024 02:07:37 GMT  
		Size: 18.9 MB (18913958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d5d0294c55c8e2b4a0761ea1eebf18f69f9d4c1846d0f84567e1edfe6e9217`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a83a411f2cf4b9fd720c3e578a348825577e84a74daff8dbfb10038588e534`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a320c69ba98bd2a4ead0142a9ee82e878541eb3d5f88492e25d026f0b0bc944`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97bc35449386503b924207a0b594a8b7459f1f88bdc3f42653bbe2b1841a475`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 19.3 MB (19269057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682ff78fabece6bcee7bf9b7da73568924352f978504e36a2cfc9110de462937`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8d54a118d4d3fe5c1dc907fadd1281ab71ea5600577a59956ba52226d5c42b`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8a9795b6d3907b92f407b716652f11fbc26030e2d49880aef8d6fdc0bfaea6`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f1a7d56c884d1afe4dc68cc0ac1f9189826bcee13efbb385acd42fc1ca3f9e`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 19.7 MB (19680496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:4d1e8b301b0c6ae81034443c38a212eec26f46cd4f59a332c68cd62eb0f09f92
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778456457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d2275e0c50e1a2778828b1c989942d819123b07583313ea0ac4522e03ce58c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 02:04:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 02:04:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 02:04:37 GMT
ENV DOCKER_VERSION=27.2.1
# Wed, 11 Sep 2024 02:04:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Wed, 11 Sep 2024 02:04:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:04:49 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Wed, 11 Sep 2024 02:04:49 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.windows-amd64.exe
# Wed, 11 Sep 2024 02:04:50 GMT
ENV DOCKER_BUILDX_SHA256=2bee3541fd1ed077d5f59141085f59345d0d0380d5749724e7088a3f02a113ca
# Wed, 11 Sep 2024 02:05:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:05:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 11 Sep 2024 02:05:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 11 Sep 2024 02:05:02 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 11 Sep 2024 02:05:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96305c41a993336ed17fc44e0e2bc51503e0e9b085c1f5cb642e396ab1d76ca5`  
		Last Modified: Wed, 11 Sep 2024 02:05:22 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90dcbc14d4e1aeb8ff8091b77163592eff3b0e11712fb83acf11cfca78be489`  
		Last Modified: Wed, 11 Sep 2024 02:05:23 GMT  
		Size: 330.4 KB (330375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae07341e5dcd520c87adee68815b0c466c03ab267fd0f757b67081ade1ff210`  
		Last Modified: Wed, 11 Sep 2024 02:05:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7973ed8b5a6d11094c8d4c2433a60c5a5fcfcb84b1f9163d275729bc8c9c75`  
		Last Modified: Wed, 11 Sep 2024 02:05:21 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076ffff23dfa564b4c5b62d9bda15f2f3257a29a8480e79f445bc1eac2976a6b`  
		Last Modified: Wed, 11 Sep 2024 02:05:23 GMT  
		Size: 18.9 MB (18911033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d1ca83016e2f178e867b86522bccc3c667320c2852da1a4d8c3ff193581105`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87986c7e4d5811794113e6437168a3f46ca14249232e5d226230840cbbeeeca`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5abefd76cb19ba3f5d50ae3b4dd66278517f9a1c2cb758f0a2898a960c55e8a`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c490aa0bb5fad395420b48468b3d32ffc9368901095cac9b73061ee54745c6`  
		Last Modified: Wed, 11 Sep 2024 02:05:20 GMT  
		Size: 19.3 MB (19264623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd8a155e1236c2faacf3433d3f3bfdbb991624d0ba0360937cca5d1e8a24ed2`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b554c6c79e64ef1bf1f3b97d2096f9cba53dc60c7ea8a8e37af03a3673285ea`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa1591f79c5c535c392829fc79152d4632d9a14cd22af2be1768c5b25ee91c0`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f570820d723f568887ddd5f8674cf19f3066dae96c6b4e052ac1b919e22596`  
		Last Modified: Wed, 11 Sep 2024 02:05:20 GMT  
		Size: 19.7 MB (19669920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:5cc4548517a5d2cd96e9f4922bbac7b8c09ecf55aec9d8941748e352a57dfe4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:4d1e8b301b0c6ae81034443c38a212eec26f46cd4f59a332c68cd62eb0f09f92
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778456457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d2275e0c50e1a2778828b1c989942d819123b07583313ea0ac4522e03ce58c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 02:04:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 02:04:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 02:04:37 GMT
ENV DOCKER_VERSION=27.2.1
# Wed, 11 Sep 2024 02:04:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Wed, 11 Sep 2024 02:04:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:04:49 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Wed, 11 Sep 2024 02:04:49 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.windows-amd64.exe
# Wed, 11 Sep 2024 02:04:50 GMT
ENV DOCKER_BUILDX_SHA256=2bee3541fd1ed077d5f59141085f59345d0d0380d5749724e7088a3f02a113ca
# Wed, 11 Sep 2024 02:05:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:05:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 11 Sep 2024 02:05:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 11 Sep 2024 02:05:02 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 11 Sep 2024 02:05:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96305c41a993336ed17fc44e0e2bc51503e0e9b085c1f5cb642e396ab1d76ca5`  
		Last Modified: Wed, 11 Sep 2024 02:05:22 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90dcbc14d4e1aeb8ff8091b77163592eff3b0e11712fb83acf11cfca78be489`  
		Last Modified: Wed, 11 Sep 2024 02:05:23 GMT  
		Size: 330.4 KB (330375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae07341e5dcd520c87adee68815b0c466c03ab267fd0f757b67081ade1ff210`  
		Last Modified: Wed, 11 Sep 2024 02:05:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7973ed8b5a6d11094c8d4c2433a60c5a5fcfcb84b1f9163d275729bc8c9c75`  
		Last Modified: Wed, 11 Sep 2024 02:05:21 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076ffff23dfa564b4c5b62d9bda15f2f3257a29a8480e79f445bc1eac2976a6b`  
		Last Modified: Wed, 11 Sep 2024 02:05:23 GMT  
		Size: 18.9 MB (18911033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d1ca83016e2f178e867b86522bccc3c667320c2852da1a4d8c3ff193581105`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87986c7e4d5811794113e6437168a3f46ca14249232e5d226230840cbbeeeca`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5abefd76cb19ba3f5d50ae3b4dd66278517f9a1c2cb758f0a2898a960c55e8a`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c490aa0bb5fad395420b48468b3d32ffc9368901095cac9b73061ee54745c6`  
		Last Modified: Wed, 11 Sep 2024 02:05:20 GMT  
		Size: 19.3 MB (19264623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd8a155e1236c2faacf3433d3f3bfdbb991624d0ba0360937cca5d1e8a24ed2`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b554c6c79e64ef1bf1f3b97d2096f9cba53dc60c7ea8a8e37af03a3673285ea`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa1591f79c5c535c392829fc79152d4632d9a14cd22af2be1768c5b25ee91c0`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f570820d723f568887ddd5f8674cf19f3066dae96c6b4e052ac1b919e22596`  
		Last Modified: Wed, 11 Sep 2024 02:05:20 GMT  
		Size: 19.7 MB (19669920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:421236c754a43a1f842fbcf8e4f9232fd85ea35de3ece64703e37089e70d5b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:a82aa3fe951a62771fff8170c24096425b50bc9e264286388152fa9b81712f5f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520410181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d257b03e5fade898fde7ea9c893f1a592471ad97e4ed6492b7b212b24c1ce0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 02:06:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 02:06:38 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 02:06:38 GMT
ENV DOCKER_VERSION=27.2.1
# Wed, 11 Sep 2024 02:06:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Wed, 11 Sep 2024 02:06:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:06:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Wed, 11 Sep 2024 02:06:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.windows-amd64.exe
# Wed, 11 Sep 2024 02:06:51 GMT
ENV DOCKER_BUILDX_SHA256=2bee3541fd1ed077d5f59141085f59345d0d0380d5749724e7088a3f02a113ca
# Wed, 11 Sep 2024 02:07:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:07:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 11 Sep 2024 02:07:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 11 Sep 2024 02:07:11 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 11 Sep 2024 02:07:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e2f86d5d1b2a5b865a052fc16b9166a550aed670add96ae7a6548a82b5b722`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8981ca84e679b362967aa517438bf611399eb20ea708bf9471e8f84100dfa7`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 342.6 KB (342630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0c9302154e848dc4bb0463644b87c8fae31baa96db751b75bc3a5d8195cbbe`  
		Last Modified: Wed, 11 Sep 2024 02:07:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41a22741d542661237a8d8e85456308c1cbd52d9498dfa0dfcbb566e1cc355a`  
		Last Modified: Wed, 11 Sep 2024 02:07:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6c4124d41c5d00b862e39fbfb5816f520bd94f02a0b82f582598effce81572`  
		Last Modified: Wed, 11 Sep 2024 02:07:37 GMT  
		Size: 18.9 MB (18913958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d5d0294c55c8e2b4a0761ea1eebf18f69f9d4c1846d0f84567e1edfe6e9217`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a83a411f2cf4b9fd720c3e578a348825577e84a74daff8dbfb10038588e534`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a320c69ba98bd2a4ead0142a9ee82e878541eb3d5f88492e25d026f0b0bc944`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97bc35449386503b924207a0b594a8b7459f1f88bdc3f42653bbe2b1841a475`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 19.3 MB (19269057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682ff78fabece6bcee7bf9b7da73568924352f978504e36a2cfc9110de462937`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8d54a118d4d3fe5c1dc907fadd1281ab71ea5600577a59956ba52226d5c42b`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8a9795b6d3907b92f407b716652f11fbc26030e2d49880aef8d6fdc0bfaea6`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f1a7d56c884d1afe4dc68cc0ac1f9189826bcee13efbb385acd42fc1ca3f9e`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 19.7 MB (19680496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.2`

```console
$ docker pull docker@sha256:294f99b7749b47d3bfac8535c231a6c47cd0f28be8205af83928b2dde18abda7
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

### `docker:27.2` - linux; amd64

```console
$ docker pull docker@sha256:9218d2dc6ab909992500f116eb49948376fb23f5cd9ccf427dd62b3d865ea49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131884120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371f9f35b2da407e86e3d81ea7a4efc0594697c3abb6b47bac15bbfa0533f293`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db09d90694836eab5370b7d5f552b34f5772781701b00fd4e7c3950519ee72`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 7.9 MB (7872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538dd9aacd297989031c915937096bfdd889838bf150c05212223a9b3507070`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfaa9e1957304899a8d16f9cf6fca1ddbf8debde833e6b68831a81b50ee6fc2`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616c0277b4c4b06061b57f23022504d07faea54188b3a5b0d5b51dfa4e990b9`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.4 MB (18432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692e2842ca25a9bf245905f6e29b66a65bbdc85f1873aae896b69370566a5f9`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cd67bc2f21b34aeca4c5627b6b4b5dbede9b76ea404dd4079e77464166d0b`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966ec96386506904d07991e403853675dc204da54a5e1fd0c1abd1e6da10197`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1d01552a20f6313745d5d6563fc8a44c75d0010cb7cd94399a1487838380`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c62cf5a0b55f78c6952456f627b45a4927bcd20a476a84feebb376a2e5afac`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 6.7 MB (6657921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3592c908208e8a16c99d3263902c97301ed446b46205bfcbb8d9ee8611123fa`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 89.2 KB (89218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd4c1986daa1bdd24f3621084f644cff84734eeb7aff037024fdf56f6aae3c1`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f41134be18ef5373326b3114ba85c9698be27a64dc12f0f60a1f5e6d0eac9`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 57.8 MB (57773398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaea47f5e1a31cc71bc565396dc93187e844d7f4ad7885746889e44dc40a4b`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a6f212eac3af392a8a5097e434764cff04c4e70ff2a9c1d4809c5c2e18d9e3`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2` - unknown; unknown

```console
$ docker pull docker@sha256:797fd1c255c0affbf4ea21c2af94c6f9904c76f433cacfb5aa44a15260ed50de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad921b63e93d9459a50c321f18aa4cad7866107facd5e54d1497bd0a6c86c6fd`

```dockerfile
```

-	Layers:
	-	`sha256:c9f2b5ad322c5b5af063de9a0bf790828d7771944a1fcec170e83a363c84a90c`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2` - linux; arm variant v6

```console
$ docker pull docker@sha256:0d871bea6fe47e7bf76b382ee2d4b128fe292b8fdb9082b21345c7d54cfdccae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123320023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cc1cb94b0e714568ec3d9021c42c78f629e704609cfc06069a093ad4a9fea0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1aa033c3dd6f9dcabf3e5db8b0d23e75bacc18083a9fc5fc3bf8dd32b531c9`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 17.1 MB (17141620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1075e78e61225557a73cb4df8bdb388a4e0a3a54d78fb029b95995467ee104`  
		Last Modified: Wed, 11 Sep 2024 02:01:31 GMT  
		Size: 17.8 MB (17783313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e371b1027e98e0af0c4a206108df3590c4135af5dd5c95267415707045a1884`  
		Last Modified: Wed, 11 Sep 2024 02:01:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226c034025ceb5a5072018428121e6627a7adea704c15385680801a1fd204fb`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dc19fcc1171071ce37cd5bee8802261a02276f6819a1116bba48770ae075f`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bf43051f6d401906c8b54ab26747cdead0e1b75ebec9c87fc12bf84d6dc5ed`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 7.0 MB (6984307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da17202765e315d32b089e1c25d097f8e0085fbb39264f5438693657418417`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 88.4 KB (88398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e960455cee8307842cd7579d74c83c6cb33ed93689bc96725f8ed7ebaf5d59b`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bbbc69f2a31b558cb399de570b4197e2b9834a828760b430ff42c27749a5b4`  
		Last Modified: Wed, 11 Sep 2024 02:50:52 GMT  
		Size: 53.5 MB (53494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103acb18844ccc79264ef2a516bb06bd5a0fecb9f01c581d3382253bdfa4423d`  
		Last Modified: Wed, 11 Sep 2024 02:50:51 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0f859154c8a30c4a41eb85bdfb5bafdd1617a0787c82c879a8a0575b531ac`  
		Last Modified: Wed, 11 Sep 2024 02:50:51 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2` - unknown; unknown

```console
$ docker pull docker@sha256:5c5a017a1a9973a3ee57ddf3ddb4efd0e946b7da75bf289ba07ff8a9143ba0a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ce3bf47c18b13d056ef62e3576f93da7e2113326d337a31b0e4d5e835a21de`

```dockerfile
```

-	Layers:
	-	`sha256:1dbc2fbc5d04bf6005bd82413353aa41ed322750380a145666a8789b6900915b`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2` - linux; arm variant v7

```console
$ docker pull docker@sha256:68d52b1f8e3a30d5c9ebe8531f1ceb2b14389dc70dc7f73fc640cc2612b0cb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121668199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28baeefb60bbf0c1f288b4ba28c02be3975f6866a625e2122122b2366329bc7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cf2b1859f16ea4a3efc3ebdcff929c005fc44c05d7202ce69bbd5258d6989a`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 17.1 MB (17129209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e839e120983d5ca2057bee14103b0d822031e067c63b69d5f7e1d0845a446`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 17.8 MB (17771142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29362d9881a8e2c6fd23dac747f90a311fd37d78cbe5bfe2bc93d137ca3f7b93`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b72324b3582fd670d40a641281f441939c93b3eec0c1a40744ce9f42d416aef`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20947c69fcf36566adb6594921006179ce40d22530bd7d0a5c2f9b50e15639`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3903b8a5e83aa88438bc00e6a21cbfb21f98d72bf4a90554fbbc9a67c624287`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 6.3 MB (6308115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a08d98b7b8a40124cdff9c9cfb28790278fd87f375c88ea1239edb53b70aedb`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 84.5 KB (84482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c31665ca29d651d05ff3ca3fdc61f6a67ce69e291415b2651008e20b66e92dc`  
		Last Modified: Wed, 11 Sep 2024 02:50:55 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdde100f6de66fb3973ccfa58803d39516f505beacbffa025f887a7a952e3af9`  
		Last Modified: Wed, 11 Sep 2024 02:50:57 GMT  
		Size: 53.5 MB (53494122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131ea12518408d5c3f587e5ce4fe43d86e73f90603ed92f2ae54b2d321e2d47a`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f824312e672e112fdb8abcca34a0ae94e522859b14b6ba6b92d991d2e996ba7`  
		Last Modified: Wed, 11 Sep 2024 02:50:57 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2` - unknown; unknown

```console
$ docker pull docker@sha256:4f69fea1e0e9bf4868790f90d7c7db9943225d34949695ace47f8784e814be93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db4c9ab2f89bb268cc28bcab911d9b7fc0a33b4e3b11b6b9baab0265727e3ae`

```dockerfile
```

-	Layers:
	-	`sha256:96e05737fa765bceaa6840ea6423d151ae12256c0d7a05d01ade85d7a178e388`  
		Last Modified: Wed, 11 Sep 2024 02:50:55 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e5140f28e7e82d172f34d88dfbd7a1bacbd4cbd3f24abdcaf1b0be485b916dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124152073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a7e2ef80ce4b0a550c648ddfb69a1953cdb927ca159fe704bf937bc8979d77`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eada7f8d96edf35fbf9cccdfe2a31683f121351212c1d270f7a73b2e1f530e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.2 MB (17186842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b544e07d92af2d47cc10db55727317ca8ccc95a899db6ce41cdd41cb820c0`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ca207ff0f9c918c07b12825084dba82e9f8c9d490f1ffcf33fe0c7b45fab2`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c5493b785a7581afc20e1db4ba86a79bd5e5e8ef3dfa1ad64620028e196eb`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e5be9720db99d659c53b6a67a1dd2ba6e958b7622248ab8dfc91c58d5c0f1d`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 7.0 MB (7034910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320bcabad1025e90ed07d105bd2724f1565672227ec5927061b082183adc6b11`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 98.7 KB (98650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9235e7f34f8cc28423dac4653e318c60d54cff3b0544a5e924074efdf31578`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9d4c07d55e9442550b66fb78c2d91de8856309dcc6875aa4c34aaa96f85316`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 53.4 MB (53398203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df4284aea7cda8255fd5026391b9b8b9db9af96da9875fe9db8f0185ac0ccd`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c51f22e855b132e7146b336aac0310cbe52e537cd77af861d9f27629b425ea6`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2` - unknown; unknown

```console
$ docker pull docker@sha256:fff328b2549d85866f264e626fb1fca2080ff3b685aa527410f3ea8ce95f38ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fd23934d6432c356a3df01ffbcf3ffbe9940918ffb9408d76137da20e3a2af`

```dockerfile
```

-	Layers:
	-	`sha256:23b22cd0119f1928542bdacdaf4016a4fa50c2fe26aa68aac38149f329c2acfd`  
		Last Modified: Wed, 11 Sep 2024 02:50:47 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2-cli`

```console
$ docker pull docker@sha256:f1e76d61b9ea8cb8eb44e93ea88091e16b4654658e883daae5f384de8f2e85b9
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

### `docker:27.2-cli` - linux; amd64

```console
$ docker pull docker@sha256:01d856527b7e1b20d8e45a5c1cef71b5286d8a28460aac196a2239e549e9579f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67357792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d932cd3128d241bc878402ddc81dadfd0a412580aa8762a4e83e90499b3e893e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 10 Sep 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db09d90694836eab5370b7d5f552b34f5772781701b00fd4e7c3950519ee72`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 7.9 MB (7872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538dd9aacd297989031c915937096bfdd889838bf150c05212223a9b3507070`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfaa9e1957304899a8d16f9cf6fca1ddbf8debde833e6b68831a81b50ee6fc2`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616c0277b4c4b06061b57f23022504d07faea54188b3a5b0d5b51dfa4e990b9`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.4 MB (18432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692e2842ca25a9bf245905f6e29b66a65bbdc85f1873aae896b69370566a5f9`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cd67bc2f21b34aeca4c5627b6b4b5dbede9b76ea404dd4079e77464166d0b`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966ec96386506904d07991e403853675dc204da54a5e1fd0c1abd1e6da10197`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1d01552a20f6313745d5d6563fc8a44c75d0010cb7cd94399a1487838380`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:fd0e8c17c33bd8f8f44ac7cb928ac835388efce409ab36d6352961a00445c13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6137457032a6de0c065094e8eae103fd4499ace40937c93c7f7eedc1e32b6c3f`

```dockerfile
```

-	Layers:
	-	`sha256:2c4ce9d43b4d0578cd2db40ddc93a6d28f57ac5b491b4124ce0f14ed8e0909e4`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:f952f57a5301422a4807829a5d3ea4eea7243bfdf5e6e2e2f388ab208c50d08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62747370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c27f5a2b9894d0f6743db7cae0f3d726b24995bb7b584c07e36b319e7fe4bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 10 Sep 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1aa033c3dd6f9dcabf3e5db8b0d23e75bacc18083a9fc5fc3bf8dd32b531c9`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 17.1 MB (17141620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1075e78e61225557a73cb4df8bdb388a4e0a3a54d78fb029b95995467ee104`  
		Last Modified: Wed, 11 Sep 2024 02:01:31 GMT  
		Size: 17.8 MB (17783313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e371b1027e98e0af0c4a206108df3590c4135af5dd5c95267415707045a1884`  
		Last Modified: Wed, 11 Sep 2024 02:01:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226c034025ceb5a5072018428121e6627a7adea704c15385680801a1fd204fb`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dc19fcc1171071ce37cd5bee8802261a02276f6819a1116bba48770ae075f`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8c67ecfc62f1593fe9a21212a907a7475fb54a41741a093fe89f9a559fb989d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b29b3ddf761b15badc7ae0959d6005bbaf8b7b2f47dbb8de4b121a4ac60a45`

```dockerfile
```

-	Layers:
	-	`sha256:0955ae0eec0014c0f03bdaaf6a297e846d68da79d1e207c148f9ee0c3c7949cf`  
		Last Modified: Wed, 11 Sep 2024 02:01:29 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:26f4d2199b7ce26c7da298d81fdef751b09bf06c28ee8accc6981d27136233e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61775678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19294d0006d84ceec939bc3ceea2f87f956a91d6308cf3ba3e5646ca19bb4f51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 10 Sep 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cf2b1859f16ea4a3efc3ebdcff929c005fc44c05d7202ce69bbd5258d6989a`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 17.1 MB (17129209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e839e120983d5ca2057bee14103b0d822031e067c63b69d5f7e1d0845a446`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 17.8 MB (17771142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29362d9881a8e2c6fd23dac747f90a311fd37d78cbe5bfe2bc93d137ca3f7b93`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b72324b3582fd670d40a641281f441939c93b3eec0c1a40744ce9f42d416aef`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20947c69fcf36566adb6594921006179ce40d22530bd7d0a5c2f9b50e15639`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f773840574922d6e659b29fbcf461f41a91b4cadf462640657a42112be60bbcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0f8ab3b7a66d0459e31f704adf548456f24de05d66c5e8d00b312bf3b16046`

```dockerfile
```

-	Layers:
	-	`sha256:df52a7f089450cdc3de9670fb900382743ef2eed9fb8fa3771a370f4474f5d87`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5b06e0f5c7cb040b54f682062dec862502064a0b33a4c28099101a752f032188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63614518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b0eae91923bc21d58136d51ddacd96eaecc82b912f73aa585eee9cbccb015a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 10 Sep 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eada7f8d96edf35fbf9cccdfe2a31683f121351212c1d270f7a73b2e1f530e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.2 MB (17186842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b544e07d92af2d47cc10db55727317ca8ccc95a899db6ce41cdd41cb820c0`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ca207ff0f9c918c07b12825084dba82e9f8c9d490f1ffcf33fe0c7b45fab2`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c5493b785a7581afc20e1db4ba86a79bd5e5e8ef3dfa1ad64620028e196eb`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:49c13ed1077c9288d6731d1c032a854f6a56f59b9976404a639ce592ccb36ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9c5ae3da4b9ff13cf06b615700faf98c4d2d79d0b0552d105de12373e85149`

```dockerfile
```

-	Layers:
	-	`sha256:83d1c6b075d68f8bb4649dcdf1ca85edc3489dfbcaf519c18a61e94f8220b96e`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 38.2 KB (38227 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2-dind`

```console
$ docker pull docker@sha256:294f99b7749b47d3bfac8535c231a6c47cd0f28be8205af83928b2dde18abda7
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

### `docker:27.2-dind` - linux; amd64

```console
$ docker pull docker@sha256:9218d2dc6ab909992500f116eb49948376fb23f5cd9ccf427dd62b3d865ea49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131884120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371f9f35b2da407e86e3d81ea7a4efc0594697c3abb6b47bac15bbfa0533f293`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db09d90694836eab5370b7d5f552b34f5772781701b00fd4e7c3950519ee72`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 7.9 MB (7872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538dd9aacd297989031c915937096bfdd889838bf150c05212223a9b3507070`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfaa9e1957304899a8d16f9cf6fca1ddbf8debde833e6b68831a81b50ee6fc2`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616c0277b4c4b06061b57f23022504d07faea54188b3a5b0d5b51dfa4e990b9`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.4 MB (18432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692e2842ca25a9bf245905f6e29b66a65bbdc85f1873aae896b69370566a5f9`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cd67bc2f21b34aeca4c5627b6b4b5dbede9b76ea404dd4079e77464166d0b`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966ec96386506904d07991e403853675dc204da54a5e1fd0c1abd1e6da10197`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1d01552a20f6313745d5d6563fc8a44c75d0010cb7cd94399a1487838380`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c62cf5a0b55f78c6952456f627b45a4927bcd20a476a84feebb376a2e5afac`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 6.7 MB (6657921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3592c908208e8a16c99d3263902c97301ed446b46205bfcbb8d9ee8611123fa`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 89.2 KB (89218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd4c1986daa1bdd24f3621084f644cff84734eeb7aff037024fdf56f6aae3c1`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f41134be18ef5373326b3114ba85c9698be27a64dc12f0f60a1f5e6d0eac9`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 57.8 MB (57773398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaea47f5e1a31cc71bc565396dc93187e844d7f4ad7885746889e44dc40a4b`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a6f212eac3af392a8a5097e434764cff04c4e70ff2a9c1d4809c5c2e18d9e3`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:797fd1c255c0affbf4ea21c2af94c6f9904c76f433cacfb5aa44a15260ed50de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad921b63e93d9459a50c321f18aa4cad7866107facd5e54d1497bd0a6c86c6fd`

```dockerfile
```

-	Layers:
	-	`sha256:c9f2b5ad322c5b5af063de9a0bf790828d7771944a1fcec170e83a363c84a90c`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:0d871bea6fe47e7bf76b382ee2d4b128fe292b8fdb9082b21345c7d54cfdccae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123320023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cc1cb94b0e714568ec3d9021c42c78f629e704609cfc06069a093ad4a9fea0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1aa033c3dd6f9dcabf3e5db8b0d23e75bacc18083a9fc5fc3bf8dd32b531c9`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 17.1 MB (17141620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1075e78e61225557a73cb4df8bdb388a4e0a3a54d78fb029b95995467ee104`  
		Last Modified: Wed, 11 Sep 2024 02:01:31 GMT  
		Size: 17.8 MB (17783313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e371b1027e98e0af0c4a206108df3590c4135af5dd5c95267415707045a1884`  
		Last Modified: Wed, 11 Sep 2024 02:01:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226c034025ceb5a5072018428121e6627a7adea704c15385680801a1fd204fb`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dc19fcc1171071ce37cd5bee8802261a02276f6819a1116bba48770ae075f`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bf43051f6d401906c8b54ab26747cdead0e1b75ebec9c87fc12bf84d6dc5ed`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 7.0 MB (6984307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da17202765e315d32b089e1c25d097f8e0085fbb39264f5438693657418417`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 88.4 KB (88398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e960455cee8307842cd7579d74c83c6cb33ed93689bc96725f8ed7ebaf5d59b`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bbbc69f2a31b558cb399de570b4197e2b9834a828760b430ff42c27749a5b4`  
		Last Modified: Wed, 11 Sep 2024 02:50:52 GMT  
		Size: 53.5 MB (53494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103acb18844ccc79264ef2a516bb06bd5a0fecb9f01c581d3382253bdfa4423d`  
		Last Modified: Wed, 11 Sep 2024 02:50:51 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0f859154c8a30c4a41eb85bdfb5bafdd1617a0787c82c879a8a0575b531ac`  
		Last Modified: Wed, 11 Sep 2024 02:50:51 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5c5a017a1a9973a3ee57ddf3ddb4efd0e946b7da75bf289ba07ff8a9143ba0a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ce3bf47c18b13d056ef62e3576f93da7e2113326d337a31b0e4d5e835a21de`

```dockerfile
```

-	Layers:
	-	`sha256:1dbc2fbc5d04bf6005bd82413353aa41ed322750380a145666a8789b6900915b`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:68d52b1f8e3a30d5c9ebe8531f1ceb2b14389dc70dc7f73fc640cc2612b0cb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121668199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28baeefb60bbf0c1f288b4ba28c02be3975f6866a625e2122122b2366329bc7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cf2b1859f16ea4a3efc3ebdcff929c005fc44c05d7202ce69bbd5258d6989a`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 17.1 MB (17129209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e839e120983d5ca2057bee14103b0d822031e067c63b69d5f7e1d0845a446`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 17.8 MB (17771142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29362d9881a8e2c6fd23dac747f90a311fd37d78cbe5bfe2bc93d137ca3f7b93`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b72324b3582fd670d40a641281f441939c93b3eec0c1a40744ce9f42d416aef`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20947c69fcf36566adb6594921006179ce40d22530bd7d0a5c2f9b50e15639`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3903b8a5e83aa88438bc00e6a21cbfb21f98d72bf4a90554fbbc9a67c624287`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 6.3 MB (6308115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a08d98b7b8a40124cdff9c9cfb28790278fd87f375c88ea1239edb53b70aedb`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 84.5 KB (84482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c31665ca29d651d05ff3ca3fdc61f6a67ce69e291415b2651008e20b66e92dc`  
		Last Modified: Wed, 11 Sep 2024 02:50:55 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdde100f6de66fb3973ccfa58803d39516f505beacbffa025f887a7a952e3af9`  
		Last Modified: Wed, 11 Sep 2024 02:50:57 GMT  
		Size: 53.5 MB (53494122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131ea12518408d5c3f587e5ce4fe43d86e73f90603ed92f2ae54b2d321e2d47a`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f824312e672e112fdb8abcca34a0ae94e522859b14b6ba6b92d991d2e996ba7`  
		Last Modified: Wed, 11 Sep 2024 02:50:57 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4f69fea1e0e9bf4868790f90d7c7db9943225d34949695ace47f8784e814be93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db4c9ab2f89bb268cc28bcab911d9b7fc0a33b4e3b11b6b9baab0265727e3ae`

```dockerfile
```

-	Layers:
	-	`sha256:96e05737fa765bceaa6840ea6423d151ae12256c0d7a05d01ade85d7a178e388`  
		Last Modified: Wed, 11 Sep 2024 02:50:55 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e5140f28e7e82d172f34d88dfbd7a1bacbd4cbd3f24abdcaf1b0be485b916dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124152073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a7e2ef80ce4b0a550c648ddfb69a1953cdb927ca159fe704bf937bc8979d77`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eada7f8d96edf35fbf9cccdfe2a31683f121351212c1d270f7a73b2e1f530e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.2 MB (17186842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b544e07d92af2d47cc10db55727317ca8ccc95a899db6ce41cdd41cb820c0`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ca207ff0f9c918c07b12825084dba82e9f8c9d490f1ffcf33fe0c7b45fab2`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c5493b785a7581afc20e1db4ba86a79bd5e5e8ef3dfa1ad64620028e196eb`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e5be9720db99d659c53b6a67a1dd2ba6e958b7622248ab8dfc91c58d5c0f1d`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 7.0 MB (7034910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320bcabad1025e90ed07d105bd2724f1565672227ec5927061b082183adc6b11`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 98.7 KB (98650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9235e7f34f8cc28423dac4653e318c60d54cff3b0544a5e924074efdf31578`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9d4c07d55e9442550b66fb78c2d91de8856309dcc6875aa4c34aaa96f85316`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 53.4 MB (53398203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df4284aea7cda8255fd5026391b9b8b9db9af96da9875fe9db8f0185ac0ccd`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c51f22e855b132e7146b336aac0310cbe52e537cd77af861d9f27629b425ea6`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:fff328b2549d85866f264e626fb1fca2080ff3b685aa527410f3ea8ce95f38ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fd23934d6432c356a3df01ffbcf3ffbe9940918ffb9408d76137da20e3a2af`

```dockerfile
```

-	Layers:
	-	`sha256:23b22cd0119f1928542bdacdaf4016a4fa50c2fe26aa68aac38149f329c2acfd`  
		Last Modified: Wed, 11 Sep 2024 02:50:47 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2-dind-rootless`

```console
$ docker pull docker@sha256:a85bf1d09cf0c684d7de3268d4c54b8bb152b79b53c1efa324cc8df94da42b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.2-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:5b34a2411903326499d2f67470d83ce97dc0183ca802e6fcf91ca1b564bf01bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154153776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e83a23dba859599f0adfa4a4b7996f23a41de2f5621f047074a9da77c6274f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db09d90694836eab5370b7d5f552b34f5772781701b00fd4e7c3950519ee72`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 7.9 MB (7872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538dd9aacd297989031c915937096bfdd889838bf150c05212223a9b3507070`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfaa9e1957304899a8d16f9cf6fca1ddbf8debde833e6b68831a81b50ee6fc2`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616c0277b4c4b06061b57f23022504d07faea54188b3a5b0d5b51dfa4e990b9`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.4 MB (18432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692e2842ca25a9bf245905f6e29b66a65bbdc85f1873aae896b69370566a5f9`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cd67bc2f21b34aeca4c5627b6b4b5dbede9b76ea404dd4079e77464166d0b`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966ec96386506904d07991e403853675dc204da54a5e1fd0c1abd1e6da10197`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1d01552a20f6313745d5d6563fc8a44c75d0010cb7cd94399a1487838380`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c62cf5a0b55f78c6952456f627b45a4927bcd20a476a84feebb376a2e5afac`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 6.7 MB (6657921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3592c908208e8a16c99d3263902c97301ed446b46205bfcbb8d9ee8611123fa`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 89.2 KB (89218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd4c1986daa1bdd24f3621084f644cff84734eeb7aff037024fdf56f6aae3c1`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f41134be18ef5373326b3114ba85c9698be27a64dc12f0f60a1f5e6d0eac9`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 57.8 MB (57773398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaea47f5e1a31cc71bc565396dc93187e844d7f4ad7885746889e44dc40a4b`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a6f212eac3af392a8a5097e434764cff04c4e70ff2a9c1d4809c5c2e18d9e3`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b065473b42eefb9a792eb005311c212c14df916c2575869263ae2fc25bd862`  
		Last Modified: Wed, 11 Sep 2024 03:48:49 GMT  
		Size: 981.0 KB (980986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852d28940731d27787147baf692114c5a57e84af5870515a9cf826785e61c97e`  
		Last Modified: Wed, 11 Sep 2024 03:48:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2754af7f7c8de794edb28a5c9f9ba8c90bdf84c274b9f556a39c0ea3240f1ab`  
		Last Modified: Wed, 11 Sep 2024 03:48:49 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636b57c4498bf4e949f7e09044a06c834e167dc3facda3697e3e1fff4b1739e8`  
		Last Modified: Wed, 11 Sep 2024 03:48:50 GMT  
		Size: 21.3 MB (21287315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f993cc096d161b79e4c922715fa6fe0c3d065ffa32abe11cf805a5937def91`  
		Last Modified: Wed, 11 Sep 2024 03:48:50 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c3fb49a3f69e9f44f3a3f159a35777da8859fb3530256aa2e196c953dfb4f8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7759138f227c5ac9b927aa368e0931f67ea0cd6196dfc9785aa8c3d4a23bacd`

```dockerfile
```

-	Layers:
	-	`sha256:7fc1f180c7e9851ada027667060ef9f9afc83a449caaccc1e42e3f58de86ba7d`  
		Last Modified: Wed, 11 Sep 2024 03:48:49 GMT  
		Size: 30.6 KB (30580 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bcedcdbefd4c0a8026ca435140dd2260a8b8de76d7f7ca5aa88030b661852828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148310987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d21859101d6a92e4bdb3cd0fc0396aab45b56110d1c29617704bda32774c45`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eada7f8d96edf35fbf9cccdfe2a31683f121351212c1d270f7a73b2e1f530e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.2 MB (17186842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b544e07d92af2d47cc10db55727317ca8ccc95a899db6ce41cdd41cb820c0`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ca207ff0f9c918c07b12825084dba82e9f8c9d490f1ffcf33fe0c7b45fab2`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c5493b785a7581afc20e1db4ba86a79bd5e5e8ef3dfa1ad64620028e196eb`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e5be9720db99d659c53b6a67a1dd2ba6e958b7622248ab8dfc91c58d5c0f1d`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 7.0 MB (7034910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320bcabad1025e90ed07d105bd2724f1565672227ec5927061b082183adc6b11`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 98.7 KB (98650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9235e7f34f8cc28423dac4653e318c60d54cff3b0544a5e924074efdf31578`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9d4c07d55e9442550b66fb78c2d91de8856309dcc6875aa4c34aaa96f85316`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 53.4 MB (53398203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df4284aea7cda8255fd5026391b9b8b9db9af96da9875fe9db8f0185ac0ccd`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c51f22e855b132e7146b336aac0310cbe52e537cd77af861d9f27629b425ea6`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61abcef331c5400bd552a2b6a5ecc6d03ecee4f12e9cf72c4a866ec26c4e2fe7`  
		Last Modified: Wed, 11 Sep 2024 03:48:43 GMT  
		Size: 1.0 MB (1023119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0a2f42af77b9a719e519573af0f3e531e92847a4b6f6095d42ffb21b48ae44`  
		Last Modified: Wed, 11 Sep 2024 03:48:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d713d1485ac825869be3a208d8d2699337d7ce096e81e2eeab4f7fc83fd0cc`  
		Last Modified: Wed, 11 Sep 2024 03:48:43 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c70f1919f2604484b0212c929c9881df57425101e48ec186fc604ca7b74c92e`  
		Last Modified: Wed, 11 Sep 2024 03:48:44 GMT  
		Size: 23.1 MB (23134441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab61b3f82263bbf4714ce5dc1a9816f6c16b3a159cd8e8cf873a94ce857aaeb1`  
		Last Modified: Wed, 11 Sep 2024 03:48:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0cdb6cb36b46b803fec1343b539275b39b36043f1df4e6fd6c3dc696980ca15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4a5c6803fcd314f69e271e0c35c18f4c05e2f48eaf0c977c298dcc6a732c71`

```dockerfile
```

-	Layers:
	-	`sha256:e6bc659420a6a66c2ebcb45c47ea7e01bff903c946a478d6fe5246ea077cdc54`  
		Last Modified: Wed, 11 Sep 2024 03:48:42 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2-windowsservercore`

```console
$ docker pull docker@sha256:27ba43da317d5f4e4a2de77459eaf2e80d335f279f539e96243b98c45a9d504e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `docker:27.2-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:a82aa3fe951a62771fff8170c24096425b50bc9e264286388152fa9b81712f5f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520410181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d257b03e5fade898fde7ea9c893f1a592471ad97e4ed6492b7b212b24c1ce0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 02:06:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 02:06:38 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 02:06:38 GMT
ENV DOCKER_VERSION=27.2.1
# Wed, 11 Sep 2024 02:06:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Wed, 11 Sep 2024 02:06:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:06:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Wed, 11 Sep 2024 02:06:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.windows-amd64.exe
# Wed, 11 Sep 2024 02:06:51 GMT
ENV DOCKER_BUILDX_SHA256=2bee3541fd1ed077d5f59141085f59345d0d0380d5749724e7088a3f02a113ca
# Wed, 11 Sep 2024 02:07:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:07:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 11 Sep 2024 02:07:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 11 Sep 2024 02:07:11 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 11 Sep 2024 02:07:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e2f86d5d1b2a5b865a052fc16b9166a550aed670add96ae7a6548a82b5b722`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8981ca84e679b362967aa517438bf611399eb20ea708bf9471e8f84100dfa7`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 342.6 KB (342630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0c9302154e848dc4bb0463644b87c8fae31baa96db751b75bc3a5d8195cbbe`  
		Last Modified: Wed, 11 Sep 2024 02:07:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41a22741d542661237a8d8e85456308c1cbd52d9498dfa0dfcbb566e1cc355a`  
		Last Modified: Wed, 11 Sep 2024 02:07:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6c4124d41c5d00b862e39fbfb5816f520bd94f02a0b82f582598effce81572`  
		Last Modified: Wed, 11 Sep 2024 02:07:37 GMT  
		Size: 18.9 MB (18913958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d5d0294c55c8e2b4a0761ea1eebf18f69f9d4c1846d0f84567e1edfe6e9217`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a83a411f2cf4b9fd720c3e578a348825577e84a74daff8dbfb10038588e534`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a320c69ba98bd2a4ead0142a9ee82e878541eb3d5f88492e25d026f0b0bc944`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97bc35449386503b924207a0b594a8b7459f1f88bdc3f42653bbe2b1841a475`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 19.3 MB (19269057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682ff78fabece6bcee7bf9b7da73568924352f978504e36a2cfc9110de462937`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8d54a118d4d3fe5c1dc907fadd1281ab71ea5600577a59956ba52226d5c42b`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8a9795b6d3907b92f407b716652f11fbc26030e2d49880aef8d6fdc0bfaea6`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f1a7d56c884d1afe4dc68cc0ac1f9189826bcee13efbb385acd42fc1ca3f9e`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 19.7 MB (19680496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.2-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:4d1e8b301b0c6ae81034443c38a212eec26f46cd4f59a332c68cd62eb0f09f92
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778456457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d2275e0c50e1a2778828b1c989942d819123b07583313ea0ac4522e03ce58c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 02:04:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 02:04:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 02:04:37 GMT
ENV DOCKER_VERSION=27.2.1
# Wed, 11 Sep 2024 02:04:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Wed, 11 Sep 2024 02:04:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:04:49 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Wed, 11 Sep 2024 02:04:49 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.windows-amd64.exe
# Wed, 11 Sep 2024 02:04:50 GMT
ENV DOCKER_BUILDX_SHA256=2bee3541fd1ed077d5f59141085f59345d0d0380d5749724e7088a3f02a113ca
# Wed, 11 Sep 2024 02:05:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:05:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 11 Sep 2024 02:05:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 11 Sep 2024 02:05:02 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 11 Sep 2024 02:05:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96305c41a993336ed17fc44e0e2bc51503e0e9b085c1f5cb642e396ab1d76ca5`  
		Last Modified: Wed, 11 Sep 2024 02:05:22 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90dcbc14d4e1aeb8ff8091b77163592eff3b0e11712fb83acf11cfca78be489`  
		Last Modified: Wed, 11 Sep 2024 02:05:23 GMT  
		Size: 330.4 KB (330375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae07341e5dcd520c87adee68815b0c466c03ab267fd0f757b67081ade1ff210`  
		Last Modified: Wed, 11 Sep 2024 02:05:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7973ed8b5a6d11094c8d4c2433a60c5a5fcfcb84b1f9163d275729bc8c9c75`  
		Last Modified: Wed, 11 Sep 2024 02:05:21 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076ffff23dfa564b4c5b62d9bda15f2f3257a29a8480e79f445bc1eac2976a6b`  
		Last Modified: Wed, 11 Sep 2024 02:05:23 GMT  
		Size: 18.9 MB (18911033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d1ca83016e2f178e867b86522bccc3c667320c2852da1a4d8c3ff193581105`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87986c7e4d5811794113e6437168a3f46ca14249232e5d226230840cbbeeeca`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5abefd76cb19ba3f5d50ae3b4dd66278517f9a1c2cb758f0a2898a960c55e8a`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c490aa0bb5fad395420b48468b3d32ffc9368901095cac9b73061ee54745c6`  
		Last Modified: Wed, 11 Sep 2024 02:05:20 GMT  
		Size: 19.3 MB (19264623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd8a155e1236c2faacf3433d3f3bfdbb991624d0ba0360937cca5d1e8a24ed2`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b554c6c79e64ef1bf1f3b97d2096f9cba53dc60c7ea8a8e37af03a3673285ea`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa1591f79c5c535c392829fc79152d4632d9a14cd22af2be1768c5b25ee91c0`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f570820d723f568887ddd5f8674cf19f3066dae96c6b4e052ac1b919e22596`  
		Last Modified: Wed, 11 Sep 2024 02:05:20 GMT  
		Size: 19.7 MB (19669920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.2-windowsservercore-1809`

```console
$ docker pull docker@sha256:5cc4548517a5d2cd96e9f4922bbac7b8c09ecf55aec9d8941748e352a57dfe4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `docker:27.2-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:4d1e8b301b0c6ae81034443c38a212eec26f46cd4f59a332c68cd62eb0f09f92
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778456457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d2275e0c50e1a2778828b1c989942d819123b07583313ea0ac4522e03ce58c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 02:04:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 02:04:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 02:04:37 GMT
ENV DOCKER_VERSION=27.2.1
# Wed, 11 Sep 2024 02:04:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Wed, 11 Sep 2024 02:04:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:04:49 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Wed, 11 Sep 2024 02:04:49 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.windows-amd64.exe
# Wed, 11 Sep 2024 02:04:50 GMT
ENV DOCKER_BUILDX_SHA256=2bee3541fd1ed077d5f59141085f59345d0d0380d5749724e7088a3f02a113ca
# Wed, 11 Sep 2024 02:05:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:05:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 11 Sep 2024 02:05:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 11 Sep 2024 02:05:02 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 11 Sep 2024 02:05:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96305c41a993336ed17fc44e0e2bc51503e0e9b085c1f5cb642e396ab1d76ca5`  
		Last Modified: Wed, 11 Sep 2024 02:05:22 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90dcbc14d4e1aeb8ff8091b77163592eff3b0e11712fb83acf11cfca78be489`  
		Last Modified: Wed, 11 Sep 2024 02:05:23 GMT  
		Size: 330.4 KB (330375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae07341e5dcd520c87adee68815b0c466c03ab267fd0f757b67081ade1ff210`  
		Last Modified: Wed, 11 Sep 2024 02:05:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7973ed8b5a6d11094c8d4c2433a60c5a5fcfcb84b1f9163d275729bc8c9c75`  
		Last Modified: Wed, 11 Sep 2024 02:05:21 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076ffff23dfa564b4c5b62d9bda15f2f3257a29a8480e79f445bc1eac2976a6b`  
		Last Modified: Wed, 11 Sep 2024 02:05:23 GMT  
		Size: 18.9 MB (18911033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d1ca83016e2f178e867b86522bccc3c667320c2852da1a4d8c3ff193581105`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87986c7e4d5811794113e6437168a3f46ca14249232e5d226230840cbbeeeca`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5abefd76cb19ba3f5d50ae3b4dd66278517f9a1c2cb758f0a2898a960c55e8a`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c490aa0bb5fad395420b48468b3d32ffc9368901095cac9b73061ee54745c6`  
		Last Modified: Wed, 11 Sep 2024 02:05:20 GMT  
		Size: 19.3 MB (19264623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd8a155e1236c2faacf3433d3f3bfdbb991624d0ba0360937cca5d1e8a24ed2`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b554c6c79e64ef1bf1f3b97d2096f9cba53dc60c7ea8a8e37af03a3673285ea`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa1591f79c5c535c392829fc79152d4632d9a14cd22af2be1768c5b25ee91c0`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f570820d723f568887ddd5f8674cf19f3066dae96c6b4e052ac1b919e22596`  
		Last Modified: Wed, 11 Sep 2024 02:05:20 GMT  
		Size: 19.7 MB (19669920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.2-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:421236c754a43a1f842fbcf8e4f9232fd85ea35de3ece64703e37089e70d5b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `docker:27.2-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:a82aa3fe951a62771fff8170c24096425b50bc9e264286388152fa9b81712f5f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520410181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d257b03e5fade898fde7ea9c893f1a592471ad97e4ed6492b7b212b24c1ce0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 02:06:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 02:06:38 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 02:06:38 GMT
ENV DOCKER_VERSION=27.2.1
# Wed, 11 Sep 2024 02:06:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Wed, 11 Sep 2024 02:06:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:06:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Wed, 11 Sep 2024 02:06:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.windows-amd64.exe
# Wed, 11 Sep 2024 02:06:51 GMT
ENV DOCKER_BUILDX_SHA256=2bee3541fd1ed077d5f59141085f59345d0d0380d5749724e7088a3f02a113ca
# Wed, 11 Sep 2024 02:07:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:07:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 11 Sep 2024 02:07:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 11 Sep 2024 02:07:11 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 11 Sep 2024 02:07:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e2f86d5d1b2a5b865a052fc16b9166a550aed670add96ae7a6548a82b5b722`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8981ca84e679b362967aa517438bf611399eb20ea708bf9471e8f84100dfa7`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 342.6 KB (342630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0c9302154e848dc4bb0463644b87c8fae31baa96db751b75bc3a5d8195cbbe`  
		Last Modified: Wed, 11 Sep 2024 02:07:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41a22741d542661237a8d8e85456308c1cbd52d9498dfa0dfcbb566e1cc355a`  
		Last Modified: Wed, 11 Sep 2024 02:07:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6c4124d41c5d00b862e39fbfb5816f520bd94f02a0b82f582598effce81572`  
		Last Modified: Wed, 11 Sep 2024 02:07:37 GMT  
		Size: 18.9 MB (18913958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d5d0294c55c8e2b4a0761ea1eebf18f69f9d4c1846d0f84567e1edfe6e9217`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a83a411f2cf4b9fd720c3e578a348825577e84a74daff8dbfb10038588e534`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a320c69ba98bd2a4ead0142a9ee82e878541eb3d5f88492e25d026f0b0bc944`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97bc35449386503b924207a0b594a8b7459f1f88bdc3f42653bbe2b1841a475`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 19.3 MB (19269057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682ff78fabece6bcee7bf9b7da73568924352f978504e36a2cfc9110de462937`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8d54a118d4d3fe5c1dc907fadd1281ab71ea5600577a59956ba52226d5c42b`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8a9795b6d3907b92f407b716652f11fbc26030e2d49880aef8d6fdc0bfaea6`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f1a7d56c884d1afe4dc68cc0ac1f9189826bcee13efbb385acd42fc1ca3f9e`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 19.7 MB (19680496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.2.1`

```console
$ docker pull docker@sha256:294f99b7749b47d3bfac8535c231a6c47cd0f28be8205af83928b2dde18abda7
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

### `docker:27.2.1` - linux; amd64

```console
$ docker pull docker@sha256:9218d2dc6ab909992500f116eb49948376fb23f5cd9ccf427dd62b3d865ea49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131884120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371f9f35b2da407e86e3d81ea7a4efc0594697c3abb6b47bac15bbfa0533f293`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db09d90694836eab5370b7d5f552b34f5772781701b00fd4e7c3950519ee72`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 7.9 MB (7872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538dd9aacd297989031c915937096bfdd889838bf150c05212223a9b3507070`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfaa9e1957304899a8d16f9cf6fca1ddbf8debde833e6b68831a81b50ee6fc2`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616c0277b4c4b06061b57f23022504d07faea54188b3a5b0d5b51dfa4e990b9`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.4 MB (18432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692e2842ca25a9bf245905f6e29b66a65bbdc85f1873aae896b69370566a5f9`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cd67bc2f21b34aeca4c5627b6b4b5dbede9b76ea404dd4079e77464166d0b`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966ec96386506904d07991e403853675dc204da54a5e1fd0c1abd1e6da10197`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1d01552a20f6313745d5d6563fc8a44c75d0010cb7cd94399a1487838380`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c62cf5a0b55f78c6952456f627b45a4927bcd20a476a84feebb376a2e5afac`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 6.7 MB (6657921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3592c908208e8a16c99d3263902c97301ed446b46205bfcbb8d9ee8611123fa`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 89.2 KB (89218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd4c1986daa1bdd24f3621084f644cff84734eeb7aff037024fdf56f6aae3c1`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f41134be18ef5373326b3114ba85c9698be27a64dc12f0f60a1f5e6d0eac9`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 57.8 MB (57773398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaea47f5e1a31cc71bc565396dc93187e844d7f4ad7885746889e44dc40a4b`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a6f212eac3af392a8a5097e434764cff04c4e70ff2a9c1d4809c5c2e18d9e3`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1` - unknown; unknown

```console
$ docker pull docker@sha256:797fd1c255c0affbf4ea21c2af94c6f9904c76f433cacfb5aa44a15260ed50de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad921b63e93d9459a50c321f18aa4cad7866107facd5e54d1497bd0a6c86c6fd`

```dockerfile
```

-	Layers:
	-	`sha256:c9f2b5ad322c5b5af063de9a0bf790828d7771944a1fcec170e83a363c84a90c`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1` - linux; arm variant v6

```console
$ docker pull docker@sha256:0d871bea6fe47e7bf76b382ee2d4b128fe292b8fdb9082b21345c7d54cfdccae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123320023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cc1cb94b0e714568ec3d9021c42c78f629e704609cfc06069a093ad4a9fea0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1aa033c3dd6f9dcabf3e5db8b0d23e75bacc18083a9fc5fc3bf8dd32b531c9`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 17.1 MB (17141620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1075e78e61225557a73cb4df8bdb388a4e0a3a54d78fb029b95995467ee104`  
		Last Modified: Wed, 11 Sep 2024 02:01:31 GMT  
		Size: 17.8 MB (17783313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e371b1027e98e0af0c4a206108df3590c4135af5dd5c95267415707045a1884`  
		Last Modified: Wed, 11 Sep 2024 02:01:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226c034025ceb5a5072018428121e6627a7adea704c15385680801a1fd204fb`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dc19fcc1171071ce37cd5bee8802261a02276f6819a1116bba48770ae075f`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bf43051f6d401906c8b54ab26747cdead0e1b75ebec9c87fc12bf84d6dc5ed`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 7.0 MB (6984307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da17202765e315d32b089e1c25d097f8e0085fbb39264f5438693657418417`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 88.4 KB (88398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e960455cee8307842cd7579d74c83c6cb33ed93689bc96725f8ed7ebaf5d59b`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bbbc69f2a31b558cb399de570b4197e2b9834a828760b430ff42c27749a5b4`  
		Last Modified: Wed, 11 Sep 2024 02:50:52 GMT  
		Size: 53.5 MB (53494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103acb18844ccc79264ef2a516bb06bd5a0fecb9f01c581d3382253bdfa4423d`  
		Last Modified: Wed, 11 Sep 2024 02:50:51 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0f859154c8a30c4a41eb85bdfb5bafdd1617a0787c82c879a8a0575b531ac`  
		Last Modified: Wed, 11 Sep 2024 02:50:51 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1` - unknown; unknown

```console
$ docker pull docker@sha256:5c5a017a1a9973a3ee57ddf3ddb4efd0e946b7da75bf289ba07ff8a9143ba0a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ce3bf47c18b13d056ef62e3576f93da7e2113326d337a31b0e4d5e835a21de`

```dockerfile
```

-	Layers:
	-	`sha256:1dbc2fbc5d04bf6005bd82413353aa41ed322750380a145666a8789b6900915b`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1` - linux; arm variant v7

```console
$ docker pull docker@sha256:68d52b1f8e3a30d5c9ebe8531f1ceb2b14389dc70dc7f73fc640cc2612b0cb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121668199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28baeefb60bbf0c1f288b4ba28c02be3975f6866a625e2122122b2366329bc7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cf2b1859f16ea4a3efc3ebdcff929c005fc44c05d7202ce69bbd5258d6989a`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 17.1 MB (17129209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e839e120983d5ca2057bee14103b0d822031e067c63b69d5f7e1d0845a446`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 17.8 MB (17771142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29362d9881a8e2c6fd23dac747f90a311fd37d78cbe5bfe2bc93d137ca3f7b93`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b72324b3582fd670d40a641281f441939c93b3eec0c1a40744ce9f42d416aef`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20947c69fcf36566adb6594921006179ce40d22530bd7d0a5c2f9b50e15639`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3903b8a5e83aa88438bc00e6a21cbfb21f98d72bf4a90554fbbc9a67c624287`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 6.3 MB (6308115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a08d98b7b8a40124cdff9c9cfb28790278fd87f375c88ea1239edb53b70aedb`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 84.5 KB (84482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c31665ca29d651d05ff3ca3fdc61f6a67ce69e291415b2651008e20b66e92dc`  
		Last Modified: Wed, 11 Sep 2024 02:50:55 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdde100f6de66fb3973ccfa58803d39516f505beacbffa025f887a7a952e3af9`  
		Last Modified: Wed, 11 Sep 2024 02:50:57 GMT  
		Size: 53.5 MB (53494122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131ea12518408d5c3f587e5ce4fe43d86e73f90603ed92f2ae54b2d321e2d47a`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f824312e672e112fdb8abcca34a0ae94e522859b14b6ba6b92d991d2e996ba7`  
		Last Modified: Wed, 11 Sep 2024 02:50:57 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1` - unknown; unknown

```console
$ docker pull docker@sha256:4f69fea1e0e9bf4868790f90d7c7db9943225d34949695ace47f8784e814be93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db4c9ab2f89bb268cc28bcab911d9b7fc0a33b4e3b11b6b9baab0265727e3ae`

```dockerfile
```

-	Layers:
	-	`sha256:96e05737fa765bceaa6840ea6423d151ae12256c0d7a05d01ade85d7a178e388`  
		Last Modified: Wed, 11 Sep 2024 02:50:55 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e5140f28e7e82d172f34d88dfbd7a1bacbd4cbd3f24abdcaf1b0be485b916dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124152073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a7e2ef80ce4b0a550c648ddfb69a1953cdb927ca159fe704bf937bc8979d77`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eada7f8d96edf35fbf9cccdfe2a31683f121351212c1d270f7a73b2e1f530e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.2 MB (17186842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b544e07d92af2d47cc10db55727317ca8ccc95a899db6ce41cdd41cb820c0`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ca207ff0f9c918c07b12825084dba82e9f8c9d490f1ffcf33fe0c7b45fab2`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c5493b785a7581afc20e1db4ba86a79bd5e5e8ef3dfa1ad64620028e196eb`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e5be9720db99d659c53b6a67a1dd2ba6e958b7622248ab8dfc91c58d5c0f1d`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 7.0 MB (7034910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320bcabad1025e90ed07d105bd2724f1565672227ec5927061b082183adc6b11`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 98.7 KB (98650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9235e7f34f8cc28423dac4653e318c60d54cff3b0544a5e924074efdf31578`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9d4c07d55e9442550b66fb78c2d91de8856309dcc6875aa4c34aaa96f85316`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 53.4 MB (53398203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df4284aea7cda8255fd5026391b9b8b9db9af96da9875fe9db8f0185ac0ccd`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c51f22e855b132e7146b336aac0310cbe52e537cd77af861d9f27629b425ea6`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1` - unknown; unknown

```console
$ docker pull docker@sha256:fff328b2549d85866f264e626fb1fca2080ff3b685aa527410f3ea8ce95f38ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fd23934d6432c356a3df01ffbcf3ffbe9940918ffb9408d76137da20e3a2af`

```dockerfile
```

-	Layers:
	-	`sha256:23b22cd0119f1928542bdacdaf4016a4fa50c2fe26aa68aac38149f329c2acfd`  
		Last Modified: Wed, 11 Sep 2024 02:50:47 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2.1-alpine3.20`

```console
$ docker pull docker@sha256:294f99b7749b47d3bfac8535c231a6c47cd0f28be8205af83928b2dde18abda7
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

### `docker:27.2.1-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:9218d2dc6ab909992500f116eb49948376fb23f5cd9ccf427dd62b3d865ea49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131884120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371f9f35b2da407e86e3d81ea7a4efc0594697c3abb6b47bac15bbfa0533f293`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db09d90694836eab5370b7d5f552b34f5772781701b00fd4e7c3950519ee72`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 7.9 MB (7872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538dd9aacd297989031c915937096bfdd889838bf150c05212223a9b3507070`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfaa9e1957304899a8d16f9cf6fca1ddbf8debde833e6b68831a81b50ee6fc2`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616c0277b4c4b06061b57f23022504d07faea54188b3a5b0d5b51dfa4e990b9`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.4 MB (18432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692e2842ca25a9bf245905f6e29b66a65bbdc85f1873aae896b69370566a5f9`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cd67bc2f21b34aeca4c5627b6b4b5dbede9b76ea404dd4079e77464166d0b`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966ec96386506904d07991e403853675dc204da54a5e1fd0c1abd1e6da10197`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1d01552a20f6313745d5d6563fc8a44c75d0010cb7cd94399a1487838380`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c62cf5a0b55f78c6952456f627b45a4927bcd20a476a84feebb376a2e5afac`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 6.7 MB (6657921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3592c908208e8a16c99d3263902c97301ed446b46205bfcbb8d9ee8611123fa`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 89.2 KB (89218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd4c1986daa1bdd24f3621084f644cff84734eeb7aff037024fdf56f6aae3c1`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f41134be18ef5373326b3114ba85c9698be27a64dc12f0f60a1f5e6d0eac9`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 57.8 MB (57773398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaea47f5e1a31cc71bc565396dc93187e844d7f4ad7885746889e44dc40a4b`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a6f212eac3af392a8a5097e434764cff04c4e70ff2a9c1d4809c5c2e18d9e3`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:797fd1c255c0affbf4ea21c2af94c6f9904c76f433cacfb5aa44a15260ed50de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad921b63e93d9459a50c321f18aa4cad7866107facd5e54d1497bd0a6c86c6fd`

```dockerfile
```

-	Layers:
	-	`sha256:c9f2b5ad322c5b5af063de9a0bf790828d7771944a1fcec170e83a363c84a90c`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:0d871bea6fe47e7bf76b382ee2d4b128fe292b8fdb9082b21345c7d54cfdccae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123320023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cc1cb94b0e714568ec3d9021c42c78f629e704609cfc06069a093ad4a9fea0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1aa033c3dd6f9dcabf3e5db8b0d23e75bacc18083a9fc5fc3bf8dd32b531c9`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 17.1 MB (17141620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1075e78e61225557a73cb4df8bdb388a4e0a3a54d78fb029b95995467ee104`  
		Last Modified: Wed, 11 Sep 2024 02:01:31 GMT  
		Size: 17.8 MB (17783313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e371b1027e98e0af0c4a206108df3590c4135af5dd5c95267415707045a1884`  
		Last Modified: Wed, 11 Sep 2024 02:01:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226c034025ceb5a5072018428121e6627a7adea704c15385680801a1fd204fb`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dc19fcc1171071ce37cd5bee8802261a02276f6819a1116bba48770ae075f`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bf43051f6d401906c8b54ab26747cdead0e1b75ebec9c87fc12bf84d6dc5ed`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 7.0 MB (6984307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da17202765e315d32b089e1c25d097f8e0085fbb39264f5438693657418417`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 88.4 KB (88398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e960455cee8307842cd7579d74c83c6cb33ed93689bc96725f8ed7ebaf5d59b`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bbbc69f2a31b558cb399de570b4197e2b9834a828760b430ff42c27749a5b4`  
		Last Modified: Wed, 11 Sep 2024 02:50:52 GMT  
		Size: 53.5 MB (53494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103acb18844ccc79264ef2a516bb06bd5a0fecb9f01c581d3382253bdfa4423d`  
		Last Modified: Wed, 11 Sep 2024 02:50:51 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0f859154c8a30c4a41eb85bdfb5bafdd1617a0787c82c879a8a0575b531ac`  
		Last Modified: Wed, 11 Sep 2024 02:50:51 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:5c5a017a1a9973a3ee57ddf3ddb4efd0e946b7da75bf289ba07ff8a9143ba0a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ce3bf47c18b13d056ef62e3576f93da7e2113326d337a31b0e4d5e835a21de`

```dockerfile
```

-	Layers:
	-	`sha256:1dbc2fbc5d04bf6005bd82413353aa41ed322750380a145666a8789b6900915b`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:68d52b1f8e3a30d5c9ebe8531f1ceb2b14389dc70dc7f73fc640cc2612b0cb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121668199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28baeefb60bbf0c1f288b4ba28c02be3975f6866a625e2122122b2366329bc7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cf2b1859f16ea4a3efc3ebdcff929c005fc44c05d7202ce69bbd5258d6989a`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 17.1 MB (17129209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e839e120983d5ca2057bee14103b0d822031e067c63b69d5f7e1d0845a446`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 17.8 MB (17771142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29362d9881a8e2c6fd23dac747f90a311fd37d78cbe5bfe2bc93d137ca3f7b93`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b72324b3582fd670d40a641281f441939c93b3eec0c1a40744ce9f42d416aef`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20947c69fcf36566adb6594921006179ce40d22530bd7d0a5c2f9b50e15639`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3903b8a5e83aa88438bc00e6a21cbfb21f98d72bf4a90554fbbc9a67c624287`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 6.3 MB (6308115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a08d98b7b8a40124cdff9c9cfb28790278fd87f375c88ea1239edb53b70aedb`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 84.5 KB (84482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c31665ca29d651d05ff3ca3fdc61f6a67ce69e291415b2651008e20b66e92dc`  
		Last Modified: Wed, 11 Sep 2024 02:50:55 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdde100f6de66fb3973ccfa58803d39516f505beacbffa025f887a7a952e3af9`  
		Last Modified: Wed, 11 Sep 2024 02:50:57 GMT  
		Size: 53.5 MB (53494122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131ea12518408d5c3f587e5ce4fe43d86e73f90603ed92f2ae54b2d321e2d47a`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f824312e672e112fdb8abcca34a0ae94e522859b14b6ba6b92d991d2e996ba7`  
		Last Modified: Wed, 11 Sep 2024 02:50:57 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:4f69fea1e0e9bf4868790f90d7c7db9943225d34949695ace47f8784e814be93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db4c9ab2f89bb268cc28bcab911d9b7fc0a33b4e3b11b6b9baab0265727e3ae`

```dockerfile
```

-	Layers:
	-	`sha256:96e05737fa765bceaa6840ea6423d151ae12256c0d7a05d01ade85d7a178e388`  
		Last Modified: Wed, 11 Sep 2024 02:50:55 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e5140f28e7e82d172f34d88dfbd7a1bacbd4cbd3f24abdcaf1b0be485b916dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124152073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a7e2ef80ce4b0a550c648ddfb69a1953cdb927ca159fe704bf937bc8979d77`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eada7f8d96edf35fbf9cccdfe2a31683f121351212c1d270f7a73b2e1f530e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.2 MB (17186842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b544e07d92af2d47cc10db55727317ca8ccc95a899db6ce41cdd41cb820c0`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ca207ff0f9c918c07b12825084dba82e9f8c9d490f1ffcf33fe0c7b45fab2`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c5493b785a7581afc20e1db4ba86a79bd5e5e8ef3dfa1ad64620028e196eb`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e5be9720db99d659c53b6a67a1dd2ba6e958b7622248ab8dfc91c58d5c0f1d`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 7.0 MB (7034910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320bcabad1025e90ed07d105bd2724f1565672227ec5927061b082183adc6b11`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 98.7 KB (98650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9235e7f34f8cc28423dac4653e318c60d54cff3b0544a5e924074efdf31578`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9d4c07d55e9442550b66fb78c2d91de8856309dcc6875aa4c34aaa96f85316`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 53.4 MB (53398203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df4284aea7cda8255fd5026391b9b8b9db9af96da9875fe9db8f0185ac0ccd`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c51f22e855b132e7146b336aac0310cbe52e537cd77af861d9f27629b425ea6`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:fff328b2549d85866f264e626fb1fca2080ff3b685aa527410f3ea8ce95f38ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fd23934d6432c356a3df01ffbcf3ffbe9940918ffb9408d76137da20e3a2af`

```dockerfile
```

-	Layers:
	-	`sha256:23b22cd0119f1928542bdacdaf4016a4fa50c2fe26aa68aac38149f329c2acfd`  
		Last Modified: Wed, 11 Sep 2024 02:50:47 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2.1-cli`

```console
$ docker pull docker@sha256:f1e76d61b9ea8cb8eb44e93ea88091e16b4654658e883daae5f384de8f2e85b9
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

### `docker:27.2.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:01d856527b7e1b20d8e45a5c1cef71b5286d8a28460aac196a2239e549e9579f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67357792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d932cd3128d241bc878402ddc81dadfd0a412580aa8762a4e83e90499b3e893e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 10 Sep 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db09d90694836eab5370b7d5f552b34f5772781701b00fd4e7c3950519ee72`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 7.9 MB (7872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538dd9aacd297989031c915937096bfdd889838bf150c05212223a9b3507070`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfaa9e1957304899a8d16f9cf6fca1ddbf8debde833e6b68831a81b50ee6fc2`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616c0277b4c4b06061b57f23022504d07faea54188b3a5b0d5b51dfa4e990b9`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.4 MB (18432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692e2842ca25a9bf245905f6e29b66a65bbdc85f1873aae896b69370566a5f9`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cd67bc2f21b34aeca4c5627b6b4b5dbede9b76ea404dd4079e77464166d0b`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966ec96386506904d07991e403853675dc204da54a5e1fd0c1abd1e6da10197`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1d01552a20f6313745d5d6563fc8a44c75d0010cb7cd94399a1487838380`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:fd0e8c17c33bd8f8f44ac7cb928ac835388efce409ab36d6352961a00445c13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6137457032a6de0c065094e8eae103fd4499ace40937c93c7f7eedc1e32b6c3f`

```dockerfile
```

-	Layers:
	-	`sha256:2c4ce9d43b4d0578cd2db40ddc93a6d28f57ac5b491b4124ce0f14ed8e0909e4`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:f952f57a5301422a4807829a5d3ea4eea7243bfdf5e6e2e2f388ab208c50d08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62747370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c27f5a2b9894d0f6743db7cae0f3d726b24995bb7b584c07e36b319e7fe4bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 10 Sep 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1aa033c3dd6f9dcabf3e5db8b0d23e75bacc18083a9fc5fc3bf8dd32b531c9`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 17.1 MB (17141620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1075e78e61225557a73cb4df8bdb388a4e0a3a54d78fb029b95995467ee104`  
		Last Modified: Wed, 11 Sep 2024 02:01:31 GMT  
		Size: 17.8 MB (17783313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e371b1027e98e0af0c4a206108df3590c4135af5dd5c95267415707045a1884`  
		Last Modified: Wed, 11 Sep 2024 02:01:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226c034025ceb5a5072018428121e6627a7adea704c15385680801a1fd204fb`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dc19fcc1171071ce37cd5bee8802261a02276f6819a1116bba48770ae075f`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8c67ecfc62f1593fe9a21212a907a7475fb54a41741a093fe89f9a559fb989d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b29b3ddf761b15badc7ae0959d6005bbaf8b7b2f47dbb8de4b121a4ac60a45`

```dockerfile
```

-	Layers:
	-	`sha256:0955ae0eec0014c0f03bdaaf6a297e846d68da79d1e207c148f9ee0c3c7949cf`  
		Last Modified: Wed, 11 Sep 2024 02:01:29 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:26f4d2199b7ce26c7da298d81fdef751b09bf06c28ee8accc6981d27136233e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61775678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19294d0006d84ceec939bc3ceea2f87f956a91d6308cf3ba3e5646ca19bb4f51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 10 Sep 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cf2b1859f16ea4a3efc3ebdcff929c005fc44c05d7202ce69bbd5258d6989a`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 17.1 MB (17129209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e839e120983d5ca2057bee14103b0d822031e067c63b69d5f7e1d0845a446`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 17.8 MB (17771142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29362d9881a8e2c6fd23dac747f90a311fd37d78cbe5bfe2bc93d137ca3f7b93`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b72324b3582fd670d40a641281f441939c93b3eec0c1a40744ce9f42d416aef`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20947c69fcf36566adb6594921006179ce40d22530bd7d0a5c2f9b50e15639`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f773840574922d6e659b29fbcf461f41a91b4cadf462640657a42112be60bbcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0f8ab3b7a66d0459e31f704adf548456f24de05d66c5e8d00b312bf3b16046`

```dockerfile
```

-	Layers:
	-	`sha256:df52a7f089450cdc3de9670fb900382743ef2eed9fb8fa3771a370f4474f5d87`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5b06e0f5c7cb040b54f682062dec862502064a0b33a4c28099101a752f032188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63614518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b0eae91923bc21d58136d51ddacd96eaecc82b912f73aa585eee9cbccb015a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 10 Sep 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eada7f8d96edf35fbf9cccdfe2a31683f121351212c1d270f7a73b2e1f530e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.2 MB (17186842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b544e07d92af2d47cc10db55727317ca8ccc95a899db6ce41cdd41cb820c0`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ca207ff0f9c918c07b12825084dba82e9f8c9d490f1ffcf33fe0c7b45fab2`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c5493b785a7581afc20e1db4ba86a79bd5e5e8ef3dfa1ad64620028e196eb`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:49c13ed1077c9288d6731d1c032a854f6a56f59b9976404a639ce592ccb36ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9c5ae3da4b9ff13cf06b615700faf98c4d2d79d0b0552d105de12373e85149`

```dockerfile
```

-	Layers:
	-	`sha256:83d1c6b075d68f8bb4649dcdf1ca85edc3489dfbcaf519c18a61e94f8220b96e`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 38.2 KB (38227 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2.1-cli-alpine3.20`

```console
$ docker pull docker@sha256:f1e76d61b9ea8cb8eb44e93ea88091e16b4654658e883daae5f384de8f2e85b9
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

### `docker:27.2.1-cli-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:01d856527b7e1b20d8e45a5c1cef71b5286d8a28460aac196a2239e549e9579f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67357792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d932cd3128d241bc878402ddc81dadfd0a412580aa8762a4e83e90499b3e893e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 10 Sep 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db09d90694836eab5370b7d5f552b34f5772781701b00fd4e7c3950519ee72`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 7.9 MB (7872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538dd9aacd297989031c915937096bfdd889838bf150c05212223a9b3507070`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfaa9e1957304899a8d16f9cf6fca1ddbf8debde833e6b68831a81b50ee6fc2`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616c0277b4c4b06061b57f23022504d07faea54188b3a5b0d5b51dfa4e990b9`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.4 MB (18432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692e2842ca25a9bf245905f6e29b66a65bbdc85f1873aae896b69370566a5f9`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cd67bc2f21b34aeca4c5627b6b4b5dbede9b76ea404dd4079e77464166d0b`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966ec96386506904d07991e403853675dc204da54a5e1fd0c1abd1e6da10197`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1d01552a20f6313745d5d6563fc8a44c75d0010cb7cd94399a1487838380`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:fd0e8c17c33bd8f8f44ac7cb928ac835388efce409ab36d6352961a00445c13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6137457032a6de0c065094e8eae103fd4499ace40937c93c7f7eedc1e32b6c3f`

```dockerfile
```

-	Layers:
	-	`sha256:2c4ce9d43b4d0578cd2db40ddc93a6d28f57ac5b491b4124ce0f14ed8e0909e4`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-cli-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:f952f57a5301422a4807829a5d3ea4eea7243bfdf5e6e2e2f388ab208c50d08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62747370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c27f5a2b9894d0f6743db7cae0f3d726b24995bb7b584c07e36b319e7fe4bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 10 Sep 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1aa033c3dd6f9dcabf3e5db8b0d23e75bacc18083a9fc5fc3bf8dd32b531c9`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 17.1 MB (17141620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1075e78e61225557a73cb4df8bdb388a4e0a3a54d78fb029b95995467ee104`  
		Last Modified: Wed, 11 Sep 2024 02:01:31 GMT  
		Size: 17.8 MB (17783313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e371b1027e98e0af0c4a206108df3590c4135af5dd5c95267415707045a1884`  
		Last Modified: Wed, 11 Sep 2024 02:01:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226c034025ceb5a5072018428121e6627a7adea704c15385680801a1fd204fb`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dc19fcc1171071ce37cd5bee8802261a02276f6819a1116bba48770ae075f`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:8c67ecfc62f1593fe9a21212a907a7475fb54a41741a093fe89f9a559fb989d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b29b3ddf761b15badc7ae0959d6005bbaf8b7b2f47dbb8de4b121a4ac60a45`

```dockerfile
```

-	Layers:
	-	`sha256:0955ae0eec0014c0f03bdaaf6a297e846d68da79d1e207c148f9ee0c3c7949cf`  
		Last Modified: Wed, 11 Sep 2024 02:01:29 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-cli-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:26f4d2199b7ce26c7da298d81fdef751b09bf06c28ee8accc6981d27136233e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61775678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19294d0006d84ceec939bc3ceea2f87f956a91d6308cf3ba3e5646ca19bb4f51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 10 Sep 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cf2b1859f16ea4a3efc3ebdcff929c005fc44c05d7202ce69bbd5258d6989a`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 17.1 MB (17129209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e839e120983d5ca2057bee14103b0d822031e067c63b69d5f7e1d0845a446`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 17.8 MB (17771142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29362d9881a8e2c6fd23dac747f90a311fd37d78cbe5bfe2bc93d137ca3f7b93`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b72324b3582fd670d40a641281f441939c93b3eec0c1a40744ce9f42d416aef`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20947c69fcf36566adb6594921006179ce40d22530bd7d0a5c2f9b50e15639`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:f773840574922d6e659b29fbcf461f41a91b4cadf462640657a42112be60bbcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0f8ab3b7a66d0459e31f704adf548456f24de05d66c5e8d00b312bf3b16046`

```dockerfile
```

-	Layers:
	-	`sha256:df52a7f089450cdc3de9670fb900382743ef2eed9fb8fa3771a370f4474f5d87`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-cli-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5b06e0f5c7cb040b54f682062dec862502064a0b33a4c28099101a752f032188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63614518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b0eae91923bc21d58136d51ddacd96eaecc82b912f73aa585eee9cbccb015a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 10 Sep 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eada7f8d96edf35fbf9cccdfe2a31683f121351212c1d270f7a73b2e1f530e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.2 MB (17186842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b544e07d92af2d47cc10db55727317ca8ccc95a899db6ce41cdd41cb820c0`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ca207ff0f9c918c07b12825084dba82e9f8c9d490f1ffcf33fe0c7b45fab2`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c5493b785a7581afc20e1db4ba86a79bd5e5e8ef3dfa1ad64620028e196eb`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:49c13ed1077c9288d6731d1c032a854f6a56f59b9976404a639ce592ccb36ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9c5ae3da4b9ff13cf06b615700faf98c4d2d79d0b0552d105de12373e85149`

```dockerfile
```

-	Layers:
	-	`sha256:83d1c6b075d68f8bb4649dcdf1ca85edc3489dfbcaf519c18a61e94f8220b96e`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 38.2 KB (38227 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2.1-dind`

```console
$ docker pull docker@sha256:294f99b7749b47d3bfac8535c231a6c47cd0f28be8205af83928b2dde18abda7
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

### `docker:27.2.1-dind` - linux; amd64

```console
$ docker pull docker@sha256:9218d2dc6ab909992500f116eb49948376fb23f5cd9ccf427dd62b3d865ea49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131884120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371f9f35b2da407e86e3d81ea7a4efc0594697c3abb6b47bac15bbfa0533f293`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db09d90694836eab5370b7d5f552b34f5772781701b00fd4e7c3950519ee72`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 7.9 MB (7872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538dd9aacd297989031c915937096bfdd889838bf150c05212223a9b3507070`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfaa9e1957304899a8d16f9cf6fca1ddbf8debde833e6b68831a81b50ee6fc2`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616c0277b4c4b06061b57f23022504d07faea54188b3a5b0d5b51dfa4e990b9`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.4 MB (18432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692e2842ca25a9bf245905f6e29b66a65bbdc85f1873aae896b69370566a5f9`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cd67bc2f21b34aeca4c5627b6b4b5dbede9b76ea404dd4079e77464166d0b`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966ec96386506904d07991e403853675dc204da54a5e1fd0c1abd1e6da10197`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1d01552a20f6313745d5d6563fc8a44c75d0010cb7cd94399a1487838380`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c62cf5a0b55f78c6952456f627b45a4927bcd20a476a84feebb376a2e5afac`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 6.7 MB (6657921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3592c908208e8a16c99d3263902c97301ed446b46205bfcbb8d9ee8611123fa`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 89.2 KB (89218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd4c1986daa1bdd24f3621084f644cff84734eeb7aff037024fdf56f6aae3c1`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f41134be18ef5373326b3114ba85c9698be27a64dc12f0f60a1f5e6d0eac9`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 57.8 MB (57773398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaea47f5e1a31cc71bc565396dc93187e844d7f4ad7885746889e44dc40a4b`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a6f212eac3af392a8a5097e434764cff04c4e70ff2a9c1d4809c5c2e18d9e3`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:797fd1c255c0affbf4ea21c2af94c6f9904c76f433cacfb5aa44a15260ed50de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad921b63e93d9459a50c321f18aa4cad7866107facd5e54d1497bd0a6c86c6fd`

```dockerfile
```

-	Layers:
	-	`sha256:c9f2b5ad322c5b5af063de9a0bf790828d7771944a1fcec170e83a363c84a90c`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:0d871bea6fe47e7bf76b382ee2d4b128fe292b8fdb9082b21345c7d54cfdccae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123320023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cc1cb94b0e714568ec3d9021c42c78f629e704609cfc06069a093ad4a9fea0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1aa033c3dd6f9dcabf3e5db8b0d23e75bacc18083a9fc5fc3bf8dd32b531c9`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 17.1 MB (17141620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1075e78e61225557a73cb4df8bdb388a4e0a3a54d78fb029b95995467ee104`  
		Last Modified: Wed, 11 Sep 2024 02:01:31 GMT  
		Size: 17.8 MB (17783313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e371b1027e98e0af0c4a206108df3590c4135af5dd5c95267415707045a1884`  
		Last Modified: Wed, 11 Sep 2024 02:01:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226c034025ceb5a5072018428121e6627a7adea704c15385680801a1fd204fb`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dc19fcc1171071ce37cd5bee8802261a02276f6819a1116bba48770ae075f`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bf43051f6d401906c8b54ab26747cdead0e1b75ebec9c87fc12bf84d6dc5ed`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 7.0 MB (6984307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da17202765e315d32b089e1c25d097f8e0085fbb39264f5438693657418417`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 88.4 KB (88398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e960455cee8307842cd7579d74c83c6cb33ed93689bc96725f8ed7ebaf5d59b`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bbbc69f2a31b558cb399de570b4197e2b9834a828760b430ff42c27749a5b4`  
		Last Modified: Wed, 11 Sep 2024 02:50:52 GMT  
		Size: 53.5 MB (53494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103acb18844ccc79264ef2a516bb06bd5a0fecb9f01c581d3382253bdfa4423d`  
		Last Modified: Wed, 11 Sep 2024 02:50:51 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0f859154c8a30c4a41eb85bdfb5bafdd1617a0787c82c879a8a0575b531ac`  
		Last Modified: Wed, 11 Sep 2024 02:50:51 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5c5a017a1a9973a3ee57ddf3ddb4efd0e946b7da75bf289ba07ff8a9143ba0a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ce3bf47c18b13d056ef62e3576f93da7e2113326d337a31b0e4d5e835a21de`

```dockerfile
```

-	Layers:
	-	`sha256:1dbc2fbc5d04bf6005bd82413353aa41ed322750380a145666a8789b6900915b`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:68d52b1f8e3a30d5c9ebe8531f1ceb2b14389dc70dc7f73fc640cc2612b0cb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121668199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28baeefb60bbf0c1f288b4ba28c02be3975f6866a625e2122122b2366329bc7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cf2b1859f16ea4a3efc3ebdcff929c005fc44c05d7202ce69bbd5258d6989a`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 17.1 MB (17129209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e839e120983d5ca2057bee14103b0d822031e067c63b69d5f7e1d0845a446`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 17.8 MB (17771142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29362d9881a8e2c6fd23dac747f90a311fd37d78cbe5bfe2bc93d137ca3f7b93`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b72324b3582fd670d40a641281f441939c93b3eec0c1a40744ce9f42d416aef`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20947c69fcf36566adb6594921006179ce40d22530bd7d0a5c2f9b50e15639`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3903b8a5e83aa88438bc00e6a21cbfb21f98d72bf4a90554fbbc9a67c624287`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 6.3 MB (6308115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a08d98b7b8a40124cdff9c9cfb28790278fd87f375c88ea1239edb53b70aedb`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 84.5 KB (84482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c31665ca29d651d05ff3ca3fdc61f6a67ce69e291415b2651008e20b66e92dc`  
		Last Modified: Wed, 11 Sep 2024 02:50:55 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdde100f6de66fb3973ccfa58803d39516f505beacbffa025f887a7a952e3af9`  
		Last Modified: Wed, 11 Sep 2024 02:50:57 GMT  
		Size: 53.5 MB (53494122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131ea12518408d5c3f587e5ce4fe43d86e73f90603ed92f2ae54b2d321e2d47a`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f824312e672e112fdb8abcca34a0ae94e522859b14b6ba6b92d991d2e996ba7`  
		Last Modified: Wed, 11 Sep 2024 02:50:57 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4f69fea1e0e9bf4868790f90d7c7db9943225d34949695ace47f8784e814be93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db4c9ab2f89bb268cc28bcab911d9b7fc0a33b4e3b11b6b9baab0265727e3ae`

```dockerfile
```

-	Layers:
	-	`sha256:96e05737fa765bceaa6840ea6423d151ae12256c0d7a05d01ade85d7a178e388`  
		Last Modified: Wed, 11 Sep 2024 02:50:55 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e5140f28e7e82d172f34d88dfbd7a1bacbd4cbd3f24abdcaf1b0be485b916dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124152073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a7e2ef80ce4b0a550c648ddfb69a1953cdb927ca159fe704bf937bc8979d77`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eada7f8d96edf35fbf9cccdfe2a31683f121351212c1d270f7a73b2e1f530e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.2 MB (17186842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b544e07d92af2d47cc10db55727317ca8ccc95a899db6ce41cdd41cb820c0`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ca207ff0f9c918c07b12825084dba82e9f8c9d490f1ffcf33fe0c7b45fab2`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c5493b785a7581afc20e1db4ba86a79bd5e5e8ef3dfa1ad64620028e196eb`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e5be9720db99d659c53b6a67a1dd2ba6e958b7622248ab8dfc91c58d5c0f1d`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 7.0 MB (7034910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320bcabad1025e90ed07d105bd2724f1565672227ec5927061b082183adc6b11`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 98.7 KB (98650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9235e7f34f8cc28423dac4653e318c60d54cff3b0544a5e924074efdf31578`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9d4c07d55e9442550b66fb78c2d91de8856309dcc6875aa4c34aaa96f85316`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 53.4 MB (53398203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df4284aea7cda8255fd5026391b9b8b9db9af96da9875fe9db8f0185ac0ccd`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c51f22e855b132e7146b336aac0310cbe52e537cd77af861d9f27629b425ea6`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:fff328b2549d85866f264e626fb1fca2080ff3b685aa527410f3ea8ce95f38ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fd23934d6432c356a3df01ffbcf3ffbe9940918ffb9408d76137da20e3a2af`

```dockerfile
```

-	Layers:
	-	`sha256:23b22cd0119f1928542bdacdaf4016a4fa50c2fe26aa68aac38149f329c2acfd`  
		Last Modified: Wed, 11 Sep 2024 02:50:47 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2.1-dind-alpine3.20`

```console
$ docker pull docker@sha256:294f99b7749b47d3bfac8535c231a6c47cd0f28be8205af83928b2dde18abda7
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

### `docker:27.2.1-dind-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:9218d2dc6ab909992500f116eb49948376fb23f5cd9ccf427dd62b3d865ea49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131884120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371f9f35b2da407e86e3d81ea7a4efc0594697c3abb6b47bac15bbfa0533f293`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db09d90694836eab5370b7d5f552b34f5772781701b00fd4e7c3950519ee72`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 7.9 MB (7872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538dd9aacd297989031c915937096bfdd889838bf150c05212223a9b3507070`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfaa9e1957304899a8d16f9cf6fca1ddbf8debde833e6b68831a81b50ee6fc2`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616c0277b4c4b06061b57f23022504d07faea54188b3a5b0d5b51dfa4e990b9`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.4 MB (18432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692e2842ca25a9bf245905f6e29b66a65bbdc85f1873aae896b69370566a5f9`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cd67bc2f21b34aeca4c5627b6b4b5dbede9b76ea404dd4079e77464166d0b`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966ec96386506904d07991e403853675dc204da54a5e1fd0c1abd1e6da10197`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1d01552a20f6313745d5d6563fc8a44c75d0010cb7cd94399a1487838380`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c62cf5a0b55f78c6952456f627b45a4927bcd20a476a84feebb376a2e5afac`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 6.7 MB (6657921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3592c908208e8a16c99d3263902c97301ed446b46205bfcbb8d9ee8611123fa`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 89.2 KB (89218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd4c1986daa1bdd24f3621084f644cff84734eeb7aff037024fdf56f6aae3c1`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f41134be18ef5373326b3114ba85c9698be27a64dc12f0f60a1f5e6d0eac9`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 57.8 MB (57773398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaea47f5e1a31cc71bc565396dc93187e844d7f4ad7885746889e44dc40a4b`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a6f212eac3af392a8a5097e434764cff04c4e70ff2a9c1d4809c5c2e18d9e3`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:797fd1c255c0affbf4ea21c2af94c6f9904c76f433cacfb5aa44a15260ed50de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad921b63e93d9459a50c321f18aa4cad7866107facd5e54d1497bd0a6c86c6fd`

```dockerfile
```

-	Layers:
	-	`sha256:c9f2b5ad322c5b5af063de9a0bf790828d7771944a1fcec170e83a363c84a90c`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-dind-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:0d871bea6fe47e7bf76b382ee2d4b128fe292b8fdb9082b21345c7d54cfdccae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123320023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cc1cb94b0e714568ec3d9021c42c78f629e704609cfc06069a093ad4a9fea0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1aa033c3dd6f9dcabf3e5db8b0d23e75bacc18083a9fc5fc3bf8dd32b531c9`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 17.1 MB (17141620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1075e78e61225557a73cb4df8bdb388a4e0a3a54d78fb029b95995467ee104`  
		Last Modified: Wed, 11 Sep 2024 02:01:31 GMT  
		Size: 17.8 MB (17783313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e371b1027e98e0af0c4a206108df3590c4135af5dd5c95267415707045a1884`  
		Last Modified: Wed, 11 Sep 2024 02:01:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226c034025ceb5a5072018428121e6627a7adea704c15385680801a1fd204fb`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dc19fcc1171071ce37cd5bee8802261a02276f6819a1116bba48770ae075f`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bf43051f6d401906c8b54ab26747cdead0e1b75ebec9c87fc12bf84d6dc5ed`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 7.0 MB (6984307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da17202765e315d32b089e1c25d097f8e0085fbb39264f5438693657418417`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 88.4 KB (88398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e960455cee8307842cd7579d74c83c6cb33ed93689bc96725f8ed7ebaf5d59b`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bbbc69f2a31b558cb399de570b4197e2b9834a828760b430ff42c27749a5b4`  
		Last Modified: Wed, 11 Sep 2024 02:50:52 GMT  
		Size: 53.5 MB (53494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103acb18844ccc79264ef2a516bb06bd5a0fecb9f01c581d3382253bdfa4423d`  
		Last Modified: Wed, 11 Sep 2024 02:50:51 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0f859154c8a30c4a41eb85bdfb5bafdd1617a0787c82c879a8a0575b531ac`  
		Last Modified: Wed, 11 Sep 2024 02:50:51 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:5c5a017a1a9973a3ee57ddf3ddb4efd0e946b7da75bf289ba07ff8a9143ba0a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ce3bf47c18b13d056ef62e3576f93da7e2113326d337a31b0e4d5e835a21de`

```dockerfile
```

-	Layers:
	-	`sha256:1dbc2fbc5d04bf6005bd82413353aa41ed322750380a145666a8789b6900915b`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-dind-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:68d52b1f8e3a30d5c9ebe8531f1ceb2b14389dc70dc7f73fc640cc2612b0cb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121668199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28baeefb60bbf0c1f288b4ba28c02be3975f6866a625e2122122b2366329bc7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cf2b1859f16ea4a3efc3ebdcff929c005fc44c05d7202ce69bbd5258d6989a`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 17.1 MB (17129209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e839e120983d5ca2057bee14103b0d822031e067c63b69d5f7e1d0845a446`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 17.8 MB (17771142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29362d9881a8e2c6fd23dac747f90a311fd37d78cbe5bfe2bc93d137ca3f7b93`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b72324b3582fd670d40a641281f441939c93b3eec0c1a40744ce9f42d416aef`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20947c69fcf36566adb6594921006179ce40d22530bd7d0a5c2f9b50e15639`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3903b8a5e83aa88438bc00e6a21cbfb21f98d72bf4a90554fbbc9a67c624287`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 6.3 MB (6308115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a08d98b7b8a40124cdff9c9cfb28790278fd87f375c88ea1239edb53b70aedb`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 84.5 KB (84482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c31665ca29d651d05ff3ca3fdc61f6a67ce69e291415b2651008e20b66e92dc`  
		Last Modified: Wed, 11 Sep 2024 02:50:55 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdde100f6de66fb3973ccfa58803d39516f505beacbffa025f887a7a952e3af9`  
		Last Modified: Wed, 11 Sep 2024 02:50:57 GMT  
		Size: 53.5 MB (53494122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131ea12518408d5c3f587e5ce4fe43d86e73f90603ed92f2ae54b2d321e2d47a`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f824312e672e112fdb8abcca34a0ae94e522859b14b6ba6b92d991d2e996ba7`  
		Last Modified: Wed, 11 Sep 2024 02:50:57 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:4f69fea1e0e9bf4868790f90d7c7db9943225d34949695ace47f8784e814be93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db4c9ab2f89bb268cc28bcab911d9b7fc0a33b4e3b11b6b9baab0265727e3ae`

```dockerfile
```

-	Layers:
	-	`sha256:96e05737fa765bceaa6840ea6423d151ae12256c0d7a05d01ade85d7a178e388`  
		Last Modified: Wed, 11 Sep 2024 02:50:55 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-dind-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e5140f28e7e82d172f34d88dfbd7a1bacbd4cbd3f24abdcaf1b0be485b916dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124152073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a7e2ef80ce4b0a550c648ddfb69a1953cdb927ca159fe704bf937bc8979d77`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eada7f8d96edf35fbf9cccdfe2a31683f121351212c1d270f7a73b2e1f530e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.2 MB (17186842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b544e07d92af2d47cc10db55727317ca8ccc95a899db6ce41cdd41cb820c0`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ca207ff0f9c918c07b12825084dba82e9f8c9d490f1ffcf33fe0c7b45fab2`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c5493b785a7581afc20e1db4ba86a79bd5e5e8ef3dfa1ad64620028e196eb`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e5be9720db99d659c53b6a67a1dd2ba6e958b7622248ab8dfc91c58d5c0f1d`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 7.0 MB (7034910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320bcabad1025e90ed07d105bd2724f1565672227ec5927061b082183adc6b11`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 98.7 KB (98650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9235e7f34f8cc28423dac4653e318c60d54cff3b0544a5e924074efdf31578`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9d4c07d55e9442550b66fb78c2d91de8856309dcc6875aa4c34aaa96f85316`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 53.4 MB (53398203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df4284aea7cda8255fd5026391b9b8b9db9af96da9875fe9db8f0185ac0ccd`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c51f22e855b132e7146b336aac0310cbe52e537cd77af861d9f27629b425ea6`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:fff328b2549d85866f264e626fb1fca2080ff3b685aa527410f3ea8ce95f38ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fd23934d6432c356a3df01ffbcf3ffbe9940918ffb9408d76137da20e3a2af`

```dockerfile
```

-	Layers:
	-	`sha256:23b22cd0119f1928542bdacdaf4016a4fa50c2fe26aa68aac38149f329c2acfd`  
		Last Modified: Wed, 11 Sep 2024 02:50:47 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2.1-dind-rootless`

```console
$ docker pull docker@sha256:a85bf1d09cf0c684d7de3268d4c54b8bb152b79b53c1efa324cc8df94da42b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.2.1-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:5b34a2411903326499d2f67470d83ce97dc0183ca802e6fcf91ca1b564bf01bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154153776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e83a23dba859599f0adfa4a4b7996f23a41de2f5621f047074a9da77c6274f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db09d90694836eab5370b7d5f552b34f5772781701b00fd4e7c3950519ee72`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 7.9 MB (7872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538dd9aacd297989031c915937096bfdd889838bf150c05212223a9b3507070`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfaa9e1957304899a8d16f9cf6fca1ddbf8debde833e6b68831a81b50ee6fc2`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616c0277b4c4b06061b57f23022504d07faea54188b3a5b0d5b51dfa4e990b9`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.4 MB (18432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692e2842ca25a9bf245905f6e29b66a65bbdc85f1873aae896b69370566a5f9`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cd67bc2f21b34aeca4c5627b6b4b5dbede9b76ea404dd4079e77464166d0b`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966ec96386506904d07991e403853675dc204da54a5e1fd0c1abd1e6da10197`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1d01552a20f6313745d5d6563fc8a44c75d0010cb7cd94399a1487838380`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c62cf5a0b55f78c6952456f627b45a4927bcd20a476a84feebb376a2e5afac`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 6.7 MB (6657921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3592c908208e8a16c99d3263902c97301ed446b46205bfcbb8d9ee8611123fa`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 89.2 KB (89218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd4c1986daa1bdd24f3621084f644cff84734eeb7aff037024fdf56f6aae3c1`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f41134be18ef5373326b3114ba85c9698be27a64dc12f0f60a1f5e6d0eac9`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 57.8 MB (57773398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaea47f5e1a31cc71bc565396dc93187e844d7f4ad7885746889e44dc40a4b`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a6f212eac3af392a8a5097e434764cff04c4e70ff2a9c1d4809c5c2e18d9e3`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b065473b42eefb9a792eb005311c212c14df916c2575869263ae2fc25bd862`  
		Last Modified: Wed, 11 Sep 2024 03:48:49 GMT  
		Size: 981.0 KB (980986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852d28940731d27787147baf692114c5a57e84af5870515a9cf826785e61c97e`  
		Last Modified: Wed, 11 Sep 2024 03:48:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2754af7f7c8de794edb28a5c9f9ba8c90bdf84c274b9f556a39c0ea3240f1ab`  
		Last Modified: Wed, 11 Sep 2024 03:48:49 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636b57c4498bf4e949f7e09044a06c834e167dc3facda3697e3e1fff4b1739e8`  
		Last Modified: Wed, 11 Sep 2024 03:48:50 GMT  
		Size: 21.3 MB (21287315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f993cc096d161b79e4c922715fa6fe0c3d065ffa32abe11cf805a5937def91`  
		Last Modified: Wed, 11 Sep 2024 03:48:50 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c3fb49a3f69e9f44f3a3f159a35777da8859fb3530256aa2e196c953dfb4f8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7759138f227c5ac9b927aa368e0931f67ea0cd6196dfc9785aa8c3d4a23bacd`

```dockerfile
```

-	Layers:
	-	`sha256:7fc1f180c7e9851ada027667060ef9f9afc83a449caaccc1e42e3f58de86ba7d`  
		Last Modified: Wed, 11 Sep 2024 03:48:49 GMT  
		Size: 30.6 KB (30580 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.2.1-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bcedcdbefd4c0a8026ca435140dd2260a8b8de76d7f7ca5aa88030b661852828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148310987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d21859101d6a92e4bdb3cd0fc0396aab45b56110d1c29617704bda32774c45`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eada7f8d96edf35fbf9cccdfe2a31683f121351212c1d270f7a73b2e1f530e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.2 MB (17186842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b544e07d92af2d47cc10db55727317ca8ccc95a899db6ce41cdd41cb820c0`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ca207ff0f9c918c07b12825084dba82e9f8c9d490f1ffcf33fe0c7b45fab2`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c5493b785a7581afc20e1db4ba86a79bd5e5e8ef3dfa1ad64620028e196eb`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e5be9720db99d659c53b6a67a1dd2ba6e958b7622248ab8dfc91c58d5c0f1d`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 7.0 MB (7034910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320bcabad1025e90ed07d105bd2724f1565672227ec5927061b082183adc6b11`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 98.7 KB (98650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9235e7f34f8cc28423dac4653e318c60d54cff3b0544a5e924074efdf31578`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9d4c07d55e9442550b66fb78c2d91de8856309dcc6875aa4c34aaa96f85316`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 53.4 MB (53398203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df4284aea7cda8255fd5026391b9b8b9db9af96da9875fe9db8f0185ac0ccd`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c51f22e855b132e7146b336aac0310cbe52e537cd77af861d9f27629b425ea6`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61abcef331c5400bd552a2b6a5ecc6d03ecee4f12e9cf72c4a866ec26c4e2fe7`  
		Last Modified: Wed, 11 Sep 2024 03:48:43 GMT  
		Size: 1.0 MB (1023119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0a2f42af77b9a719e519573af0f3e531e92847a4b6f6095d42ffb21b48ae44`  
		Last Modified: Wed, 11 Sep 2024 03:48:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d713d1485ac825869be3a208d8d2699337d7ce096e81e2eeab4f7fc83fd0cc`  
		Last Modified: Wed, 11 Sep 2024 03:48:43 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c70f1919f2604484b0212c929c9881df57425101e48ec186fc604ca7b74c92e`  
		Last Modified: Wed, 11 Sep 2024 03:48:44 GMT  
		Size: 23.1 MB (23134441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab61b3f82263bbf4714ce5dc1a9816f6c16b3a159cd8e8cf873a94ce857aaeb1`  
		Last Modified: Wed, 11 Sep 2024 03:48:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.2.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0cdb6cb36b46b803fec1343b539275b39b36043f1df4e6fd6c3dc696980ca15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4a5c6803fcd314f69e271e0c35c18f4c05e2f48eaf0c977c298dcc6a732c71`

```dockerfile
```

-	Layers:
	-	`sha256:e6bc659420a6a66c2ebcb45c47ea7e01bff903c946a478d6fe5246ea077cdc54`  
		Last Modified: Wed, 11 Sep 2024 03:48:42 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.2.1-windowsservercore`

```console
$ docker pull docker@sha256:27ba43da317d5f4e4a2de77459eaf2e80d335f279f539e96243b98c45a9d504e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `docker:27.2.1-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:a82aa3fe951a62771fff8170c24096425b50bc9e264286388152fa9b81712f5f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520410181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d257b03e5fade898fde7ea9c893f1a592471ad97e4ed6492b7b212b24c1ce0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 02:06:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 02:06:38 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 02:06:38 GMT
ENV DOCKER_VERSION=27.2.1
# Wed, 11 Sep 2024 02:06:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Wed, 11 Sep 2024 02:06:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:06:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Wed, 11 Sep 2024 02:06:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.windows-amd64.exe
# Wed, 11 Sep 2024 02:06:51 GMT
ENV DOCKER_BUILDX_SHA256=2bee3541fd1ed077d5f59141085f59345d0d0380d5749724e7088a3f02a113ca
# Wed, 11 Sep 2024 02:07:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:07:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 11 Sep 2024 02:07:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 11 Sep 2024 02:07:11 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 11 Sep 2024 02:07:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e2f86d5d1b2a5b865a052fc16b9166a550aed670add96ae7a6548a82b5b722`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8981ca84e679b362967aa517438bf611399eb20ea708bf9471e8f84100dfa7`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 342.6 KB (342630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0c9302154e848dc4bb0463644b87c8fae31baa96db751b75bc3a5d8195cbbe`  
		Last Modified: Wed, 11 Sep 2024 02:07:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41a22741d542661237a8d8e85456308c1cbd52d9498dfa0dfcbb566e1cc355a`  
		Last Modified: Wed, 11 Sep 2024 02:07:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6c4124d41c5d00b862e39fbfb5816f520bd94f02a0b82f582598effce81572`  
		Last Modified: Wed, 11 Sep 2024 02:07:37 GMT  
		Size: 18.9 MB (18913958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d5d0294c55c8e2b4a0761ea1eebf18f69f9d4c1846d0f84567e1edfe6e9217`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a83a411f2cf4b9fd720c3e578a348825577e84a74daff8dbfb10038588e534`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a320c69ba98bd2a4ead0142a9ee82e878541eb3d5f88492e25d026f0b0bc944`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97bc35449386503b924207a0b594a8b7459f1f88bdc3f42653bbe2b1841a475`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 19.3 MB (19269057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682ff78fabece6bcee7bf9b7da73568924352f978504e36a2cfc9110de462937`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8d54a118d4d3fe5c1dc907fadd1281ab71ea5600577a59956ba52226d5c42b`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8a9795b6d3907b92f407b716652f11fbc26030e2d49880aef8d6fdc0bfaea6`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f1a7d56c884d1afe4dc68cc0ac1f9189826bcee13efbb385acd42fc1ca3f9e`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 19.7 MB (19680496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.2.1-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:4d1e8b301b0c6ae81034443c38a212eec26f46cd4f59a332c68cd62eb0f09f92
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778456457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d2275e0c50e1a2778828b1c989942d819123b07583313ea0ac4522e03ce58c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 02:04:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 02:04:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 02:04:37 GMT
ENV DOCKER_VERSION=27.2.1
# Wed, 11 Sep 2024 02:04:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Wed, 11 Sep 2024 02:04:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:04:49 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Wed, 11 Sep 2024 02:04:49 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.windows-amd64.exe
# Wed, 11 Sep 2024 02:04:50 GMT
ENV DOCKER_BUILDX_SHA256=2bee3541fd1ed077d5f59141085f59345d0d0380d5749724e7088a3f02a113ca
# Wed, 11 Sep 2024 02:05:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:05:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 11 Sep 2024 02:05:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 11 Sep 2024 02:05:02 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 11 Sep 2024 02:05:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96305c41a993336ed17fc44e0e2bc51503e0e9b085c1f5cb642e396ab1d76ca5`  
		Last Modified: Wed, 11 Sep 2024 02:05:22 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90dcbc14d4e1aeb8ff8091b77163592eff3b0e11712fb83acf11cfca78be489`  
		Last Modified: Wed, 11 Sep 2024 02:05:23 GMT  
		Size: 330.4 KB (330375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae07341e5dcd520c87adee68815b0c466c03ab267fd0f757b67081ade1ff210`  
		Last Modified: Wed, 11 Sep 2024 02:05:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7973ed8b5a6d11094c8d4c2433a60c5a5fcfcb84b1f9163d275729bc8c9c75`  
		Last Modified: Wed, 11 Sep 2024 02:05:21 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076ffff23dfa564b4c5b62d9bda15f2f3257a29a8480e79f445bc1eac2976a6b`  
		Last Modified: Wed, 11 Sep 2024 02:05:23 GMT  
		Size: 18.9 MB (18911033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d1ca83016e2f178e867b86522bccc3c667320c2852da1a4d8c3ff193581105`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87986c7e4d5811794113e6437168a3f46ca14249232e5d226230840cbbeeeca`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5abefd76cb19ba3f5d50ae3b4dd66278517f9a1c2cb758f0a2898a960c55e8a`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c490aa0bb5fad395420b48468b3d32ffc9368901095cac9b73061ee54745c6`  
		Last Modified: Wed, 11 Sep 2024 02:05:20 GMT  
		Size: 19.3 MB (19264623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd8a155e1236c2faacf3433d3f3bfdbb991624d0ba0360937cca5d1e8a24ed2`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b554c6c79e64ef1bf1f3b97d2096f9cba53dc60c7ea8a8e37af03a3673285ea`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa1591f79c5c535c392829fc79152d4632d9a14cd22af2be1768c5b25ee91c0`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f570820d723f568887ddd5f8674cf19f3066dae96c6b4e052ac1b919e22596`  
		Last Modified: Wed, 11 Sep 2024 02:05:20 GMT  
		Size: 19.7 MB (19669920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.2.1-windowsservercore-1809`

```console
$ docker pull docker@sha256:5cc4548517a5d2cd96e9f4922bbac7b8c09ecf55aec9d8941748e352a57dfe4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `docker:27.2.1-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:4d1e8b301b0c6ae81034443c38a212eec26f46cd4f59a332c68cd62eb0f09f92
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778456457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d2275e0c50e1a2778828b1c989942d819123b07583313ea0ac4522e03ce58c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 02:04:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 02:04:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 02:04:37 GMT
ENV DOCKER_VERSION=27.2.1
# Wed, 11 Sep 2024 02:04:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Wed, 11 Sep 2024 02:04:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:04:49 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Wed, 11 Sep 2024 02:04:49 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.windows-amd64.exe
# Wed, 11 Sep 2024 02:04:50 GMT
ENV DOCKER_BUILDX_SHA256=2bee3541fd1ed077d5f59141085f59345d0d0380d5749724e7088a3f02a113ca
# Wed, 11 Sep 2024 02:05:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:05:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 11 Sep 2024 02:05:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 11 Sep 2024 02:05:02 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 11 Sep 2024 02:05:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96305c41a993336ed17fc44e0e2bc51503e0e9b085c1f5cb642e396ab1d76ca5`  
		Last Modified: Wed, 11 Sep 2024 02:05:22 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90dcbc14d4e1aeb8ff8091b77163592eff3b0e11712fb83acf11cfca78be489`  
		Last Modified: Wed, 11 Sep 2024 02:05:23 GMT  
		Size: 330.4 KB (330375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae07341e5dcd520c87adee68815b0c466c03ab267fd0f757b67081ade1ff210`  
		Last Modified: Wed, 11 Sep 2024 02:05:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7973ed8b5a6d11094c8d4c2433a60c5a5fcfcb84b1f9163d275729bc8c9c75`  
		Last Modified: Wed, 11 Sep 2024 02:05:21 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076ffff23dfa564b4c5b62d9bda15f2f3257a29a8480e79f445bc1eac2976a6b`  
		Last Modified: Wed, 11 Sep 2024 02:05:23 GMT  
		Size: 18.9 MB (18911033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d1ca83016e2f178e867b86522bccc3c667320c2852da1a4d8c3ff193581105`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87986c7e4d5811794113e6437168a3f46ca14249232e5d226230840cbbeeeca`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5abefd76cb19ba3f5d50ae3b4dd66278517f9a1c2cb758f0a2898a960c55e8a`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c490aa0bb5fad395420b48468b3d32ffc9368901095cac9b73061ee54745c6`  
		Last Modified: Wed, 11 Sep 2024 02:05:20 GMT  
		Size: 19.3 MB (19264623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd8a155e1236c2faacf3433d3f3bfdbb991624d0ba0360937cca5d1e8a24ed2`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b554c6c79e64ef1bf1f3b97d2096f9cba53dc60c7ea8a8e37af03a3673285ea`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa1591f79c5c535c392829fc79152d4632d9a14cd22af2be1768c5b25ee91c0`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f570820d723f568887ddd5f8674cf19f3066dae96c6b4e052ac1b919e22596`  
		Last Modified: Wed, 11 Sep 2024 02:05:20 GMT  
		Size: 19.7 MB (19669920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.2.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:421236c754a43a1f842fbcf8e4f9232fd85ea35de3ece64703e37089e70d5b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `docker:27.2.1-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:a82aa3fe951a62771fff8170c24096425b50bc9e264286388152fa9b81712f5f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520410181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d257b03e5fade898fde7ea9c893f1a592471ad97e4ed6492b7b212b24c1ce0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 02:06:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 02:06:38 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 02:06:38 GMT
ENV DOCKER_VERSION=27.2.1
# Wed, 11 Sep 2024 02:06:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Wed, 11 Sep 2024 02:06:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:06:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Wed, 11 Sep 2024 02:06:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.windows-amd64.exe
# Wed, 11 Sep 2024 02:06:51 GMT
ENV DOCKER_BUILDX_SHA256=2bee3541fd1ed077d5f59141085f59345d0d0380d5749724e7088a3f02a113ca
# Wed, 11 Sep 2024 02:07:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:07:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 11 Sep 2024 02:07:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 11 Sep 2024 02:07:11 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 11 Sep 2024 02:07:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e2f86d5d1b2a5b865a052fc16b9166a550aed670add96ae7a6548a82b5b722`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8981ca84e679b362967aa517438bf611399eb20ea708bf9471e8f84100dfa7`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 342.6 KB (342630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0c9302154e848dc4bb0463644b87c8fae31baa96db751b75bc3a5d8195cbbe`  
		Last Modified: Wed, 11 Sep 2024 02:07:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41a22741d542661237a8d8e85456308c1cbd52d9498dfa0dfcbb566e1cc355a`  
		Last Modified: Wed, 11 Sep 2024 02:07:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6c4124d41c5d00b862e39fbfb5816f520bd94f02a0b82f582598effce81572`  
		Last Modified: Wed, 11 Sep 2024 02:07:37 GMT  
		Size: 18.9 MB (18913958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d5d0294c55c8e2b4a0761ea1eebf18f69f9d4c1846d0f84567e1edfe6e9217`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a83a411f2cf4b9fd720c3e578a348825577e84a74daff8dbfb10038588e534`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a320c69ba98bd2a4ead0142a9ee82e878541eb3d5f88492e25d026f0b0bc944`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97bc35449386503b924207a0b594a8b7459f1f88bdc3f42653bbe2b1841a475`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 19.3 MB (19269057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682ff78fabece6bcee7bf9b7da73568924352f978504e36a2cfc9110de462937`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8d54a118d4d3fe5c1dc907fadd1281ab71ea5600577a59956ba52226d5c42b`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8a9795b6d3907b92f407b716652f11fbc26030e2d49880aef8d6fdc0bfaea6`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f1a7d56c884d1afe4dc68cc0ac1f9189826bcee13efbb385acd42fc1ca3f9e`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 19.7 MB (19680496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:f1e76d61b9ea8cb8eb44e93ea88091e16b4654658e883daae5f384de8f2e85b9
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
$ docker pull docker@sha256:01d856527b7e1b20d8e45a5c1cef71b5286d8a28460aac196a2239e549e9579f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67357792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d932cd3128d241bc878402ddc81dadfd0a412580aa8762a4e83e90499b3e893e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 10 Sep 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db09d90694836eab5370b7d5f552b34f5772781701b00fd4e7c3950519ee72`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 7.9 MB (7872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538dd9aacd297989031c915937096bfdd889838bf150c05212223a9b3507070`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfaa9e1957304899a8d16f9cf6fca1ddbf8debde833e6b68831a81b50ee6fc2`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616c0277b4c4b06061b57f23022504d07faea54188b3a5b0d5b51dfa4e990b9`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.4 MB (18432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692e2842ca25a9bf245905f6e29b66a65bbdc85f1873aae896b69370566a5f9`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cd67bc2f21b34aeca4c5627b6b4b5dbede9b76ea404dd4079e77464166d0b`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966ec96386506904d07991e403853675dc204da54a5e1fd0c1abd1e6da10197`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1d01552a20f6313745d5d6563fc8a44c75d0010cb7cd94399a1487838380`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:fd0e8c17c33bd8f8f44ac7cb928ac835388efce409ab36d6352961a00445c13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6137457032a6de0c065094e8eae103fd4499ace40937c93c7f7eedc1e32b6c3f`

```dockerfile
```

-	Layers:
	-	`sha256:2c4ce9d43b4d0578cd2db40ddc93a6d28f57ac5b491b4124ce0f14ed8e0909e4`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:f952f57a5301422a4807829a5d3ea4eea7243bfdf5e6e2e2f388ab208c50d08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62747370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c27f5a2b9894d0f6743db7cae0f3d726b24995bb7b584c07e36b319e7fe4bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 10 Sep 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1aa033c3dd6f9dcabf3e5db8b0d23e75bacc18083a9fc5fc3bf8dd32b531c9`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 17.1 MB (17141620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1075e78e61225557a73cb4df8bdb388a4e0a3a54d78fb029b95995467ee104`  
		Last Modified: Wed, 11 Sep 2024 02:01:31 GMT  
		Size: 17.8 MB (17783313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e371b1027e98e0af0c4a206108df3590c4135af5dd5c95267415707045a1884`  
		Last Modified: Wed, 11 Sep 2024 02:01:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226c034025ceb5a5072018428121e6627a7adea704c15385680801a1fd204fb`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dc19fcc1171071ce37cd5bee8802261a02276f6819a1116bba48770ae075f`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:8c67ecfc62f1593fe9a21212a907a7475fb54a41741a093fe89f9a559fb989d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b29b3ddf761b15badc7ae0959d6005bbaf8b7b2f47dbb8de4b121a4ac60a45`

```dockerfile
```

-	Layers:
	-	`sha256:0955ae0eec0014c0f03bdaaf6a297e846d68da79d1e207c148f9ee0c3c7949cf`  
		Last Modified: Wed, 11 Sep 2024 02:01:29 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:26f4d2199b7ce26c7da298d81fdef751b09bf06c28ee8accc6981d27136233e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61775678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19294d0006d84ceec939bc3ceea2f87f956a91d6308cf3ba3e5646ca19bb4f51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 10 Sep 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cf2b1859f16ea4a3efc3ebdcff929c005fc44c05d7202ce69bbd5258d6989a`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 17.1 MB (17129209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e839e120983d5ca2057bee14103b0d822031e067c63b69d5f7e1d0845a446`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 17.8 MB (17771142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29362d9881a8e2c6fd23dac747f90a311fd37d78cbe5bfe2bc93d137ca3f7b93`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b72324b3582fd670d40a641281f441939c93b3eec0c1a40744ce9f42d416aef`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20947c69fcf36566adb6594921006179ce40d22530bd7d0a5c2f9b50e15639`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:f773840574922d6e659b29fbcf461f41a91b4cadf462640657a42112be60bbcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0f8ab3b7a66d0459e31f704adf548456f24de05d66c5e8d00b312bf3b16046`

```dockerfile
```

-	Layers:
	-	`sha256:df52a7f089450cdc3de9670fb900382743ef2eed9fb8fa3771a370f4474f5d87`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5b06e0f5c7cb040b54f682062dec862502064a0b33a4c28099101a752f032188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63614518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b0eae91923bc21d58136d51ddacd96eaecc82b912f73aa585eee9cbccb015a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 10 Sep 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 10 Sep 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 10 Sep 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eada7f8d96edf35fbf9cccdfe2a31683f121351212c1d270f7a73b2e1f530e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.2 MB (17186842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b544e07d92af2d47cc10db55727317ca8ccc95a899db6ce41cdd41cb820c0`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ca207ff0f9c918c07b12825084dba82e9f8c9d490f1ffcf33fe0c7b45fab2`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c5493b785a7581afc20e1db4ba86a79bd5e5e8ef3dfa1ad64620028e196eb`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:49c13ed1077c9288d6731d1c032a854f6a56f59b9976404a639ce592ccb36ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9c5ae3da4b9ff13cf06b615700faf98c4d2d79d0b0552d105de12373e85149`

```dockerfile
```

-	Layers:
	-	`sha256:83d1c6b075d68f8bb4649dcdf1ca85edc3489dfbcaf519c18a61e94f8220b96e`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 38.2 KB (38227 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:294f99b7749b47d3bfac8535c231a6c47cd0f28be8205af83928b2dde18abda7
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
$ docker pull docker@sha256:9218d2dc6ab909992500f116eb49948376fb23f5cd9ccf427dd62b3d865ea49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131884120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371f9f35b2da407e86e3d81ea7a4efc0594697c3abb6b47bac15bbfa0533f293`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db09d90694836eab5370b7d5f552b34f5772781701b00fd4e7c3950519ee72`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 7.9 MB (7872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538dd9aacd297989031c915937096bfdd889838bf150c05212223a9b3507070`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfaa9e1957304899a8d16f9cf6fca1ddbf8debde833e6b68831a81b50ee6fc2`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616c0277b4c4b06061b57f23022504d07faea54188b3a5b0d5b51dfa4e990b9`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.4 MB (18432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692e2842ca25a9bf245905f6e29b66a65bbdc85f1873aae896b69370566a5f9`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cd67bc2f21b34aeca4c5627b6b4b5dbede9b76ea404dd4079e77464166d0b`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966ec96386506904d07991e403853675dc204da54a5e1fd0c1abd1e6da10197`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1d01552a20f6313745d5d6563fc8a44c75d0010cb7cd94399a1487838380`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c62cf5a0b55f78c6952456f627b45a4927bcd20a476a84feebb376a2e5afac`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 6.7 MB (6657921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3592c908208e8a16c99d3263902c97301ed446b46205bfcbb8d9ee8611123fa`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 89.2 KB (89218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd4c1986daa1bdd24f3621084f644cff84734eeb7aff037024fdf56f6aae3c1`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f41134be18ef5373326b3114ba85c9698be27a64dc12f0f60a1f5e6d0eac9`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 57.8 MB (57773398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaea47f5e1a31cc71bc565396dc93187e844d7f4ad7885746889e44dc40a4b`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a6f212eac3af392a8a5097e434764cff04c4e70ff2a9c1d4809c5c2e18d9e3`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:797fd1c255c0affbf4ea21c2af94c6f9904c76f433cacfb5aa44a15260ed50de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad921b63e93d9459a50c321f18aa4cad7866107facd5e54d1497bd0a6c86c6fd`

```dockerfile
```

-	Layers:
	-	`sha256:c9f2b5ad322c5b5af063de9a0bf790828d7771944a1fcec170e83a363c84a90c`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:0d871bea6fe47e7bf76b382ee2d4b128fe292b8fdb9082b21345c7d54cfdccae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123320023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cc1cb94b0e714568ec3d9021c42c78f629e704609cfc06069a093ad4a9fea0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1aa033c3dd6f9dcabf3e5db8b0d23e75bacc18083a9fc5fc3bf8dd32b531c9`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 17.1 MB (17141620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1075e78e61225557a73cb4df8bdb388a4e0a3a54d78fb029b95995467ee104`  
		Last Modified: Wed, 11 Sep 2024 02:01:31 GMT  
		Size: 17.8 MB (17783313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e371b1027e98e0af0c4a206108df3590c4135af5dd5c95267415707045a1884`  
		Last Modified: Wed, 11 Sep 2024 02:01:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226c034025ceb5a5072018428121e6627a7adea704c15385680801a1fd204fb`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dc19fcc1171071ce37cd5bee8802261a02276f6819a1116bba48770ae075f`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bf43051f6d401906c8b54ab26747cdead0e1b75ebec9c87fc12bf84d6dc5ed`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 7.0 MB (6984307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da17202765e315d32b089e1c25d097f8e0085fbb39264f5438693657418417`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 88.4 KB (88398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e960455cee8307842cd7579d74c83c6cb33ed93689bc96725f8ed7ebaf5d59b`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bbbc69f2a31b558cb399de570b4197e2b9834a828760b430ff42c27749a5b4`  
		Last Modified: Wed, 11 Sep 2024 02:50:52 GMT  
		Size: 53.5 MB (53494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103acb18844ccc79264ef2a516bb06bd5a0fecb9f01c581d3382253bdfa4423d`  
		Last Modified: Wed, 11 Sep 2024 02:50:51 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0f859154c8a30c4a41eb85bdfb5bafdd1617a0787c82c879a8a0575b531ac`  
		Last Modified: Wed, 11 Sep 2024 02:50:51 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:5c5a017a1a9973a3ee57ddf3ddb4efd0e946b7da75bf289ba07ff8a9143ba0a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ce3bf47c18b13d056ef62e3576f93da7e2113326d337a31b0e4d5e835a21de`

```dockerfile
```

-	Layers:
	-	`sha256:1dbc2fbc5d04bf6005bd82413353aa41ed322750380a145666a8789b6900915b`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:68d52b1f8e3a30d5c9ebe8531f1ceb2b14389dc70dc7f73fc640cc2612b0cb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121668199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28baeefb60bbf0c1f288b4ba28c02be3975f6866a625e2122122b2366329bc7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cf2b1859f16ea4a3efc3ebdcff929c005fc44c05d7202ce69bbd5258d6989a`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 17.1 MB (17129209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e839e120983d5ca2057bee14103b0d822031e067c63b69d5f7e1d0845a446`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 17.8 MB (17771142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29362d9881a8e2c6fd23dac747f90a311fd37d78cbe5bfe2bc93d137ca3f7b93`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b72324b3582fd670d40a641281f441939c93b3eec0c1a40744ce9f42d416aef`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20947c69fcf36566adb6594921006179ce40d22530bd7d0a5c2f9b50e15639`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3903b8a5e83aa88438bc00e6a21cbfb21f98d72bf4a90554fbbc9a67c624287`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 6.3 MB (6308115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a08d98b7b8a40124cdff9c9cfb28790278fd87f375c88ea1239edb53b70aedb`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 84.5 KB (84482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c31665ca29d651d05ff3ca3fdc61f6a67ce69e291415b2651008e20b66e92dc`  
		Last Modified: Wed, 11 Sep 2024 02:50:55 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdde100f6de66fb3973ccfa58803d39516f505beacbffa025f887a7a952e3af9`  
		Last Modified: Wed, 11 Sep 2024 02:50:57 GMT  
		Size: 53.5 MB (53494122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131ea12518408d5c3f587e5ce4fe43d86e73f90603ed92f2ae54b2d321e2d47a`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f824312e672e112fdb8abcca34a0ae94e522859b14b6ba6b92d991d2e996ba7`  
		Last Modified: Wed, 11 Sep 2024 02:50:57 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:4f69fea1e0e9bf4868790f90d7c7db9943225d34949695ace47f8784e814be93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db4c9ab2f89bb268cc28bcab911d9b7fc0a33b4e3b11b6b9baab0265727e3ae`

```dockerfile
```

-	Layers:
	-	`sha256:96e05737fa765bceaa6840ea6423d151ae12256c0d7a05d01ade85d7a178e388`  
		Last Modified: Wed, 11 Sep 2024 02:50:55 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e5140f28e7e82d172f34d88dfbd7a1bacbd4cbd3f24abdcaf1b0be485b916dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124152073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a7e2ef80ce4b0a550c648ddfb69a1953cdb927ca159fe704bf937bc8979d77`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eada7f8d96edf35fbf9cccdfe2a31683f121351212c1d270f7a73b2e1f530e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.2 MB (17186842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b544e07d92af2d47cc10db55727317ca8ccc95a899db6ce41cdd41cb820c0`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ca207ff0f9c918c07b12825084dba82e9f8c9d490f1ffcf33fe0c7b45fab2`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c5493b785a7581afc20e1db4ba86a79bd5e5e8ef3dfa1ad64620028e196eb`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e5be9720db99d659c53b6a67a1dd2ba6e958b7622248ab8dfc91c58d5c0f1d`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 7.0 MB (7034910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320bcabad1025e90ed07d105bd2724f1565672227ec5927061b082183adc6b11`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 98.7 KB (98650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9235e7f34f8cc28423dac4653e318c60d54cff3b0544a5e924074efdf31578`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9d4c07d55e9442550b66fb78c2d91de8856309dcc6875aa4c34aaa96f85316`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 53.4 MB (53398203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df4284aea7cda8255fd5026391b9b8b9db9af96da9875fe9db8f0185ac0ccd`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c51f22e855b132e7146b336aac0310cbe52e537cd77af861d9f27629b425ea6`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:fff328b2549d85866f264e626fb1fca2080ff3b685aa527410f3ea8ce95f38ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fd23934d6432c356a3df01ffbcf3ffbe9940918ffb9408d76137da20e3a2af`

```dockerfile
```

-	Layers:
	-	`sha256:23b22cd0119f1928542bdacdaf4016a4fa50c2fe26aa68aac38149f329c2acfd`  
		Last Modified: Wed, 11 Sep 2024 02:50:47 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:a85bf1d09cf0c684d7de3268d4c54b8bb152b79b53c1efa324cc8df94da42b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:5b34a2411903326499d2f67470d83ce97dc0183ca802e6fcf91ca1b564bf01bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154153776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e83a23dba859599f0adfa4a4b7996f23a41de2f5621f047074a9da77c6274f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db09d90694836eab5370b7d5f552b34f5772781701b00fd4e7c3950519ee72`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 7.9 MB (7872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538dd9aacd297989031c915937096bfdd889838bf150c05212223a9b3507070`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfaa9e1957304899a8d16f9cf6fca1ddbf8debde833e6b68831a81b50ee6fc2`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616c0277b4c4b06061b57f23022504d07faea54188b3a5b0d5b51dfa4e990b9`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.4 MB (18432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692e2842ca25a9bf245905f6e29b66a65bbdc85f1873aae896b69370566a5f9`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cd67bc2f21b34aeca4c5627b6b4b5dbede9b76ea404dd4079e77464166d0b`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966ec96386506904d07991e403853675dc204da54a5e1fd0c1abd1e6da10197`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1d01552a20f6313745d5d6563fc8a44c75d0010cb7cd94399a1487838380`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c62cf5a0b55f78c6952456f627b45a4927bcd20a476a84feebb376a2e5afac`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 6.7 MB (6657921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3592c908208e8a16c99d3263902c97301ed446b46205bfcbb8d9ee8611123fa`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 89.2 KB (89218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd4c1986daa1bdd24f3621084f644cff84734eeb7aff037024fdf56f6aae3c1`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f41134be18ef5373326b3114ba85c9698be27a64dc12f0f60a1f5e6d0eac9`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 57.8 MB (57773398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaea47f5e1a31cc71bc565396dc93187e844d7f4ad7885746889e44dc40a4b`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a6f212eac3af392a8a5097e434764cff04c4e70ff2a9c1d4809c5c2e18d9e3`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b065473b42eefb9a792eb005311c212c14df916c2575869263ae2fc25bd862`  
		Last Modified: Wed, 11 Sep 2024 03:48:49 GMT  
		Size: 981.0 KB (980986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852d28940731d27787147baf692114c5a57e84af5870515a9cf826785e61c97e`  
		Last Modified: Wed, 11 Sep 2024 03:48:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2754af7f7c8de794edb28a5c9f9ba8c90bdf84c274b9f556a39c0ea3240f1ab`  
		Last Modified: Wed, 11 Sep 2024 03:48:49 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636b57c4498bf4e949f7e09044a06c834e167dc3facda3697e3e1fff4b1739e8`  
		Last Modified: Wed, 11 Sep 2024 03:48:50 GMT  
		Size: 21.3 MB (21287315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f993cc096d161b79e4c922715fa6fe0c3d065ffa32abe11cf805a5937def91`  
		Last Modified: Wed, 11 Sep 2024 03:48:50 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c3fb49a3f69e9f44f3a3f159a35777da8859fb3530256aa2e196c953dfb4f8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7759138f227c5ac9b927aa368e0931f67ea0cd6196dfc9785aa8c3d4a23bacd`

```dockerfile
```

-	Layers:
	-	`sha256:7fc1f180c7e9851ada027667060ef9f9afc83a449caaccc1e42e3f58de86ba7d`  
		Last Modified: Wed, 11 Sep 2024 03:48:49 GMT  
		Size: 30.6 KB (30580 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bcedcdbefd4c0a8026ca435140dd2260a8b8de76d7f7ca5aa88030b661852828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148310987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d21859101d6a92e4bdb3cd0fc0396aab45b56110d1c29617704bda32774c45`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eada7f8d96edf35fbf9cccdfe2a31683f121351212c1d270f7a73b2e1f530e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.2 MB (17186842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b544e07d92af2d47cc10db55727317ca8ccc95a899db6ce41cdd41cb820c0`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ca207ff0f9c918c07b12825084dba82e9f8c9d490f1ffcf33fe0c7b45fab2`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c5493b785a7581afc20e1db4ba86a79bd5e5e8ef3dfa1ad64620028e196eb`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e5be9720db99d659c53b6a67a1dd2ba6e958b7622248ab8dfc91c58d5c0f1d`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 7.0 MB (7034910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320bcabad1025e90ed07d105bd2724f1565672227ec5927061b082183adc6b11`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 98.7 KB (98650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9235e7f34f8cc28423dac4653e318c60d54cff3b0544a5e924074efdf31578`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9d4c07d55e9442550b66fb78c2d91de8856309dcc6875aa4c34aaa96f85316`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 53.4 MB (53398203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df4284aea7cda8255fd5026391b9b8b9db9af96da9875fe9db8f0185ac0ccd`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c51f22e855b132e7146b336aac0310cbe52e537cd77af861d9f27629b425ea6`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61abcef331c5400bd552a2b6a5ecc6d03ecee4f12e9cf72c4a866ec26c4e2fe7`  
		Last Modified: Wed, 11 Sep 2024 03:48:43 GMT  
		Size: 1.0 MB (1023119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0a2f42af77b9a719e519573af0f3e531e92847a4b6f6095d42ffb21b48ae44`  
		Last Modified: Wed, 11 Sep 2024 03:48:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d713d1485ac825869be3a208d8d2699337d7ce096e81e2eeab4f7fc83fd0cc`  
		Last Modified: Wed, 11 Sep 2024 03:48:43 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c70f1919f2604484b0212c929c9881df57425101e48ec186fc604ca7b74c92e`  
		Last Modified: Wed, 11 Sep 2024 03:48:44 GMT  
		Size: 23.1 MB (23134441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab61b3f82263bbf4714ce5dc1a9816f6c16b3a159cd8e8cf873a94ce857aaeb1`  
		Last Modified: Wed, 11 Sep 2024 03:48:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0cdb6cb36b46b803fec1343b539275b39b36043f1df4e6fd6c3dc696980ca15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4a5c6803fcd314f69e271e0c35c18f4c05e2f48eaf0c977c298dcc6a732c71`

```dockerfile
```

-	Layers:
	-	`sha256:e6bc659420a6a66c2ebcb45c47ea7e01bff903c946a478d6fe5246ea077cdc54`  
		Last Modified: Wed, 11 Sep 2024 03:48:42 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:294f99b7749b47d3bfac8535c231a6c47cd0f28be8205af83928b2dde18abda7
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
$ docker pull docker@sha256:9218d2dc6ab909992500f116eb49948376fb23f5cd9ccf427dd62b3d865ea49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131884120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371f9f35b2da407e86e3d81ea7a4efc0594697c3abb6b47bac15bbfa0533f293`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db09d90694836eab5370b7d5f552b34f5772781701b00fd4e7c3950519ee72`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 7.9 MB (7872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538dd9aacd297989031c915937096bfdd889838bf150c05212223a9b3507070`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfaa9e1957304899a8d16f9cf6fca1ddbf8debde833e6b68831a81b50ee6fc2`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616c0277b4c4b06061b57f23022504d07faea54188b3a5b0d5b51dfa4e990b9`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.4 MB (18432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692e2842ca25a9bf245905f6e29b66a65bbdc85f1873aae896b69370566a5f9`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cd67bc2f21b34aeca4c5627b6b4b5dbede9b76ea404dd4079e77464166d0b`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966ec96386506904d07991e403853675dc204da54a5e1fd0c1abd1e6da10197`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1d01552a20f6313745d5d6563fc8a44c75d0010cb7cd94399a1487838380`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c62cf5a0b55f78c6952456f627b45a4927bcd20a476a84feebb376a2e5afac`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 6.7 MB (6657921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3592c908208e8a16c99d3263902c97301ed446b46205bfcbb8d9ee8611123fa`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 89.2 KB (89218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd4c1986daa1bdd24f3621084f644cff84734eeb7aff037024fdf56f6aae3c1`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f41134be18ef5373326b3114ba85c9698be27a64dc12f0f60a1f5e6d0eac9`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 57.8 MB (57773398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaea47f5e1a31cc71bc565396dc93187e844d7f4ad7885746889e44dc40a4b`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a6f212eac3af392a8a5097e434764cff04c4e70ff2a9c1d4809c5c2e18d9e3`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:797fd1c255c0affbf4ea21c2af94c6f9904c76f433cacfb5aa44a15260ed50de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad921b63e93d9459a50c321f18aa4cad7866107facd5e54d1497bd0a6c86c6fd`

```dockerfile
```

-	Layers:
	-	`sha256:c9f2b5ad322c5b5af063de9a0bf790828d7771944a1fcec170e83a363c84a90c`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:0d871bea6fe47e7bf76b382ee2d4b128fe292b8fdb9082b21345c7d54cfdccae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123320023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cc1cb94b0e714568ec3d9021c42c78f629e704609cfc06069a093ad4a9fea0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1aa033c3dd6f9dcabf3e5db8b0d23e75bacc18083a9fc5fc3bf8dd32b531c9`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 17.1 MB (17141620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1075e78e61225557a73cb4df8bdb388a4e0a3a54d78fb029b95995467ee104`  
		Last Modified: Wed, 11 Sep 2024 02:01:31 GMT  
		Size: 17.8 MB (17783313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e371b1027e98e0af0c4a206108df3590c4135af5dd5c95267415707045a1884`  
		Last Modified: Wed, 11 Sep 2024 02:01:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226c034025ceb5a5072018428121e6627a7adea704c15385680801a1fd204fb`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dc19fcc1171071ce37cd5bee8802261a02276f6819a1116bba48770ae075f`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bf43051f6d401906c8b54ab26747cdead0e1b75ebec9c87fc12bf84d6dc5ed`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 7.0 MB (6984307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da17202765e315d32b089e1c25d097f8e0085fbb39264f5438693657418417`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 88.4 KB (88398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e960455cee8307842cd7579d74c83c6cb33ed93689bc96725f8ed7ebaf5d59b`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bbbc69f2a31b558cb399de570b4197e2b9834a828760b430ff42c27749a5b4`  
		Last Modified: Wed, 11 Sep 2024 02:50:52 GMT  
		Size: 53.5 MB (53494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103acb18844ccc79264ef2a516bb06bd5a0fecb9f01c581d3382253bdfa4423d`  
		Last Modified: Wed, 11 Sep 2024 02:50:51 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0f859154c8a30c4a41eb85bdfb5bafdd1617a0787c82c879a8a0575b531ac`  
		Last Modified: Wed, 11 Sep 2024 02:50:51 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:5c5a017a1a9973a3ee57ddf3ddb4efd0e946b7da75bf289ba07ff8a9143ba0a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ce3bf47c18b13d056ef62e3576f93da7e2113326d337a31b0e4d5e835a21de`

```dockerfile
```

-	Layers:
	-	`sha256:1dbc2fbc5d04bf6005bd82413353aa41ed322750380a145666a8789b6900915b`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:68d52b1f8e3a30d5c9ebe8531f1ceb2b14389dc70dc7f73fc640cc2612b0cb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121668199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28baeefb60bbf0c1f288b4ba28c02be3975f6866a625e2122122b2366329bc7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cf2b1859f16ea4a3efc3ebdcff929c005fc44c05d7202ce69bbd5258d6989a`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 17.1 MB (17129209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e839e120983d5ca2057bee14103b0d822031e067c63b69d5f7e1d0845a446`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 17.8 MB (17771142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29362d9881a8e2c6fd23dac747f90a311fd37d78cbe5bfe2bc93d137ca3f7b93`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b72324b3582fd670d40a641281f441939c93b3eec0c1a40744ce9f42d416aef`  
		Last Modified: Wed, 11 Sep 2024 02:01:57 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20947c69fcf36566adb6594921006179ce40d22530bd7d0a5c2f9b50e15639`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3903b8a5e83aa88438bc00e6a21cbfb21f98d72bf4a90554fbbc9a67c624287`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 6.3 MB (6308115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a08d98b7b8a40124cdff9c9cfb28790278fd87f375c88ea1239edb53b70aedb`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 84.5 KB (84482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c31665ca29d651d05ff3ca3fdc61f6a67ce69e291415b2651008e20b66e92dc`  
		Last Modified: Wed, 11 Sep 2024 02:50:55 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdde100f6de66fb3973ccfa58803d39516f505beacbffa025f887a7a952e3af9`  
		Last Modified: Wed, 11 Sep 2024 02:50:57 GMT  
		Size: 53.5 MB (53494122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131ea12518408d5c3f587e5ce4fe43d86e73f90603ed92f2ae54b2d321e2d47a`  
		Last Modified: Wed, 11 Sep 2024 02:50:56 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f824312e672e112fdb8abcca34a0ae94e522859b14b6ba6b92d991d2e996ba7`  
		Last Modified: Wed, 11 Sep 2024 02:50:57 GMT  
		Size: 3.3 KB (3266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:4f69fea1e0e9bf4868790f90d7c7db9943225d34949695ace47f8784e814be93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db4c9ab2f89bb268cc28bcab911d9b7fc0a33b4e3b11b6b9baab0265727e3ae`

```dockerfile
```

-	Layers:
	-	`sha256:96e05737fa765bceaa6840ea6423d151ae12256c0d7a05d01ade85d7a178e388`  
		Last Modified: Wed, 11 Sep 2024 02:50:55 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e5140f28e7e82d172f34d88dfbd7a1bacbd4cbd3f24abdcaf1b0be485b916dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124152073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a7e2ef80ce4b0a550c648ddfb69a1953cdb927ca159fe704bf937bc8979d77`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eada7f8d96edf35fbf9cccdfe2a31683f121351212c1d270f7a73b2e1f530e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.2 MB (17186842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b544e07d92af2d47cc10db55727317ca8ccc95a899db6ce41cdd41cb820c0`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ca207ff0f9c918c07b12825084dba82e9f8c9d490f1ffcf33fe0c7b45fab2`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c5493b785a7581afc20e1db4ba86a79bd5e5e8ef3dfa1ad64620028e196eb`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e5be9720db99d659c53b6a67a1dd2ba6e958b7622248ab8dfc91c58d5c0f1d`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 7.0 MB (7034910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320bcabad1025e90ed07d105bd2724f1565672227ec5927061b082183adc6b11`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 98.7 KB (98650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9235e7f34f8cc28423dac4653e318c60d54cff3b0544a5e924074efdf31578`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9d4c07d55e9442550b66fb78c2d91de8856309dcc6875aa4c34aaa96f85316`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 53.4 MB (53398203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df4284aea7cda8255fd5026391b9b8b9db9af96da9875fe9db8f0185ac0ccd`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c51f22e855b132e7146b336aac0310cbe52e537cd77af861d9f27629b425ea6`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:fff328b2549d85866f264e626fb1fca2080ff3b685aa527410f3ea8ce95f38ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fd23934d6432c356a3df01ffbcf3ffbe9940918ffb9408d76137da20e3a2af`

```dockerfile
```

-	Layers:
	-	`sha256:23b22cd0119f1928542bdacdaf4016a4fa50c2fe26aa68aac38149f329c2acfd`  
		Last Modified: Wed, 11 Sep 2024 02:50:47 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:27ba43da317d5f4e4a2de77459eaf2e80d335f279f539e96243b98c45a9d504e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:a82aa3fe951a62771fff8170c24096425b50bc9e264286388152fa9b81712f5f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520410181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d257b03e5fade898fde7ea9c893f1a592471ad97e4ed6492b7b212b24c1ce0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 02:06:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 02:06:38 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 02:06:38 GMT
ENV DOCKER_VERSION=27.2.1
# Wed, 11 Sep 2024 02:06:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Wed, 11 Sep 2024 02:06:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:06:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Wed, 11 Sep 2024 02:06:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.windows-amd64.exe
# Wed, 11 Sep 2024 02:06:51 GMT
ENV DOCKER_BUILDX_SHA256=2bee3541fd1ed077d5f59141085f59345d0d0380d5749724e7088a3f02a113ca
# Wed, 11 Sep 2024 02:07:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:07:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 11 Sep 2024 02:07:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 11 Sep 2024 02:07:11 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 11 Sep 2024 02:07:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e2f86d5d1b2a5b865a052fc16b9166a550aed670add96ae7a6548a82b5b722`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8981ca84e679b362967aa517438bf611399eb20ea708bf9471e8f84100dfa7`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 342.6 KB (342630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0c9302154e848dc4bb0463644b87c8fae31baa96db751b75bc3a5d8195cbbe`  
		Last Modified: Wed, 11 Sep 2024 02:07:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41a22741d542661237a8d8e85456308c1cbd52d9498dfa0dfcbb566e1cc355a`  
		Last Modified: Wed, 11 Sep 2024 02:07:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6c4124d41c5d00b862e39fbfb5816f520bd94f02a0b82f582598effce81572`  
		Last Modified: Wed, 11 Sep 2024 02:07:37 GMT  
		Size: 18.9 MB (18913958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d5d0294c55c8e2b4a0761ea1eebf18f69f9d4c1846d0f84567e1edfe6e9217`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a83a411f2cf4b9fd720c3e578a348825577e84a74daff8dbfb10038588e534`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a320c69ba98bd2a4ead0142a9ee82e878541eb3d5f88492e25d026f0b0bc944`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97bc35449386503b924207a0b594a8b7459f1f88bdc3f42653bbe2b1841a475`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 19.3 MB (19269057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682ff78fabece6bcee7bf9b7da73568924352f978504e36a2cfc9110de462937`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8d54a118d4d3fe5c1dc907fadd1281ab71ea5600577a59956ba52226d5c42b`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8a9795b6d3907b92f407b716652f11fbc26030e2d49880aef8d6fdc0bfaea6`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f1a7d56c884d1afe4dc68cc0ac1f9189826bcee13efbb385acd42fc1ca3f9e`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 19.7 MB (19680496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:4d1e8b301b0c6ae81034443c38a212eec26f46cd4f59a332c68cd62eb0f09f92
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778456457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d2275e0c50e1a2778828b1c989942d819123b07583313ea0ac4522e03ce58c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 02:04:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 02:04:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 02:04:37 GMT
ENV DOCKER_VERSION=27.2.1
# Wed, 11 Sep 2024 02:04:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Wed, 11 Sep 2024 02:04:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:04:49 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Wed, 11 Sep 2024 02:04:49 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.windows-amd64.exe
# Wed, 11 Sep 2024 02:04:50 GMT
ENV DOCKER_BUILDX_SHA256=2bee3541fd1ed077d5f59141085f59345d0d0380d5749724e7088a3f02a113ca
# Wed, 11 Sep 2024 02:05:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:05:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 11 Sep 2024 02:05:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 11 Sep 2024 02:05:02 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 11 Sep 2024 02:05:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96305c41a993336ed17fc44e0e2bc51503e0e9b085c1f5cb642e396ab1d76ca5`  
		Last Modified: Wed, 11 Sep 2024 02:05:22 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90dcbc14d4e1aeb8ff8091b77163592eff3b0e11712fb83acf11cfca78be489`  
		Last Modified: Wed, 11 Sep 2024 02:05:23 GMT  
		Size: 330.4 KB (330375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae07341e5dcd520c87adee68815b0c466c03ab267fd0f757b67081ade1ff210`  
		Last Modified: Wed, 11 Sep 2024 02:05:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7973ed8b5a6d11094c8d4c2433a60c5a5fcfcb84b1f9163d275729bc8c9c75`  
		Last Modified: Wed, 11 Sep 2024 02:05:21 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076ffff23dfa564b4c5b62d9bda15f2f3257a29a8480e79f445bc1eac2976a6b`  
		Last Modified: Wed, 11 Sep 2024 02:05:23 GMT  
		Size: 18.9 MB (18911033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d1ca83016e2f178e867b86522bccc3c667320c2852da1a4d8c3ff193581105`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87986c7e4d5811794113e6437168a3f46ca14249232e5d226230840cbbeeeca`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5abefd76cb19ba3f5d50ae3b4dd66278517f9a1c2cb758f0a2898a960c55e8a`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c490aa0bb5fad395420b48468b3d32ffc9368901095cac9b73061ee54745c6`  
		Last Modified: Wed, 11 Sep 2024 02:05:20 GMT  
		Size: 19.3 MB (19264623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd8a155e1236c2faacf3433d3f3bfdbb991624d0ba0360937cca5d1e8a24ed2`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b554c6c79e64ef1bf1f3b97d2096f9cba53dc60c7ea8a8e37af03a3673285ea`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa1591f79c5c535c392829fc79152d4632d9a14cd22af2be1768c5b25ee91c0`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f570820d723f568887ddd5f8674cf19f3066dae96c6b4e052ac1b919e22596`  
		Last Modified: Wed, 11 Sep 2024 02:05:20 GMT  
		Size: 19.7 MB (19669920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:5cc4548517a5d2cd96e9f4922bbac7b8c09ecf55aec9d8941748e352a57dfe4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:4d1e8b301b0c6ae81034443c38a212eec26f46cd4f59a332c68cd62eb0f09f92
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778456457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d2275e0c50e1a2778828b1c989942d819123b07583313ea0ac4522e03ce58c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 02:04:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 02:04:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 02:04:37 GMT
ENV DOCKER_VERSION=27.2.1
# Wed, 11 Sep 2024 02:04:38 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Wed, 11 Sep 2024 02:04:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:04:49 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Wed, 11 Sep 2024 02:04:49 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.windows-amd64.exe
# Wed, 11 Sep 2024 02:04:50 GMT
ENV DOCKER_BUILDX_SHA256=2bee3541fd1ed077d5f59141085f59345d0d0380d5749724e7088a3f02a113ca
# Wed, 11 Sep 2024 02:05:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:05:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 11 Sep 2024 02:05:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 11 Sep 2024 02:05:02 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 11 Sep 2024 02:05:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96305c41a993336ed17fc44e0e2bc51503e0e9b085c1f5cb642e396ab1d76ca5`  
		Last Modified: Wed, 11 Sep 2024 02:05:22 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90dcbc14d4e1aeb8ff8091b77163592eff3b0e11712fb83acf11cfca78be489`  
		Last Modified: Wed, 11 Sep 2024 02:05:23 GMT  
		Size: 330.4 KB (330375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae07341e5dcd520c87adee68815b0c466c03ab267fd0f757b67081ade1ff210`  
		Last Modified: Wed, 11 Sep 2024 02:05:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7973ed8b5a6d11094c8d4c2433a60c5a5fcfcb84b1f9163d275729bc8c9c75`  
		Last Modified: Wed, 11 Sep 2024 02:05:21 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076ffff23dfa564b4c5b62d9bda15f2f3257a29a8480e79f445bc1eac2976a6b`  
		Last Modified: Wed, 11 Sep 2024 02:05:23 GMT  
		Size: 18.9 MB (18911033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d1ca83016e2f178e867b86522bccc3c667320c2852da1a4d8c3ff193581105`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87986c7e4d5811794113e6437168a3f46ca14249232e5d226230840cbbeeeca`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5abefd76cb19ba3f5d50ae3b4dd66278517f9a1c2cb758f0a2898a960c55e8a`  
		Last Modified: Wed, 11 Sep 2024 02:05:19 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c490aa0bb5fad395420b48468b3d32ffc9368901095cac9b73061ee54745c6`  
		Last Modified: Wed, 11 Sep 2024 02:05:20 GMT  
		Size: 19.3 MB (19264623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd8a155e1236c2faacf3433d3f3bfdbb991624d0ba0360937cca5d1e8a24ed2`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b554c6c79e64ef1bf1f3b97d2096f9cba53dc60c7ea8a8e37af03a3673285ea`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa1591f79c5c535c392829fc79152d4632d9a14cd22af2be1768c5b25ee91c0`  
		Last Modified: Wed, 11 Sep 2024 02:05:17 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f570820d723f568887ddd5f8674cf19f3066dae96c6b4e052ac1b919e22596`  
		Last Modified: Wed, 11 Sep 2024 02:05:20 GMT  
		Size: 19.7 MB (19669920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:421236c754a43a1f842fbcf8e4f9232fd85ea35de3ece64703e37089e70d5b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:a82aa3fe951a62771fff8170c24096425b50bc9e264286388152fa9b81712f5f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520410181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d257b03e5fade898fde7ea9c893f1a592471ad97e4ed6492b7b212b24c1ce0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 02:06:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 02:06:38 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 02:06:38 GMT
ENV DOCKER_VERSION=27.2.1
# Wed, 11 Sep 2024 02:06:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Wed, 11 Sep 2024 02:06:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:06:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Wed, 11 Sep 2024 02:06:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.windows-amd64.exe
# Wed, 11 Sep 2024 02:06:51 GMT
ENV DOCKER_BUILDX_SHA256=2bee3541fd1ed077d5f59141085f59345d0d0380d5749724e7088a3f02a113ca
# Wed, 11 Sep 2024 02:07:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 02:07:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Wed, 11 Sep 2024 02:07:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-windows-x86_64.exe
# Wed, 11 Sep 2024 02:07:11 GMT
ENV DOCKER_COMPOSE_SHA256=59cd2bd789ab2e5920674b8ac5d17a19a684b1622f17c847cc7361e832508d25
# Wed, 11 Sep 2024 02:07:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e2f86d5d1b2a5b865a052fc16b9166a550aed670add96ae7a6548a82b5b722`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8981ca84e679b362967aa517438bf611399eb20ea708bf9471e8f84100dfa7`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 342.6 KB (342630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0c9302154e848dc4bb0463644b87c8fae31baa96db751b75bc3a5d8195cbbe`  
		Last Modified: Wed, 11 Sep 2024 02:07:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41a22741d542661237a8d8e85456308c1cbd52d9498dfa0dfcbb566e1cc355a`  
		Last Modified: Wed, 11 Sep 2024 02:07:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6c4124d41c5d00b862e39fbfb5816f520bd94f02a0b82f582598effce81572`  
		Last Modified: Wed, 11 Sep 2024 02:07:37 GMT  
		Size: 18.9 MB (18913958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d5d0294c55c8e2b4a0761ea1eebf18f69f9d4c1846d0f84567e1edfe6e9217`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a83a411f2cf4b9fd720c3e578a348825577e84a74daff8dbfb10038588e534`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a320c69ba98bd2a4ead0142a9ee82e878541eb3d5f88492e25d026f0b0bc944`  
		Last Modified: Wed, 11 Sep 2024 02:07:34 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97bc35449386503b924207a0b594a8b7459f1f88bdc3f42653bbe2b1841a475`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 19.3 MB (19269057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682ff78fabece6bcee7bf9b7da73568924352f978504e36a2cfc9110de462937`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8d54a118d4d3fe5c1dc907fadd1281ab71ea5600577a59956ba52226d5c42b`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8a9795b6d3907b92f407b716652f11fbc26030e2d49880aef8d6fdc0bfaea6`  
		Last Modified: Wed, 11 Sep 2024 02:07:33 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f1a7d56c884d1afe4dc68cc0ac1f9189826bcee13efbb385acd42fc1ca3f9e`  
		Last Modified: Wed, 11 Sep 2024 02:07:36 GMT  
		Size: 19.7 MB (19680496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
