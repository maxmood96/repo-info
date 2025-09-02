## `docker:28-rc-dind-rootless`

```console
$ docker pull docker@sha256:96d43cea3a433395bfc191d14f0704f7c6354df6d22ab0ba2315ebc4be2f2d96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:13973c14639e67170e80d53cdffec3a0aa2abf91af7f44123fcd4d62489bf13a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169357295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd553a4acc618c05e5817a34d4797f514677ab803c021a877b0a99a712e2a301`
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
# Mon, 01 Sep 2025 11:04:21 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.4.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.4.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 01 Sep 2025 11:04:21 GMT
USER rootless
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
	-	`sha256:598348789e371084e8c46f82138bc89698f0712480349293d93f5a1cd3599762`  
		Last Modified: Mon, 01 Sep 2025 22:44:45 GMT  
		Size: 3.4 MB (3398450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c937c46c6f50a41d452b921ef4ce5efc2ff828973a6d81dc575ae2d7ac623f6d`  
		Last Modified: Mon, 01 Sep 2025 22:44:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56e6c4a399bc2d1a87c3a4443257cfff243733405ad873f2e5d245c1e0efb9a`  
		Last Modified: Mon, 01 Sep 2025 22:44:46 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93d37687730c10898820bcb4bfe550f2dbfd7006ac004c9d6113a6176c7d62d`  
		Last Modified: Mon, 01 Sep 2025 22:44:49 GMT  
		Size: 17.6 MB (17590873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3286a952c9bd5d007088c64ec1164e0d296af7df8cdc750f5e21d625d771489f`  
		Last Modified: Mon, 01 Sep 2025 22:44:46 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:8e955db42109aa138151c93a47f5473b40d2a3d1b0ccabc0a8d00da4bcea3604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e11c427458f81916f4b9eda4290f9eb4a6176efff0627a0ac2b18d9db4fba1`

```dockerfile
```

-	Layers:
	-	`sha256:ab469fca0599d8c76746ffe74e5d0dbfa9a74d43030c7903f014b3154f497d9a`  
		Last Modified: Mon, 01 Sep 2025 23:08:33 GMT  
		Size: 30.4 KB (30389 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:53b32e65442e9438729172ce45d1bf35520de99bc6fb2cea1c28c1e76a3ac654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160730601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ecb90d9da802801b689ac7a6e10fa12ad44254001e21667cdff2026e8aba78`
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
# Mon, 01 Sep 2025 11:04:21 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.4.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.4.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 01 Sep 2025 11:04:21 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 01 Sep 2025 11:04:21 GMT
USER rootless
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
	-	`sha256:44f8e9fdcf21b44512c047ec6ab8e5326931683789d4b56a3ef6c1f5892782ac`  
		Last Modified: Mon, 01 Sep 2025 23:14:18 GMT  
		Size: 3.4 MB (3389994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b4c0ba315588322f8e69bd599aee56048a4437d78c81917c4dc4032d43b427`  
		Last Modified: Mon, 01 Sep 2025 23:14:18 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dafaa0cd3337e5de47a2950da799af854fc7225d67bb744e11ec28c6fbc3fa0`  
		Last Modified: Mon, 01 Sep 2025 23:14:18 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460678a6b10e2a7b43e1556ebec88149ed9bdf007d5ec758bfeb34a62d99e4c3`  
		Last Modified: Mon, 01 Sep 2025 23:14:19 GMT  
		Size: 18.0 MB (18019232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542c5d03d935faeaab43e137e5c10cb8617c18b93ed7a86eb9d30f7f72c031f0`  
		Last Modified: Mon, 01 Sep 2025 23:14:18 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:e229d634fc00a69e56d6ad9b67056a736975c1642dd2762f768797d4035f936d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc4555789f28946ae0a0b1e84983cf0750532bc7b4e91cc74dabbb97867f8c0`

```dockerfile
```

-	Layers:
	-	`sha256:a61417460528c2f3282e77fba6aee2ed47dd1ffcb4135fd0ff05664a6c80dc45`  
		Last Modified: Tue, 02 Sep 2025 02:07:42 GMT  
		Size: 30.5 KB (30547 bytes)  
		MIME: application/vnd.in-toto+json
