## `docker:dind`

```console
$ docker pull docker@sha256:dc7e8a79a9128d5b79634d797eec4b569c617be87bc8adf6c555471b666b8390
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
$ docker pull docker@sha256:2b7a1976c4a53cf6aa1763846a2017c19d7111b397aebface32e146ac78ad044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127283315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13eace1e41339036e4e89c7c1819f6ef2eeaebd98800e7848cc042f410b953e7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 21:16:36 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DOCKER_VERSION=26.0.0
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-x86_64'; 			sha256='53641b8a28419f947bc58c085e0c39b97a209b6e875a25c585e7fab44ff48576'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv6'; 			sha256='a123b79b530a65c7381ca8bb3b29cde7177f4f260984a127d998c9696cae794c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv7'; 			sha256='8ea72e93e8da8259d7d5d051f3c65dc14c44a23d5ebc6939394d7d03b147e238'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-aarch64'; 			sha256='b9f303c9f9db75ecf18ea6fc516b3dc54a3e54f3b3d8e7f1a449416522958bc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-ppc64le'; 			sha256='dc067ab61239cef3d2e145d37fcd68c1fc2320c6728d77a9a4ec4fb0e6c6dd64'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-riscv64'; 			sha256='a17f07604fa74c661e62d5e27ae358f8a611f42bb9a4a147cec76b8bb591bea4'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-s390x'; 			sha256='9e613275e5fa46cb864d3f2fccb10e3239b879527d075490b03e381df56c397c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 20 Mar 2024 21:16:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 21:16:36 GMT
CMD ["sh"]
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
VOLUME [/var/lib/docker]
# Wed, 20 Mar 2024 21:16:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 20 Mar 2024 21:16:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 20 Mar 2024 21:16:36 GMT
CMD []
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdb6de66fda55f56b7ab6980c7fdf2d9e209da3033cb0293c8cc704e8bb0ef6`  
		Last Modified: Wed, 20 Mar 2024 23:48:44 GMT  
		Size: 2.0 MB (2026147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c771eb93ec5bd3520e736684668f082f4167bb9d73a6eed2520ef23b9f4ba463`  
		Last Modified: Wed, 20 Mar 2024 23:48:44 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e29b047ab04ee6e37f7104f68c68fd6564bca7a8bfbef36deeeb169afce2ceb`  
		Last Modified: Wed, 20 Mar 2024 23:48:44 GMT  
		Size: 17.0 MB (16973517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3710403c640747ba94b0f415725d0f404e5d8d95b7b88a226d8fd8f57ea7b605`  
		Last Modified: Wed, 20 Mar 2024 23:48:44 GMT  
		Size: 18.0 MB (17982281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9679d11221eb6a98e00943212fe88ad57e8d6701c23767650140f9c5805e38c3`  
		Last Modified: Wed, 20 Mar 2024 23:48:45 GMT  
		Size: 18.2 MB (18222096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f4d5ff082daa1c68098588fd89ed23af01bd914cfb3ec97ae11d3a8cf0729b`  
		Last Modified: Wed, 20 Mar 2024 23:48:45 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8619895a28173934e99763760b58c76a7ec1b136d94cf3a281292e2984c6e0a7`  
		Last Modified: Wed, 20 Mar 2024 23:48:45 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54189544cd145f9ab133431d29eaee6f2e849df9ad60fe5e8121d779a13756d`  
		Last Modified: Wed, 20 Mar 2024 23:48:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84a70fc4b4ac552e4449a9cd8356f7efcd9ed154188aef0f38954cb7c5973e2`  
		Last Modified: Thu, 21 Mar 2024 00:48:48 GMT  
		Size: 12.2 MB (12157265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d627717fa4a5a770bd9113e3c050487b245cb4050a46f34ad85cce1e56fd46b9`  
		Last Modified: Thu, 21 Mar 2024 00:48:48 GMT  
		Size: 89.1 KB (89122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae029e9742abfe15291798ff75afdced4917d3faf251f017bf9b428bd61ed1c`  
		Last Modified: Thu, 21 Mar 2024 00:48:48 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb1a6803abba8cf22071521a60d65e410ff4140270b183aca37126523cd61fa`  
		Last Modified: Thu, 21 Mar 2024 00:48:49 GMT  
		Size: 56.4 MB (56415837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19a36bc3c9deea901b487fbe183cbdc5903239559b8d8b0d7ec0837525e7289`  
		Last Modified: Thu, 21 Mar 2024 00:48:49 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46bb1846743f5d20c9a85768a2008ffbb52b19cc55ff7a5aa6a09a2de753bd5`  
		Last Modified: Thu, 21 Mar 2024 00:48:49 GMT  
		Size: 3.3 KB (3251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:2bf2e086288da86ab904652bc46deeff981cdfafcbcc8d3007d4766a42504471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **880.9 KB (880856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d517ba2fb3dfc2973aa0242b0e919b0a6b96949c5892d3a2a689e1ad2422f91a`

```dockerfile
```

-	Layers:
	-	`sha256:c2465df492bd9e618aebc45c925a7086872da7e46ec44ffdcfde53e54c16c351`  
		Last Modified: Thu, 21 Mar 2024 00:48:48 GMT  
		Size: 844.6 KB (844604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84c7972304a2ec65d059f47bf3ffcb76c9dbb1739245e6cef8d8cab53951064d`  
		Last Modified: Thu, 21 Mar 2024 00:48:48 GMT  
		Size: 36.3 KB (36252 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:4a360f34b3ff46ee082d6a3737b2957f6f7e8574bc3dc12b00df35ce314a69c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119156087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736c9cf173f750b7912ba202907b81abcad20c709187b6b51fe60aa6c8192c63`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_VERSION=25.0.5
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-x86_64'; 			sha256='53641b8a28419f947bc58c085e0c39b97a209b6e875a25c585e7fab44ff48576'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv6'; 			sha256='a123b79b530a65c7381ca8bb3b29cde7177f4f260984a127d998c9696cae794c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv7'; 			sha256='8ea72e93e8da8259d7d5d051f3c65dc14c44a23d5ebc6939394d7d03b147e238'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-aarch64'; 			sha256='b9f303c9f9db75ecf18ea6fc516b3dc54a3e54f3b3d8e7f1a449416522958bc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-ppc64le'; 			sha256='dc067ab61239cef3d2e145d37fcd68c1fc2320c6728d77a9a4ec4fb0e6c6dd64'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-riscv64'; 			sha256='a17f07604fa74c661e62d5e27ae358f8a611f42bb9a4a147cec76b8bb591bea4'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-s390x'; 			sha256='9e613275e5fa46cb864d3f2fccb10e3239b879527d075490b03e381df56c397c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Mar 2024 21:53:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
CMD ["sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
VOLUME [/var/lib/docker]
# Tue, 19 Mar 2024 21:53:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 Mar 2024 21:53:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
CMD []
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01caa1f2ad567ce3e9411d6fbb1a235b66eeb21d7eeb46ed1e27573cd84ee81`  
		Last Modified: Tue, 19 Mar 2024 11:24:20 GMT  
		Size: 2.1 MB (2116767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecefc70f328ab16c814c8e8d5e971c89cc79c0aaf9f67e97ba9e353d4689fd7`  
		Last Modified: Tue, 19 Mar 2024 11:24:19 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c46c89da93c1e514fde40a9bedc8bdec9c647ac9a3fc969df984e06fed01b76`  
		Last Modified: Wed, 20 Mar 2024 00:48:49 GMT  
		Size: 15.3 MB (15274104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8822134e50060fa90a050854faaecf2fc26a7fbd99dbe2d38b370791be194527`  
		Last Modified: Wed, 20 Mar 2024 00:48:49 GMT  
		Size: 16.8 MB (16818357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee3d3701903ee7ad1ffa7925952b0b7fade8356bd65ad0d94b277ccabf3d36a`  
		Last Modified: Wed, 20 Mar 2024 00:48:49 GMT  
		Size: 17.2 MB (17219031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59ecef79be5c285b3c4fe3379bb54699d6fb56fea51528e0c1e3d52529f4933`  
		Last Modified: Wed, 20 Mar 2024 00:48:48 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f16d1d565131f175e13979fa87ff6b51d3c07ce76bada87148a4598337e22a`  
		Last Modified: Wed, 20 Mar 2024 00:48:49 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e858a793aa05ca39c5477b549d241b19b5e941cef33e68de9424015ec84bff77`  
		Last Modified: Wed, 20 Mar 2024 00:48:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b5036f918aeb3832d71fa0ccdd80ee5ca1ccffd117f579a274a3a419a1806c`  
		Last Modified: Wed, 20 Mar 2024 04:02:04 GMT  
		Size: 12.4 MB (12433668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e06ebb46a274c484f66dd0014ec4737db871bc2bbaa14e5ec00b0fa69622090`  
		Last Modified: Wed, 20 Mar 2024 04:02:03 GMT  
		Size: 88.4 KB (88351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa82aa6c0400963485160d75c585c7d87de484295333d9ee46b081e44dc58cc`  
		Last Modified: Wed, 20 Mar 2024 04:02:03 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8b7a8fdb404e5242f979a054adb13835262876c6112e08293a61a85f790ffd`  
		Last Modified: Wed, 20 Mar 2024 04:02:05 GMT  
		Size: 52.0 MB (52032095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61de8b50e95b52289f65e10dcff40a42e966e55cc693085d80c9b861b5de3e8b`  
		Last Modified: Wed, 20 Mar 2024 04:02:04 GMT  
		Size: 1.5 KB (1507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4942ee2e38d0f4699e87dc4b2561b5df77e40411c5f8eddf80d3966dd3f7c9b1`  
		Last Modified: Wed, 20 Mar 2024 04:02:04 GMT  
		Size: 3.2 KB (3248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:d4508547c8ac7e6460cfe3fe0c8ea6c67b24f02a20e691dc9a87285af99911e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a090f81e2b423a75cdf7798fdfcd470322b93c07013ba3caaca51789a54eb0b1`

```dockerfile
```

-	Layers:
	-	`sha256:a3292cb44bf8b048f98a37bcfcdaf700a7e67c364347f92066861bda8fc66238`  
		Last Modified: Wed, 20 Mar 2024 04:02:02 GMT  
		Size: 37.5 KB (37492 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:8839d5b99470fa824dfb2a547dc45c71640a9f98ac5ff4ef11e7f96dd1c52fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118259970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821ff3d9b560769e9463dd6f4643700790ed8e8a0a55c829e674f263630f7b42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 21:16:36 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DOCKER_VERSION=26.0.0
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-x86_64'; 			sha256='53641b8a28419f947bc58c085e0c39b97a209b6e875a25c585e7fab44ff48576'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv6'; 			sha256='a123b79b530a65c7381ca8bb3b29cde7177f4f260984a127d998c9696cae794c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv7'; 			sha256='8ea72e93e8da8259d7d5d051f3c65dc14c44a23d5ebc6939394d7d03b147e238'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-aarch64'; 			sha256='b9f303c9f9db75ecf18ea6fc516b3dc54a3e54f3b3d8e7f1a449416522958bc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-ppc64le'; 			sha256='dc067ab61239cef3d2e145d37fcd68c1fc2320c6728d77a9a4ec4fb0e6c6dd64'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-riscv64'; 			sha256='a17f07604fa74c661e62d5e27ae358f8a611f42bb9a4a147cec76b8bb591bea4'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-s390x'; 			sha256='9e613275e5fa46cb864d3f2fccb10e3239b879527d075490b03e381df56c397c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 20 Mar 2024 21:16:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 21:16:36 GMT
CMD ["sh"]
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
VOLUME [/var/lib/docker]
# Wed, 20 Mar 2024 21:16:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 20 Mar 2024 21:16:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 20 Mar 2024 21:16:36 GMT
CMD []
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62203ebc003cf77a4ff92a3c67a89cd14dcf1adf84fb125d2f3329ad08ad9a61`  
		Last Modified: Sat, 16 Mar 2024 15:21:10 GMT  
		Size: 1.9 MB (1896160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8418dd6a88f431ade9efd4277500a4c6483d9ac98459ff95a86dbfde7d02e2a`  
		Last Modified: Sat, 16 Mar 2024 15:21:10 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379a08f7972893d46b71e7b905cdc61d943b0d710bae6cd5d41985a5bb36f184`  
		Last Modified: Wed, 20 Mar 2024 23:55:51 GMT  
		Size: 15.3 MB (15347101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709298659c489dcbb4eb40106515d6d66d8044bcf98e5880042f03dcfec5c8fb`  
		Last Modified: Wed, 20 Mar 2024 23:55:51 GMT  
		Size: 16.8 MB (16804622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b2c6f906582539ea6382813ee8ef718777a8b8b8584178e30acb1431a9c930`  
		Last Modified: Wed, 20 Mar 2024 23:55:57 GMT  
		Size: 17.2 MB (17207777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db38281afc48ce14d28f654bc6bf095140b86c2265b4784d235f79b1f935848`  
		Last Modified: Wed, 20 Mar 2024 23:55:51 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c84d702e8a91df02f6bde02ca30235406feb024d33b8eebeecb644e053b254`  
		Last Modified: Wed, 20 Mar 2024 23:55:52 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503357f5dee4c4d0f24ac158696ac81f972fa195014a48e2afb690028f514bde`  
		Last Modified: Wed, 20 Mar 2024 23:55:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b0bb7f3f1aa819aa834721a36fc57e133759f042793bd1916c3bdc7d032fa8`  
		Last Modified: Thu, 21 Mar 2024 00:49:18 GMT  
		Size: 11.3 MB (11274374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45731b9332ed01bcff5a5b5793f51248c319ebd3a5730dabeb685373db69aaa7`  
		Last Modified: Thu, 21 Mar 2024 00:49:18 GMT  
		Size: 84.3 KB (84272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca3140f38ea958a49d77bc54abc26f513e91dd7dac1a35bf7ae666db695dada`  
		Last Modified: Thu, 21 Mar 2024 00:49:17 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38777d0d105d363fb11142f959ce427812b71cf690b65668478bd56c44da4f25`  
		Last Modified: Thu, 21 Mar 2024 00:49:19 GMT  
		Size: 52.7 MB (52718446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8854647d41ed86e66a1d8ce3da7bf2055d34b12897ed6f1ce2bfa353229a538`  
		Last Modified: Thu, 21 Mar 2024 00:49:18 GMT  
		Size: 1.5 KB (1507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b36bc9f33b95952d00b483664a35441d684065126970759be12cf509dd990c`  
		Last Modified: Thu, 21 Mar 2024 00:49:19 GMT  
		Size: 3.2 KB (3249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:82729cb7de9a554c56cc009cf4b39574745b8d4ff5df7894dfcd2e0631757952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **878.2 KB (878240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4f4f92fb7c422277c4f10267c77a40cdb42ba2533f3c9cea7dbc3d7106d41f`

```dockerfile
```

-	Layers:
	-	`sha256:885d4abdbd0e7db664da3540ac668b8640138ba4fc0660b1d80213accc1fc11c`  
		Last Modified: Thu, 21 Mar 2024 00:49:17 GMT  
		Size: 841.8 KB (841763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea1e97ea9052730a6e4d4b279d2f934f19012fd58aee48dec05b2369092ca08e`  
		Last Modified: Thu, 21 Mar 2024 00:49:16 GMT  
		Size: 36.5 KB (36477 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0036002d7421b2bd84f75a92ecad945f64196473796930ba640df45bb3095444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119130506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2f107776dc2380a3b617a2dc9637e3fb9940dfda8284c6fa9064a5caf512a0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 21:16:36 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DOCKER_VERSION=26.0.0
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-x86_64'; 			sha256='53641b8a28419f947bc58c085e0c39b97a209b6e875a25c585e7fab44ff48576'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv6'; 			sha256='a123b79b530a65c7381ca8bb3b29cde7177f4f260984a127d998c9696cae794c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv7'; 			sha256='8ea72e93e8da8259d7d5d051f3c65dc14c44a23d5ebc6939394d7d03b147e238'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-aarch64'; 			sha256='b9f303c9f9db75ecf18ea6fc516b3dc54a3e54f3b3d8e7f1a449416522958bc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-ppc64le'; 			sha256='dc067ab61239cef3d2e145d37fcd68c1fc2320c6728d77a9a4ec4fb0e6c6dd64'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-riscv64'; 			sha256='a17f07604fa74c661e62d5e27ae358f8a611f42bb9a4a147cec76b8bb591bea4'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-s390x'; 			sha256='9e613275e5fa46cb864d3f2fccb10e3239b879527d075490b03e381df56c397c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 20 Mar 2024 21:16:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 21:16:36 GMT
CMD ["sh"]
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
VOLUME [/var/lib/docker]
# Wed, 20 Mar 2024 21:16:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 20 Mar 2024 21:16:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 20 Mar 2024 21:16:36 GMT
CMD []
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b275a3377f65492f727dc46aa2b70be6ec8ff96583fcd9a7b699692b5170bc`  
		Last Modified: Sat, 16 Mar 2024 04:06:09 GMT  
		Size: 2.0 MB (2019704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c53acdebd8fb391eae546ed72149f049f8ab4d594f12c74c49be04cc3b9708`  
		Last Modified: Sat, 16 Mar 2024 04:06:08 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11eaffe3eb71643155936daeaa1598d665bd3ce7e4cd7ce7540eda599ce5e7fe`  
		Last Modified: Thu, 21 Mar 2024 00:17:46 GMT  
		Size: 16.0 MB (15983712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee06d9bd87570975d69f1b498d43c5d73ee2272dc95ec1a0ef1cf417a2b4e81`  
		Last Modified: Thu, 21 Mar 2024 00:17:45 GMT  
		Size: 16.3 MB (16349527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1191475ba843b6a7b58a34750c8fc5c83a35c5f212896c2e4d6b77ecbefb6423`  
		Last Modified: Thu, 21 Mar 2024 00:17:45 GMT  
		Size: 16.6 MB (16646385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c88be67c0117bd503d23f28ad5b45b25ecfb7628f837ae5113c17215f2937b0`  
		Last Modified: Thu, 21 Mar 2024 00:17:44 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278db795eefd693016f140e271573617967766e9f1704547b9cf05c70c0371f1`  
		Last Modified: Thu, 21 Mar 2024 00:17:45 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bfdf52f00c8fa42ad500f264ea4a47b356994afc3541680b9b1253fb5beb5a`  
		Last Modified: Thu, 21 Mar 2024 00:17:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8997fd33190b834e020b09bb7d44884c36cf233282c93f086ec4010aa04ec88`  
		Last Modified: Thu, 21 Mar 2024 00:56:17 GMT  
		Size: 12.6 MB (12626677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c50c3777946e92c19ce357fca8ed4dd5e90da5fe72c40c864a896c41a269b3`  
		Last Modified: Thu, 21 Mar 2024 00:56:17 GMT  
		Size: 98.4 KB (98382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2adc59ed1e5f99ce02c632963166b495636fa93b73b262ee28d342ff09114e`  
		Last Modified: Thu, 21 Mar 2024 00:56:16 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32afe2a18f42403b60b5d6b42f939242c06b3f260e1e097f90dee6bd96f38aa`  
		Last Modified: Thu, 21 Mar 2024 00:56:19 GMT  
		Size: 52.1 MB (52050082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14cfebf1168baa896bed38483638f97cf38b0f6b71b9afb196a49580a782efd`  
		Last Modified: Thu, 21 Mar 2024 00:56:17 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff185d1d549d254f0134cf7d78dca08cac3c91d79272c017fb7a4de024336a4d`  
		Last Modified: Thu, 21 Mar 2024 00:56:18 GMT  
		Size: 3.3 KB (3251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:e77bca04cc53877a5e79ea6ab040c13d3e42aa92c87f30e984222d19f43cc019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.0 KB (875987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec5226bebb206917b7823f52c02cf4694854d3c6cc4c0eee7dad8e04abf12df`

```dockerfile
```

-	Layers:
	-	`sha256:418ca2d282047f0c8ec03652d6ab2258fa5fc336307266cc81d1ce3451f00015`  
		Last Modified: Thu, 21 Mar 2024 00:56:16 GMT  
		Size: 839.7 KB (839658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edd8ce2f2d89b379aed2a2c3ee2a8762151071b0ab55592271962734e562fdf2`  
		Last Modified: Thu, 21 Mar 2024 00:56:16 GMT  
		Size: 36.3 KB (36329 bytes)  
		MIME: application/vnd.in-toto+json
