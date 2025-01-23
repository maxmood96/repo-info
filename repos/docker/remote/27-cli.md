## `docker:27-cli`

```console
$ docker pull docker@sha256:1d07d717b4bce04c3446175b3d4bd6c7c16567fd8f061e992ad6c28f2d49054e
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
$ docker pull docker@sha256:e1b7fa9b2d15b445084ecae08fb67d249c7748725a8731e0ef2d5fb5c54dba9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70091097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383208bbb6b0c1a0e235f583f3c8b7f80529e4ba7b91ff4952e988a75e57437b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4543eb003ef94a05439cb5446e2fe5d1a1318a77a5ecd0f7ce0f77bfde1f61`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 8.1 MB (8060130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9b66b6f01517380357ef07c7409f00407748f8e744c0eb5ed5efe498c2e5bb`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df855c4e32dd197ba449da2be8641932cbc5879636990104ef951c56eaf1b82`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 18.8 MB (18848905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b6742bd2d5a6242c709b92cf93f22139461e1ff302a6f601fd1cabf1af7580`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 20.2 MB (20234555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9af9ba02f40bd06616eacbd5670ba2485bd87a92b4c972cf5bf1120ff27aa1b`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 19.3 MB (19303637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1193bea83fc8c129bcfd73718e8e96feb49527eb743470a8f08e0ccc8a9ec2b3`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcae3e6f1bf5bb5465e3db71bb733f3cacc996333fbee14a57bef4eb56ce912`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3046ca50013a72571a456c1a5437df9fe09fe9be0f35107d9a6a20518449da42`  
		Last Modified: Thu, 23 Jan 2025 01:27:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:13bf5de648cb5dcec33c01c66cc8cc55752b09fd237dce16215654738d142689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07d5481f565c713cf6c1f3c29a788fe00c89b8ec831200bf121baa5ffc40bde`

```dockerfile
```

-	Layers:
	-	`sha256:d631712da516c7c8bd3f89066d3f8f96905f5d19845d63d390476765e524e735`  
		Last Modified: Thu, 23 Jan 2025 01:27:44 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:67daf59d1ebdf055fc86f315690f99720fe2e76c422f47c3f15cbd59798a7781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65161798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8395e26813af8fba5ddfef47bb16e82d996373cb799de4b15c2204ffe8725ca3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 23 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ad6872f504f55fd5dfe94a791ed8ab685db4ba2dd3480eb2ad66b1bb83da0b`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 8.0 MB (7972910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5ebb3ae482a680f38002a6478f8abc7edcd1bf788e37724c95efe3e0a74f1d`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed4e5240126a237686beb0364732ea8fb90b8222bb79ece3b01bc65f11255f8`  
		Last Modified: Thu, 23 Jan 2025 01:08:51 GMT  
		Size: 16.9 MB (16866758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc64aa21acc52ff9715cac0a1c9950afe80cf8a4ea1a68baec921a635cb58a9b`  
		Last Modified: Thu, 23 Jan 2025 01:28:10 GMT  
		Size: 18.8 MB (18843713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ac9ccf0752d89cd64424f0e836d6a53bcf608d2ade5c57f9e268310298d7c8`  
		Last Modified: Thu, 23 Jan 2025 01:28:10 GMT  
		Size: 18.1 MB (18112376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee11d500ae760463d5de6d7e1832499db3e5428c8aa304592b37e53e49d17d5`  
		Last Modified: Thu, 23 Jan 2025 01:28:09 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e7eeefb54f6e84b1a476d04890600e732afcfbb674962f1d0af1f84c3b20f8`  
		Last Modified: Thu, 23 Jan 2025 01:28:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089baa8d0b7e233427ebf7a6ec651326f37ce677522489b2445fa3a8ddf54820`  
		Last Modified: Thu, 23 Jan 2025 01:28:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:5b461226ce2d9537eecdcd27c8103b253c6453c497ac8b2c67e62f43b19e4651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769dd3e9bae0849e1af06e8b2ed0bb521e30956eb80ad18e01d1fbd4072b8976`

```dockerfile
```

-	Layers:
	-	`sha256:0a463fb4d15db5c2a23b7371f79cc40b855f69ffe02bd964e646b412a881d150`  
		Last Modified: Thu, 23 Jan 2025 01:28:08 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:0091be5184eae4250fc1cb11a01fe5ea066d1b7a846c67a6d23e817d010260a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64176388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7773e8edbbc039cd622aa68e12968928793e28dc0fd375c732981a7e42162a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 00:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 21 Jan 2025 00:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 00:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429d04febd7f7d8a507ee9f0b3e686f63959da9eba7f9c44aacc0c4760e6b8eb`  
		Last Modified: Wed, 08 Jan 2025 18:35:55 GMT  
		Size: 7.3 MB (7293917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da18b0856209e09ddb1746d60b57bafc68fcbeaa264f0dfab0a99340b19e366`  
		Last Modified: Wed, 08 Jan 2025 18:35:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5996ab38076f0774003f44724032451fe6ca5dabac501d8d7c3c5fa97e0af314`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 16.9 MB (16855885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae33248751ec9a79f58a4b5b036cbf06d54ce37e0337b057fe5feb29d5576c54`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.8 MB (18827879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe30b6cc54a36bcb0b47969de63a47bee866698b3335e056bea81d1f547300f`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.1 MB (18099434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb99b6ce2a5d6c24986aa65b46e2672a77c8786cd542e0f1cc0967e176b9730`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470915df3823069dd34a72bb0ab32165b071326af067df85e9a6e1e4f27915e5`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5fee2110e481e5f9251d6258c88fe9cfe286d091a0bcfe656ffabe01cc0920`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d503a1f6ea902951cfe37f5418137ffcd9c643beb7df1964bd2e45c83ef6f07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d161766fb8c4a9cb705ff2b79fe8c2fc98c84779426e81316089633605422d`

```dockerfile
```

-	Layers:
	-	`sha256:79bd3d5210a7b1bf892a818f3142ff8a95fb47d2845f0667fb2b28d4ed3d1b6b`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a6f1a1a24027716e44d9b7a08b7252bf33c60403dd92c77bf863d625a15bf302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65972403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e581c2c02c852d766afb66b604dbd45f44c1bdd42eb5cb2c127663c9e3954b41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec20a21d400e81f258665c9fa5849d2c7ba24b4de03a742e8538c1bef7e27a91`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 8.1 MB (8074433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096e83f3bf8d9c9663050fffbf6001a4b4c64063767caf6034435482946e868`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81d88fa93e9698f02174fedda46b7e4d4a7848fb4becc244b4d1a555dd8310`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.8 MB (17794934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb6a03fdaacc664f430ce86287a4271bee03d19bb128b8a7213b99a6f96f481`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 18.5 MB (18458801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f7858947f86175049e46b646baae6b31030133aab3b8edff362fb088fc4f8e`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.6 MB (17649724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d26eff37b83930827b77743baadb558085a649ead199f07714b954eb0dd51`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1de09753b3d0b8f79e3432cdce068dffbda225f2e81c2957533f3327035213`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73304a9727a8fc131f990495c4cab698bb7ec30ea44994cde426b7ae97f6e36d`  
		Last Modified: Wed, 22 Jan 2025 21:05:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d47d71a04452163577e439ccf4d91457ac4ab2f7fa68cc32517b973eae562185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bbc8c969ef865647e5cf02166f155e554bf917314e431725c57c35399e34f1`

```dockerfile
```

-	Layers:
	-	`sha256:15793555fc85eacaeec2b45b37d648b58e45b2ba5fcb0e42884c619c7eb12885`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json
