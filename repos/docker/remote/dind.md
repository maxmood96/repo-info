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
