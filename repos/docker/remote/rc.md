## `docker:rc`

```console
$ docker pull docker@sha256:5dfc7babf28d58f917a770c16f58fa350273c5f2b6f20eedf74f19955d55c6d7
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

### `docker:rc` - linux; amd64

```console
$ docker pull docker@sha256:3975fd750b8d248d9d6fa735b04ec9d1a7ca782b87d09e996b4c664dde8051d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148366634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24fd0ee44d4913afe18a9e39f204d1591485e5299de2d37141a70696489f7d6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENV DOCKER_VERSION=28.4.0-rc.1
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.4.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.4.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.4.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.4.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.27.0
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-amd64'; 			sha256='4f5e5a1b6dd0d6ff8476c8def7602d1eeedcb6f602e8dcd45079d352247eba06'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm-v6'; 			sha256='216ef84b075c270ab2f0bbcf9fcedfb0175226349714a129b7806b4b3f1a460c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm-v7'; 			sha256='b7184384910ed1b3726f7dc340e3c644640fc5f7028c6ccdfda843cfbcb3fb67'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm64'; 			sha256='e3519d085710d2502c673380f763596ae0b378d0ae8976ccbb14adaed82327ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-ppc64le'; 			sha256='e2bc5c418f680fa7ddb8782eea00a56725189ef672019db62b9f526d120afb08'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-riscv64'; 			sha256='e4f3b40472e3784bf5254eb399aa640205f349ee7c4839db989313d91258b7c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-s390x'; 			sha256='75c24bc03e809ead2e80840280359e3327965c6c1535d0fdc8d48cc86355eecb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 01 Sep 2025 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Sep 2025 11:04:21 GMT
CMD ["sh"]
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.4.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.4.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.4.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.4.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
VOLUME [/var/lib/docker]
# Mon, 01 Sep 2025 11:04:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 01 Sep 2025 11:04:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 01 Sep 2025 11:04:21 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855bb8122650b79f874085b2b9923ac9ab77877c2298ebdf6f524a027ac0e258`  
		Last Modified: Mon, 01 Sep 2025 22:34:37 GMT  
		Size: 8.2 MB (8198112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59966ccf38d532e7ce7ba37f1f365ec883b74e67545152d415e7401973c98833`  
		Last Modified: Mon, 01 Sep 2025 22:34:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdb41d2807ea42b91501cffd1e69ca2ced92c7513f113394bfcfdcc424f9d5b`  
		Last Modified: Mon, 01 Sep 2025 22:34:40 GMT  
		Size: 20.4 MB (20431049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2480be39e61e22a4250846d84a5631bccbbb4ed503f4aa64417865aa8f726671`  
		Last Modified: Mon, 01 Sep 2025 22:34:38 GMT  
		Size: 22.1 MB (22110959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642cc705d619123eefb9a1ef6285c889bc4604fa95e8be4bded92fa316bc3da3`  
		Last Modified: Mon, 01 Sep 2025 22:34:38 GMT  
		Size: 21.5 MB (21458858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30cd981ff5737f590dbbfd1e8ab635291601a96beb16e2ae0570787b905212c`  
		Last Modified: Mon, 01 Sep 2025 22:34:36 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a13e66bc894e08f3fde0f01071ca9b6986a4d19e71f69bc8c892a61cf0b212`  
		Last Modified: Mon, 01 Sep 2025 22:34:36 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a47483df9276bd5299203430462111cfca7ed7ecdeb71b178e766001d43a7cd`  
		Last Modified: Mon, 01 Sep 2025 22:34:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585e027fb85fc38f426e542cf7ee34c233b19b95b7ecfec6b5d13cc29f56c654`  
		Last Modified: Mon, 01 Sep 2025 22:39:41 GMT  
		Size: 9.5 MB (9502566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13673c0c70060cd25dfdfb3a50b77074f47f059b4e4a0dbd5dbf2eb6bfed2590`  
		Last Modified: Mon, 01 Sep 2025 22:39:41 GMT  
		Size: 90.2 KB (90228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327fa5c7bb80283265292b5a2a496d1c8e5e95a18e8bafa90e595e91e1227be1`  
		Last Modified: Mon, 01 Sep 2025 22:39:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fcedb0a9db9e8e7118fddf3090a2d7a2fc09089ef22d8bf02d3cd53c7d59b1`  
		Last Modified: Mon, 01 Sep 2025 22:39:47 GMT  
		Size: 62.8 MB (62767018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd040b66bb112eee07d08c2f38e4a616544de271d5a8389b8ed724362b5cc095`  
		Last Modified: Mon, 01 Sep 2025 22:39:41 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c474a8430d897b00b27a41900d0c2e1f877f21ceef9c114ce27f4b03bcee40a`  
		Last Modified: Mon, 01 Sep 2025 22:39:40 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:b356620cf4c57e7b163fd9fbc54d0bdb7c1cd1a84609b4e54dc8eeec475ceec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 KB (34115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb0cad55b9a7c6a994a0b06b433008418c75cc522e7822c034d277f27b2fdc8`

```dockerfile
```

-	Layers:
	-	`sha256:af66f69a4f42bc04691df7dd4f7a98a2ebc0177b13986cc4ce474d64b24127ca`  
		Last Modified: Mon, 01 Sep 2025 23:08:05 GMT  
		Size: 34.1 KB (34115 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc` - linux; arm variant v6

```console
$ docker pull docker@sha256:d0dc30ca58997a187ba1348ae7b398b3396050612aef403a028de6a7347db79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139049297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4cee4c391d3dfe53aadc3c14085752d849b2d4ed3e4155d91c5529dae26d73`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENV DOCKER_VERSION=28.4.0-rc.1
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.4.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.4.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.4.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.4.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.27.0
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-amd64'; 			sha256='4f5e5a1b6dd0d6ff8476c8def7602d1eeedcb6f602e8dcd45079d352247eba06'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm-v6'; 			sha256='216ef84b075c270ab2f0bbcf9fcedfb0175226349714a129b7806b4b3f1a460c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm-v7'; 			sha256='b7184384910ed1b3726f7dc340e3c644640fc5f7028c6ccdfda843cfbcb3fb67'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm64'; 			sha256='e3519d085710d2502c673380f763596ae0b378d0ae8976ccbb14adaed82327ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-ppc64le'; 			sha256='e2bc5c418f680fa7ddb8782eea00a56725189ef672019db62b9f526d120afb08'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-riscv64'; 			sha256='e4f3b40472e3784bf5254eb399aa640205f349ee7c4839db989313d91258b7c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-s390x'; 			sha256='75c24bc03e809ead2e80840280359e3327965c6c1535d0fdc8d48cc86355eecb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 01 Sep 2025 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Sep 2025 11:04:21 GMT
CMD ["sh"]
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.4.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.4.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.4.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.4.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
VOLUME [/var/lib/docker]
# Mon, 01 Sep 2025 11:04:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 01 Sep 2025 11:04:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 01 Sep 2025 11:04:21 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ce1d9c46363a71ba401cac675003f756791ab33648cc5d23a922a80975ca21`  
		Last Modified: Mon, 01 Sep 2025 22:37:48 GMT  
		Size: 18.4 MB (18422454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d7c551fc6821b1e13b8a396cd41b1b4dbdfa505cfd4e3efa03dc37ad3ecbde`  
		Last Modified: Mon, 01 Sep 2025 22:37:50 GMT  
		Size: 20.7 MB (20705295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6545ca0a02cf3bde55a07e0cdaec622cf84de056ba107a463b8038a95f1f5ba`  
		Last Modified: Mon, 01 Sep 2025 22:37:49 GMT  
		Size: 20.2 MB (20184048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955ea0ace00677c591c0404a01f7524d54132fa722de45b334f4c0bf95049ad8`  
		Last Modified: Mon, 01 Sep 2025 22:37:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64143a7ec45d312833171f5b4518669424b71893f57e8a3ca70f40b86c816d7d`  
		Last Modified: Mon, 01 Sep 2025 22:37:47 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f1efa395b58fde6bad6811c259b445b80130a9ac81c429688206be4a309d7c`  
		Last Modified: Mon, 01 Sep 2025 22:37:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64875afa05fbd77800bf64b0ca1d1750316ca3ecc0a622ba508bce3b893f8d6e`  
		Last Modified: Mon, 01 Sep 2025 22:47:10 GMT  
		Size: 9.5 MB (9461623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ca4fd39bddd80dbb47165f2964c3be56dae14a3d5adf98aafd51c14eb00b47`  
		Last Modified: Mon, 01 Sep 2025 22:47:03 GMT  
		Size: 89.8 KB (89801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58a9c2a5e2287a53a4480b915a972e36f705fa8efe4b5a6d8b12833d4a64628`  
		Last Modified: Mon, 01 Sep 2025 22:47:03 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408daf98750aee8969d91f80ce886636ca07156868f47a87c9ec2316b7477d27`  
		Last Modified: Mon, 01 Sep 2025 22:47:06 GMT  
		Size: 58.6 MB (58573324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1250bd68e09400a622753c36a54034d91b45c6533ed19a040332020b62815f`  
		Last Modified: Mon, 01 Sep 2025 22:47:03 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1063dfd7c585cb22aaa70a8c9dafb2d74ed896d45f2be06f5de9e4c5c7aedf1c`  
		Last Modified: Mon, 01 Sep 2025 22:47:03 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:a41a7d4196b6a59ded1868bae63de5249a3a8e941cd7fea27586979543f4f171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dff3eecfa1e4420015d602f762977d2baad3753c6a2bc86be18317599d4344f`

```dockerfile
```

-	Layers:
	-	`sha256:3a58d6f66f1d19c9646d4b96b1cc17e7336f823a51b2df2608b59925414878b8`  
		Last Modified: Mon, 01 Sep 2025 23:08:08 GMT  
		Size: 34.3 KB (34275 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc` - linux; arm variant v7

```console
$ docker pull docker@sha256:4cae1d1fb35d36fd38d17584f5afb812550aea43001408f938006526a0c7e4a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137009390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9ee62de2a71a2ae836d5365e4c8d103e43034bbf65fc5927092f53894ede89`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENV DOCKER_VERSION=28.4.0-rc.1
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.4.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.4.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.4.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.4.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.27.0
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-amd64'; 			sha256='4f5e5a1b6dd0d6ff8476c8def7602d1eeedcb6f602e8dcd45079d352247eba06'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm-v6'; 			sha256='216ef84b075c270ab2f0bbcf9fcedfb0175226349714a129b7806b4b3f1a460c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm-v7'; 			sha256='b7184384910ed1b3726f7dc340e3c644640fc5f7028c6ccdfda843cfbcb3fb67'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm64'; 			sha256='e3519d085710d2502c673380f763596ae0b378d0ae8976ccbb14adaed82327ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-ppc64le'; 			sha256='e2bc5c418f680fa7ddb8782eea00a56725189ef672019db62b9f526d120afb08'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-riscv64'; 			sha256='e4f3b40472e3784bf5254eb399aa640205f349ee7c4839db989313d91258b7c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-s390x'; 			sha256='75c24bc03e809ead2e80840280359e3327965c6c1535d0fdc8d48cc86355eecb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 01 Sep 2025 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Sep 2025 11:04:21 GMT
CMD ["sh"]
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.4.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.4.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.4.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.4.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
VOLUME [/var/lib/docker]
# Mon, 01 Sep 2025 11:04:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 01 Sep 2025 11:04:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 01 Sep 2025 11:04:21 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d106bca932a97020327632265244813f7f94284278622461dff3d6581b4a61df`  
		Last Modified: Mon, 01 Sep 2025 22:43:40 GMT  
		Size: 18.4 MB (18406621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8e26633acf02d7e07e2ceae119eeaa78eb1b461761906b40f058ba9c7bb5be`  
		Last Modified: Mon, 01 Sep 2025 22:43:40 GMT  
		Size: 20.7 MB (20689994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5a34bb70d8de823387be619c980ca42aca7897e5c6e23d53a1a367776a008d`  
		Last Modified: Mon, 01 Sep 2025 22:43:40 GMT  
		Size: 20.2 MB (20165954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9752380ab04b7a0fbee8ea6e078afc3a24b83a3fb1ed6ae8de3a9eee629c2ca`  
		Last Modified: Mon, 01 Sep 2025 22:43:39 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d67b14b01599974c719a82094581af91cd1bd86c39fe81cec68b92c0a5e012`  
		Last Modified: Mon, 01 Sep 2025 22:43:39 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f613ba8025d2d4509a7cdb7c2f5f24be5728f48383f4074845eb35a0d45f7fbc`  
		Last Modified: Mon, 01 Sep 2025 22:43:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9ee0639d9aa5ef2b2e1206dfaecae41f24480c1eb86dbb3049d0d2c486053a`  
		Last Modified: Mon, 01 Sep 2025 23:12:10 GMT  
		Size: 8.6 MB (8603132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924c7dc084a4f52c8f81799b7e77379748ea4e0b438af8702c1fb742523a7543`  
		Last Modified: Mon, 01 Sep 2025 23:12:09 GMT  
		Size: 86.2 KB (86242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ec5e97ba94d976f88081faa81469f84a806a8dbbca36c0641009f781ea00fc`  
		Last Modified: Mon, 01 Sep 2025 23:12:09 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b134752cb3cdefa7ab5219e4da9bd6b0386a5b844a587cc2ccfbb6b6ff7e6`  
		Last Modified: Mon, 01 Sep 2025 23:12:14 GMT  
		Size: 58.4 MB (58400282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58b8e05433d68beb1b9f9de53b79f98914f74c15707321db21d7ab97857b16f`  
		Last Modified: Mon, 01 Sep 2025 23:12:09 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0230980a1fb45fe28450f3c55d003cba293c0277db74702854b56fe26aa0180b`  
		Last Modified: Mon, 01 Sep 2025 23:12:09 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:0e0e10c638947ef2f42764e37a9f3dc954b15e2c8d8c900c551125ad13ddbc3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275a2e0a24cf50bf578f6a1fe26fae25a5cea8424746e27c4b66173d7544e881`

```dockerfile
```

-	Layers:
	-	`sha256:b3a973da1dffef345b82e40c71af603933b2910c29f55ffd9c42e34435b8188b`  
		Last Modified: Tue, 02 Sep 2025 02:07:37 GMT  
		Size: 34.3 KB (34274 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6c284115c2dc995ce1d8903c304348c0a4d49f30b3d90790e76dd0bb6e01cfe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139320034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caad63c192b64420683dc7a34baf30fdc1a362be6e451678221bb33ca355e1f5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 11:04:21 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENV DOCKER_VERSION=28.4.0-rc.1
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.4.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.4.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.4.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.4.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENV DOCKER_BUILDX_VERSION=0.27.0
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-amd64'; 			sha256='4f5e5a1b6dd0d6ff8476c8def7602d1eeedcb6f602e8dcd45079d352247eba06'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm-v6'; 			sha256='216ef84b075c270ab2f0bbcf9fcedfb0175226349714a129b7806b4b3f1a460c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm-v7'; 			sha256='b7184384910ed1b3726f7dc340e3c644640fc5f7028c6ccdfda843cfbcb3fb67'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-arm64'; 			sha256='e3519d085710d2502c673380f763596ae0b378d0ae8976ccbb14adaed82327ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-ppc64le'; 			sha256='e2bc5c418f680fa7ddb8782eea00a56725189ef672019db62b9f526d120afb08'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-riscv64'; 			sha256='e4f3b40472e3784bf5254eb399aa640205f349ee7c4839db989313d91258b7c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.linux-s390x'; 			sha256='75c24bc03e809ead2e80840280359e3327965c6c1535d0fdc8d48cc86355eecb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 01 Sep 2025 11:04:21 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Sep 2025 11:04:21 GMT
CMD ["sh"]
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.4.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.4.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.4.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.4.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
VOLUME [/var/lib/docker]
# Mon, 01 Sep 2025 11:04:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 01 Sep 2025 11:04:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 01 Sep 2025 11:04:21 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a98d9bd1c98d5bc0f4f83ecbf97795bacbd61dae146e0fc275ea201de741c02`  
		Last Modified: Mon, 01 Sep 2025 22:36:49 GMT  
		Size: 8.2 MB (8217722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cf89aa83613cd9b2aa9454fdfe2bfb97fdd57d1721c2314b4b8ca69f4f2b53`  
		Last Modified: Mon, 01 Sep 2025 22:36:48 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58be790dbd673c7daf1391c152ee73e4abd49475370a02fd2d7366344d608622`  
		Last Modified: Mon, 01 Sep 2025 22:36:51 GMT  
		Size: 19.2 MB (19235982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e7697f76ee7cc6f5a55b6770effed589314e04412422df374ad6c4548cf1bd`  
		Last Modified: Mon, 01 Sep 2025 22:36:51 GMT  
		Size: 20.2 MB (20230134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d04fe3e1afcdb03c2a9c1ebea820d39f89893b6525ad58e29c61211814b95dd`  
		Last Modified: Mon, 01 Sep 2025 22:36:51 GMT  
		Size: 19.7 MB (19677169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5006699bf52a3b7ef79865343380f20dc1381c1f25ccd46c3e03b6e7d68444`  
		Last Modified: Mon, 01 Sep 2025 22:36:50 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69794224c5f458693975917688ec4ba72459cade40db59237aa2e64e1657b41`  
		Last Modified: Mon, 01 Sep 2025 22:36:50 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940ea76d3952b37f1fec064e8f62e642abe74286d5c46525a048ab5b127525ba`  
		Last Modified: Mon, 01 Sep 2025 22:36:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28edf8f4effb94952cd8b2d641401069571ab4819f9057e691c1458b316e9341`  
		Last Modified: Mon, 01 Sep 2025 23:04:37 GMT  
		Size: 10.0 MB (10031331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7920adb874607664fc0a5e655e7aa6dc65b6e564d052e69d2486ffaf554f1ed5`  
		Last Modified: Mon, 01 Sep 2025 23:04:36 GMT  
		Size: 99.3 KB (99318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51e96a77ef4e32c3d12a3a791339772563647aa2fafd8a8721a72eb82970525`  
		Last Modified: Mon, 01 Sep 2025 23:04:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3c4a832e186136cedca819db95168711c97e72f8367a39cb1f27fc7f71a986`  
		Last Modified: Mon, 01 Sep 2025 23:04:43 GMT  
		Size: 57.7 MB (57689476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4271b802c3f7cfb54b3b9c014ea5e30d9ba7ba08d125457b531f6860fb759bcd`  
		Last Modified: Mon, 01 Sep 2025 23:04:36 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583942ed05bbd5cccfa36de3aa2e15529890ec96af9a93ed91801e46da7b1510`  
		Last Modified: Mon, 01 Sep 2025 23:04:36 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:2495b17a5fcefb33226b41ee47e452b45c06756200c1cd933a039cce8185bd94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012086b188476f40fffca1b91c5bffcfb4edb199bee572cfe62c7f821da5e928`

```dockerfile
```

-	Layers:
	-	`sha256:5f7d3ec4032da6af68ebd6d61ab24a283aaed2b1744589092a27688dceef4c6d`  
		Last Modified: Mon, 01 Sep 2025 23:08:14 GMT  
		Size: 34.3 KB (34333 bytes)  
		MIME: application/vnd.in-toto+json
