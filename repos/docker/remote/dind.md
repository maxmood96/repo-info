## `docker:dind`

```console
$ docker pull docker@sha256:2632da0d24924b179adf1c2e6f4ea6fb866747e84baea6b2ffaa8bff982ce102
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
$ docker pull docker@sha256:4e52dcbcf86f5222648bc411cb32287f7b8480c97558eab0fee7b8b5a9376ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132453445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1d12601bcc26aa495bdd31656cc1dcd1af1aed441274bb9caaefd35bb72b15`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_VERSION=27.0.3
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 01 Jul 2024 11:04:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
CMD ["sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
VOLUME [/var/lib/docker]
# Mon, 01 Jul 2024 11:04:46 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 01 Jul 2024 11:04:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
CMD []
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea18b09b0fcf30f41de316e4be4630fa0085dd94362b76aaae0c35827240fe63`  
		Last Modified: Wed, 03 Jul 2024 18:59:08 GMT  
		Size: 7.9 MB (7870364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c587ddc277589bb9c72eeb5fbbcf6860bd0465893f589c4c3e0a4b6134f170f9`  
		Last Modified: Wed, 03 Jul 2024 18:59:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b725fb2fbdc90fe93a63ef892f3d1b10bbed51d4791123b7f52765d01026bfff`  
		Last Modified: Wed, 03 Jul 2024 18:59:08 GMT  
		Size: 18.1 MB (18069816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd7f4f004af27720761919213789283fca9b94ec840fac6dc63771b863dc209`  
		Last Modified: Wed, 03 Jul 2024 18:59:08 GMT  
		Size: 18.2 MB (18178863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51f2aba2b6c7d97d70869735f836b2fbbd83375594cef8bdb99340d4fcc1368`  
		Last Modified: Wed, 03 Jul 2024 18:59:09 GMT  
		Size: 18.8 MB (18792449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e3db14824ad6370d69d2b0a3734a1320fbc7748d59560e01317cd4fc7f9898`  
		Last Modified: Wed, 03 Jul 2024 18:59:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f815063ff6c589428018dd82119692cad98408cccf8120ba6a901c9af6947308`  
		Last Modified: Wed, 03 Jul 2024 18:59:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad1a5a3e7f7e049ed56c2463db4a985f16cf9b868247be666062a9bce642601`  
		Last Modified: Wed, 03 Jul 2024 18:59:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01555ddc68a34e209d1fbf6f1960ff9fdc1d26ebdecad01938edd3cd4f306b2d`  
		Last Modified: Wed, 03 Jul 2024 19:52:22 GMT  
		Size: 9.1 MB (9064451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd2768edf585b867d9b95e1c72a608d1299d561bdc7b063ae0f1e37d8c85254`  
		Last Modified: Wed, 03 Jul 2024 19:52:22 GMT  
		Size: 89.2 KB (89198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8d9adefda6fe53a3040c45d72166b4083cca367c95b61354f991d5b3b1bfc6`  
		Last Modified: Wed, 03 Jul 2024 19:52:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50053650ae9f64717a4d1403e29466f3f906fdb116e7892490fc3ad18244b34b`  
		Last Modified: Wed, 03 Jul 2024 19:52:23 GMT  
		Size: 56.8 MB (56756513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74df8d071d8ebc1116d5337ef637d62415950d42968813491a2d729b12073b1`  
		Last Modified: Wed, 03 Jul 2024 19:52:23 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c7ab8838b2afd334460c3dbe2690afcf765c4cf8446ee349e802cd8f74fb09`  
		Last Modified: Wed, 03 Jul 2024 19:52:23 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:046c962e9619ad472fac0b732935e5e64219c9db34350b6d0cbd51ace45f5559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d721c4317555f8d7692509953b6dac6cc4b68e3b4a544992102b0d95e8eb1c2`

```dockerfile
```

-	Layers:
	-	`sha256:928a3c3864a05b47df7750261490338856de1dfa520c88671dce8ffc94d8b2ec`  
		Last Modified: Wed, 03 Jul 2024 19:52:22 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:78bd4c0e5e46241d5bd2701dda820a06d96b6052818011722e1af5385329fd8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124486258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1ca5c57909eb3a75bae382d81b50c40a1058b060a07b83fe36d6b13c6fe3e8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_VERSION=27.0.3
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 01 Jul 2024 11:04:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
CMD ["sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
VOLUME [/var/lib/docker]
# Mon, 01 Jul 2024 11:04:46 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 01 Jul 2024 11:04:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
CMD []
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfeb2003b64a3510951cdee1b23367446ef14e267b9b7ca4781a09809f69215`  
		Last Modified: Wed, 03 Jul 2024 18:59:06 GMT  
		Size: 7.8 MB (7801046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409a05758aa32aec5f4e80ec82e4afc5cb6b200a6f65ff4aebaa5a75f6907a20`  
		Last Modified: Wed, 03 Jul 2024 18:59:05 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f3afc9302b4993803b1b0f592eaa8758c46f6f8457274a5fb7d6ca800f2526`  
		Last Modified: Wed, 03 Jul 2024 18:59:06 GMT  
		Size: 16.3 MB (16345552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c44e401e67e43cfca9dd5ef13617faea2d182c090dc047848df380b742476b5`  
		Last Modified: Wed, 03 Jul 2024 18:59:06 GMT  
		Size: 17.0 MB (17010829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32940c50a2a1686a1283a8e89b2542d0e11f641abb2fec974d485a67e361a773`  
		Last Modified: Wed, 03 Jul 2024 18:59:07 GMT  
		Size: 17.8 MB (17751827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3c852aa7ad688303a6cf8934c4dc02c778b82832f7531607fae534e1ee2da9`  
		Last Modified: Wed, 03 Jul 2024 18:59:07 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371fcd5c00ebd6ad222e0aa4ec88a71fe4fce3c8d8126cdf82a7c3d72c721c98`  
		Last Modified: Wed, 03 Jul 2024 18:59:07 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648c440ef60ffeb9b920da024079144062e96f5f7826d6570e04dd07bc067b50`  
		Last Modified: Wed, 03 Jul 2024 18:59:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d272e10308a48872b8fb898bec08f66331a8ecd86853ab3376a2b6409b558e5`  
		Last Modified: Wed, 03 Jul 2024 19:52:16 GMT  
		Size: 9.1 MB (9058457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007fc1f8f0cef0006ee4271b4016d9489614d1138c0fb286d52d291ee394a908`  
		Last Modified: Wed, 03 Jul 2024 19:52:15 GMT  
		Size: 88.4 KB (88401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f806a53c39d71f4b379f191a14f5e819d4a4417c620181f22d8ba8306df5ff43`  
		Last Modified: Wed, 03 Jul 2024 19:52:15 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca84bdbe83a62a252aa5725425f3a5218413b155d8f6019851134a87ff889b`  
		Last Modified: Wed, 03 Jul 2024 19:52:17 GMT  
		Size: 53.1 MB (53055046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4a08d3fc0712fbc8c9a458d08b116ac02ed6c2f5efbcef60963d55979e0f12`  
		Last Modified: Wed, 03 Jul 2024 19:52:16 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5522749d6b5fea2f4512f2ba60a26e139b97ed159ae6889d06b2d0d68031a0a`  
		Last Modified: Wed, 03 Jul 2024 19:52:16 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:950a30fdfb7309110d0a5c116cd1ecf67fa0a81f9798433ce7bd273dbcd4c646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b3df384eb1b9747d965eea95fe3435fe2275d854f6b4f718d860f3d6c9e47b`

```dockerfile
```

-	Layers:
	-	`sha256:2a9a617743200734214eac70e8195801932d101e47c01dcdde5ccb712f7479d5`  
		Last Modified: Wed, 03 Jul 2024 19:52:14 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:854b2a7a0bcc1993b71822e777081b150063fd6b9492dd4de825f121be2130d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122686721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e3d3cb183e295ecf1a749d5cf0951ca287ebd70102f40c8f797ac3075a9355`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_VERSION=27.0.3
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 01 Jul 2024 11:04:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
CMD ["sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
VOLUME [/var/lib/docker]
# Mon, 01 Jul 2024 11:04:46 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 01 Jul 2024 11:04:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
CMD []
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b684400d12517e9572d17fa04c13284bc751f64e7c32733b1e31613d957319`  
		Last Modified: Wed, 03 Jul 2024 19:58:11 GMT  
		Size: 7.1 MB (7140901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f9a281c7cb0cf11879cec30177bc3e4c694f9728dc15358742f7c4bc62b128`  
		Last Modified: Wed, 03 Jul 2024 19:58:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce0a299470b8fe53c9e6f5d12fe2f7388faaa8add55a43bedfb84e5538a641f`  
		Last Modified: Wed, 03 Jul 2024 19:58:11 GMT  
		Size: 16.3 MB (16339187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f75d8a56741b55aefd4b8be2904024e8896c2cdbf4cbb92651ad0f37717b71`  
		Last Modified: Wed, 03 Jul 2024 19:58:11 GMT  
		Size: 17.0 MB (16998013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f14e579dd8a6f22e6f25aecb26b4965dc6a1c1cf3f5e1b36b42cea86c42b8f`  
		Last Modified: Wed, 03 Jul 2024 19:58:12 GMT  
		Size: 17.7 MB (17736237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21a29ae89beda794c7dcf19b6f51cf8018ef44db3dc204903dfe636e63e9f7e`  
		Last Modified: Wed, 03 Jul 2024 19:58:12 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef639d66c3279c578c5f2d87e80893792bbb8523fe5cddc6ee2a091b666a15b`  
		Last Modified: Wed, 03 Jul 2024 19:58:12 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ef5239f2509905e394927770ccd4e119a7c38abe5d76d82ba5956e7d3c065f`  
		Last Modified: Wed, 03 Jul 2024 19:58:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e862a0979cbe05cf6dde495b8b4c651959e59c5f26ed1fd736f694ebe6040e`  
		Last Modified: Wed, 03 Jul 2024 20:57:34 GMT  
		Size: 8.2 MB (8230016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31efa949bd81879bbb740c7ab1cdae1b14fb666d338d508831ee112bd70ef909`  
		Last Modified: Wed, 03 Jul 2024 20:57:34 GMT  
		Size: 84.5 KB (84480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b6de791bb52ef533e66f7757a6a8035f83b49055acb089a55923a12fc0970d`  
		Last Modified: Wed, 03 Jul 2024 20:57:34 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0978ce7a7b7eb69d01179dc016e8d3db9cc1049da7aed59fe5bc5d8059c720c9`  
		Last Modified: Wed, 03 Jul 2024 20:57:36 GMT  
		Size: 53.1 MB (53055089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2addc2cf4b71081084be3395f2bc8fbed18770a71a17fb7219cbe5b1ba59fc`  
		Last Modified: Wed, 03 Jul 2024 20:57:35 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164f3180c306625ff60a4e7a26f09b498f576677b90a9ba539f6c5cee357da3d`  
		Last Modified: Wed, 03 Jul 2024 20:57:35 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:42174c2e33f60bbd34480ebdc0ece30c11bdfde13b1f2aa5cc419401cb0104ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59d0d24ec8f8c4b9e4ce31c8b061bd497bd0decacc3328ba359927d5871edc1`

```dockerfile
```

-	Layers:
	-	`sha256:40a529cc1e08bf4e2e238bcdc030d9b1f8d376d32091eb5a2fa99979b7ec6112`  
		Last Modified: Wed, 03 Jul 2024 20:57:33 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1d606fff4d93fce3855b05e4c2cedec10459ab7f699b098c274eda0c342d799a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125122230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c2b15344948c629a0721d737cffa789f87d7241996001ffd9b3678542d74a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_VERSION=27.0.3
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 01 Jul 2024 11:04:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
CMD ["sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
VOLUME [/var/lib/docker]
# Mon, 01 Jul 2024 11:04:46 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 01 Jul 2024 11:04:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
CMD []
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d0a0e3728c638822326d4bd5741e292d7e5ff128e1ca81be05bf3dd691c8ed`  
		Last Modified: Wed, 03 Jul 2024 19:22:52 GMT  
		Size: 8.0 MB (7976917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4644cf50cadd0e57adc9327b67f3ff25a810337384ce8eda69b6fd36e3b76e`  
		Last Modified: Wed, 03 Jul 2024 19:22:51 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8d8c1a1efde10d9dcf86ff6c7668c5cf4a06e301df832937824f473c0277b1`  
		Last Modified: Wed, 03 Jul 2024 19:22:52 GMT  
		Size: 17.0 MB (17028613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab207bffba8887154ad82826c5f66b1c63c186b75561b1d7bd160dd97eb57cdf`  
		Last Modified: Wed, 03 Jul 2024 19:22:52 GMT  
		Size: 16.5 MB (16538043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e63d18d586c1d5c41def684ba0b50f47483aa044eb408710beea6b177bcbbd5`  
		Last Modified: Wed, 03 Jul 2024 19:22:53 GMT  
		Size: 17.2 MB (17151904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d71d5104b3b8710c683e69f394d30820ef8eee4fb63895116e3c3569cc6245`  
		Last Modified: Wed, 03 Jul 2024 19:22:53 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debf694d3effa8c3910673e0202a28f9bd04ce22846c12863c3026ad9999352e`  
		Last Modified: Wed, 03 Jul 2024 19:22:53 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5ce67d342e7c6ef4606557c466c2e83b5cc9f08d6cdf9c6ee86f6fb51b2d22`  
		Last Modified: Wed, 03 Jul 2024 19:22:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103ce7f4925a1f86aa7a92595ee0e5d1f9e94e98b8d1a3ce1f0200d2ba1f3cfc`  
		Last Modified: Wed, 03 Jul 2024 19:52:13 GMT  
		Size: 9.9 MB (9855366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a708e0df79b27699920446715658e3b2d22085f7bc056c09db0a20f5d25febe1`  
		Last Modified: Wed, 03 Jul 2024 19:52:12 GMT  
		Size: 98.6 KB (98629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f58e0f3b7c2d7a3fb673fef8aa418936bd8f99418908e8f5684b6b94546fe0`  
		Last Modified: Wed, 03 Jul 2024 19:52:12 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca140d0302d8d16c584aa311aeee797de75f504ffc412eab3406452a370f078`  
		Last Modified: Wed, 03 Jul 2024 19:52:14 GMT  
		Size: 52.4 MB (52376023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af57c928a61466cdfbd54cafcc7cd743db0501547b284b81e1d2f523658ee55d`  
		Last Modified: Wed, 03 Jul 2024 19:52:13 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a37e6259b006c4281c286ea627573f576b71b448e00c2e4a11722625c6f6ec`  
		Last Modified: Wed, 03 Jul 2024 19:52:13 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:ea0c6ca48f3d8224a78d6143e04c0922d5817faf7d82ffacee1947d489ff2306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae22381be85f419c76e8f0d15c68e3c887c16eda3416cb202db3cc05250cd4c`

```dockerfile
```

-	Layers:
	-	`sha256:dc65f3311712688d38667a09189a718672db3d5eef87451fd9a6aaa5f1023ab8`  
		Last Modified: Wed, 03 Jul 2024 19:52:12 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json
