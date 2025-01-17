<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:27`](#docker27)
-	[`docker:27-cli`](#docker27-cli)
-	[`docker:27-dind`](#docker27-dind)
-	[`docker:27-dind-rootless`](#docker27-dind-rootless)
-	[`docker:27-windowsservercore`](#docker27-windowsservercore)
-	[`docker:27-windowsservercore-1809`](#docker27-windowsservercore-1809)
-	[`docker:27-windowsservercore-ltsc2022`](#docker27-windowsservercore-ltsc2022)
-	[`docker:27.5`](#docker275)
-	[`docker:27.5-cli`](#docker275-cli)
-	[`docker:27.5-dind`](#docker275-dind)
-	[`docker:27.5-dind-rootless`](#docker275-dind-rootless)
-	[`docker:27.5-windowsservercore`](#docker275-windowsservercore)
-	[`docker:27.5-windowsservercore-1809`](#docker275-windowsservercore-1809)
-	[`docker:27.5-windowsservercore-ltsc2022`](#docker275-windowsservercore-ltsc2022)
-	[`docker:27.5.0`](#docker2750)
-	[`docker:27.5.0-alpine3.21`](#docker2750-alpine321)
-	[`docker:27.5.0-cli`](#docker2750-cli)
-	[`docker:27.5.0-cli-alpine3.21`](#docker2750-cli-alpine321)
-	[`docker:27.5.0-dind`](#docker2750-dind)
-	[`docker:27.5.0-dind-alpine3.21`](#docker2750-dind-alpine321)
-	[`docker:27.5.0-dind-rootless`](#docker2750-dind-rootless)
-	[`docker:27.5.0-windowsservercore`](#docker2750-windowsservercore)
-	[`docker:27.5.0-windowsservercore-1809`](#docker2750-windowsservercore-1809)
-	[`docker:27.5.0-windowsservercore-ltsc2022`](#docker2750-windowsservercore-ltsc2022)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)

## `docker:27`

```console
$ docker pull docker@sha256:45b80efde6892498e1160c3be8eb7cc67732863caac98d2a79af24398ff1c106
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
$ docker pull docker@sha256:328fee4531eccdcfe52b61ba73c849a649cacad29fba1a4129c95b40e0f2196c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133867713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b300b8cdc5f2ac4f108ecdd418f3ea30e35b4ee1018ff818ca39dd3f0bc7aadd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db0ef5f6406167c28a55dbfc0fbbd527a8e8ee10b1ed0053a74bb5847f467b`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 8.1 MB (8060096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2617d81eedcf635e1fd94dc905266de252ae0d642c05465bb5c57e7b9e5b0`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e4c1fa9475c483015ff35cb0ca5fae973e6192bd7d355b798024cc3f6436c`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18849459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af4884fbc706fb37435cc7859f05891c18eaec536721e17e5a97361694520c3`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18798866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851762183788567546d15646f8ce06871883255ad227fb13b88d2c2e58ef7fa4`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 19.3 MB (19303643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d84c454f28e907e0f1f5996d71027092830cabefb6c3f3a8d0d9fb3b332b9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ada9115c6a1e6e261a5250211382c99910811092b2791e7b32073c01bd5817`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06335ef68f056dd7837956156616452c5087a436b0ddbbc94fcb4493390d9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e423b3161e65b5d155f4fee197bb34b95aaaf9034e25661cc942130922d5553f`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 6.7 MB (6733536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8d12927cbc5b132f3d989c2f32cf8fe0e3d4f9136fc784f675b40aa6e2caa5`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 89.4 KB (89425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326df6d9eb79ca016d6f1723d5ca2bced72bd36fd014e852b493a43a6447c10e`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa7701ffbf173fdb6f7999d28b78600828e770ef8de8c26f6767ff8d3413253`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 58.4 MB (58383027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40544ceb254c83f9677202983636becd2547551930652c6928a91b62c6b26529`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13647f78c45bebb40dba9ffe52c4bce8371d4edda349c507012fe1300ff50732`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:683d1639ff61791a2eae0ec63a422d289dc4e28394eb8e39ccf17b56e1737122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556810057e6ba7d14c45298e2761fef6923333526367bb7e64510b0649dd514e`

```dockerfile
```

-	Layers:
	-	`sha256:18fa62c94f21565d5f5d2b2d15c416dce24b5ac429609729db340cc622a08d00`  
		Last Modified: Fri, 17 Jan 2025 02:09:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v6

```console
$ docker pull docker@sha256:872158a8fc908710ac79c7d0c61287953a6593ef365f7593fbc9ee6d449ca9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124949669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bbc03711f0e14a6963ddb7043e52c2f66782fc50b0319107b2712a9107fc28`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
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
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea778430c11317962e3aa40444717aa8dc546fc65595ea9fd6e73d36310902f`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 17.4 MB (17448787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea230caf38f20e83e44f4dc9f84ff4fb52580e6d973dd8ecd2952cd36ad2a21`  
		Last Modified: Fri, 17 Jan 2025 01:27:49 GMT  
		Size: 18.1 MB (18112354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97006a84267c6bca594ceb4a5bf26d607f5bdef93912e07f6e846be4422b1c`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e59e6b008d5c5752b4a7993bd0b52b1db7dc2dfa774314f4f775cc22afa320`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89fe821a62ed4869930b04fc18ac60cf2bda17c09431466d8459ccc0c3549e2`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fe55d9784a2a762c0d6ed72664929cdf9284a3a888e3089d5e9220628c6b45`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 7.0 MB (7041413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d364c50ad8b6c6c862e3e6daa1c4cf0a6e8c8433c8a71cffd144f766f0e4fb23`  
		Last Modified: Fri, 17 Jan 2025 02:11:06 GMT  
		Size: 89.1 KB (89085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0620df6bfe0a1bc90f013a4bb494501716e787d271b7bc5969ecbc24b43756`  
		Last Modified: Fri, 17 Jan 2025 02:11:06 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bd936df8e147b648aa1a39d212c1624e064452a47059063133cd6adf29f7c7`  
		Last Modified: Fri, 17 Jan 2025 02:11:08 GMT  
		Size: 54.0 MB (54047054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966301da011cd0c70e74a358f99db4b9f43762dd18ed38f53665e9a24e880c4b`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b29247ae6bfe40191a231dba9717f4ca4bf21ec2c13c3606f0ace4b34eb7c43`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 3.3 KB (3267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:dd0a36256908be42678ad2890166b0e84a6246797662f2b93f3cd6f24ab68906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9af519ad2f15c502e5c17cfd4e3767beadd551d1851f350066b158eb41c6913`

```dockerfile
```

-	Layers:
	-	`sha256:ce130b032bac1fce394cc92324e72573e50caf69fdb9c099daad2c98bd8d9a1d`  
		Last Modified: Fri, 17 Jan 2025 02:11:05 GMT  
		Size: 34.8 KB (34764 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v7

```console
$ docker pull docker@sha256:29597558c26c7e456f9d4350b94f208a69114260adc21bdae0619f9a7749c34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64123e8eceb16c151befc29738868d17cd6b828c82a96cc2b46a182f62e48eab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
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
	-	`sha256:1d1f394b9e9ceefe286b141a6fce91d86072ca709baf5dc4447f3d5a6db9a163`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 17.4 MB (17427588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755932338966055de46ecbdb4e46288f1f52af30c0f57960411eed7bcbc876d0`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 18.1 MB (18099438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215cf40534564c9b7b71ea6e20aa6912ca15008a9c2dd68162c3efe4fc20e65b`  
		Last Modified: Fri, 17 Jan 2025 01:28:02 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb652a32cd1bd43600fe45d89a2455ab0b882887bfabe0664dc9eb749e932a1`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe784566335013d539f74a4e2e151368fe7ddd75a3583e15b1cbafc6eca14a`  
		Last Modified: Fri, 17 Jan 2025 01:28:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cd34d15034bf9fbabde6b6c4ec8bbfe56b0ee1dad07a86eef7f6d83a4829e5`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 6.4 MB (6367554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049bb15c92b4ba59ad113b753dc6305190eb3111a77ec5b86b8ca81c7dbc59f2`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 85.2 KB (85236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefdea776978b937e65e37c006d81238b97221fac666606609e7569cc915f005`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8ab79af5c8f7891f9b4d14518c40aae4efd8acb30339e416de829cf962a8ae`  
		Last Modified: Fri, 17 Jan 2025 02:25:24 GMT  
		Size: 54.0 MB (54047069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4015624859fadb74f8744fab8fe858c4a95b1d5fde6a26c00f709c761fb7908`  
		Last Modified: Fri, 17 Jan 2025 02:25:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935f17568aab4f3b97b7a27a57821ab17388667d24fa04ed2ac2b295bc4217bf`  
		Last Modified: Fri, 17 Jan 2025 02:25:23 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:8fb08780d366a366517f413dc5e7ef73a7f5209ce4924d234dfb98829cba86d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7820bc0b8d0f7ee1b9d6587b10f5355904f51e675ddd0a337e25edb87b5578`

```dockerfile
```

-	Layers:
	-	`sha256:0857811d7117af260dff536135d5b9462e12a604d988f0bbcfa5c98ac94002c1`  
		Last Modified: Fri, 17 Jan 2025 02:25:20 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:be6a2bf3869c0b2ce79cbea0de54fc0151be9915cb61572b8fee8ae231380fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125658359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98a7305162cf56e40d783f72a96aafbe29862ec4cf094baab60b961b874e8a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98031a3690358e9e338c7b900ff223767ca20fe8d3581d723971bb5d3e97df6e`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 8.1 MB (8074417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c05adf332c68788c150e330500d99375063fb5fccac4eca47664fef925fe6`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05df1af7190779d81ae1d2a2f6bab0f116cd0911eaf925ea3b7c88d84e4dca`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.8 MB (17795742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373537e5e27b254a2e83716ef135b83be0eaffa0fbb7dd7e588802f57c22952f`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.1 MB (17106465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8781806a16e281a8c480f7f429497d259f378f76366f5b8a2047861a9a0eb`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 17.6 MB (17649723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd429dc70fde0e965c93f4ea2aa21344379a0f8461e5e8fb3a260e92129bfbd7`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1709b08f9705b3f6af9978783f2fb732992ff039699fdbc0a842595dbcb3bf9`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d18f467488432eff104e17eebdd3b73776125d5155413e82a70fac1ad2d50de`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eb3998a0993954da71d972744c4ceafe57b9e96dcb75f4d7626277df3d4176`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 7.0 MB (6981841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b5a025a6a9bf0b06bba2fe135db13911e1dcf31474e69df77b00520bbd3191`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 97.8 KB (97784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0743b347437f8517c3560af97d8923ca391286f17acbe0558f46b28c8c8c4d2`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49595e55dbff2fe86a9c4da769bc6a7679b3da9c2279eed30873af6bb678e195`  
		Last Modified: Fri, 17 Jan 2025 02:28:29 GMT  
		Size: 54.0 MB (53952083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3849eac5f1cf6d7788301e473e712d6bf6d77e0e01c3829c96b4dec4acf623d8`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb83a6536a87f2c86efa17f506102254efe83bcb5e283b31a0db94d18505dde5`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:66c420a8f09f46b8c9153ce490d112d23b47a11ae227e02b316ba27641ad742e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83edc878bc62dd15adedb843a231f657257baa90509166b729e8665157592cd7`

```dockerfile
```

-	Layers:
	-	`sha256:60f641b6e35d2698c4ef8617324030bdddce902f61a5ed2f117f633f27b92da8`  
		Last Modified: Fri, 17 Jan 2025 02:28:25 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-cli`

```console
$ docker pull docker@sha256:7c10b867b5da6f0ecbac463defeaa490c1d2816cb02fe4e14d2994ad9c3812cd
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
$ docker pull docker@sha256:b219ac7db8149403917bdea481b4e8bdc9e48c492e12d6aa2b0ad8e11b323316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68655933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cc102d4a93a8704667364b5cfb93d9dcc26a6a861645223f2d4893b3ed723a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.0
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db0ef5f6406167c28a55dbfc0fbbd527a8e8ee10b1ed0053a74bb5847f467b`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 8.1 MB (8060096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2617d81eedcf635e1fd94dc905266de252ae0d642c05465bb5c57e7b9e5b0`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e4c1fa9475c483015ff35cb0ca5fae973e6192bd7d355b798024cc3f6436c`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18849459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af4884fbc706fb37435cc7859f05891c18eaec536721e17e5a97361694520c3`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18798866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851762183788567546d15646f8ce06871883255ad227fb13b88d2c2e58ef7fa4`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 19.3 MB (19303643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d84c454f28e907e0f1f5996d71027092830cabefb6c3f3a8d0d9fb3b332b9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ada9115c6a1e6e261a5250211382c99910811092b2791e7b32073c01bd5817`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06335ef68f056dd7837956156616452c5087a436b0ddbbc94fcb4493390d9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:bfcde7282475bfa1b52d54c2ccea12401ee915b605e1d578a5081bb4a69627bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8044174370b4166bc88d8f825313d5221505fa7b2ba129e316bb4e292d4a93d8`

```dockerfile
```

-	Layers:
	-	`sha256:f5e0658d18f9353954b3b81fc16fe0b3e32f0e667af202b4f413c79dce6a3b96`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:f52fb18fdfc78a4af51b84ac7d2b5fca13b8e3e09b1067aa849e9f04030c2c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63766314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74e5406e29303780211a38cb58677a0c6a96a6aa5ce396f86ae128d852cc85d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.0
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
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
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea778430c11317962e3aa40444717aa8dc546fc65595ea9fd6e73d36310902f`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 17.4 MB (17448787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea230caf38f20e83e44f4dc9f84ff4fb52580e6d973dd8ecd2952cd36ad2a21`  
		Last Modified: Fri, 17 Jan 2025 01:27:49 GMT  
		Size: 18.1 MB (18112354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97006a84267c6bca594ceb4a5bf26d607f5bdef93912e07f6e846be4422b1c`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e59e6b008d5c5752b4a7993bd0b52b1db7dc2dfa774314f4f775cc22afa320`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89fe821a62ed4869930b04fc18ac60cf2bda17c09431466d8459ccc0c3549e2`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:dce530002422cd3b77135d6ae618300706585d7d6deebc956b7425231442feeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c540c5273aba065d46aa7fa9ca86bfb8aa222597b3283936e19bbdef868628f6`

```dockerfile
```

-	Layers:
	-	`sha256:532ebdac6902ef2db952873eeeaf73c981703befe573cd7cbe0eaacd64aa031f`  
		Last Modified: Fri, 17 Jan 2025 01:27:47 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:9e993e3871a714198e4b947664c5f228a5d7982b3515670942d8a495f03485eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62776105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde14708064af6f21da2b23403c4e90218556fb6cf1508302904ef370691f99c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.0
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
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
	-	`sha256:1d1f394b9e9ceefe286b141a6fce91d86072ca709baf5dc4447f3d5a6db9a163`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 17.4 MB (17427588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755932338966055de46ecbdb4e46288f1f52af30c0f57960411eed7bcbc876d0`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 18.1 MB (18099438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215cf40534564c9b7b71ea6e20aa6912ca15008a9c2dd68162c3efe4fc20e65b`  
		Last Modified: Fri, 17 Jan 2025 01:28:02 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb652a32cd1bd43600fe45d89a2455ab0b882887bfabe0664dc9eb749e932a1`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe784566335013d539f74a4e2e151368fe7ddd75a3583e15b1cbafc6eca14a`  
		Last Modified: Fri, 17 Jan 2025 01:28:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:dfca36c13fd1337794df037f0fc30b729677e432669884ebcb2f92429c838457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4905f7d813489e8a4204010015fb7509e3c94934b1b88e1418f21f37a337a6f`

```dockerfile
```

-	Layers:
	-	`sha256:89c06eb5c6c66dfe6a2640b9ccf35cdc3ab8ca4ac9883f9fb2b69b8aba4d80e3`  
		Last Modified: Fri, 17 Jan 2025 01:28:01 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a121337c9287fdc11e04a8a12708f639e8c3ba427945f4539df65679aee3ee8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64620861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d961a7c95de71f4706af938b3c55efbe8f7379a1c212212251b71732ea4c5cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.0
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98031a3690358e9e338c7b900ff223767ca20fe8d3581d723971bb5d3e97df6e`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 8.1 MB (8074417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c05adf332c68788c150e330500d99375063fb5fccac4eca47664fef925fe6`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05df1af7190779d81ae1d2a2f6bab0f116cd0911eaf925ea3b7c88d84e4dca`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.8 MB (17795742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373537e5e27b254a2e83716ef135b83be0eaffa0fbb7dd7e588802f57c22952f`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.1 MB (17106465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8781806a16e281a8c480f7f429497d259f378f76366f5b8a2047861a9a0eb`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 17.6 MB (17649723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd429dc70fde0e965c93f4ea2aa21344379a0f8461e5e8fb3a260e92129bfbd7`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1709b08f9705b3f6af9978783f2fb732992ff039699fdbc0a842595dbcb3bf9`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d18f467488432eff104e17eebdd3b73776125d5155413e82a70fac1ad2d50de`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1d010e0b0f4fa82a5b3ba475d15bffbaf6b9481a3a2c85a608aa6f1be93f4160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a79ec7a8c697907793b7bd322196ef33a33e0ae9eb4ea0f46752d9aa591878`

```dockerfile
```

-	Layers:
	-	`sha256:1ce07430fc5561a2375bb4a6167743bb1bef6046817bf347a9a3f3373a4cfc4b`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind`

```console
$ docker pull docker@sha256:45b80efde6892498e1160c3be8eb7cc67732863caac98d2a79af24398ff1c106
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
$ docker pull docker@sha256:328fee4531eccdcfe52b61ba73c849a649cacad29fba1a4129c95b40e0f2196c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133867713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b300b8cdc5f2ac4f108ecdd418f3ea30e35b4ee1018ff818ca39dd3f0bc7aadd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db0ef5f6406167c28a55dbfc0fbbd527a8e8ee10b1ed0053a74bb5847f467b`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 8.1 MB (8060096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2617d81eedcf635e1fd94dc905266de252ae0d642c05465bb5c57e7b9e5b0`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e4c1fa9475c483015ff35cb0ca5fae973e6192bd7d355b798024cc3f6436c`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18849459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af4884fbc706fb37435cc7859f05891c18eaec536721e17e5a97361694520c3`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18798866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851762183788567546d15646f8ce06871883255ad227fb13b88d2c2e58ef7fa4`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 19.3 MB (19303643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d84c454f28e907e0f1f5996d71027092830cabefb6c3f3a8d0d9fb3b332b9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ada9115c6a1e6e261a5250211382c99910811092b2791e7b32073c01bd5817`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06335ef68f056dd7837956156616452c5087a436b0ddbbc94fcb4493390d9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e423b3161e65b5d155f4fee197bb34b95aaaf9034e25661cc942130922d5553f`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 6.7 MB (6733536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8d12927cbc5b132f3d989c2f32cf8fe0e3d4f9136fc784f675b40aa6e2caa5`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 89.4 KB (89425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326df6d9eb79ca016d6f1723d5ca2bced72bd36fd014e852b493a43a6447c10e`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa7701ffbf173fdb6f7999d28b78600828e770ef8de8c26f6767ff8d3413253`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 58.4 MB (58383027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40544ceb254c83f9677202983636becd2547551930652c6928a91b62c6b26529`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13647f78c45bebb40dba9ffe52c4bce8371d4edda349c507012fe1300ff50732`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:683d1639ff61791a2eae0ec63a422d289dc4e28394eb8e39ccf17b56e1737122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556810057e6ba7d14c45298e2761fef6923333526367bb7e64510b0649dd514e`

```dockerfile
```

-	Layers:
	-	`sha256:18fa62c94f21565d5f5d2b2d15c416dce24b5ac429609729db340cc622a08d00`  
		Last Modified: Fri, 17 Jan 2025 02:09:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:872158a8fc908710ac79c7d0c61287953a6593ef365f7593fbc9ee6d449ca9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124949669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bbc03711f0e14a6963ddb7043e52c2f66782fc50b0319107b2712a9107fc28`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
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
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea778430c11317962e3aa40444717aa8dc546fc65595ea9fd6e73d36310902f`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 17.4 MB (17448787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea230caf38f20e83e44f4dc9f84ff4fb52580e6d973dd8ecd2952cd36ad2a21`  
		Last Modified: Fri, 17 Jan 2025 01:27:49 GMT  
		Size: 18.1 MB (18112354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97006a84267c6bca594ceb4a5bf26d607f5bdef93912e07f6e846be4422b1c`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e59e6b008d5c5752b4a7993bd0b52b1db7dc2dfa774314f4f775cc22afa320`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89fe821a62ed4869930b04fc18ac60cf2bda17c09431466d8459ccc0c3549e2`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fe55d9784a2a762c0d6ed72664929cdf9284a3a888e3089d5e9220628c6b45`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 7.0 MB (7041413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d364c50ad8b6c6c862e3e6daa1c4cf0a6e8c8433c8a71cffd144f766f0e4fb23`  
		Last Modified: Fri, 17 Jan 2025 02:11:06 GMT  
		Size: 89.1 KB (89085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0620df6bfe0a1bc90f013a4bb494501716e787d271b7bc5969ecbc24b43756`  
		Last Modified: Fri, 17 Jan 2025 02:11:06 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bd936df8e147b648aa1a39d212c1624e064452a47059063133cd6adf29f7c7`  
		Last Modified: Fri, 17 Jan 2025 02:11:08 GMT  
		Size: 54.0 MB (54047054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966301da011cd0c70e74a358f99db4b9f43762dd18ed38f53665e9a24e880c4b`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b29247ae6bfe40191a231dba9717f4ca4bf21ec2c13c3606f0ace4b34eb7c43`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 3.3 KB (3267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:dd0a36256908be42678ad2890166b0e84a6246797662f2b93f3cd6f24ab68906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9af519ad2f15c502e5c17cfd4e3767beadd551d1851f350066b158eb41c6913`

```dockerfile
```

-	Layers:
	-	`sha256:ce130b032bac1fce394cc92324e72573e50caf69fdb9c099daad2c98bd8d9a1d`  
		Last Modified: Fri, 17 Jan 2025 02:11:05 GMT  
		Size: 34.8 KB (34764 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:29597558c26c7e456f9d4350b94f208a69114260adc21bdae0619f9a7749c34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64123e8eceb16c151befc29738868d17cd6b828c82a96cc2b46a182f62e48eab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
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
	-	`sha256:1d1f394b9e9ceefe286b141a6fce91d86072ca709baf5dc4447f3d5a6db9a163`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 17.4 MB (17427588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755932338966055de46ecbdb4e46288f1f52af30c0f57960411eed7bcbc876d0`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 18.1 MB (18099438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215cf40534564c9b7b71ea6e20aa6912ca15008a9c2dd68162c3efe4fc20e65b`  
		Last Modified: Fri, 17 Jan 2025 01:28:02 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb652a32cd1bd43600fe45d89a2455ab0b882887bfabe0664dc9eb749e932a1`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe784566335013d539f74a4e2e151368fe7ddd75a3583e15b1cbafc6eca14a`  
		Last Modified: Fri, 17 Jan 2025 01:28:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cd34d15034bf9fbabde6b6c4ec8bbfe56b0ee1dad07a86eef7f6d83a4829e5`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 6.4 MB (6367554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049bb15c92b4ba59ad113b753dc6305190eb3111a77ec5b86b8ca81c7dbc59f2`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 85.2 KB (85236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefdea776978b937e65e37c006d81238b97221fac666606609e7569cc915f005`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8ab79af5c8f7891f9b4d14518c40aae4efd8acb30339e416de829cf962a8ae`  
		Last Modified: Fri, 17 Jan 2025 02:25:24 GMT  
		Size: 54.0 MB (54047069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4015624859fadb74f8744fab8fe858c4a95b1d5fde6a26c00f709c761fb7908`  
		Last Modified: Fri, 17 Jan 2025 02:25:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935f17568aab4f3b97b7a27a57821ab17388667d24fa04ed2ac2b295bc4217bf`  
		Last Modified: Fri, 17 Jan 2025 02:25:23 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8fb08780d366a366517f413dc5e7ef73a7f5209ce4924d234dfb98829cba86d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7820bc0b8d0f7ee1b9d6587b10f5355904f51e675ddd0a337e25edb87b5578`

```dockerfile
```

-	Layers:
	-	`sha256:0857811d7117af260dff536135d5b9462e12a604d988f0bbcfa5c98ac94002c1`  
		Last Modified: Fri, 17 Jan 2025 02:25:20 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:be6a2bf3869c0b2ce79cbea0de54fc0151be9915cb61572b8fee8ae231380fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125658359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98a7305162cf56e40d783f72a96aafbe29862ec4cf094baab60b961b874e8a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98031a3690358e9e338c7b900ff223767ca20fe8d3581d723971bb5d3e97df6e`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 8.1 MB (8074417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c05adf332c68788c150e330500d99375063fb5fccac4eca47664fef925fe6`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05df1af7190779d81ae1d2a2f6bab0f116cd0911eaf925ea3b7c88d84e4dca`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.8 MB (17795742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373537e5e27b254a2e83716ef135b83be0eaffa0fbb7dd7e588802f57c22952f`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.1 MB (17106465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8781806a16e281a8c480f7f429497d259f378f76366f5b8a2047861a9a0eb`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 17.6 MB (17649723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd429dc70fde0e965c93f4ea2aa21344379a0f8461e5e8fb3a260e92129bfbd7`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1709b08f9705b3f6af9978783f2fb732992ff039699fdbc0a842595dbcb3bf9`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d18f467488432eff104e17eebdd3b73776125d5155413e82a70fac1ad2d50de`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eb3998a0993954da71d972744c4ceafe57b9e96dcb75f4d7626277df3d4176`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 7.0 MB (6981841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b5a025a6a9bf0b06bba2fe135db13911e1dcf31474e69df77b00520bbd3191`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 97.8 KB (97784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0743b347437f8517c3560af97d8923ca391286f17acbe0558f46b28c8c8c4d2`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49595e55dbff2fe86a9c4da769bc6a7679b3da9c2279eed30873af6bb678e195`  
		Last Modified: Fri, 17 Jan 2025 02:28:29 GMT  
		Size: 54.0 MB (53952083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3849eac5f1cf6d7788301e473e712d6bf6d77e0e01c3829c96b4dec4acf623d8`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb83a6536a87f2c86efa17f506102254efe83bcb5e283b31a0db94d18505dde5`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:66c420a8f09f46b8c9153ce490d112d23b47a11ae227e02b316ba27641ad742e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83edc878bc62dd15adedb843a231f657257baa90509166b729e8665157592cd7`

```dockerfile
```

-	Layers:
	-	`sha256:60f641b6e35d2698c4ef8617324030bdddce902f61a5ed2f117f633f27b92da8`  
		Last Modified: Fri, 17 Jan 2025 02:28:25 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:a2eb1cdc0a6e73e7bb35ef6dcbae5eed1198b4bca80bdb43392e53fe8810dac2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:873e54eb4ecdc9f413abacfb497523561c23f3532678e2c7893393646e10a50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156159516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a995afc276d185bce60731d4ddc05950b70c859778a9280024a3322eccc42f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db0ef5f6406167c28a55dbfc0fbbd527a8e8ee10b1ed0053a74bb5847f467b`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 8.1 MB (8060096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2617d81eedcf635e1fd94dc905266de252ae0d642c05465bb5c57e7b9e5b0`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e4c1fa9475c483015ff35cb0ca5fae973e6192bd7d355b798024cc3f6436c`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18849459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af4884fbc706fb37435cc7859f05891c18eaec536721e17e5a97361694520c3`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18798866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851762183788567546d15646f8ce06871883255ad227fb13b88d2c2e58ef7fa4`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 19.3 MB (19303643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d84c454f28e907e0f1f5996d71027092830cabefb6c3f3a8d0d9fb3b332b9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ada9115c6a1e6e261a5250211382c99910811092b2791e7b32073c01bd5817`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06335ef68f056dd7837956156616452c5087a436b0ddbbc94fcb4493390d9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e423b3161e65b5d155f4fee197bb34b95aaaf9034e25661cc942130922d5553f`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 6.7 MB (6733536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8d12927cbc5b132f3d989c2f32cf8fe0e3d4f9136fc784f675b40aa6e2caa5`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 89.4 KB (89425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326df6d9eb79ca016d6f1723d5ca2bced72bd36fd014e852b493a43a6447c10e`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa7701ffbf173fdb6f7999d28b78600828e770ef8de8c26f6767ff8d3413253`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 58.4 MB (58383027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40544ceb254c83f9677202983636becd2547551930652c6928a91b62c6b26529`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13647f78c45bebb40dba9ffe52c4bce8371d4edda349c507012fe1300ff50732`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66dc758ea69526e85c86620347676a493debe5c819cb7693f6902867778933e`  
		Last Modified: Fri, 17 Jan 2025 03:10:06 GMT  
		Size: 986.6 KB (986590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a769f32782fd44a1e305c6cd1ded3edecb5694f58954d3cc7b391478329db7f`  
		Last Modified: Fri, 17 Jan 2025 03:10:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f44cdf5fe82b821bf859dd7dc946f6fc747355176a01766fcb0f5bf94b122b`  
		Last Modified: Fri, 17 Jan 2025 03:10:06 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3258dbd3a9e8b790797ba1dfba1986498142bdce2e5fe2d92401acf136c2e82`  
		Last Modified: Fri, 17 Jan 2025 03:10:06 GMT  
		Size: 21.3 MB (21303864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0b43ebf5168b463eec3f98a035bb526d262c7ea182a4512d55af1403efb938`  
		Last Modified: Fri, 17 Jan 2025 03:10:07 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9c775d2142f922fee9a01cd1a263b620904b5742c972910af90e7648c88d3568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5a4e42c5ba363bc8aef3cb74e50dab63c9734c25f86d36792612a546031595`

```dockerfile
```

-	Layers:
	-	`sha256:ecb34284584c52d63e44745705b82df95475a84099839e3c14388a6214ea5f01`  
		Last Modified: Fri, 17 Jan 2025 03:10:05 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:46448a2b08fe5a5504d5f1691183d0fc974fdcfa3b17884c071bc93726c19a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149829070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e0f743e506c55a8233123a5803840a26c7e9f78903b01aee2dd8554580f7ba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98031a3690358e9e338c7b900ff223767ca20fe8d3581d723971bb5d3e97df6e`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 8.1 MB (8074417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c05adf332c68788c150e330500d99375063fb5fccac4eca47664fef925fe6`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05df1af7190779d81ae1d2a2f6bab0f116cd0911eaf925ea3b7c88d84e4dca`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.8 MB (17795742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373537e5e27b254a2e83716ef135b83be0eaffa0fbb7dd7e588802f57c22952f`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.1 MB (17106465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8781806a16e281a8c480f7f429497d259f378f76366f5b8a2047861a9a0eb`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 17.6 MB (17649723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd429dc70fde0e965c93f4ea2aa21344379a0f8461e5e8fb3a260e92129bfbd7`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1709b08f9705b3f6af9978783f2fb732992ff039699fdbc0a842595dbcb3bf9`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d18f467488432eff104e17eebdd3b73776125d5155413e82a70fac1ad2d50de`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eb3998a0993954da71d972744c4ceafe57b9e96dcb75f4d7626277df3d4176`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 7.0 MB (6981841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b5a025a6a9bf0b06bba2fe135db13911e1dcf31474e69df77b00520bbd3191`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 97.8 KB (97784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0743b347437f8517c3560af97d8923ca391286f17acbe0558f46b28c8c8c4d2`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49595e55dbff2fe86a9c4da769bc6a7679b3da9c2279eed30873af6bb678e195`  
		Last Modified: Fri, 17 Jan 2025 02:28:29 GMT  
		Size: 54.0 MB (53952083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3849eac5f1cf6d7788301e473e712d6bf6d77e0e01c3829c96b4dec4acf623d8`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb83a6536a87f2c86efa17f506102254efe83bcb5e283b31a0db94d18505dde5`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3982d96f5df89ee494fa458304355e30ef199bf1f1eda6c8b3dd607ca23d13`  
		Last Modified: Fri, 17 Jan 2025 03:27:30 GMT  
		Size: 1.0 MB (1014204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2b21cd3eb15dce210b7517a6be34965beddec2dc6e9384736e6bb97cc71618`  
		Last Modified: Fri, 17 Jan 2025 03:27:30 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4956e53894609bd8273c577579d49372b1b3f24cd142be4357a8b0e4873b2f90`  
		Last Modified: Fri, 17 Jan 2025 03:27:30 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5cc90ddeee38314b0dceef56e97746323daddce4a63b1dcfa6183891f64d39`  
		Last Modified: Fri, 17 Jan 2025 03:27:47 GMT  
		Size: 23.2 MB (23155160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889d5be2190a9406c5b1b3356b8b527176fc46f76cb5d40192b120061af4949f`  
		Last Modified: Fri, 17 Jan 2025 03:27:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:60876bd91d54cb65a601c27c85c7d8eda74c6a2f025325d12829c4f0173616a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7259e4a52601951b094f318099af2a7f82d03f417f9a37fe03194189522e619f`

```dockerfile
```

-	Layers:
	-	`sha256:1b563391abe23859090df83bb0dd41ef65f19bc25be6210520c59171a5564c22`  
		Last Modified: Fri, 17 Jan 2025 03:27:28 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:147774e53a5cba9011ba41fc0a6031a0fe2a38be3ea00ada24c7c986bfe3e895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:1ddbeca1f26cfd027cd80d7c22a37038dc7a5b749a4cc162893d982e25611f9e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2321733461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa6fd542e3201d9417d1c00e4e8e4ea67053d989ef8279153b1c3c1a73390dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 17 Jan 2025 01:32:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 17 Jan 2025 01:32:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 17 Jan 2025 01:32:29 GMT
ENV DOCKER_VERSION=27.5.0
# Fri, 17 Jan 2025 01:32:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Fri, 17 Jan 2025 01:32:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:32:38 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Fri, 17 Jan 2025 01:32:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Fri, 17 Jan 2025 01:32:40 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Fri, 17 Jan 2025 01:32:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:32:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Fri, 17 Jan 2025 01:32:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Fri, 17 Jan 2025 01:32:49 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Fri, 17 Jan 2025 01:32:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a2b5f44002e9945660f33fac78eda870ab26d14af8237ced3f7d6eebafc482`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203a2deeff1a6f93e060d1f072f55c5e625f7a8ba0b5b650ea6a24ec493e906f`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 357.5 KB (357481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892a6f8fa8324bfeb4612f7a42f4557afd5e082b76d6eb091e0de676dc19d26b`  
		Last Modified: Fri, 17 Jan 2025 01:33:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c45ea49c7511c526fac9de55eb8d1ec854cf7c24e175e514d4f76d393a1492f`  
		Last Modified: Fri, 17 Jan 2025 01:33:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e5b7f87ce7df7acc0870faf1a629a49f3f3b7865260274227fe01eb5fbe059`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 19.2 MB (19163659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1792865d58e6d13c7f1f82e4bd2c626a933e6f6a35db76e7a561e7feea4d7313`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc28b08ea10f6f26ceaad44e423332916af104c6c64d5c832f500bc690e15bf`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3b113153c6bc3cc9533ce2cde3d40a1feae4f3c43de591454bc66cabd8b7d6`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab2a02883224978a44c53d67303e6399cfa8291fd4878a7d28d1b9f9c86e0fb`  
		Last Modified: Fri, 17 Jan 2025 01:33:03 GMT  
		Size: 19.6 MB (19646321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9674894f9e36062ebb2d60558e37eb1e25270606e64a963e2154eca16d22a1`  
		Last Modified: Fri, 17 Jan 2025 01:33:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6baac49af4fea3c6c40c4380c6c83141230ecf225b612fef2dcb0860d12bd3`  
		Last Modified: Fri, 17 Jan 2025 01:33:00 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6f04636f816d025e0fcb207436d479348f6902a7b726b00fc0b08c4c91da5`  
		Last Modified: Fri, 17 Jan 2025 01:33:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff25e05ad1368fb78eb59c79e73d3276e7d77771072037ec3e43ca5409067c78`  
		Last Modified: Fri, 17 Jan 2025 01:33:03 GMT  
		Size: 20.2 MB (20169201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:a4691c37ea78600875afbfe9b5f3193ad202961501db79accf2e4169f9b42021
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181529728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1056e0f7366117381694ae8dcdba87d790f109eb17c3d003ef5aef0219256f5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 17 Jan 2025 01:33:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 17 Jan 2025 01:34:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 17 Jan 2025 01:34:31 GMT
ENV DOCKER_VERSION=27.5.0
# Fri, 17 Jan 2025 01:34:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Fri, 17 Jan 2025 01:34:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:34:45 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Fri, 17 Jan 2025 01:34:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Fri, 17 Jan 2025 01:34:46 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Fri, 17 Jan 2025 01:34:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:34:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Fri, 17 Jan 2025 01:34:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Fri, 17 Jan 2025 01:34:58 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Fri, 17 Jan 2025 01:35:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e6274df071a7d5a5db2dfcfdd09b3e5619a6a91cdf7f97ab0e499ce20fbadc`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75379368627062a255445132b6e6f800fa70735daa6088bd9a26716f97d8c20`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 341.5 KB (341471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d991c76af457bbd0d51a6c717c7269b73a45c7241bb22f2ea0a2140d7e5df9b`  
		Last Modified: Fri, 17 Jan 2025 01:35:16 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499d890bbe543c9fa6a376c2cc02860b9d28c3ceb3333573c42123258c044874`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1c11b12baeb8dbd4b7d91eb54b5d14a02ae0cf432615ea004e1e19f8f39c1d`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 19.2 MB (19160387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3235fd67ddd40cdaef5899c144213bba7245b4307f2902f0aebdf497c8d724`  
		Last Modified: Fri, 17 Jan 2025 01:35:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b03c5d4a69994a8004df958ddad06c5afbcc59f276c99989342f8400bf8d7d3`  
		Last Modified: Fri, 17 Jan 2025 01:35:14 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604799b0a87e0da3e79003c6f7f3b8c0ee9f49d2a0fd3da26c55e2d59e5a56ce`  
		Last Modified: Fri, 17 Jan 2025 01:35:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35965d90f9d46033f9e870e8cd2fb5125759d0ab816adacb4c3977e8b124b395`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 19.6 MB (19638065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2795117faa51777ee5591503a846e643112eed007983483a0799b0aba498c98`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e460c490d0afd58b3f2e390983623e89cd4a1f9bafe9b32435fdb41e2c37e99`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54d5078572cf39f63c8f5cc06830bd0716dcc480240b5200491cf747e26c12a`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb52aa115ea25674a9b875dd187041c15e8bd3b155bf96774b70758ad0f61e4`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 20.2 MB (20165876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:3b3e4d8d1726d5fb5d874f245b2d80913ac5431e62e2beed2d21e7966bd16079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:a4691c37ea78600875afbfe9b5f3193ad202961501db79accf2e4169f9b42021
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181529728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1056e0f7366117381694ae8dcdba87d790f109eb17c3d003ef5aef0219256f5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 17 Jan 2025 01:33:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 17 Jan 2025 01:34:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 17 Jan 2025 01:34:31 GMT
ENV DOCKER_VERSION=27.5.0
# Fri, 17 Jan 2025 01:34:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Fri, 17 Jan 2025 01:34:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:34:45 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Fri, 17 Jan 2025 01:34:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Fri, 17 Jan 2025 01:34:46 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Fri, 17 Jan 2025 01:34:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:34:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Fri, 17 Jan 2025 01:34:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Fri, 17 Jan 2025 01:34:58 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Fri, 17 Jan 2025 01:35:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e6274df071a7d5a5db2dfcfdd09b3e5619a6a91cdf7f97ab0e499ce20fbadc`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75379368627062a255445132b6e6f800fa70735daa6088bd9a26716f97d8c20`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 341.5 KB (341471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d991c76af457bbd0d51a6c717c7269b73a45c7241bb22f2ea0a2140d7e5df9b`  
		Last Modified: Fri, 17 Jan 2025 01:35:16 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499d890bbe543c9fa6a376c2cc02860b9d28c3ceb3333573c42123258c044874`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1c11b12baeb8dbd4b7d91eb54b5d14a02ae0cf432615ea004e1e19f8f39c1d`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 19.2 MB (19160387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3235fd67ddd40cdaef5899c144213bba7245b4307f2902f0aebdf497c8d724`  
		Last Modified: Fri, 17 Jan 2025 01:35:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b03c5d4a69994a8004df958ddad06c5afbcc59f276c99989342f8400bf8d7d3`  
		Last Modified: Fri, 17 Jan 2025 01:35:14 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604799b0a87e0da3e79003c6f7f3b8c0ee9f49d2a0fd3da26c55e2d59e5a56ce`  
		Last Modified: Fri, 17 Jan 2025 01:35:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35965d90f9d46033f9e870e8cd2fb5125759d0ab816adacb4c3977e8b124b395`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 19.6 MB (19638065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2795117faa51777ee5591503a846e643112eed007983483a0799b0aba498c98`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e460c490d0afd58b3f2e390983623e89cd4a1f9bafe9b32435fdb41e2c37e99`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54d5078572cf39f63c8f5cc06830bd0716dcc480240b5200491cf747e26c12a`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb52aa115ea25674a9b875dd187041c15e8bd3b155bf96774b70758ad0f61e4`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 20.2 MB (20165876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:3bde2a2a6f2192672461cfec2b8264a4927348c274db2b6495e18ce39d141cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:1ddbeca1f26cfd027cd80d7c22a37038dc7a5b749a4cc162893d982e25611f9e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2321733461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa6fd542e3201d9417d1c00e4e8e4ea67053d989ef8279153b1c3c1a73390dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 17 Jan 2025 01:32:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 17 Jan 2025 01:32:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 17 Jan 2025 01:32:29 GMT
ENV DOCKER_VERSION=27.5.0
# Fri, 17 Jan 2025 01:32:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Fri, 17 Jan 2025 01:32:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:32:38 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Fri, 17 Jan 2025 01:32:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Fri, 17 Jan 2025 01:32:40 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Fri, 17 Jan 2025 01:32:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:32:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Fri, 17 Jan 2025 01:32:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Fri, 17 Jan 2025 01:32:49 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Fri, 17 Jan 2025 01:32:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a2b5f44002e9945660f33fac78eda870ab26d14af8237ced3f7d6eebafc482`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203a2deeff1a6f93e060d1f072f55c5e625f7a8ba0b5b650ea6a24ec493e906f`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 357.5 KB (357481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892a6f8fa8324bfeb4612f7a42f4557afd5e082b76d6eb091e0de676dc19d26b`  
		Last Modified: Fri, 17 Jan 2025 01:33:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c45ea49c7511c526fac9de55eb8d1ec854cf7c24e175e514d4f76d393a1492f`  
		Last Modified: Fri, 17 Jan 2025 01:33:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e5b7f87ce7df7acc0870faf1a629a49f3f3b7865260274227fe01eb5fbe059`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 19.2 MB (19163659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1792865d58e6d13c7f1f82e4bd2c626a933e6f6a35db76e7a561e7feea4d7313`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc28b08ea10f6f26ceaad44e423332916af104c6c64d5c832f500bc690e15bf`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3b113153c6bc3cc9533ce2cde3d40a1feae4f3c43de591454bc66cabd8b7d6`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab2a02883224978a44c53d67303e6399cfa8291fd4878a7d28d1b9f9c86e0fb`  
		Last Modified: Fri, 17 Jan 2025 01:33:03 GMT  
		Size: 19.6 MB (19646321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9674894f9e36062ebb2d60558e37eb1e25270606e64a963e2154eca16d22a1`  
		Last Modified: Fri, 17 Jan 2025 01:33:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6baac49af4fea3c6c40c4380c6c83141230ecf225b612fef2dcb0860d12bd3`  
		Last Modified: Fri, 17 Jan 2025 01:33:00 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6f04636f816d025e0fcb207436d479348f6902a7b726b00fc0b08c4c91da5`  
		Last Modified: Fri, 17 Jan 2025 01:33:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff25e05ad1368fb78eb59c79e73d3276e7d77771072037ec3e43ca5409067c78`  
		Last Modified: Fri, 17 Jan 2025 01:33:03 GMT  
		Size: 20.2 MB (20169201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5`

```console
$ docker pull docker@sha256:45b80efde6892498e1160c3be8eb7cc67732863caac98d2a79af24398ff1c106
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

### `docker:27.5` - linux; amd64

```console
$ docker pull docker@sha256:328fee4531eccdcfe52b61ba73c849a649cacad29fba1a4129c95b40e0f2196c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133867713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b300b8cdc5f2ac4f108ecdd418f3ea30e35b4ee1018ff818ca39dd3f0bc7aadd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db0ef5f6406167c28a55dbfc0fbbd527a8e8ee10b1ed0053a74bb5847f467b`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 8.1 MB (8060096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2617d81eedcf635e1fd94dc905266de252ae0d642c05465bb5c57e7b9e5b0`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e4c1fa9475c483015ff35cb0ca5fae973e6192bd7d355b798024cc3f6436c`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18849459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af4884fbc706fb37435cc7859f05891c18eaec536721e17e5a97361694520c3`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18798866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851762183788567546d15646f8ce06871883255ad227fb13b88d2c2e58ef7fa4`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 19.3 MB (19303643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d84c454f28e907e0f1f5996d71027092830cabefb6c3f3a8d0d9fb3b332b9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ada9115c6a1e6e261a5250211382c99910811092b2791e7b32073c01bd5817`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06335ef68f056dd7837956156616452c5087a436b0ddbbc94fcb4493390d9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e423b3161e65b5d155f4fee197bb34b95aaaf9034e25661cc942130922d5553f`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 6.7 MB (6733536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8d12927cbc5b132f3d989c2f32cf8fe0e3d4f9136fc784f675b40aa6e2caa5`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 89.4 KB (89425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326df6d9eb79ca016d6f1723d5ca2bced72bd36fd014e852b493a43a6447c10e`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa7701ffbf173fdb6f7999d28b78600828e770ef8de8c26f6767ff8d3413253`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 58.4 MB (58383027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40544ceb254c83f9677202983636becd2547551930652c6928a91b62c6b26529`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13647f78c45bebb40dba9ffe52c4bce8371d4edda349c507012fe1300ff50732`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5` - unknown; unknown

```console
$ docker pull docker@sha256:683d1639ff61791a2eae0ec63a422d289dc4e28394eb8e39ccf17b56e1737122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556810057e6ba7d14c45298e2761fef6923333526367bb7e64510b0649dd514e`

```dockerfile
```

-	Layers:
	-	`sha256:18fa62c94f21565d5f5d2b2d15c416dce24b5ac429609729db340cc622a08d00`  
		Last Modified: Fri, 17 Jan 2025 02:09:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5` - linux; arm variant v6

```console
$ docker pull docker@sha256:872158a8fc908710ac79c7d0c61287953a6593ef365f7593fbc9ee6d449ca9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124949669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bbc03711f0e14a6963ddb7043e52c2f66782fc50b0319107b2712a9107fc28`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
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
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea778430c11317962e3aa40444717aa8dc546fc65595ea9fd6e73d36310902f`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 17.4 MB (17448787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea230caf38f20e83e44f4dc9f84ff4fb52580e6d973dd8ecd2952cd36ad2a21`  
		Last Modified: Fri, 17 Jan 2025 01:27:49 GMT  
		Size: 18.1 MB (18112354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97006a84267c6bca594ceb4a5bf26d607f5bdef93912e07f6e846be4422b1c`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e59e6b008d5c5752b4a7993bd0b52b1db7dc2dfa774314f4f775cc22afa320`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89fe821a62ed4869930b04fc18ac60cf2bda17c09431466d8459ccc0c3549e2`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fe55d9784a2a762c0d6ed72664929cdf9284a3a888e3089d5e9220628c6b45`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 7.0 MB (7041413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d364c50ad8b6c6c862e3e6daa1c4cf0a6e8c8433c8a71cffd144f766f0e4fb23`  
		Last Modified: Fri, 17 Jan 2025 02:11:06 GMT  
		Size: 89.1 KB (89085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0620df6bfe0a1bc90f013a4bb494501716e787d271b7bc5969ecbc24b43756`  
		Last Modified: Fri, 17 Jan 2025 02:11:06 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bd936df8e147b648aa1a39d212c1624e064452a47059063133cd6adf29f7c7`  
		Last Modified: Fri, 17 Jan 2025 02:11:08 GMT  
		Size: 54.0 MB (54047054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966301da011cd0c70e74a358f99db4b9f43762dd18ed38f53665e9a24e880c4b`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b29247ae6bfe40191a231dba9717f4ca4bf21ec2c13c3606f0ace4b34eb7c43`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 3.3 KB (3267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5` - unknown; unknown

```console
$ docker pull docker@sha256:dd0a36256908be42678ad2890166b0e84a6246797662f2b93f3cd6f24ab68906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9af519ad2f15c502e5c17cfd4e3767beadd551d1851f350066b158eb41c6913`

```dockerfile
```

-	Layers:
	-	`sha256:ce130b032bac1fce394cc92324e72573e50caf69fdb9c099daad2c98bd8d9a1d`  
		Last Modified: Fri, 17 Jan 2025 02:11:05 GMT  
		Size: 34.8 KB (34764 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5` - linux; arm variant v7

```console
$ docker pull docker@sha256:29597558c26c7e456f9d4350b94f208a69114260adc21bdae0619f9a7749c34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64123e8eceb16c151befc29738868d17cd6b828c82a96cc2b46a182f62e48eab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
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
	-	`sha256:1d1f394b9e9ceefe286b141a6fce91d86072ca709baf5dc4447f3d5a6db9a163`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 17.4 MB (17427588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755932338966055de46ecbdb4e46288f1f52af30c0f57960411eed7bcbc876d0`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 18.1 MB (18099438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215cf40534564c9b7b71ea6e20aa6912ca15008a9c2dd68162c3efe4fc20e65b`  
		Last Modified: Fri, 17 Jan 2025 01:28:02 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb652a32cd1bd43600fe45d89a2455ab0b882887bfabe0664dc9eb749e932a1`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe784566335013d539f74a4e2e151368fe7ddd75a3583e15b1cbafc6eca14a`  
		Last Modified: Fri, 17 Jan 2025 01:28:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cd34d15034bf9fbabde6b6c4ec8bbfe56b0ee1dad07a86eef7f6d83a4829e5`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 6.4 MB (6367554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049bb15c92b4ba59ad113b753dc6305190eb3111a77ec5b86b8ca81c7dbc59f2`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 85.2 KB (85236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefdea776978b937e65e37c006d81238b97221fac666606609e7569cc915f005`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8ab79af5c8f7891f9b4d14518c40aae4efd8acb30339e416de829cf962a8ae`  
		Last Modified: Fri, 17 Jan 2025 02:25:24 GMT  
		Size: 54.0 MB (54047069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4015624859fadb74f8744fab8fe858c4a95b1d5fde6a26c00f709c761fb7908`  
		Last Modified: Fri, 17 Jan 2025 02:25:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935f17568aab4f3b97b7a27a57821ab17388667d24fa04ed2ac2b295bc4217bf`  
		Last Modified: Fri, 17 Jan 2025 02:25:23 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5` - unknown; unknown

```console
$ docker pull docker@sha256:8fb08780d366a366517f413dc5e7ef73a7f5209ce4924d234dfb98829cba86d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7820bc0b8d0f7ee1b9d6587b10f5355904f51e675ddd0a337e25edb87b5578`

```dockerfile
```

-	Layers:
	-	`sha256:0857811d7117af260dff536135d5b9462e12a604d988f0bbcfa5c98ac94002c1`  
		Last Modified: Fri, 17 Jan 2025 02:25:20 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:be6a2bf3869c0b2ce79cbea0de54fc0151be9915cb61572b8fee8ae231380fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125658359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98a7305162cf56e40d783f72a96aafbe29862ec4cf094baab60b961b874e8a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98031a3690358e9e338c7b900ff223767ca20fe8d3581d723971bb5d3e97df6e`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 8.1 MB (8074417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c05adf332c68788c150e330500d99375063fb5fccac4eca47664fef925fe6`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05df1af7190779d81ae1d2a2f6bab0f116cd0911eaf925ea3b7c88d84e4dca`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.8 MB (17795742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373537e5e27b254a2e83716ef135b83be0eaffa0fbb7dd7e588802f57c22952f`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.1 MB (17106465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8781806a16e281a8c480f7f429497d259f378f76366f5b8a2047861a9a0eb`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 17.6 MB (17649723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd429dc70fde0e965c93f4ea2aa21344379a0f8461e5e8fb3a260e92129bfbd7`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1709b08f9705b3f6af9978783f2fb732992ff039699fdbc0a842595dbcb3bf9`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d18f467488432eff104e17eebdd3b73776125d5155413e82a70fac1ad2d50de`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eb3998a0993954da71d972744c4ceafe57b9e96dcb75f4d7626277df3d4176`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 7.0 MB (6981841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b5a025a6a9bf0b06bba2fe135db13911e1dcf31474e69df77b00520bbd3191`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 97.8 KB (97784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0743b347437f8517c3560af97d8923ca391286f17acbe0558f46b28c8c8c4d2`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49595e55dbff2fe86a9c4da769bc6a7679b3da9c2279eed30873af6bb678e195`  
		Last Modified: Fri, 17 Jan 2025 02:28:29 GMT  
		Size: 54.0 MB (53952083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3849eac5f1cf6d7788301e473e712d6bf6d77e0e01c3829c96b4dec4acf623d8`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb83a6536a87f2c86efa17f506102254efe83bcb5e283b31a0db94d18505dde5`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5` - unknown; unknown

```console
$ docker pull docker@sha256:66c420a8f09f46b8c9153ce490d112d23b47a11ae227e02b316ba27641ad742e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83edc878bc62dd15adedb843a231f657257baa90509166b729e8665157592cd7`

```dockerfile
```

-	Layers:
	-	`sha256:60f641b6e35d2698c4ef8617324030bdddce902f61a5ed2f117f633f27b92da8`  
		Last Modified: Fri, 17 Jan 2025 02:28:25 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5-cli`

```console
$ docker pull docker@sha256:7c10b867b5da6f0ecbac463defeaa490c1d2816cb02fe4e14d2994ad9c3812cd
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

### `docker:27.5-cli` - linux; amd64

```console
$ docker pull docker@sha256:b219ac7db8149403917bdea481b4e8bdc9e48c492e12d6aa2b0ad8e11b323316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68655933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cc102d4a93a8704667364b5cfb93d9dcc26a6a861645223f2d4893b3ed723a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.0
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db0ef5f6406167c28a55dbfc0fbbd527a8e8ee10b1ed0053a74bb5847f467b`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 8.1 MB (8060096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2617d81eedcf635e1fd94dc905266de252ae0d642c05465bb5c57e7b9e5b0`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e4c1fa9475c483015ff35cb0ca5fae973e6192bd7d355b798024cc3f6436c`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18849459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af4884fbc706fb37435cc7859f05891c18eaec536721e17e5a97361694520c3`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18798866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851762183788567546d15646f8ce06871883255ad227fb13b88d2c2e58ef7fa4`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 19.3 MB (19303643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d84c454f28e907e0f1f5996d71027092830cabefb6c3f3a8d0d9fb3b332b9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ada9115c6a1e6e261a5250211382c99910811092b2791e7b32073c01bd5817`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06335ef68f056dd7837956156616452c5087a436b0ddbbc94fcb4493390d9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:bfcde7282475bfa1b52d54c2ccea12401ee915b605e1d578a5081bb4a69627bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8044174370b4166bc88d8f825313d5221505fa7b2ba129e316bb4e292d4a93d8`

```dockerfile
```

-	Layers:
	-	`sha256:f5e0658d18f9353954b3b81fc16fe0b3e32f0e667af202b4f413c79dce6a3b96`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:f52fb18fdfc78a4af51b84ac7d2b5fca13b8e3e09b1067aa849e9f04030c2c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63766314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74e5406e29303780211a38cb58677a0c6a96a6aa5ce396f86ae128d852cc85d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.0
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
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
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea778430c11317962e3aa40444717aa8dc546fc65595ea9fd6e73d36310902f`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 17.4 MB (17448787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea230caf38f20e83e44f4dc9f84ff4fb52580e6d973dd8ecd2952cd36ad2a21`  
		Last Modified: Fri, 17 Jan 2025 01:27:49 GMT  
		Size: 18.1 MB (18112354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97006a84267c6bca594ceb4a5bf26d607f5bdef93912e07f6e846be4422b1c`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e59e6b008d5c5752b4a7993bd0b52b1db7dc2dfa774314f4f775cc22afa320`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89fe821a62ed4869930b04fc18ac60cf2bda17c09431466d8459ccc0c3549e2`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:dce530002422cd3b77135d6ae618300706585d7d6deebc956b7425231442feeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c540c5273aba065d46aa7fa9ca86bfb8aa222597b3283936e19bbdef868628f6`

```dockerfile
```

-	Layers:
	-	`sha256:532ebdac6902ef2db952873eeeaf73c981703befe573cd7cbe0eaacd64aa031f`  
		Last Modified: Fri, 17 Jan 2025 01:27:47 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:9e993e3871a714198e4b947664c5f228a5d7982b3515670942d8a495f03485eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62776105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde14708064af6f21da2b23403c4e90218556fb6cf1508302904ef370691f99c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.0
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
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
	-	`sha256:1d1f394b9e9ceefe286b141a6fce91d86072ca709baf5dc4447f3d5a6db9a163`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 17.4 MB (17427588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755932338966055de46ecbdb4e46288f1f52af30c0f57960411eed7bcbc876d0`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 18.1 MB (18099438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215cf40534564c9b7b71ea6e20aa6912ca15008a9c2dd68162c3efe4fc20e65b`  
		Last Modified: Fri, 17 Jan 2025 01:28:02 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb652a32cd1bd43600fe45d89a2455ab0b882887bfabe0664dc9eb749e932a1`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe784566335013d539f74a4e2e151368fe7ddd75a3583e15b1cbafc6eca14a`  
		Last Modified: Fri, 17 Jan 2025 01:28:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:dfca36c13fd1337794df037f0fc30b729677e432669884ebcb2f92429c838457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4905f7d813489e8a4204010015fb7509e3c94934b1b88e1418f21f37a337a6f`

```dockerfile
```

-	Layers:
	-	`sha256:89c06eb5c6c66dfe6a2640b9ccf35cdc3ab8ca4ac9883f9fb2b69b8aba4d80e3`  
		Last Modified: Fri, 17 Jan 2025 01:28:01 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a121337c9287fdc11e04a8a12708f639e8c3ba427945f4539df65679aee3ee8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64620861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d961a7c95de71f4706af938b3c55efbe8f7379a1c212212251b71732ea4c5cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.0
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98031a3690358e9e338c7b900ff223767ca20fe8d3581d723971bb5d3e97df6e`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 8.1 MB (8074417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c05adf332c68788c150e330500d99375063fb5fccac4eca47664fef925fe6`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05df1af7190779d81ae1d2a2f6bab0f116cd0911eaf925ea3b7c88d84e4dca`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.8 MB (17795742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373537e5e27b254a2e83716ef135b83be0eaffa0fbb7dd7e588802f57c22952f`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.1 MB (17106465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8781806a16e281a8c480f7f429497d259f378f76366f5b8a2047861a9a0eb`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 17.6 MB (17649723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd429dc70fde0e965c93f4ea2aa21344379a0f8461e5e8fb3a260e92129bfbd7`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1709b08f9705b3f6af9978783f2fb732992ff039699fdbc0a842595dbcb3bf9`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d18f467488432eff104e17eebdd3b73776125d5155413e82a70fac1ad2d50de`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1d010e0b0f4fa82a5b3ba475d15bffbaf6b9481a3a2c85a608aa6f1be93f4160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a79ec7a8c697907793b7bd322196ef33a33e0ae9eb4ea0f46752d9aa591878`

```dockerfile
```

-	Layers:
	-	`sha256:1ce07430fc5561a2375bb4a6167743bb1bef6046817bf347a9a3f3373a4cfc4b`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5-dind`

```console
$ docker pull docker@sha256:45b80efde6892498e1160c3be8eb7cc67732863caac98d2a79af24398ff1c106
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

### `docker:27.5-dind` - linux; amd64

```console
$ docker pull docker@sha256:328fee4531eccdcfe52b61ba73c849a649cacad29fba1a4129c95b40e0f2196c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133867713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b300b8cdc5f2ac4f108ecdd418f3ea30e35b4ee1018ff818ca39dd3f0bc7aadd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db0ef5f6406167c28a55dbfc0fbbd527a8e8ee10b1ed0053a74bb5847f467b`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 8.1 MB (8060096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2617d81eedcf635e1fd94dc905266de252ae0d642c05465bb5c57e7b9e5b0`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e4c1fa9475c483015ff35cb0ca5fae973e6192bd7d355b798024cc3f6436c`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18849459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af4884fbc706fb37435cc7859f05891c18eaec536721e17e5a97361694520c3`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18798866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851762183788567546d15646f8ce06871883255ad227fb13b88d2c2e58ef7fa4`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 19.3 MB (19303643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d84c454f28e907e0f1f5996d71027092830cabefb6c3f3a8d0d9fb3b332b9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ada9115c6a1e6e261a5250211382c99910811092b2791e7b32073c01bd5817`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06335ef68f056dd7837956156616452c5087a436b0ddbbc94fcb4493390d9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e423b3161e65b5d155f4fee197bb34b95aaaf9034e25661cc942130922d5553f`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 6.7 MB (6733536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8d12927cbc5b132f3d989c2f32cf8fe0e3d4f9136fc784f675b40aa6e2caa5`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 89.4 KB (89425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326df6d9eb79ca016d6f1723d5ca2bced72bd36fd014e852b493a43a6447c10e`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa7701ffbf173fdb6f7999d28b78600828e770ef8de8c26f6767ff8d3413253`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 58.4 MB (58383027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40544ceb254c83f9677202983636becd2547551930652c6928a91b62c6b26529`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13647f78c45bebb40dba9ffe52c4bce8371d4edda349c507012fe1300ff50732`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:683d1639ff61791a2eae0ec63a422d289dc4e28394eb8e39ccf17b56e1737122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556810057e6ba7d14c45298e2761fef6923333526367bb7e64510b0649dd514e`

```dockerfile
```

-	Layers:
	-	`sha256:18fa62c94f21565d5f5d2b2d15c416dce24b5ac429609729db340cc622a08d00`  
		Last Modified: Fri, 17 Jan 2025 02:09:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:872158a8fc908710ac79c7d0c61287953a6593ef365f7593fbc9ee6d449ca9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124949669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bbc03711f0e14a6963ddb7043e52c2f66782fc50b0319107b2712a9107fc28`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
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
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea778430c11317962e3aa40444717aa8dc546fc65595ea9fd6e73d36310902f`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 17.4 MB (17448787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea230caf38f20e83e44f4dc9f84ff4fb52580e6d973dd8ecd2952cd36ad2a21`  
		Last Modified: Fri, 17 Jan 2025 01:27:49 GMT  
		Size: 18.1 MB (18112354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97006a84267c6bca594ceb4a5bf26d607f5bdef93912e07f6e846be4422b1c`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e59e6b008d5c5752b4a7993bd0b52b1db7dc2dfa774314f4f775cc22afa320`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89fe821a62ed4869930b04fc18ac60cf2bda17c09431466d8459ccc0c3549e2`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fe55d9784a2a762c0d6ed72664929cdf9284a3a888e3089d5e9220628c6b45`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 7.0 MB (7041413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d364c50ad8b6c6c862e3e6daa1c4cf0a6e8c8433c8a71cffd144f766f0e4fb23`  
		Last Modified: Fri, 17 Jan 2025 02:11:06 GMT  
		Size: 89.1 KB (89085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0620df6bfe0a1bc90f013a4bb494501716e787d271b7bc5969ecbc24b43756`  
		Last Modified: Fri, 17 Jan 2025 02:11:06 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bd936df8e147b648aa1a39d212c1624e064452a47059063133cd6adf29f7c7`  
		Last Modified: Fri, 17 Jan 2025 02:11:08 GMT  
		Size: 54.0 MB (54047054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966301da011cd0c70e74a358f99db4b9f43762dd18ed38f53665e9a24e880c4b`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b29247ae6bfe40191a231dba9717f4ca4bf21ec2c13c3606f0ace4b34eb7c43`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 3.3 KB (3267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:dd0a36256908be42678ad2890166b0e84a6246797662f2b93f3cd6f24ab68906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9af519ad2f15c502e5c17cfd4e3767beadd551d1851f350066b158eb41c6913`

```dockerfile
```

-	Layers:
	-	`sha256:ce130b032bac1fce394cc92324e72573e50caf69fdb9c099daad2c98bd8d9a1d`  
		Last Modified: Fri, 17 Jan 2025 02:11:05 GMT  
		Size: 34.8 KB (34764 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:29597558c26c7e456f9d4350b94f208a69114260adc21bdae0619f9a7749c34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64123e8eceb16c151befc29738868d17cd6b828c82a96cc2b46a182f62e48eab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
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
	-	`sha256:1d1f394b9e9ceefe286b141a6fce91d86072ca709baf5dc4447f3d5a6db9a163`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 17.4 MB (17427588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755932338966055de46ecbdb4e46288f1f52af30c0f57960411eed7bcbc876d0`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 18.1 MB (18099438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215cf40534564c9b7b71ea6e20aa6912ca15008a9c2dd68162c3efe4fc20e65b`  
		Last Modified: Fri, 17 Jan 2025 01:28:02 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb652a32cd1bd43600fe45d89a2455ab0b882887bfabe0664dc9eb749e932a1`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe784566335013d539f74a4e2e151368fe7ddd75a3583e15b1cbafc6eca14a`  
		Last Modified: Fri, 17 Jan 2025 01:28:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cd34d15034bf9fbabde6b6c4ec8bbfe56b0ee1dad07a86eef7f6d83a4829e5`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 6.4 MB (6367554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049bb15c92b4ba59ad113b753dc6305190eb3111a77ec5b86b8ca81c7dbc59f2`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 85.2 KB (85236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefdea776978b937e65e37c006d81238b97221fac666606609e7569cc915f005`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8ab79af5c8f7891f9b4d14518c40aae4efd8acb30339e416de829cf962a8ae`  
		Last Modified: Fri, 17 Jan 2025 02:25:24 GMT  
		Size: 54.0 MB (54047069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4015624859fadb74f8744fab8fe858c4a95b1d5fde6a26c00f709c761fb7908`  
		Last Modified: Fri, 17 Jan 2025 02:25:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935f17568aab4f3b97b7a27a57821ab17388667d24fa04ed2ac2b295bc4217bf`  
		Last Modified: Fri, 17 Jan 2025 02:25:23 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8fb08780d366a366517f413dc5e7ef73a7f5209ce4924d234dfb98829cba86d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7820bc0b8d0f7ee1b9d6587b10f5355904f51e675ddd0a337e25edb87b5578`

```dockerfile
```

-	Layers:
	-	`sha256:0857811d7117af260dff536135d5b9462e12a604d988f0bbcfa5c98ac94002c1`  
		Last Modified: Fri, 17 Jan 2025 02:25:20 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:be6a2bf3869c0b2ce79cbea0de54fc0151be9915cb61572b8fee8ae231380fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125658359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98a7305162cf56e40d783f72a96aafbe29862ec4cf094baab60b961b874e8a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98031a3690358e9e338c7b900ff223767ca20fe8d3581d723971bb5d3e97df6e`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 8.1 MB (8074417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c05adf332c68788c150e330500d99375063fb5fccac4eca47664fef925fe6`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05df1af7190779d81ae1d2a2f6bab0f116cd0911eaf925ea3b7c88d84e4dca`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.8 MB (17795742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373537e5e27b254a2e83716ef135b83be0eaffa0fbb7dd7e588802f57c22952f`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.1 MB (17106465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8781806a16e281a8c480f7f429497d259f378f76366f5b8a2047861a9a0eb`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 17.6 MB (17649723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd429dc70fde0e965c93f4ea2aa21344379a0f8461e5e8fb3a260e92129bfbd7`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1709b08f9705b3f6af9978783f2fb732992ff039699fdbc0a842595dbcb3bf9`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d18f467488432eff104e17eebdd3b73776125d5155413e82a70fac1ad2d50de`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eb3998a0993954da71d972744c4ceafe57b9e96dcb75f4d7626277df3d4176`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 7.0 MB (6981841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b5a025a6a9bf0b06bba2fe135db13911e1dcf31474e69df77b00520bbd3191`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 97.8 KB (97784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0743b347437f8517c3560af97d8923ca391286f17acbe0558f46b28c8c8c4d2`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49595e55dbff2fe86a9c4da769bc6a7679b3da9c2279eed30873af6bb678e195`  
		Last Modified: Fri, 17 Jan 2025 02:28:29 GMT  
		Size: 54.0 MB (53952083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3849eac5f1cf6d7788301e473e712d6bf6d77e0e01c3829c96b4dec4acf623d8`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb83a6536a87f2c86efa17f506102254efe83bcb5e283b31a0db94d18505dde5`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:66c420a8f09f46b8c9153ce490d112d23b47a11ae227e02b316ba27641ad742e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83edc878bc62dd15adedb843a231f657257baa90509166b729e8665157592cd7`

```dockerfile
```

-	Layers:
	-	`sha256:60f641b6e35d2698c4ef8617324030bdddce902f61a5ed2f117f633f27b92da8`  
		Last Modified: Fri, 17 Jan 2025 02:28:25 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5-dind-rootless`

```console
$ docker pull docker@sha256:a2eb1cdc0a6e73e7bb35ef6dcbae5eed1198b4bca80bdb43392e53fe8810dac2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.5-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:873e54eb4ecdc9f413abacfb497523561c23f3532678e2c7893393646e10a50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156159516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a995afc276d185bce60731d4ddc05950b70c859778a9280024a3322eccc42f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db0ef5f6406167c28a55dbfc0fbbd527a8e8ee10b1ed0053a74bb5847f467b`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 8.1 MB (8060096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2617d81eedcf635e1fd94dc905266de252ae0d642c05465bb5c57e7b9e5b0`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e4c1fa9475c483015ff35cb0ca5fae973e6192bd7d355b798024cc3f6436c`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18849459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af4884fbc706fb37435cc7859f05891c18eaec536721e17e5a97361694520c3`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18798866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851762183788567546d15646f8ce06871883255ad227fb13b88d2c2e58ef7fa4`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 19.3 MB (19303643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d84c454f28e907e0f1f5996d71027092830cabefb6c3f3a8d0d9fb3b332b9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ada9115c6a1e6e261a5250211382c99910811092b2791e7b32073c01bd5817`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06335ef68f056dd7837956156616452c5087a436b0ddbbc94fcb4493390d9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e423b3161e65b5d155f4fee197bb34b95aaaf9034e25661cc942130922d5553f`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 6.7 MB (6733536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8d12927cbc5b132f3d989c2f32cf8fe0e3d4f9136fc784f675b40aa6e2caa5`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 89.4 KB (89425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326df6d9eb79ca016d6f1723d5ca2bced72bd36fd014e852b493a43a6447c10e`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa7701ffbf173fdb6f7999d28b78600828e770ef8de8c26f6767ff8d3413253`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 58.4 MB (58383027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40544ceb254c83f9677202983636becd2547551930652c6928a91b62c6b26529`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13647f78c45bebb40dba9ffe52c4bce8371d4edda349c507012fe1300ff50732`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66dc758ea69526e85c86620347676a493debe5c819cb7693f6902867778933e`  
		Last Modified: Fri, 17 Jan 2025 03:10:06 GMT  
		Size: 986.6 KB (986590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a769f32782fd44a1e305c6cd1ded3edecb5694f58954d3cc7b391478329db7f`  
		Last Modified: Fri, 17 Jan 2025 03:10:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f44cdf5fe82b821bf859dd7dc946f6fc747355176a01766fcb0f5bf94b122b`  
		Last Modified: Fri, 17 Jan 2025 03:10:06 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3258dbd3a9e8b790797ba1dfba1986498142bdce2e5fe2d92401acf136c2e82`  
		Last Modified: Fri, 17 Jan 2025 03:10:06 GMT  
		Size: 21.3 MB (21303864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0b43ebf5168b463eec3f98a035bb526d262c7ea182a4512d55af1403efb938`  
		Last Modified: Fri, 17 Jan 2025 03:10:07 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9c775d2142f922fee9a01cd1a263b620904b5742c972910af90e7648c88d3568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5a4e42c5ba363bc8aef3cb74e50dab63c9734c25f86d36792612a546031595`

```dockerfile
```

-	Layers:
	-	`sha256:ecb34284584c52d63e44745705b82df95475a84099839e3c14388a6214ea5f01`  
		Last Modified: Fri, 17 Jan 2025 03:10:05 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:46448a2b08fe5a5504d5f1691183d0fc974fdcfa3b17884c071bc93726c19a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149829070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e0f743e506c55a8233123a5803840a26c7e9f78903b01aee2dd8554580f7ba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98031a3690358e9e338c7b900ff223767ca20fe8d3581d723971bb5d3e97df6e`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 8.1 MB (8074417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c05adf332c68788c150e330500d99375063fb5fccac4eca47664fef925fe6`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05df1af7190779d81ae1d2a2f6bab0f116cd0911eaf925ea3b7c88d84e4dca`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.8 MB (17795742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373537e5e27b254a2e83716ef135b83be0eaffa0fbb7dd7e588802f57c22952f`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.1 MB (17106465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8781806a16e281a8c480f7f429497d259f378f76366f5b8a2047861a9a0eb`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 17.6 MB (17649723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd429dc70fde0e965c93f4ea2aa21344379a0f8461e5e8fb3a260e92129bfbd7`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1709b08f9705b3f6af9978783f2fb732992ff039699fdbc0a842595dbcb3bf9`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d18f467488432eff104e17eebdd3b73776125d5155413e82a70fac1ad2d50de`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eb3998a0993954da71d972744c4ceafe57b9e96dcb75f4d7626277df3d4176`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 7.0 MB (6981841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b5a025a6a9bf0b06bba2fe135db13911e1dcf31474e69df77b00520bbd3191`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 97.8 KB (97784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0743b347437f8517c3560af97d8923ca391286f17acbe0558f46b28c8c8c4d2`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49595e55dbff2fe86a9c4da769bc6a7679b3da9c2279eed30873af6bb678e195`  
		Last Modified: Fri, 17 Jan 2025 02:28:29 GMT  
		Size: 54.0 MB (53952083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3849eac5f1cf6d7788301e473e712d6bf6d77e0e01c3829c96b4dec4acf623d8`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb83a6536a87f2c86efa17f506102254efe83bcb5e283b31a0db94d18505dde5`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3982d96f5df89ee494fa458304355e30ef199bf1f1eda6c8b3dd607ca23d13`  
		Last Modified: Fri, 17 Jan 2025 03:27:30 GMT  
		Size: 1.0 MB (1014204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2b21cd3eb15dce210b7517a6be34965beddec2dc6e9384736e6bb97cc71618`  
		Last Modified: Fri, 17 Jan 2025 03:27:30 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4956e53894609bd8273c577579d49372b1b3f24cd142be4357a8b0e4873b2f90`  
		Last Modified: Fri, 17 Jan 2025 03:27:30 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5cc90ddeee38314b0dceef56e97746323daddce4a63b1dcfa6183891f64d39`  
		Last Modified: Fri, 17 Jan 2025 03:27:47 GMT  
		Size: 23.2 MB (23155160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889d5be2190a9406c5b1b3356b8b527176fc46f76cb5d40192b120061af4949f`  
		Last Modified: Fri, 17 Jan 2025 03:27:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:60876bd91d54cb65a601c27c85c7d8eda74c6a2f025325d12829c4f0173616a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7259e4a52601951b094f318099af2a7f82d03f417f9a37fe03194189522e619f`

```dockerfile
```

-	Layers:
	-	`sha256:1b563391abe23859090df83bb0dd41ef65f19bc25be6210520c59171a5564c22`  
		Last Modified: Fri, 17 Jan 2025 03:27:28 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5-windowsservercore`

```console
$ docker pull docker@sha256:147774e53a5cba9011ba41fc0a6031a0fe2a38be3ea00ada24c7c986bfe3e895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `docker:27.5-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:1ddbeca1f26cfd027cd80d7c22a37038dc7a5b749a4cc162893d982e25611f9e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2321733461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa6fd542e3201d9417d1c00e4e8e4ea67053d989ef8279153b1c3c1a73390dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 17 Jan 2025 01:32:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 17 Jan 2025 01:32:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 17 Jan 2025 01:32:29 GMT
ENV DOCKER_VERSION=27.5.0
# Fri, 17 Jan 2025 01:32:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Fri, 17 Jan 2025 01:32:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:32:38 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Fri, 17 Jan 2025 01:32:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Fri, 17 Jan 2025 01:32:40 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Fri, 17 Jan 2025 01:32:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:32:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Fri, 17 Jan 2025 01:32:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Fri, 17 Jan 2025 01:32:49 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Fri, 17 Jan 2025 01:32:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a2b5f44002e9945660f33fac78eda870ab26d14af8237ced3f7d6eebafc482`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203a2deeff1a6f93e060d1f072f55c5e625f7a8ba0b5b650ea6a24ec493e906f`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 357.5 KB (357481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892a6f8fa8324bfeb4612f7a42f4557afd5e082b76d6eb091e0de676dc19d26b`  
		Last Modified: Fri, 17 Jan 2025 01:33:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c45ea49c7511c526fac9de55eb8d1ec854cf7c24e175e514d4f76d393a1492f`  
		Last Modified: Fri, 17 Jan 2025 01:33:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e5b7f87ce7df7acc0870faf1a629a49f3f3b7865260274227fe01eb5fbe059`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 19.2 MB (19163659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1792865d58e6d13c7f1f82e4bd2c626a933e6f6a35db76e7a561e7feea4d7313`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc28b08ea10f6f26ceaad44e423332916af104c6c64d5c832f500bc690e15bf`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3b113153c6bc3cc9533ce2cde3d40a1feae4f3c43de591454bc66cabd8b7d6`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab2a02883224978a44c53d67303e6399cfa8291fd4878a7d28d1b9f9c86e0fb`  
		Last Modified: Fri, 17 Jan 2025 01:33:03 GMT  
		Size: 19.6 MB (19646321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9674894f9e36062ebb2d60558e37eb1e25270606e64a963e2154eca16d22a1`  
		Last Modified: Fri, 17 Jan 2025 01:33:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6baac49af4fea3c6c40c4380c6c83141230ecf225b612fef2dcb0860d12bd3`  
		Last Modified: Fri, 17 Jan 2025 01:33:00 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6f04636f816d025e0fcb207436d479348f6902a7b726b00fc0b08c4c91da5`  
		Last Modified: Fri, 17 Jan 2025 01:33:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff25e05ad1368fb78eb59c79e73d3276e7d77771072037ec3e43ca5409067c78`  
		Last Modified: Fri, 17 Jan 2025 01:33:03 GMT  
		Size: 20.2 MB (20169201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.5-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:a4691c37ea78600875afbfe9b5f3193ad202961501db79accf2e4169f9b42021
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181529728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1056e0f7366117381694ae8dcdba87d790f109eb17c3d003ef5aef0219256f5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 17 Jan 2025 01:33:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 17 Jan 2025 01:34:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 17 Jan 2025 01:34:31 GMT
ENV DOCKER_VERSION=27.5.0
# Fri, 17 Jan 2025 01:34:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Fri, 17 Jan 2025 01:34:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:34:45 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Fri, 17 Jan 2025 01:34:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Fri, 17 Jan 2025 01:34:46 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Fri, 17 Jan 2025 01:34:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:34:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Fri, 17 Jan 2025 01:34:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Fri, 17 Jan 2025 01:34:58 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Fri, 17 Jan 2025 01:35:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e6274df071a7d5a5db2dfcfdd09b3e5619a6a91cdf7f97ab0e499ce20fbadc`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75379368627062a255445132b6e6f800fa70735daa6088bd9a26716f97d8c20`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 341.5 KB (341471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d991c76af457bbd0d51a6c717c7269b73a45c7241bb22f2ea0a2140d7e5df9b`  
		Last Modified: Fri, 17 Jan 2025 01:35:16 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499d890bbe543c9fa6a376c2cc02860b9d28c3ceb3333573c42123258c044874`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1c11b12baeb8dbd4b7d91eb54b5d14a02ae0cf432615ea004e1e19f8f39c1d`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 19.2 MB (19160387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3235fd67ddd40cdaef5899c144213bba7245b4307f2902f0aebdf497c8d724`  
		Last Modified: Fri, 17 Jan 2025 01:35:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b03c5d4a69994a8004df958ddad06c5afbcc59f276c99989342f8400bf8d7d3`  
		Last Modified: Fri, 17 Jan 2025 01:35:14 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604799b0a87e0da3e79003c6f7f3b8c0ee9f49d2a0fd3da26c55e2d59e5a56ce`  
		Last Modified: Fri, 17 Jan 2025 01:35:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35965d90f9d46033f9e870e8cd2fb5125759d0ab816adacb4c3977e8b124b395`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 19.6 MB (19638065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2795117faa51777ee5591503a846e643112eed007983483a0799b0aba498c98`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e460c490d0afd58b3f2e390983623e89cd4a1f9bafe9b32435fdb41e2c37e99`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54d5078572cf39f63c8f5cc06830bd0716dcc480240b5200491cf747e26c12a`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb52aa115ea25674a9b875dd187041c15e8bd3b155bf96774b70758ad0f61e4`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 20.2 MB (20165876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5-windowsservercore-1809`

```console
$ docker pull docker@sha256:3b3e4d8d1726d5fb5d874f245b2d80913ac5431e62e2beed2d21e7966bd16079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `docker:27.5-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:a4691c37ea78600875afbfe9b5f3193ad202961501db79accf2e4169f9b42021
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181529728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1056e0f7366117381694ae8dcdba87d790f109eb17c3d003ef5aef0219256f5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 17 Jan 2025 01:33:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 17 Jan 2025 01:34:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 17 Jan 2025 01:34:31 GMT
ENV DOCKER_VERSION=27.5.0
# Fri, 17 Jan 2025 01:34:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Fri, 17 Jan 2025 01:34:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:34:45 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Fri, 17 Jan 2025 01:34:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Fri, 17 Jan 2025 01:34:46 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Fri, 17 Jan 2025 01:34:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:34:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Fri, 17 Jan 2025 01:34:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Fri, 17 Jan 2025 01:34:58 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Fri, 17 Jan 2025 01:35:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e6274df071a7d5a5db2dfcfdd09b3e5619a6a91cdf7f97ab0e499ce20fbadc`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75379368627062a255445132b6e6f800fa70735daa6088bd9a26716f97d8c20`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 341.5 KB (341471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d991c76af457bbd0d51a6c717c7269b73a45c7241bb22f2ea0a2140d7e5df9b`  
		Last Modified: Fri, 17 Jan 2025 01:35:16 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499d890bbe543c9fa6a376c2cc02860b9d28c3ceb3333573c42123258c044874`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1c11b12baeb8dbd4b7d91eb54b5d14a02ae0cf432615ea004e1e19f8f39c1d`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 19.2 MB (19160387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3235fd67ddd40cdaef5899c144213bba7245b4307f2902f0aebdf497c8d724`  
		Last Modified: Fri, 17 Jan 2025 01:35:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b03c5d4a69994a8004df958ddad06c5afbcc59f276c99989342f8400bf8d7d3`  
		Last Modified: Fri, 17 Jan 2025 01:35:14 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604799b0a87e0da3e79003c6f7f3b8c0ee9f49d2a0fd3da26c55e2d59e5a56ce`  
		Last Modified: Fri, 17 Jan 2025 01:35:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35965d90f9d46033f9e870e8cd2fb5125759d0ab816adacb4c3977e8b124b395`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 19.6 MB (19638065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2795117faa51777ee5591503a846e643112eed007983483a0799b0aba498c98`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e460c490d0afd58b3f2e390983623e89cd4a1f9bafe9b32435fdb41e2c37e99`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54d5078572cf39f63c8f5cc06830bd0716dcc480240b5200491cf747e26c12a`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb52aa115ea25674a9b875dd187041c15e8bd3b155bf96774b70758ad0f61e4`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 20.2 MB (20165876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:3bde2a2a6f2192672461cfec2b8264a4927348c274db2b6495e18ce39d141cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `docker:27.5-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:1ddbeca1f26cfd027cd80d7c22a37038dc7a5b749a4cc162893d982e25611f9e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2321733461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa6fd542e3201d9417d1c00e4e8e4ea67053d989ef8279153b1c3c1a73390dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 17 Jan 2025 01:32:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 17 Jan 2025 01:32:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 17 Jan 2025 01:32:29 GMT
ENV DOCKER_VERSION=27.5.0
# Fri, 17 Jan 2025 01:32:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Fri, 17 Jan 2025 01:32:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:32:38 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Fri, 17 Jan 2025 01:32:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Fri, 17 Jan 2025 01:32:40 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Fri, 17 Jan 2025 01:32:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:32:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Fri, 17 Jan 2025 01:32:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Fri, 17 Jan 2025 01:32:49 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Fri, 17 Jan 2025 01:32:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a2b5f44002e9945660f33fac78eda870ab26d14af8237ced3f7d6eebafc482`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203a2deeff1a6f93e060d1f072f55c5e625f7a8ba0b5b650ea6a24ec493e906f`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 357.5 KB (357481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892a6f8fa8324bfeb4612f7a42f4557afd5e082b76d6eb091e0de676dc19d26b`  
		Last Modified: Fri, 17 Jan 2025 01:33:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c45ea49c7511c526fac9de55eb8d1ec854cf7c24e175e514d4f76d393a1492f`  
		Last Modified: Fri, 17 Jan 2025 01:33:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e5b7f87ce7df7acc0870faf1a629a49f3f3b7865260274227fe01eb5fbe059`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 19.2 MB (19163659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1792865d58e6d13c7f1f82e4bd2c626a933e6f6a35db76e7a561e7feea4d7313`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc28b08ea10f6f26ceaad44e423332916af104c6c64d5c832f500bc690e15bf`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3b113153c6bc3cc9533ce2cde3d40a1feae4f3c43de591454bc66cabd8b7d6`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab2a02883224978a44c53d67303e6399cfa8291fd4878a7d28d1b9f9c86e0fb`  
		Last Modified: Fri, 17 Jan 2025 01:33:03 GMT  
		Size: 19.6 MB (19646321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9674894f9e36062ebb2d60558e37eb1e25270606e64a963e2154eca16d22a1`  
		Last Modified: Fri, 17 Jan 2025 01:33:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6baac49af4fea3c6c40c4380c6c83141230ecf225b612fef2dcb0860d12bd3`  
		Last Modified: Fri, 17 Jan 2025 01:33:00 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6f04636f816d025e0fcb207436d479348f6902a7b726b00fc0b08c4c91da5`  
		Last Modified: Fri, 17 Jan 2025 01:33:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff25e05ad1368fb78eb59c79e73d3276e7d77771072037ec3e43ca5409067c78`  
		Last Modified: Fri, 17 Jan 2025 01:33:03 GMT  
		Size: 20.2 MB (20169201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5.0`

```console
$ docker pull docker@sha256:45b80efde6892498e1160c3be8eb7cc67732863caac98d2a79af24398ff1c106
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

### `docker:27.5.0` - linux; amd64

```console
$ docker pull docker@sha256:328fee4531eccdcfe52b61ba73c849a649cacad29fba1a4129c95b40e0f2196c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133867713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b300b8cdc5f2ac4f108ecdd418f3ea30e35b4ee1018ff818ca39dd3f0bc7aadd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db0ef5f6406167c28a55dbfc0fbbd527a8e8ee10b1ed0053a74bb5847f467b`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 8.1 MB (8060096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2617d81eedcf635e1fd94dc905266de252ae0d642c05465bb5c57e7b9e5b0`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e4c1fa9475c483015ff35cb0ca5fae973e6192bd7d355b798024cc3f6436c`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18849459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af4884fbc706fb37435cc7859f05891c18eaec536721e17e5a97361694520c3`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18798866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851762183788567546d15646f8ce06871883255ad227fb13b88d2c2e58ef7fa4`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 19.3 MB (19303643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d84c454f28e907e0f1f5996d71027092830cabefb6c3f3a8d0d9fb3b332b9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ada9115c6a1e6e261a5250211382c99910811092b2791e7b32073c01bd5817`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06335ef68f056dd7837956156616452c5087a436b0ddbbc94fcb4493390d9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e423b3161e65b5d155f4fee197bb34b95aaaf9034e25661cc942130922d5553f`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 6.7 MB (6733536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8d12927cbc5b132f3d989c2f32cf8fe0e3d4f9136fc784f675b40aa6e2caa5`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 89.4 KB (89425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326df6d9eb79ca016d6f1723d5ca2bced72bd36fd014e852b493a43a6447c10e`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa7701ffbf173fdb6f7999d28b78600828e770ef8de8c26f6767ff8d3413253`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 58.4 MB (58383027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40544ceb254c83f9677202983636becd2547551930652c6928a91b62c6b26529`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13647f78c45bebb40dba9ffe52c4bce8371d4edda349c507012fe1300ff50732`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0` - unknown; unknown

```console
$ docker pull docker@sha256:683d1639ff61791a2eae0ec63a422d289dc4e28394eb8e39ccf17b56e1737122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556810057e6ba7d14c45298e2761fef6923333526367bb7e64510b0649dd514e`

```dockerfile
```

-	Layers:
	-	`sha256:18fa62c94f21565d5f5d2b2d15c416dce24b5ac429609729db340cc622a08d00`  
		Last Modified: Fri, 17 Jan 2025 02:09:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0` - linux; arm variant v6

```console
$ docker pull docker@sha256:872158a8fc908710ac79c7d0c61287953a6593ef365f7593fbc9ee6d449ca9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124949669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bbc03711f0e14a6963ddb7043e52c2f66782fc50b0319107b2712a9107fc28`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
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
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea778430c11317962e3aa40444717aa8dc546fc65595ea9fd6e73d36310902f`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 17.4 MB (17448787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea230caf38f20e83e44f4dc9f84ff4fb52580e6d973dd8ecd2952cd36ad2a21`  
		Last Modified: Fri, 17 Jan 2025 01:27:49 GMT  
		Size: 18.1 MB (18112354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97006a84267c6bca594ceb4a5bf26d607f5bdef93912e07f6e846be4422b1c`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e59e6b008d5c5752b4a7993bd0b52b1db7dc2dfa774314f4f775cc22afa320`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89fe821a62ed4869930b04fc18ac60cf2bda17c09431466d8459ccc0c3549e2`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fe55d9784a2a762c0d6ed72664929cdf9284a3a888e3089d5e9220628c6b45`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 7.0 MB (7041413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d364c50ad8b6c6c862e3e6daa1c4cf0a6e8c8433c8a71cffd144f766f0e4fb23`  
		Last Modified: Fri, 17 Jan 2025 02:11:06 GMT  
		Size: 89.1 KB (89085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0620df6bfe0a1bc90f013a4bb494501716e787d271b7bc5969ecbc24b43756`  
		Last Modified: Fri, 17 Jan 2025 02:11:06 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bd936df8e147b648aa1a39d212c1624e064452a47059063133cd6adf29f7c7`  
		Last Modified: Fri, 17 Jan 2025 02:11:08 GMT  
		Size: 54.0 MB (54047054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966301da011cd0c70e74a358f99db4b9f43762dd18ed38f53665e9a24e880c4b`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b29247ae6bfe40191a231dba9717f4ca4bf21ec2c13c3606f0ace4b34eb7c43`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 3.3 KB (3267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0` - unknown; unknown

```console
$ docker pull docker@sha256:dd0a36256908be42678ad2890166b0e84a6246797662f2b93f3cd6f24ab68906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9af519ad2f15c502e5c17cfd4e3767beadd551d1851f350066b158eb41c6913`

```dockerfile
```

-	Layers:
	-	`sha256:ce130b032bac1fce394cc92324e72573e50caf69fdb9c099daad2c98bd8d9a1d`  
		Last Modified: Fri, 17 Jan 2025 02:11:05 GMT  
		Size: 34.8 KB (34764 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0` - linux; arm variant v7

```console
$ docker pull docker@sha256:29597558c26c7e456f9d4350b94f208a69114260adc21bdae0619f9a7749c34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64123e8eceb16c151befc29738868d17cd6b828c82a96cc2b46a182f62e48eab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
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
	-	`sha256:1d1f394b9e9ceefe286b141a6fce91d86072ca709baf5dc4447f3d5a6db9a163`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 17.4 MB (17427588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755932338966055de46ecbdb4e46288f1f52af30c0f57960411eed7bcbc876d0`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 18.1 MB (18099438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215cf40534564c9b7b71ea6e20aa6912ca15008a9c2dd68162c3efe4fc20e65b`  
		Last Modified: Fri, 17 Jan 2025 01:28:02 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb652a32cd1bd43600fe45d89a2455ab0b882887bfabe0664dc9eb749e932a1`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe784566335013d539f74a4e2e151368fe7ddd75a3583e15b1cbafc6eca14a`  
		Last Modified: Fri, 17 Jan 2025 01:28:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cd34d15034bf9fbabde6b6c4ec8bbfe56b0ee1dad07a86eef7f6d83a4829e5`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 6.4 MB (6367554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049bb15c92b4ba59ad113b753dc6305190eb3111a77ec5b86b8ca81c7dbc59f2`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 85.2 KB (85236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefdea776978b937e65e37c006d81238b97221fac666606609e7569cc915f005`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8ab79af5c8f7891f9b4d14518c40aae4efd8acb30339e416de829cf962a8ae`  
		Last Modified: Fri, 17 Jan 2025 02:25:24 GMT  
		Size: 54.0 MB (54047069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4015624859fadb74f8744fab8fe858c4a95b1d5fde6a26c00f709c761fb7908`  
		Last Modified: Fri, 17 Jan 2025 02:25:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935f17568aab4f3b97b7a27a57821ab17388667d24fa04ed2ac2b295bc4217bf`  
		Last Modified: Fri, 17 Jan 2025 02:25:23 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0` - unknown; unknown

```console
$ docker pull docker@sha256:8fb08780d366a366517f413dc5e7ef73a7f5209ce4924d234dfb98829cba86d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7820bc0b8d0f7ee1b9d6587b10f5355904f51e675ddd0a337e25edb87b5578`

```dockerfile
```

-	Layers:
	-	`sha256:0857811d7117af260dff536135d5b9462e12a604d988f0bbcfa5c98ac94002c1`  
		Last Modified: Fri, 17 Jan 2025 02:25:20 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:be6a2bf3869c0b2ce79cbea0de54fc0151be9915cb61572b8fee8ae231380fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125658359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98a7305162cf56e40d783f72a96aafbe29862ec4cf094baab60b961b874e8a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98031a3690358e9e338c7b900ff223767ca20fe8d3581d723971bb5d3e97df6e`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 8.1 MB (8074417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c05adf332c68788c150e330500d99375063fb5fccac4eca47664fef925fe6`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05df1af7190779d81ae1d2a2f6bab0f116cd0911eaf925ea3b7c88d84e4dca`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.8 MB (17795742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373537e5e27b254a2e83716ef135b83be0eaffa0fbb7dd7e588802f57c22952f`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.1 MB (17106465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8781806a16e281a8c480f7f429497d259f378f76366f5b8a2047861a9a0eb`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 17.6 MB (17649723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd429dc70fde0e965c93f4ea2aa21344379a0f8461e5e8fb3a260e92129bfbd7`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1709b08f9705b3f6af9978783f2fb732992ff039699fdbc0a842595dbcb3bf9`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d18f467488432eff104e17eebdd3b73776125d5155413e82a70fac1ad2d50de`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eb3998a0993954da71d972744c4ceafe57b9e96dcb75f4d7626277df3d4176`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 7.0 MB (6981841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b5a025a6a9bf0b06bba2fe135db13911e1dcf31474e69df77b00520bbd3191`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 97.8 KB (97784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0743b347437f8517c3560af97d8923ca391286f17acbe0558f46b28c8c8c4d2`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49595e55dbff2fe86a9c4da769bc6a7679b3da9c2279eed30873af6bb678e195`  
		Last Modified: Fri, 17 Jan 2025 02:28:29 GMT  
		Size: 54.0 MB (53952083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3849eac5f1cf6d7788301e473e712d6bf6d77e0e01c3829c96b4dec4acf623d8`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb83a6536a87f2c86efa17f506102254efe83bcb5e283b31a0db94d18505dde5`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0` - unknown; unknown

```console
$ docker pull docker@sha256:66c420a8f09f46b8c9153ce490d112d23b47a11ae227e02b316ba27641ad742e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83edc878bc62dd15adedb843a231f657257baa90509166b729e8665157592cd7`

```dockerfile
```

-	Layers:
	-	`sha256:60f641b6e35d2698c4ef8617324030bdddce902f61a5ed2f117f633f27b92da8`  
		Last Modified: Fri, 17 Jan 2025 02:28:25 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5.0-alpine3.21`

```console
$ docker pull docker@sha256:45b80efde6892498e1160c3be8eb7cc67732863caac98d2a79af24398ff1c106
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

### `docker:27.5.0-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:328fee4531eccdcfe52b61ba73c849a649cacad29fba1a4129c95b40e0f2196c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133867713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b300b8cdc5f2ac4f108ecdd418f3ea30e35b4ee1018ff818ca39dd3f0bc7aadd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db0ef5f6406167c28a55dbfc0fbbd527a8e8ee10b1ed0053a74bb5847f467b`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 8.1 MB (8060096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2617d81eedcf635e1fd94dc905266de252ae0d642c05465bb5c57e7b9e5b0`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e4c1fa9475c483015ff35cb0ca5fae973e6192bd7d355b798024cc3f6436c`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18849459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af4884fbc706fb37435cc7859f05891c18eaec536721e17e5a97361694520c3`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18798866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851762183788567546d15646f8ce06871883255ad227fb13b88d2c2e58ef7fa4`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 19.3 MB (19303643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d84c454f28e907e0f1f5996d71027092830cabefb6c3f3a8d0d9fb3b332b9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ada9115c6a1e6e261a5250211382c99910811092b2791e7b32073c01bd5817`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06335ef68f056dd7837956156616452c5087a436b0ddbbc94fcb4493390d9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e423b3161e65b5d155f4fee197bb34b95aaaf9034e25661cc942130922d5553f`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 6.7 MB (6733536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8d12927cbc5b132f3d989c2f32cf8fe0e3d4f9136fc784f675b40aa6e2caa5`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 89.4 KB (89425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326df6d9eb79ca016d6f1723d5ca2bced72bd36fd014e852b493a43a6447c10e`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa7701ffbf173fdb6f7999d28b78600828e770ef8de8c26f6767ff8d3413253`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 58.4 MB (58383027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40544ceb254c83f9677202983636becd2547551930652c6928a91b62c6b26529`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13647f78c45bebb40dba9ffe52c4bce8371d4edda349c507012fe1300ff50732`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:683d1639ff61791a2eae0ec63a422d289dc4e28394eb8e39ccf17b56e1737122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556810057e6ba7d14c45298e2761fef6923333526367bb7e64510b0649dd514e`

```dockerfile
```

-	Layers:
	-	`sha256:18fa62c94f21565d5f5d2b2d15c416dce24b5ac429609729db340cc622a08d00`  
		Last Modified: Fri, 17 Jan 2025 02:09:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:872158a8fc908710ac79c7d0c61287953a6593ef365f7593fbc9ee6d449ca9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124949669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bbc03711f0e14a6963ddb7043e52c2f66782fc50b0319107b2712a9107fc28`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
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
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea778430c11317962e3aa40444717aa8dc546fc65595ea9fd6e73d36310902f`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 17.4 MB (17448787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea230caf38f20e83e44f4dc9f84ff4fb52580e6d973dd8ecd2952cd36ad2a21`  
		Last Modified: Fri, 17 Jan 2025 01:27:49 GMT  
		Size: 18.1 MB (18112354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97006a84267c6bca594ceb4a5bf26d607f5bdef93912e07f6e846be4422b1c`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e59e6b008d5c5752b4a7993bd0b52b1db7dc2dfa774314f4f775cc22afa320`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89fe821a62ed4869930b04fc18ac60cf2bda17c09431466d8459ccc0c3549e2`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fe55d9784a2a762c0d6ed72664929cdf9284a3a888e3089d5e9220628c6b45`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 7.0 MB (7041413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d364c50ad8b6c6c862e3e6daa1c4cf0a6e8c8433c8a71cffd144f766f0e4fb23`  
		Last Modified: Fri, 17 Jan 2025 02:11:06 GMT  
		Size: 89.1 KB (89085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0620df6bfe0a1bc90f013a4bb494501716e787d271b7bc5969ecbc24b43756`  
		Last Modified: Fri, 17 Jan 2025 02:11:06 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bd936df8e147b648aa1a39d212c1624e064452a47059063133cd6adf29f7c7`  
		Last Modified: Fri, 17 Jan 2025 02:11:08 GMT  
		Size: 54.0 MB (54047054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966301da011cd0c70e74a358f99db4b9f43762dd18ed38f53665e9a24e880c4b`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b29247ae6bfe40191a231dba9717f4ca4bf21ec2c13c3606f0ace4b34eb7c43`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 3.3 KB (3267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:dd0a36256908be42678ad2890166b0e84a6246797662f2b93f3cd6f24ab68906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9af519ad2f15c502e5c17cfd4e3767beadd551d1851f350066b158eb41c6913`

```dockerfile
```

-	Layers:
	-	`sha256:ce130b032bac1fce394cc92324e72573e50caf69fdb9c099daad2c98bd8d9a1d`  
		Last Modified: Fri, 17 Jan 2025 02:11:05 GMT  
		Size: 34.8 KB (34764 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:29597558c26c7e456f9d4350b94f208a69114260adc21bdae0619f9a7749c34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64123e8eceb16c151befc29738868d17cd6b828c82a96cc2b46a182f62e48eab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
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
	-	`sha256:1d1f394b9e9ceefe286b141a6fce91d86072ca709baf5dc4447f3d5a6db9a163`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 17.4 MB (17427588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755932338966055de46ecbdb4e46288f1f52af30c0f57960411eed7bcbc876d0`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 18.1 MB (18099438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215cf40534564c9b7b71ea6e20aa6912ca15008a9c2dd68162c3efe4fc20e65b`  
		Last Modified: Fri, 17 Jan 2025 01:28:02 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb652a32cd1bd43600fe45d89a2455ab0b882887bfabe0664dc9eb749e932a1`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe784566335013d539f74a4e2e151368fe7ddd75a3583e15b1cbafc6eca14a`  
		Last Modified: Fri, 17 Jan 2025 01:28:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cd34d15034bf9fbabde6b6c4ec8bbfe56b0ee1dad07a86eef7f6d83a4829e5`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 6.4 MB (6367554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049bb15c92b4ba59ad113b753dc6305190eb3111a77ec5b86b8ca81c7dbc59f2`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 85.2 KB (85236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefdea776978b937e65e37c006d81238b97221fac666606609e7569cc915f005`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8ab79af5c8f7891f9b4d14518c40aae4efd8acb30339e416de829cf962a8ae`  
		Last Modified: Fri, 17 Jan 2025 02:25:24 GMT  
		Size: 54.0 MB (54047069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4015624859fadb74f8744fab8fe858c4a95b1d5fde6a26c00f709c761fb7908`  
		Last Modified: Fri, 17 Jan 2025 02:25:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935f17568aab4f3b97b7a27a57821ab17388667d24fa04ed2ac2b295bc4217bf`  
		Last Modified: Fri, 17 Jan 2025 02:25:23 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:8fb08780d366a366517f413dc5e7ef73a7f5209ce4924d234dfb98829cba86d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7820bc0b8d0f7ee1b9d6587b10f5355904f51e675ddd0a337e25edb87b5578`

```dockerfile
```

-	Layers:
	-	`sha256:0857811d7117af260dff536135d5b9462e12a604d988f0bbcfa5c98ac94002c1`  
		Last Modified: Fri, 17 Jan 2025 02:25:20 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:be6a2bf3869c0b2ce79cbea0de54fc0151be9915cb61572b8fee8ae231380fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125658359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98a7305162cf56e40d783f72a96aafbe29862ec4cf094baab60b961b874e8a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98031a3690358e9e338c7b900ff223767ca20fe8d3581d723971bb5d3e97df6e`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 8.1 MB (8074417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c05adf332c68788c150e330500d99375063fb5fccac4eca47664fef925fe6`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05df1af7190779d81ae1d2a2f6bab0f116cd0911eaf925ea3b7c88d84e4dca`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.8 MB (17795742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373537e5e27b254a2e83716ef135b83be0eaffa0fbb7dd7e588802f57c22952f`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.1 MB (17106465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8781806a16e281a8c480f7f429497d259f378f76366f5b8a2047861a9a0eb`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 17.6 MB (17649723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd429dc70fde0e965c93f4ea2aa21344379a0f8461e5e8fb3a260e92129bfbd7`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1709b08f9705b3f6af9978783f2fb732992ff039699fdbc0a842595dbcb3bf9`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d18f467488432eff104e17eebdd3b73776125d5155413e82a70fac1ad2d50de`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eb3998a0993954da71d972744c4ceafe57b9e96dcb75f4d7626277df3d4176`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 7.0 MB (6981841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b5a025a6a9bf0b06bba2fe135db13911e1dcf31474e69df77b00520bbd3191`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 97.8 KB (97784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0743b347437f8517c3560af97d8923ca391286f17acbe0558f46b28c8c8c4d2`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49595e55dbff2fe86a9c4da769bc6a7679b3da9c2279eed30873af6bb678e195`  
		Last Modified: Fri, 17 Jan 2025 02:28:29 GMT  
		Size: 54.0 MB (53952083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3849eac5f1cf6d7788301e473e712d6bf6d77e0e01c3829c96b4dec4acf623d8`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb83a6536a87f2c86efa17f506102254efe83bcb5e283b31a0db94d18505dde5`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:66c420a8f09f46b8c9153ce490d112d23b47a11ae227e02b316ba27641ad742e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83edc878bc62dd15adedb843a231f657257baa90509166b729e8665157592cd7`

```dockerfile
```

-	Layers:
	-	`sha256:60f641b6e35d2698c4ef8617324030bdddce902f61a5ed2f117f633f27b92da8`  
		Last Modified: Fri, 17 Jan 2025 02:28:25 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5.0-cli`

```console
$ docker pull docker@sha256:7c10b867b5da6f0ecbac463defeaa490c1d2816cb02fe4e14d2994ad9c3812cd
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

### `docker:27.5.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:b219ac7db8149403917bdea481b4e8bdc9e48c492e12d6aa2b0ad8e11b323316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68655933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cc102d4a93a8704667364b5cfb93d9dcc26a6a861645223f2d4893b3ed723a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.0
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db0ef5f6406167c28a55dbfc0fbbd527a8e8ee10b1ed0053a74bb5847f467b`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 8.1 MB (8060096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2617d81eedcf635e1fd94dc905266de252ae0d642c05465bb5c57e7b9e5b0`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e4c1fa9475c483015ff35cb0ca5fae973e6192bd7d355b798024cc3f6436c`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18849459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af4884fbc706fb37435cc7859f05891c18eaec536721e17e5a97361694520c3`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18798866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851762183788567546d15646f8ce06871883255ad227fb13b88d2c2e58ef7fa4`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 19.3 MB (19303643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d84c454f28e907e0f1f5996d71027092830cabefb6c3f3a8d0d9fb3b332b9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ada9115c6a1e6e261a5250211382c99910811092b2791e7b32073c01bd5817`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06335ef68f056dd7837956156616452c5087a436b0ddbbc94fcb4493390d9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:bfcde7282475bfa1b52d54c2ccea12401ee915b605e1d578a5081bb4a69627bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8044174370b4166bc88d8f825313d5221505fa7b2ba129e316bb4e292d4a93d8`

```dockerfile
```

-	Layers:
	-	`sha256:f5e0658d18f9353954b3b81fc16fe0b3e32f0e667af202b4f413c79dce6a3b96`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:f52fb18fdfc78a4af51b84ac7d2b5fca13b8e3e09b1067aa849e9f04030c2c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63766314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74e5406e29303780211a38cb58677a0c6a96a6aa5ce396f86ae128d852cc85d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.0
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
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
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea778430c11317962e3aa40444717aa8dc546fc65595ea9fd6e73d36310902f`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 17.4 MB (17448787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea230caf38f20e83e44f4dc9f84ff4fb52580e6d973dd8ecd2952cd36ad2a21`  
		Last Modified: Fri, 17 Jan 2025 01:27:49 GMT  
		Size: 18.1 MB (18112354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97006a84267c6bca594ceb4a5bf26d607f5bdef93912e07f6e846be4422b1c`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e59e6b008d5c5752b4a7993bd0b52b1db7dc2dfa774314f4f775cc22afa320`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89fe821a62ed4869930b04fc18ac60cf2bda17c09431466d8459ccc0c3549e2`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:dce530002422cd3b77135d6ae618300706585d7d6deebc956b7425231442feeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c540c5273aba065d46aa7fa9ca86bfb8aa222597b3283936e19bbdef868628f6`

```dockerfile
```

-	Layers:
	-	`sha256:532ebdac6902ef2db952873eeeaf73c981703befe573cd7cbe0eaacd64aa031f`  
		Last Modified: Fri, 17 Jan 2025 01:27:47 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:9e993e3871a714198e4b947664c5f228a5d7982b3515670942d8a495f03485eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62776105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde14708064af6f21da2b23403c4e90218556fb6cf1508302904ef370691f99c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.0
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
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
	-	`sha256:1d1f394b9e9ceefe286b141a6fce91d86072ca709baf5dc4447f3d5a6db9a163`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 17.4 MB (17427588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755932338966055de46ecbdb4e46288f1f52af30c0f57960411eed7bcbc876d0`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 18.1 MB (18099438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215cf40534564c9b7b71ea6e20aa6912ca15008a9c2dd68162c3efe4fc20e65b`  
		Last Modified: Fri, 17 Jan 2025 01:28:02 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb652a32cd1bd43600fe45d89a2455ab0b882887bfabe0664dc9eb749e932a1`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe784566335013d539f74a4e2e151368fe7ddd75a3583e15b1cbafc6eca14a`  
		Last Modified: Fri, 17 Jan 2025 01:28:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:dfca36c13fd1337794df037f0fc30b729677e432669884ebcb2f92429c838457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4905f7d813489e8a4204010015fb7509e3c94934b1b88e1418f21f37a337a6f`

```dockerfile
```

-	Layers:
	-	`sha256:89c06eb5c6c66dfe6a2640b9ccf35cdc3ab8ca4ac9883f9fb2b69b8aba4d80e3`  
		Last Modified: Fri, 17 Jan 2025 01:28:01 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a121337c9287fdc11e04a8a12708f639e8c3ba427945f4539df65679aee3ee8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64620861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d961a7c95de71f4706af938b3c55efbe8f7379a1c212212251b71732ea4c5cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.0
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98031a3690358e9e338c7b900ff223767ca20fe8d3581d723971bb5d3e97df6e`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 8.1 MB (8074417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c05adf332c68788c150e330500d99375063fb5fccac4eca47664fef925fe6`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05df1af7190779d81ae1d2a2f6bab0f116cd0911eaf925ea3b7c88d84e4dca`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.8 MB (17795742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373537e5e27b254a2e83716ef135b83be0eaffa0fbb7dd7e588802f57c22952f`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.1 MB (17106465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8781806a16e281a8c480f7f429497d259f378f76366f5b8a2047861a9a0eb`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 17.6 MB (17649723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd429dc70fde0e965c93f4ea2aa21344379a0f8461e5e8fb3a260e92129bfbd7`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1709b08f9705b3f6af9978783f2fb732992ff039699fdbc0a842595dbcb3bf9`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d18f467488432eff104e17eebdd3b73776125d5155413e82a70fac1ad2d50de`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1d010e0b0f4fa82a5b3ba475d15bffbaf6b9481a3a2c85a608aa6f1be93f4160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a79ec7a8c697907793b7bd322196ef33a33e0ae9eb4ea0f46752d9aa591878`

```dockerfile
```

-	Layers:
	-	`sha256:1ce07430fc5561a2375bb4a6167743bb1bef6046817bf347a9a3f3373a4cfc4b`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5.0-cli-alpine3.21`

```console
$ docker pull docker@sha256:7c10b867b5da6f0ecbac463defeaa490c1d2816cb02fe4e14d2994ad9c3812cd
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

### `docker:27.5.0-cli-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:b219ac7db8149403917bdea481b4e8bdc9e48c492e12d6aa2b0ad8e11b323316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68655933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cc102d4a93a8704667364b5cfb93d9dcc26a6a861645223f2d4893b3ed723a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.0
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db0ef5f6406167c28a55dbfc0fbbd527a8e8ee10b1ed0053a74bb5847f467b`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 8.1 MB (8060096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2617d81eedcf635e1fd94dc905266de252ae0d642c05465bb5c57e7b9e5b0`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e4c1fa9475c483015ff35cb0ca5fae973e6192bd7d355b798024cc3f6436c`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18849459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af4884fbc706fb37435cc7859f05891c18eaec536721e17e5a97361694520c3`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18798866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851762183788567546d15646f8ce06871883255ad227fb13b88d2c2e58ef7fa4`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 19.3 MB (19303643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d84c454f28e907e0f1f5996d71027092830cabefb6c3f3a8d0d9fb3b332b9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ada9115c6a1e6e261a5250211382c99910811092b2791e7b32073c01bd5817`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06335ef68f056dd7837956156616452c5087a436b0ddbbc94fcb4493390d9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:bfcde7282475bfa1b52d54c2ccea12401ee915b605e1d578a5081bb4a69627bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8044174370b4166bc88d8f825313d5221505fa7b2ba129e316bb4e292d4a93d8`

```dockerfile
```

-	Layers:
	-	`sha256:f5e0658d18f9353954b3b81fc16fe0b3e32f0e667af202b4f413c79dce6a3b96`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-cli-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:f52fb18fdfc78a4af51b84ac7d2b5fca13b8e3e09b1067aa849e9f04030c2c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63766314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74e5406e29303780211a38cb58677a0c6a96a6aa5ce396f86ae128d852cc85d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.0
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
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
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea778430c11317962e3aa40444717aa8dc546fc65595ea9fd6e73d36310902f`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 17.4 MB (17448787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea230caf38f20e83e44f4dc9f84ff4fb52580e6d973dd8ecd2952cd36ad2a21`  
		Last Modified: Fri, 17 Jan 2025 01:27:49 GMT  
		Size: 18.1 MB (18112354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97006a84267c6bca594ceb4a5bf26d607f5bdef93912e07f6e846be4422b1c`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e59e6b008d5c5752b4a7993bd0b52b1db7dc2dfa774314f4f775cc22afa320`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89fe821a62ed4869930b04fc18ac60cf2bda17c09431466d8459ccc0c3549e2`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:dce530002422cd3b77135d6ae618300706585d7d6deebc956b7425231442feeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c540c5273aba065d46aa7fa9ca86bfb8aa222597b3283936e19bbdef868628f6`

```dockerfile
```

-	Layers:
	-	`sha256:532ebdac6902ef2db952873eeeaf73c981703befe573cd7cbe0eaacd64aa031f`  
		Last Modified: Fri, 17 Jan 2025 01:27:47 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-cli-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:9e993e3871a714198e4b947664c5f228a5d7982b3515670942d8a495f03485eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62776105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde14708064af6f21da2b23403c4e90218556fb6cf1508302904ef370691f99c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.0
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
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
	-	`sha256:1d1f394b9e9ceefe286b141a6fce91d86072ca709baf5dc4447f3d5a6db9a163`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 17.4 MB (17427588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755932338966055de46ecbdb4e46288f1f52af30c0f57960411eed7bcbc876d0`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 18.1 MB (18099438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215cf40534564c9b7b71ea6e20aa6912ca15008a9c2dd68162c3efe4fc20e65b`  
		Last Modified: Fri, 17 Jan 2025 01:28:02 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb652a32cd1bd43600fe45d89a2455ab0b882887bfabe0664dc9eb749e932a1`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe784566335013d539f74a4e2e151368fe7ddd75a3583e15b1cbafc6eca14a`  
		Last Modified: Fri, 17 Jan 2025 01:28:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:dfca36c13fd1337794df037f0fc30b729677e432669884ebcb2f92429c838457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4905f7d813489e8a4204010015fb7509e3c94934b1b88e1418f21f37a337a6f`

```dockerfile
```

-	Layers:
	-	`sha256:89c06eb5c6c66dfe6a2640b9ccf35cdc3ab8ca4ac9883f9fb2b69b8aba4d80e3`  
		Last Modified: Fri, 17 Jan 2025 01:28:01 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-cli-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a121337c9287fdc11e04a8a12708f639e8c3ba427945f4539df65679aee3ee8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64620861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d961a7c95de71f4706af938b3c55efbe8f7379a1c212212251b71732ea4c5cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.0
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98031a3690358e9e338c7b900ff223767ca20fe8d3581d723971bb5d3e97df6e`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 8.1 MB (8074417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c05adf332c68788c150e330500d99375063fb5fccac4eca47664fef925fe6`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05df1af7190779d81ae1d2a2f6bab0f116cd0911eaf925ea3b7c88d84e4dca`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.8 MB (17795742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373537e5e27b254a2e83716ef135b83be0eaffa0fbb7dd7e588802f57c22952f`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.1 MB (17106465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8781806a16e281a8c480f7f429497d259f378f76366f5b8a2047861a9a0eb`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 17.6 MB (17649723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd429dc70fde0e965c93f4ea2aa21344379a0f8461e5e8fb3a260e92129bfbd7`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1709b08f9705b3f6af9978783f2fb732992ff039699fdbc0a842595dbcb3bf9`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d18f467488432eff104e17eebdd3b73776125d5155413e82a70fac1ad2d50de`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:1d010e0b0f4fa82a5b3ba475d15bffbaf6b9481a3a2c85a608aa6f1be93f4160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a79ec7a8c697907793b7bd322196ef33a33e0ae9eb4ea0f46752d9aa591878`

```dockerfile
```

-	Layers:
	-	`sha256:1ce07430fc5561a2375bb4a6167743bb1bef6046817bf347a9a3f3373a4cfc4b`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5.0-dind`

```console
$ docker pull docker@sha256:45b80efde6892498e1160c3be8eb7cc67732863caac98d2a79af24398ff1c106
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

### `docker:27.5.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:328fee4531eccdcfe52b61ba73c849a649cacad29fba1a4129c95b40e0f2196c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133867713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b300b8cdc5f2ac4f108ecdd418f3ea30e35b4ee1018ff818ca39dd3f0bc7aadd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db0ef5f6406167c28a55dbfc0fbbd527a8e8ee10b1ed0053a74bb5847f467b`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 8.1 MB (8060096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2617d81eedcf635e1fd94dc905266de252ae0d642c05465bb5c57e7b9e5b0`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e4c1fa9475c483015ff35cb0ca5fae973e6192bd7d355b798024cc3f6436c`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18849459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af4884fbc706fb37435cc7859f05891c18eaec536721e17e5a97361694520c3`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18798866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851762183788567546d15646f8ce06871883255ad227fb13b88d2c2e58ef7fa4`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 19.3 MB (19303643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d84c454f28e907e0f1f5996d71027092830cabefb6c3f3a8d0d9fb3b332b9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ada9115c6a1e6e261a5250211382c99910811092b2791e7b32073c01bd5817`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06335ef68f056dd7837956156616452c5087a436b0ddbbc94fcb4493390d9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e423b3161e65b5d155f4fee197bb34b95aaaf9034e25661cc942130922d5553f`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 6.7 MB (6733536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8d12927cbc5b132f3d989c2f32cf8fe0e3d4f9136fc784f675b40aa6e2caa5`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 89.4 KB (89425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326df6d9eb79ca016d6f1723d5ca2bced72bd36fd014e852b493a43a6447c10e`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa7701ffbf173fdb6f7999d28b78600828e770ef8de8c26f6767ff8d3413253`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 58.4 MB (58383027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40544ceb254c83f9677202983636becd2547551930652c6928a91b62c6b26529`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13647f78c45bebb40dba9ffe52c4bce8371d4edda349c507012fe1300ff50732`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:683d1639ff61791a2eae0ec63a422d289dc4e28394eb8e39ccf17b56e1737122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556810057e6ba7d14c45298e2761fef6923333526367bb7e64510b0649dd514e`

```dockerfile
```

-	Layers:
	-	`sha256:18fa62c94f21565d5f5d2b2d15c416dce24b5ac429609729db340cc622a08d00`  
		Last Modified: Fri, 17 Jan 2025 02:09:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:872158a8fc908710ac79c7d0c61287953a6593ef365f7593fbc9ee6d449ca9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124949669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bbc03711f0e14a6963ddb7043e52c2f66782fc50b0319107b2712a9107fc28`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
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
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea778430c11317962e3aa40444717aa8dc546fc65595ea9fd6e73d36310902f`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 17.4 MB (17448787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea230caf38f20e83e44f4dc9f84ff4fb52580e6d973dd8ecd2952cd36ad2a21`  
		Last Modified: Fri, 17 Jan 2025 01:27:49 GMT  
		Size: 18.1 MB (18112354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97006a84267c6bca594ceb4a5bf26d607f5bdef93912e07f6e846be4422b1c`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e59e6b008d5c5752b4a7993bd0b52b1db7dc2dfa774314f4f775cc22afa320`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89fe821a62ed4869930b04fc18ac60cf2bda17c09431466d8459ccc0c3549e2`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fe55d9784a2a762c0d6ed72664929cdf9284a3a888e3089d5e9220628c6b45`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 7.0 MB (7041413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d364c50ad8b6c6c862e3e6daa1c4cf0a6e8c8433c8a71cffd144f766f0e4fb23`  
		Last Modified: Fri, 17 Jan 2025 02:11:06 GMT  
		Size: 89.1 KB (89085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0620df6bfe0a1bc90f013a4bb494501716e787d271b7bc5969ecbc24b43756`  
		Last Modified: Fri, 17 Jan 2025 02:11:06 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bd936df8e147b648aa1a39d212c1624e064452a47059063133cd6adf29f7c7`  
		Last Modified: Fri, 17 Jan 2025 02:11:08 GMT  
		Size: 54.0 MB (54047054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966301da011cd0c70e74a358f99db4b9f43762dd18ed38f53665e9a24e880c4b`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b29247ae6bfe40191a231dba9717f4ca4bf21ec2c13c3606f0ace4b34eb7c43`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 3.3 KB (3267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:dd0a36256908be42678ad2890166b0e84a6246797662f2b93f3cd6f24ab68906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9af519ad2f15c502e5c17cfd4e3767beadd551d1851f350066b158eb41c6913`

```dockerfile
```

-	Layers:
	-	`sha256:ce130b032bac1fce394cc92324e72573e50caf69fdb9c099daad2c98bd8d9a1d`  
		Last Modified: Fri, 17 Jan 2025 02:11:05 GMT  
		Size: 34.8 KB (34764 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:29597558c26c7e456f9d4350b94f208a69114260adc21bdae0619f9a7749c34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64123e8eceb16c151befc29738868d17cd6b828c82a96cc2b46a182f62e48eab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
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
	-	`sha256:1d1f394b9e9ceefe286b141a6fce91d86072ca709baf5dc4447f3d5a6db9a163`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 17.4 MB (17427588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755932338966055de46ecbdb4e46288f1f52af30c0f57960411eed7bcbc876d0`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 18.1 MB (18099438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215cf40534564c9b7b71ea6e20aa6912ca15008a9c2dd68162c3efe4fc20e65b`  
		Last Modified: Fri, 17 Jan 2025 01:28:02 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb652a32cd1bd43600fe45d89a2455ab0b882887bfabe0664dc9eb749e932a1`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe784566335013d539f74a4e2e151368fe7ddd75a3583e15b1cbafc6eca14a`  
		Last Modified: Fri, 17 Jan 2025 01:28:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cd34d15034bf9fbabde6b6c4ec8bbfe56b0ee1dad07a86eef7f6d83a4829e5`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 6.4 MB (6367554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049bb15c92b4ba59ad113b753dc6305190eb3111a77ec5b86b8ca81c7dbc59f2`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 85.2 KB (85236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefdea776978b937e65e37c006d81238b97221fac666606609e7569cc915f005`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8ab79af5c8f7891f9b4d14518c40aae4efd8acb30339e416de829cf962a8ae`  
		Last Modified: Fri, 17 Jan 2025 02:25:24 GMT  
		Size: 54.0 MB (54047069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4015624859fadb74f8744fab8fe858c4a95b1d5fde6a26c00f709c761fb7908`  
		Last Modified: Fri, 17 Jan 2025 02:25:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935f17568aab4f3b97b7a27a57821ab17388667d24fa04ed2ac2b295bc4217bf`  
		Last Modified: Fri, 17 Jan 2025 02:25:23 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8fb08780d366a366517f413dc5e7ef73a7f5209ce4924d234dfb98829cba86d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7820bc0b8d0f7ee1b9d6587b10f5355904f51e675ddd0a337e25edb87b5578`

```dockerfile
```

-	Layers:
	-	`sha256:0857811d7117af260dff536135d5b9462e12a604d988f0bbcfa5c98ac94002c1`  
		Last Modified: Fri, 17 Jan 2025 02:25:20 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:be6a2bf3869c0b2ce79cbea0de54fc0151be9915cb61572b8fee8ae231380fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125658359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98a7305162cf56e40d783f72a96aafbe29862ec4cf094baab60b961b874e8a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98031a3690358e9e338c7b900ff223767ca20fe8d3581d723971bb5d3e97df6e`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 8.1 MB (8074417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c05adf332c68788c150e330500d99375063fb5fccac4eca47664fef925fe6`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05df1af7190779d81ae1d2a2f6bab0f116cd0911eaf925ea3b7c88d84e4dca`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.8 MB (17795742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373537e5e27b254a2e83716ef135b83be0eaffa0fbb7dd7e588802f57c22952f`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.1 MB (17106465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8781806a16e281a8c480f7f429497d259f378f76366f5b8a2047861a9a0eb`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 17.6 MB (17649723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd429dc70fde0e965c93f4ea2aa21344379a0f8461e5e8fb3a260e92129bfbd7`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1709b08f9705b3f6af9978783f2fb732992ff039699fdbc0a842595dbcb3bf9`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d18f467488432eff104e17eebdd3b73776125d5155413e82a70fac1ad2d50de`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eb3998a0993954da71d972744c4ceafe57b9e96dcb75f4d7626277df3d4176`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 7.0 MB (6981841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b5a025a6a9bf0b06bba2fe135db13911e1dcf31474e69df77b00520bbd3191`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 97.8 KB (97784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0743b347437f8517c3560af97d8923ca391286f17acbe0558f46b28c8c8c4d2`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49595e55dbff2fe86a9c4da769bc6a7679b3da9c2279eed30873af6bb678e195`  
		Last Modified: Fri, 17 Jan 2025 02:28:29 GMT  
		Size: 54.0 MB (53952083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3849eac5f1cf6d7788301e473e712d6bf6d77e0e01c3829c96b4dec4acf623d8`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb83a6536a87f2c86efa17f506102254efe83bcb5e283b31a0db94d18505dde5`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:66c420a8f09f46b8c9153ce490d112d23b47a11ae227e02b316ba27641ad742e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83edc878bc62dd15adedb843a231f657257baa90509166b729e8665157592cd7`

```dockerfile
```

-	Layers:
	-	`sha256:60f641b6e35d2698c4ef8617324030bdddce902f61a5ed2f117f633f27b92da8`  
		Last Modified: Fri, 17 Jan 2025 02:28:25 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5.0-dind-alpine3.21`

```console
$ docker pull docker@sha256:45b80efde6892498e1160c3be8eb7cc67732863caac98d2a79af24398ff1c106
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

### `docker:27.5.0-dind-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:328fee4531eccdcfe52b61ba73c849a649cacad29fba1a4129c95b40e0f2196c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133867713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b300b8cdc5f2ac4f108ecdd418f3ea30e35b4ee1018ff818ca39dd3f0bc7aadd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db0ef5f6406167c28a55dbfc0fbbd527a8e8ee10b1ed0053a74bb5847f467b`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 8.1 MB (8060096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2617d81eedcf635e1fd94dc905266de252ae0d642c05465bb5c57e7b9e5b0`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e4c1fa9475c483015ff35cb0ca5fae973e6192bd7d355b798024cc3f6436c`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18849459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af4884fbc706fb37435cc7859f05891c18eaec536721e17e5a97361694520c3`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18798866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851762183788567546d15646f8ce06871883255ad227fb13b88d2c2e58ef7fa4`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 19.3 MB (19303643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d84c454f28e907e0f1f5996d71027092830cabefb6c3f3a8d0d9fb3b332b9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ada9115c6a1e6e261a5250211382c99910811092b2791e7b32073c01bd5817`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06335ef68f056dd7837956156616452c5087a436b0ddbbc94fcb4493390d9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e423b3161e65b5d155f4fee197bb34b95aaaf9034e25661cc942130922d5553f`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 6.7 MB (6733536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8d12927cbc5b132f3d989c2f32cf8fe0e3d4f9136fc784f675b40aa6e2caa5`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 89.4 KB (89425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326df6d9eb79ca016d6f1723d5ca2bced72bd36fd014e852b493a43a6447c10e`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa7701ffbf173fdb6f7999d28b78600828e770ef8de8c26f6767ff8d3413253`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 58.4 MB (58383027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40544ceb254c83f9677202983636becd2547551930652c6928a91b62c6b26529`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13647f78c45bebb40dba9ffe52c4bce8371d4edda349c507012fe1300ff50732`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:683d1639ff61791a2eae0ec63a422d289dc4e28394eb8e39ccf17b56e1737122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556810057e6ba7d14c45298e2761fef6923333526367bb7e64510b0649dd514e`

```dockerfile
```

-	Layers:
	-	`sha256:18fa62c94f21565d5f5d2b2d15c416dce24b5ac429609729db340cc622a08d00`  
		Last Modified: Fri, 17 Jan 2025 02:09:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-dind-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:872158a8fc908710ac79c7d0c61287953a6593ef365f7593fbc9ee6d449ca9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124949669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bbc03711f0e14a6963ddb7043e52c2f66782fc50b0319107b2712a9107fc28`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
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
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea778430c11317962e3aa40444717aa8dc546fc65595ea9fd6e73d36310902f`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 17.4 MB (17448787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea230caf38f20e83e44f4dc9f84ff4fb52580e6d973dd8ecd2952cd36ad2a21`  
		Last Modified: Fri, 17 Jan 2025 01:27:49 GMT  
		Size: 18.1 MB (18112354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97006a84267c6bca594ceb4a5bf26d607f5bdef93912e07f6e846be4422b1c`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e59e6b008d5c5752b4a7993bd0b52b1db7dc2dfa774314f4f775cc22afa320`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89fe821a62ed4869930b04fc18ac60cf2bda17c09431466d8459ccc0c3549e2`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fe55d9784a2a762c0d6ed72664929cdf9284a3a888e3089d5e9220628c6b45`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 7.0 MB (7041413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d364c50ad8b6c6c862e3e6daa1c4cf0a6e8c8433c8a71cffd144f766f0e4fb23`  
		Last Modified: Fri, 17 Jan 2025 02:11:06 GMT  
		Size: 89.1 KB (89085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0620df6bfe0a1bc90f013a4bb494501716e787d271b7bc5969ecbc24b43756`  
		Last Modified: Fri, 17 Jan 2025 02:11:06 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bd936df8e147b648aa1a39d212c1624e064452a47059063133cd6adf29f7c7`  
		Last Modified: Fri, 17 Jan 2025 02:11:08 GMT  
		Size: 54.0 MB (54047054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966301da011cd0c70e74a358f99db4b9f43762dd18ed38f53665e9a24e880c4b`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b29247ae6bfe40191a231dba9717f4ca4bf21ec2c13c3606f0ace4b34eb7c43`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 3.3 KB (3267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:dd0a36256908be42678ad2890166b0e84a6246797662f2b93f3cd6f24ab68906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9af519ad2f15c502e5c17cfd4e3767beadd551d1851f350066b158eb41c6913`

```dockerfile
```

-	Layers:
	-	`sha256:ce130b032bac1fce394cc92324e72573e50caf69fdb9c099daad2c98bd8d9a1d`  
		Last Modified: Fri, 17 Jan 2025 02:11:05 GMT  
		Size: 34.8 KB (34764 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-dind-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:29597558c26c7e456f9d4350b94f208a69114260adc21bdae0619f9a7749c34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64123e8eceb16c151befc29738868d17cd6b828c82a96cc2b46a182f62e48eab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
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
	-	`sha256:1d1f394b9e9ceefe286b141a6fce91d86072ca709baf5dc4447f3d5a6db9a163`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 17.4 MB (17427588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755932338966055de46ecbdb4e46288f1f52af30c0f57960411eed7bcbc876d0`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 18.1 MB (18099438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215cf40534564c9b7b71ea6e20aa6912ca15008a9c2dd68162c3efe4fc20e65b`  
		Last Modified: Fri, 17 Jan 2025 01:28:02 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb652a32cd1bd43600fe45d89a2455ab0b882887bfabe0664dc9eb749e932a1`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe784566335013d539f74a4e2e151368fe7ddd75a3583e15b1cbafc6eca14a`  
		Last Modified: Fri, 17 Jan 2025 01:28:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cd34d15034bf9fbabde6b6c4ec8bbfe56b0ee1dad07a86eef7f6d83a4829e5`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 6.4 MB (6367554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049bb15c92b4ba59ad113b753dc6305190eb3111a77ec5b86b8ca81c7dbc59f2`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 85.2 KB (85236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefdea776978b937e65e37c006d81238b97221fac666606609e7569cc915f005`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8ab79af5c8f7891f9b4d14518c40aae4efd8acb30339e416de829cf962a8ae`  
		Last Modified: Fri, 17 Jan 2025 02:25:24 GMT  
		Size: 54.0 MB (54047069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4015624859fadb74f8744fab8fe858c4a95b1d5fde6a26c00f709c761fb7908`  
		Last Modified: Fri, 17 Jan 2025 02:25:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935f17568aab4f3b97b7a27a57821ab17388667d24fa04ed2ac2b295bc4217bf`  
		Last Modified: Fri, 17 Jan 2025 02:25:23 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:8fb08780d366a366517f413dc5e7ef73a7f5209ce4924d234dfb98829cba86d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7820bc0b8d0f7ee1b9d6587b10f5355904f51e675ddd0a337e25edb87b5578`

```dockerfile
```

-	Layers:
	-	`sha256:0857811d7117af260dff536135d5b9462e12a604d988f0bbcfa5c98ac94002c1`  
		Last Modified: Fri, 17 Jan 2025 02:25:20 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-dind-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:be6a2bf3869c0b2ce79cbea0de54fc0151be9915cb61572b8fee8ae231380fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125658359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98a7305162cf56e40d783f72a96aafbe29862ec4cf094baab60b961b874e8a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98031a3690358e9e338c7b900ff223767ca20fe8d3581d723971bb5d3e97df6e`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 8.1 MB (8074417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c05adf332c68788c150e330500d99375063fb5fccac4eca47664fef925fe6`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05df1af7190779d81ae1d2a2f6bab0f116cd0911eaf925ea3b7c88d84e4dca`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.8 MB (17795742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373537e5e27b254a2e83716ef135b83be0eaffa0fbb7dd7e588802f57c22952f`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.1 MB (17106465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8781806a16e281a8c480f7f429497d259f378f76366f5b8a2047861a9a0eb`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 17.6 MB (17649723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd429dc70fde0e965c93f4ea2aa21344379a0f8461e5e8fb3a260e92129bfbd7`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1709b08f9705b3f6af9978783f2fb732992ff039699fdbc0a842595dbcb3bf9`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d18f467488432eff104e17eebdd3b73776125d5155413e82a70fac1ad2d50de`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eb3998a0993954da71d972744c4ceafe57b9e96dcb75f4d7626277df3d4176`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 7.0 MB (6981841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b5a025a6a9bf0b06bba2fe135db13911e1dcf31474e69df77b00520bbd3191`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 97.8 KB (97784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0743b347437f8517c3560af97d8923ca391286f17acbe0558f46b28c8c8c4d2`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49595e55dbff2fe86a9c4da769bc6a7679b3da9c2279eed30873af6bb678e195`  
		Last Modified: Fri, 17 Jan 2025 02:28:29 GMT  
		Size: 54.0 MB (53952083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3849eac5f1cf6d7788301e473e712d6bf6d77e0e01c3829c96b4dec4acf623d8`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb83a6536a87f2c86efa17f506102254efe83bcb5e283b31a0db94d18505dde5`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:66c420a8f09f46b8c9153ce490d112d23b47a11ae227e02b316ba27641ad742e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83edc878bc62dd15adedb843a231f657257baa90509166b729e8665157592cd7`

```dockerfile
```

-	Layers:
	-	`sha256:60f641b6e35d2698c4ef8617324030bdddce902f61a5ed2f117f633f27b92da8`  
		Last Modified: Fri, 17 Jan 2025 02:28:25 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5.0-dind-rootless`

```console
$ docker pull docker@sha256:a2eb1cdc0a6e73e7bb35ef6dcbae5eed1198b4bca80bdb43392e53fe8810dac2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.5.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:873e54eb4ecdc9f413abacfb497523561c23f3532678e2c7893393646e10a50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156159516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a995afc276d185bce60731d4ddc05950b70c859778a9280024a3322eccc42f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db0ef5f6406167c28a55dbfc0fbbd527a8e8ee10b1ed0053a74bb5847f467b`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 8.1 MB (8060096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2617d81eedcf635e1fd94dc905266de252ae0d642c05465bb5c57e7b9e5b0`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e4c1fa9475c483015ff35cb0ca5fae973e6192bd7d355b798024cc3f6436c`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18849459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af4884fbc706fb37435cc7859f05891c18eaec536721e17e5a97361694520c3`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18798866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851762183788567546d15646f8ce06871883255ad227fb13b88d2c2e58ef7fa4`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 19.3 MB (19303643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d84c454f28e907e0f1f5996d71027092830cabefb6c3f3a8d0d9fb3b332b9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ada9115c6a1e6e261a5250211382c99910811092b2791e7b32073c01bd5817`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06335ef68f056dd7837956156616452c5087a436b0ddbbc94fcb4493390d9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e423b3161e65b5d155f4fee197bb34b95aaaf9034e25661cc942130922d5553f`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 6.7 MB (6733536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8d12927cbc5b132f3d989c2f32cf8fe0e3d4f9136fc784f675b40aa6e2caa5`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 89.4 KB (89425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326df6d9eb79ca016d6f1723d5ca2bced72bd36fd014e852b493a43a6447c10e`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa7701ffbf173fdb6f7999d28b78600828e770ef8de8c26f6767ff8d3413253`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 58.4 MB (58383027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40544ceb254c83f9677202983636becd2547551930652c6928a91b62c6b26529`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13647f78c45bebb40dba9ffe52c4bce8371d4edda349c507012fe1300ff50732`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66dc758ea69526e85c86620347676a493debe5c819cb7693f6902867778933e`  
		Last Modified: Fri, 17 Jan 2025 03:10:06 GMT  
		Size: 986.6 KB (986590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a769f32782fd44a1e305c6cd1ded3edecb5694f58954d3cc7b391478329db7f`  
		Last Modified: Fri, 17 Jan 2025 03:10:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f44cdf5fe82b821bf859dd7dc946f6fc747355176a01766fcb0f5bf94b122b`  
		Last Modified: Fri, 17 Jan 2025 03:10:06 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3258dbd3a9e8b790797ba1dfba1986498142bdce2e5fe2d92401acf136c2e82`  
		Last Modified: Fri, 17 Jan 2025 03:10:06 GMT  
		Size: 21.3 MB (21303864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0b43ebf5168b463eec3f98a035bb526d262c7ea182a4512d55af1403efb938`  
		Last Modified: Fri, 17 Jan 2025 03:10:07 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9c775d2142f922fee9a01cd1a263b620904b5742c972910af90e7648c88d3568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5a4e42c5ba363bc8aef3cb74e50dab63c9734c25f86d36792612a546031595`

```dockerfile
```

-	Layers:
	-	`sha256:ecb34284584c52d63e44745705b82df95475a84099839e3c14388a6214ea5f01`  
		Last Modified: Fri, 17 Jan 2025 03:10:05 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:46448a2b08fe5a5504d5f1691183d0fc974fdcfa3b17884c071bc93726c19a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149829070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e0f743e506c55a8233123a5803840a26c7e9f78903b01aee2dd8554580f7ba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98031a3690358e9e338c7b900ff223767ca20fe8d3581d723971bb5d3e97df6e`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 8.1 MB (8074417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c05adf332c68788c150e330500d99375063fb5fccac4eca47664fef925fe6`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05df1af7190779d81ae1d2a2f6bab0f116cd0911eaf925ea3b7c88d84e4dca`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.8 MB (17795742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373537e5e27b254a2e83716ef135b83be0eaffa0fbb7dd7e588802f57c22952f`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.1 MB (17106465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8781806a16e281a8c480f7f429497d259f378f76366f5b8a2047861a9a0eb`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 17.6 MB (17649723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd429dc70fde0e965c93f4ea2aa21344379a0f8461e5e8fb3a260e92129bfbd7`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1709b08f9705b3f6af9978783f2fb732992ff039699fdbc0a842595dbcb3bf9`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d18f467488432eff104e17eebdd3b73776125d5155413e82a70fac1ad2d50de`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eb3998a0993954da71d972744c4ceafe57b9e96dcb75f4d7626277df3d4176`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 7.0 MB (6981841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b5a025a6a9bf0b06bba2fe135db13911e1dcf31474e69df77b00520bbd3191`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 97.8 KB (97784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0743b347437f8517c3560af97d8923ca391286f17acbe0558f46b28c8c8c4d2`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49595e55dbff2fe86a9c4da769bc6a7679b3da9c2279eed30873af6bb678e195`  
		Last Modified: Fri, 17 Jan 2025 02:28:29 GMT  
		Size: 54.0 MB (53952083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3849eac5f1cf6d7788301e473e712d6bf6d77e0e01c3829c96b4dec4acf623d8`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb83a6536a87f2c86efa17f506102254efe83bcb5e283b31a0db94d18505dde5`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3982d96f5df89ee494fa458304355e30ef199bf1f1eda6c8b3dd607ca23d13`  
		Last Modified: Fri, 17 Jan 2025 03:27:30 GMT  
		Size: 1.0 MB (1014204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2b21cd3eb15dce210b7517a6be34965beddec2dc6e9384736e6bb97cc71618`  
		Last Modified: Fri, 17 Jan 2025 03:27:30 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4956e53894609bd8273c577579d49372b1b3f24cd142be4357a8b0e4873b2f90`  
		Last Modified: Fri, 17 Jan 2025 03:27:30 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5cc90ddeee38314b0dceef56e97746323daddce4a63b1dcfa6183891f64d39`  
		Last Modified: Fri, 17 Jan 2025 03:27:47 GMT  
		Size: 23.2 MB (23155160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889d5be2190a9406c5b1b3356b8b527176fc46f76cb5d40192b120061af4949f`  
		Last Modified: Fri, 17 Jan 2025 03:27:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:60876bd91d54cb65a601c27c85c7d8eda74c6a2f025325d12829c4f0173616a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7259e4a52601951b094f318099af2a7f82d03f417f9a37fe03194189522e619f`

```dockerfile
```

-	Layers:
	-	`sha256:1b563391abe23859090df83bb0dd41ef65f19bc25be6210520c59171a5564c22`  
		Last Modified: Fri, 17 Jan 2025 03:27:28 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5.0-windowsservercore`

```console
$ docker pull docker@sha256:147774e53a5cba9011ba41fc0a6031a0fe2a38be3ea00ada24c7c986bfe3e895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `docker:27.5.0-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:1ddbeca1f26cfd027cd80d7c22a37038dc7a5b749a4cc162893d982e25611f9e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2321733461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa6fd542e3201d9417d1c00e4e8e4ea67053d989ef8279153b1c3c1a73390dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 17 Jan 2025 01:32:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 17 Jan 2025 01:32:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 17 Jan 2025 01:32:29 GMT
ENV DOCKER_VERSION=27.5.0
# Fri, 17 Jan 2025 01:32:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Fri, 17 Jan 2025 01:32:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:32:38 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Fri, 17 Jan 2025 01:32:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Fri, 17 Jan 2025 01:32:40 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Fri, 17 Jan 2025 01:32:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:32:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Fri, 17 Jan 2025 01:32:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Fri, 17 Jan 2025 01:32:49 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Fri, 17 Jan 2025 01:32:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a2b5f44002e9945660f33fac78eda870ab26d14af8237ced3f7d6eebafc482`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203a2deeff1a6f93e060d1f072f55c5e625f7a8ba0b5b650ea6a24ec493e906f`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 357.5 KB (357481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892a6f8fa8324bfeb4612f7a42f4557afd5e082b76d6eb091e0de676dc19d26b`  
		Last Modified: Fri, 17 Jan 2025 01:33:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c45ea49c7511c526fac9de55eb8d1ec854cf7c24e175e514d4f76d393a1492f`  
		Last Modified: Fri, 17 Jan 2025 01:33:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e5b7f87ce7df7acc0870faf1a629a49f3f3b7865260274227fe01eb5fbe059`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 19.2 MB (19163659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1792865d58e6d13c7f1f82e4bd2c626a933e6f6a35db76e7a561e7feea4d7313`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc28b08ea10f6f26ceaad44e423332916af104c6c64d5c832f500bc690e15bf`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3b113153c6bc3cc9533ce2cde3d40a1feae4f3c43de591454bc66cabd8b7d6`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab2a02883224978a44c53d67303e6399cfa8291fd4878a7d28d1b9f9c86e0fb`  
		Last Modified: Fri, 17 Jan 2025 01:33:03 GMT  
		Size: 19.6 MB (19646321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9674894f9e36062ebb2d60558e37eb1e25270606e64a963e2154eca16d22a1`  
		Last Modified: Fri, 17 Jan 2025 01:33:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6baac49af4fea3c6c40c4380c6c83141230ecf225b612fef2dcb0860d12bd3`  
		Last Modified: Fri, 17 Jan 2025 01:33:00 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6f04636f816d025e0fcb207436d479348f6902a7b726b00fc0b08c4c91da5`  
		Last Modified: Fri, 17 Jan 2025 01:33:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff25e05ad1368fb78eb59c79e73d3276e7d77771072037ec3e43ca5409067c78`  
		Last Modified: Fri, 17 Jan 2025 01:33:03 GMT  
		Size: 20.2 MB (20169201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.5.0-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:a4691c37ea78600875afbfe9b5f3193ad202961501db79accf2e4169f9b42021
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181529728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1056e0f7366117381694ae8dcdba87d790f109eb17c3d003ef5aef0219256f5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 17 Jan 2025 01:33:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 17 Jan 2025 01:34:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 17 Jan 2025 01:34:31 GMT
ENV DOCKER_VERSION=27.5.0
# Fri, 17 Jan 2025 01:34:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Fri, 17 Jan 2025 01:34:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:34:45 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Fri, 17 Jan 2025 01:34:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Fri, 17 Jan 2025 01:34:46 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Fri, 17 Jan 2025 01:34:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:34:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Fri, 17 Jan 2025 01:34:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Fri, 17 Jan 2025 01:34:58 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Fri, 17 Jan 2025 01:35:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e6274df071a7d5a5db2dfcfdd09b3e5619a6a91cdf7f97ab0e499ce20fbadc`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75379368627062a255445132b6e6f800fa70735daa6088bd9a26716f97d8c20`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 341.5 KB (341471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d991c76af457bbd0d51a6c717c7269b73a45c7241bb22f2ea0a2140d7e5df9b`  
		Last Modified: Fri, 17 Jan 2025 01:35:16 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499d890bbe543c9fa6a376c2cc02860b9d28c3ceb3333573c42123258c044874`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1c11b12baeb8dbd4b7d91eb54b5d14a02ae0cf432615ea004e1e19f8f39c1d`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 19.2 MB (19160387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3235fd67ddd40cdaef5899c144213bba7245b4307f2902f0aebdf497c8d724`  
		Last Modified: Fri, 17 Jan 2025 01:35:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b03c5d4a69994a8004df958ddad06c5afbcc59f276c99989342f8400bf8d7d3`  
		Last Modified: Fri, 17 Jan 2025 01:35:14 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604799b0a87e0da3e79003c6f7f3b8c0ee9f49d2a0fd3da26c55e2d59e5a56ce`  
		Last Modified: Fri, 17 Jan 2025 01:35:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35965d90f9d46033f9e870e8cd2fb5125759d0ab816adacb4c3977e8b124b395`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 19.6 MB (19638065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2795117faa51777ee5591503a846e643112eed007983483a0799b0aba498c98`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e460c490d0afd58b3f2e390983623e89cd4a1f9bafe9b32435fdb41e2c37e99`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54d5078572cf39f63c8f5cc06830bd0716dcc480240b5200491cf747e26c12a`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb52aa115ea25674a9b875dd187041c15e8bd3b155bf96774b70758ad0f61e4`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 20.2 MB (20165876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:3b3e4d8d1726d5fb5d874f245b2d80913ac5431e62e2beed2d21e7966bd16079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `docker:27.5.0-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:a4691c37ea78600875afbfe9b5f3193ad202961501db79accf2e4169f9b42021
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181529728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1056e0f7366117381694ae8dcdba87d790f109eb17c3d003ef5aef0219256f5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 17 Jan 2025 01:33:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 17 Jan 2025 01:34:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 17 Jan 2025 01:34:31 GMT
ENV DOCKER_VERSION=27.5.0
# Fri, 17 Jan 2025 01:34:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Fri, 17 Jan 2025 01:34:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:34:45 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Fri, 17 Jan 2025 01:34:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Fri, 17 Jan 2025 01:34:46 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Fri, 17 Jan 2025 01:34:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:34:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Fri, 17 Jan 2025 01:34:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Fri, 17 Jan 2025 01:34:58 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Fri, 17 Jan 2025 01:35:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e6274df071a7d5a5db2dfcfdd09b3e5619a6a91cdf7f97ab0e499ce20fbadc`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75379368627062a255445132b6e6f800fa70735daa6088bd9a26716f97d8c20`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 341.5 KB (341471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d991c76af457bbd0d51a6c717c7269b73a45c7241bb22f2ea0a2140d7e5df9b`  
		Last Modified: Fri, 17 Jan 2025 01:35:16 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499d890bbe543c9fa6a376c2cc02860b9d28c3ceb3333573c42123258c044874`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1c11b12baeb8dbd4b7d91eb54b5d14a02ae0cf432615ea004e1e19f8f39c1d`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 19.2 MB (19160387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3235fd67ddd40cdaef5899c144213bba7245b4307f2902f0aebdf497c8d724`  
		Last Modified: Fri, 17 Jan 2025 01:35:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b03c5d4a69994a8004df958ddad06c5afbcc59f276c99989342f8400bf8d7d3`  
		Last Modified: Fri, 17 Jan 2025 01:35:14 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604799b0a87e0da3e79003c6f7f3b8c0ee9f49d2a0fd3da26c55e2d59e5a56ce`  
		Last Modified: Fri, 17 Jan 2025 01:35:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35965d90f9d46033f9e870e8cd2fb5125759d0ab816adacb4c3977e8b124b395`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 19.6 MB (19638065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2795117faa51777ee5591503a846e643112eed007983483a0799b0aba498c98`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e460c490d0afd58b3f2e390983623e89cd4a1f9bafe9b32435fdb41e2c37e99`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54d5078572cf39f63c8f5cc06830bd0716dcc480240b5200491cf747e26c12a`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb52aa115ea25674a9b875dd187041c15e8bd3b155bf96774b70758ad0f61e4`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 20.2 MB (20165876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:3bde2a2a6f2192672461cfec2b8264a4927348c274db2b6495e18ce39d141cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `docker:27.5.0-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:1ddbeca1f26cfd027cd80d7c22a37038dc7a5b749a4cc162893d982e25611f9e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2321733461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa6fd542e3201d9417d1c00e4e8e4ea67053d989ef8279153b1c3c1a73390dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 17 Jan 2025 01:32:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 17 Jan 2025 01:32:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 17 Jan 2025 01:32:29 GMT
ENV DOCKER_VERSION=27.5.0
# Fri, 17 Jan 2025 01:32:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Fri, 17 Jan 2025 01:32:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:32:38 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Fri, 17 Jan 2025 01:32:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Fri, 17 Jan 2025 01:32:40 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Fri, 17 Jan 2025 01:32:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:32:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Fri, 17 Jan 2025 01:32:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Fri, 17 Jan 2025 01:32:49 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Fri, 17 Jan 2025 01:32:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a2b5f44002e9945660f33fac78eda870ab26d14af8237ced3f7d6eebafc482`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203a2deeff1a6f93e060d1f072f55c5e625f7a8ba0b5b650ea6a24ec493e906f`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 357.5 KB (357481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892a6f8fa8324bfeb4612f7a42f4557afd5e082b76d6eb091e0de676dc19d26b`  
		Last Modified: Fri, 17 Jan 2025 01:33:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c45ea49c7511c526fac9de55eb8d1ec854cf7c24e175e514d4f76d393a1492f`  
		Last Modified: Fri, 17 Jan 2025 01:33:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e5b7f87ce7df7acc0870faf1a629a49f3f3b7865260274227fe01eb5fbe059`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 19.2 MB (19163659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1792865d58e6d13c7f1f82e4bd2c626a933e6f6a35db76e7a561e7feea4d7313`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc28b08ea10f6f26ceaad44e423332916af104c6c64d5c832f500bc690e15bf`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3b113153c6bc3cc9533ce2cde3d40a1feae4f3c43de591454bc66cabd8b7d6`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab2a02883224978a44c53d67303e6399cfa8291fd4878a7d28d1b9f9c86e0fb`  
		Last Modified: Fri, 17 Jan 2025 01:33:03 GMT  
		Size: 19.6 MB (19646321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9674894f9e36062ebb2d60558e37eb1e25270606e64a963e2154eca16d22a1`  
		Last Modified: Fri, 17 Jan 2025 01:33:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6baac49af4fea3c6c40c4380c6c83141230ecf225b612fef2dcb0860d12bd3`  
		Last Modified: Fri, 17 Jan 2025 01:33:00 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6f04636f816d025e0fcb207436d479348f6902a7b726b00fc0b08c4c91da5`  
		Last Modified: Fri, 17 Jan 2025 01:33:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff25e05ad1368fb78eb59c79e73d3276e7d77771072037ec3e43ca5409067c78`  
		Last Modified: Fri, 17 Jan 2025 01:33:03 GMT  
		Size: 20.2 MB (20169201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:7c10b867b5da6f0ecbac463defeaa490c1d2816cb02fe4e14d2994ad9c3812cd
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
$ docker pull docker@sha256:b219ac7db8149403917bdea481b4e8bdc9e48c492e12d6aa2b0ad8e11b323316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68655933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cc102d4a93a8704667364b5cfb93d9dcc26a6a861645223f2d4893b3ed723a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.0
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db0ef5f6406167c28a55dbfc0fbbd527a8e8ee10b1ed0053a74bb5847f467b`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 8.1 MB (8060096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2617d81eedcf635e1fd94dc905266de252ae0d642c05465bb5c57e7b9e5b0`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e4c1fa9475c483015ff35cb0ca5fae973e6192bd7d355b798024cc3f6436c`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18849459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af4884fbc706fb37435cc7859f05891c18eaec536721e17e5a97361694520c3`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18798866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851762183788567546d15646f8ce06871883255ad227fb13b88d2c2e58ef7fa4`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 19.3 MB (19303643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d84c454f28e907e0f1f5996d71027092830cabefb6c3f3a8d0d9fb3b332b9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ada9115c6a1e6e261a5250211382c99910811092b2791e7b32073c01bd5817`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06335ef68f056dd7837956156616452c5087a436b0ddbbc94fcb4493390d9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:bfcde7282475bfa1b52d54c2ccea12401ee915b605e1d578a5081bb4a69627bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8044174370b4166bc88d8f825313d5221505fa7b2ba129e316bb4e292d4a93d8`

```dockerfile
```

-	Layers:
	-	`sha256:f5e0658d18f9353954b3b81fc16fe0b3e32f0e667af202b4f413c79dce6a3b96`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:f52fb18fdfc78a4af51b84ac7d2b5fca13b8e3e09b1067aa849e9f04030c2c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63766314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74e5406e29303780211a38cb58677a0c6a96a6aa5ce396f86ae128d852cc85d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.0
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
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
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea778430c11317962e3aa40444717aa8dc546fc65595ea9fd6e73d36310902f`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 17.4 MB (17448787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea230caf38f20e83e44f4dc9f84ff4fb52580e6d973dd8ecd2952cd36ad2a21`  
		Last Modified: Fri, 17 Jan 2025 01:27:49 GMT  
		Size: 18.1 MB (18112354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97006a84267c6bca594ceb4a5bf26d607f5bdef93912e07f6e846be4422b1c`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e59e6b008d5c5752b4a7993bd0b52b1db7dc2dfa774314f4f775cc22afa320`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89fe821a62ed4869930b04fc18ac60cf2bda17c09431466d8459ccc0c3549e2`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:dce530002422cd3b77135d6ae618300706585d7d6deebc956b7425231442feeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c540c5273aba065d46aa7fa9ca86bfb8aa222597b3283936e19bbdef868628f6`

```dockerfile
```

-	Layers:
	-	`sha256:532ebdac6902ef2db952873eeeaf73c981703befe573cd7cbe0eaacd64aa031f`  
		Last Modified: Fri, 17 Jan 2025 01:27:47 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:9e993e3871a714198e4b947664c5f228a5d7982b3515670942d8a495f03485eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62776105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde14708064af6f21da2b23403c4e90218556fb6cf1508302904ef370691f99c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.0
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
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
	-	`sha256:1d1f394b9e9ceefe286b141a6fce91d86072ca709baf5dc4447f3d5a6db9a163`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 17.4 MB (17427588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755932338966055de46ecbdb4e46288f1f52af30c0f57960411eed7bcbc876d0`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 18.1 MB (18099438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215cf40534564c9b7b71ea6e20aa6912ca15008a9c2dd68162c3efe4fc20e65b`  
		Last Modified: Fri, 17 Jan 2025 01:28:02 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb652a32cd1bd43600fe45d89a2455ab0b882887bfabe0664dc9eb749e932a1`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe784566335013d539f74a4e2e151368fe7ddd75a3583e15b1cbafc6eca14a`  
		Last Modified: Fri, 17 Jan 2025 01:28:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:dfca36c13fd1337794df037f0fc30b729677e432669884ebcb2f92429c838457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4905f7d813489e8a4204010015fb7509e3c94934b1b88e1418f21f37a337a6f`

```dockerfile
```

-	Layers:
	-	`sha256:89c06eb5c6c66dfe6a2640b9ccf35cdc3ab8ca4ac9883f9fb2b69b8aba4d80e3`  
		Last Modified: Fri, 17 Jan 2025 01:28:01 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a121337c9287fdc11e04a8a12708f639e8c3ba427945f4539df65679aee3ee8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64620861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d961a7c95de71f4706af938b3c55efbe8f7379a1c212212251b71732ea4c5cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_VERSION=27.5.0
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Thu, 16 Jan 2025 00:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 Jan 2025 00:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 Jan 2025 00:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jan 2025 00:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98031a3690358e9e338c7b900ff223767ca20fe8d3581d723971bb5d3e97df6e`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 8.1 MB (8074417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c05adf332c68788c150e330500d99375063fb5fccac4eca47664fef925fe6`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05df1af7190779d81ae1d2a2f6bab0f116cd0911eaf925ea3b7c88d84e4dca`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.8 MB (17795742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373537e5e27b254a2e83716ef135b83be0eaffa0fbb7dd7e588802f57c22952f`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.1 MB (17106465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8781806a16e281a8c480f7f429497d259f378f76366f5b8a2047861a9a0eb`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 17.6 MB (17649723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd429dc70fde0e965c93f4ea2aa21344379a0f8461e5e8fb3a260e92129bfbd7`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1709b08f9705b3f6af9978783f2fb732992ff039699fdbc0a842595dbcb3bf9`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d18f467488432eff104e17eebdd3b73776125d5155413e82a70fac1ad2d50de`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:1d010e0b0f4fa82a5b3ba475d15bffbaf6b9481a3a2c85a608aa6f1be93f4160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a79ec7a8c697907793b7bd322196ef33a33e0ae9eb4ea0f46752d9aa591878`

```dockerfile
```

-	Layers:
	-	`sha256:1ce07430fc5561a2375bb4a6167743bb1bef6046817bf347a9a3f3373a4cfc4b`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:45b80efde6892498e1160c3be8eb7cc67732863caac98d2a79af24398ff1c106
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
$ docker pull docker@sha256:328fee4531eccdcfe52b61ba73c849a649cacad29fba1a4129c95b40e0f2196c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133867713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b300b8cdc5f2ac4f108ecdd418f3ea30e35b4ee1018ff818ca39dd3f0bc7aadd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db0ef5f6406167c28a55dbfc0fbbd527a8e8ee10b1ed0053a74bb5847f467b`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 8.1 MB (8060096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2617d81eedcf635e1fd94dc905266de252ae0d642c05465bb5c57e7b9e5b0`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e4c1fa9475c483015ff35cb0ca5fae973e6192bd7d355b798024cc3f6436c`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18849459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af4884fbc706fb37435cc7859f05891c18eaec536721e17e5a97361694520c3`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18798866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851762183788567546d15646f8ce06871883255ad227fb13b88d2c2e58ef7fa4`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 19.3 MB (19303643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d84c454f28e907e0f1f5996d71027092830cabefb6c3f3a8d0d9fb3b332b9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ada9115c6a1e6e261a5250211382c99910811092b2791e7b32073c01bd5817`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06335ef68f056dd7837956156616452c5087a436b0ddbbc94fcb4493390d9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e423b3161e65b5d155f4fee197bb34b95aaaf9034e25661cc942130922d5553f`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 6.7 MB (6733536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8d12927cbc5b132f3d989c2f32cf8fe0e3d4f9136fc784f675b40aa6e2caa5`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 89.4 KB (89425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326df6d9eb79ca016d6f1723d5ca2bced72bd36fd014e852b493a43a6447c10e`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa7701ffbf173fdb6f7999d28b78600828e770ef8de8c26f6767ff8d3413253`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 58.4 MB (58383027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40544ceb254c83f9677202983636becd2547551930652c6928a91b62c6b26529`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13647f78c45bebb40dba9ffe52c4bce8371d4edda349c507012fe1300ff50732`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:683d1639ff61791a2eae0ec63a422d289dc4e28394eb8e39ccf17b56e1737122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556810057e6ba7d14c45298e2761fef6923333526367bb7e64510b0649dd514e`

```dockerfile
```

-	Layers:
	-	`sha256:18fa62c94f21565d5f5d2b2d15c416dce24b5ac429609729db340cc622a08d00`  
		Last Modified: Fri, 17 Jan 2025 02:09:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:872158a8fc908710ac79c7d0c61287953a6593ef365f7593fbc9ee6d449ca9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124949669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bbc03711f0e14a6963ddb7043e52c2f66782fc50b0319107b2712a9107fc28`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
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
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea778430c11317962e3aa40444717aa8dc546fc65595ea9fd6e73d36310902f`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 17.4 MB (17448787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea230caf38f20e83e44f4dc9f84ff4fb52580e6d973dd8ecd2952cd36ad2a21`  
		Last Modified: Fri, 17 Jan 2025 01:27:49 GMT  
		Size: 18.1 MB (18112354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97006a84267c6bca594ceb4a5bf26d607f5bdef93912e07f6e846be4422b1c`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e59e6b008d5c5752b4a7993bd0b52b1db7dc2dfa774314f4f775cc22afa320`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89fe821a62ed4869930b04fc18ac60cf2bda17c09431466d8459ccc0c3549e2`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fe55d9784a2a762c0d6ed72664929cdf9284a3a888e3089d5e9220628c6b45`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 7.0 MB (7041413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d364c50ad8b6c6c862e3e6daa1c4cf0a6e8c8433c8a71cffd144f766f0e4fb23`  
		Last Modified: Fri, 17 Jan 2025 02:11:06 GMT  
		Size: 89.1 KB (89085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0620df6bfe0a1bc90f013a4bb494501716e787d271b7bc5969ecbc24b43756`  
		Last Modified: Fri, 17 Jan 2025 02:11:06 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bd936df8e147b648aa1a39d212c1624e064452a47059063133cd6adf29f7c7`  
		Last Modified: Fri, 17 Jan 2025 02:11:08 GMT  
		Size: 54.0 MB (54047054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966301da011cd0c70e74a358f99db4b9f43762dd18ed38f53665e9a24e880c4b`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b29247ae6bfe40191a231dba9717f4ca4bf21ec2c13c3606f0ace4b34eb7c43`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 3.3 KB (3267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:dd0a36256908be42678ad2890166b0e84a6246797662f2b93f3cd6f24ab68906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9af519ad2f15c502e5c17cfd4e3767beadd551d1851f350066b158eb41c6913`

```dockerfile
```

-	Layers:
	-	`sha256:ce130b032bac1fce394cc92324e72573e50caf69fdb9c099daad2c98bd8d9a1d`  
		Last Modified: Fri, 17 Jan 2025 02:11:05 GMT  
		Size: 34.8 KB (34764 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:29597558c26c7e456f9d4350b94f208a69114260adc21bdae0619f9a7749c34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64123e8eceb16c151befc29738868d17cd6b828c82a96cc2b46a182f62e48eab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
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
	-	`sha256:1d1f394b9e9ceefe286b141a6fce91d86072ca709baf5dc4447f3d5a6db9a163`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 17.4 MB (17427588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755932338966055de46ecbdb4e46288f1f52af30c0f57960411eed7bcbc876d0`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 18.1 MB (18099438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215cf40534564c9b7b71ea6e20aa6912ca15008a9c2dd68162c3efe4fc20e65b`  
		Last Modified: Fri, 17 Jan 2025 01:28:02 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb652a32cd1bd43600fe45d89a2455ab0b882887bfabe0664dc9eb749e932a1`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe784566335013d539f74a4e2e151368fe7ddd75a3583e15b1cbafc6eca14a`  
		Last Modified: Fri, 17 Jan 2025 01:28:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cd34d15034bf9fbabde6b6c4ec8bbfe56b0ee1dad07a86eef7f6d83a4829e5`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 6.4 MB (6367554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049bb15c92b4ba59ad113b753dc6305190eb3111a77ec5b86b8ca81c7dbc59f2`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 85.2 KB (85236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefdea776978b937e65e37c006d81238b97221fac666606609e7569cc915f005`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8ab79af5c8f7891f9b4d14518c40aae4efd8acb30339e416de829cf962a8ae`  
		Last Modified: Fri, 17 Jan 2025 02:25:24 GMT  
		Size: 54.0 MB (54047069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4015624859fadb74f8744fab8fe858c4a95b1d5fde6a26c00f709c761fb7908`  
		Last Modified: Fri, 17 Jan 2025 02:25:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935f17568aab4f3b97b7a27a57821ab17388667d24fa04ed2ac2b295bc4217bf`  
		Last Modified: Fri, 17 Jan 2025 02:25:23 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:8fb08780d366a366517f413dc5e7ef73a7f5209ce4924d234dfb98829cba86d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7820bc0b8d0f7ee1b9d6587b10f5355904f51e675ddd0a337e25edb87b5578`

```dockerfile
```

-	Layers:
	-	`sha256:0857811d7117af260dff536135d5b9462e12a604d988f0bbcfa5c98ac94002c1`  
		Last Modified: Fri, 17 Jan 2025 02:25:20 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:be6a2bf3869c0b2ce79cbea0de54fc0151be9915cb61572b8fee8ae231380fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125658359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98a7305162cf56e40d783f72a96aafbe29862ec4cf094baab60b961b874e8a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98031a3690358e9e338c7b900ff223767ca20fe8d3581d723971bb5d3e97df6e`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 8.1 MB (8074417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c05adf332c68788c150e330500d99375063fb5fccac4eca47664fef925fe6`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05df1af7190779d81ae1d2a2f6bab0f116cd0911eaf925ea3b7c88d84e4dca`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.8 MB (17795742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373537e5e27b254a2e83716ef135b83be0eaffa0fbb7dd7e588802f57c22952f`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.1 MB (17106465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8781806a16e281a8c480f7f429497d259f378f76366f5b8a2047861a9a0eb`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 17.6 MB (17649723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd429dc70fde0e965c93f4ea2aa21344379a0f8461e5e8fb3a260e92129bfbd7`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1709b08f9705b3f6af9978783f2fb732992ff039699fdbc0a842595dbcb3bf9`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d18f467488432eff104e17eebdd3b73776125d5155413e82a70fac1ad2d50de`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eb3998a0993954da71d972744c4ceafe57b9e96dcb75f4d7626277df3d4176`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 7.0 MB (6981841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b5a025a6a9bf0b06bba2fe135db13911e1dcf31474e69df77b00520bbd3191`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 97.8 KB (97784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0743b347437f8517c3560af97d8923ca391286f17acbe0558f46b28c8c8c4d2`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49595e55dbff2fe86a9c4da769bc6a7679b3da9c2279eed30873af6bb678e195`  
		Last Modified: Fri, 17 Jan 2025 02:28:29 GMT  
		Size: 54.0 MB (53952083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3849eac5f1cf6d7788301e473e712d6bf6d77e0e01c3829c96b4dec4acf623d8`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb83a6536a87f2c86efa17f506102254efe83bcb5e283b31a0db94d18505dde5`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:66c420a8f09f46b8c9153ce490d112d23b47a11ae227e02b316ba27641ad742e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83edc878bc62dd15adedb843a231f657257baa90509166b729e8665157592cd7`

```dockerfile
```

-	Layers:
	-	`sha256:60f641b6e35d2698c4ef8617324030bdddce902f61a5ed2f117f633f27b92da8`  
		Last Modified: Fri, 17 Jan 2025 02:28:25 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:a2eb1cdc0a6e73e7bb35ef6dcbae5eed1198b4bca80bdb43392e53fe8810dac2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:873e54eb4ecdc9f413abacfb497523561c23f3532678e2c7893393646e10a50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156159516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a995afc276d185bce60731d4ddc05950b70c859778a9280024a3322eccc42f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db0ef5f6406167c28a55dbfc0fbbd527a8e8ee10b1ed0053a74bb5847f467b`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 8.1 MB (8060096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2617d81eedcf635e1fd94dc905266de252ae0d642c05465bb5c57e7b9e5b0`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e4c1fa9475c483015ff35cb0ca5fae973e6192bd7d355b798024cc3f6436c`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18849459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af4884fbc706fb37435cc7859f05891c18eaec536721e17e5a97361694520c3`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18798866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851762183788567546d15646f8ce06871883255ad227fb13b88d2c2e58ef7fa4`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 19.3 MB (19303643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d84c454f28e907e0f1f5996d71027092830cabefb6c3f3a8d0d9fb3b332b9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ada9115c6a1e6e261a5250211382c99910811092b2791e7b32073c01bd5817`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06335ef68f056dd7837956156616452c5087a436b0ddbbc94fcb4493390d9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e423b3161e65b5d155f4fee197bb34b95aaaf9034e25661cc942130922d5553f`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 6.7 MB (6733536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8d12927cbc5b132f3d989c2f32cf8fe0e3d4f9136fc784f675b40aa6e2caa5`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 89.4 KB (89425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326df6d9eb79ca016d6f1723d5ca2bced72bd36fd014e852b493a43a6447c10e`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa7701ffbf173fdb6f7999d28b78600828e770ef8de8c26f6767ff8d3413253`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 58.4 MB (58383027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40544ceb254c83f9677202983636becd2547551930652c6928a91b62c6b26529`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13647f78c45bebb40dba9ffe52c4bce8371d4edda349c507012fe1300ff50732`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66dc758ea69526e85c86620347676a493debe5c819cb7693f6902867778933e`  
		Last Modified: Fri, 17 Jan 2025 03:10:06 GMT  
		Size: 986.6 KB (986590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a769f32782fd44a1e305c6cd1ded3edecb5694f58954d3cc7b391478329db7f`  
		Last Modified: Fri, 17 Jan 2025 03:10:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f44cdf5fe82b821bf859dd7dc946f6fc747355176a01766fcb0f5bf94b122b`  
		Last Modified: Fri, 17 Jan 2025 03:10:06 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3258dbd3a9e8b790797ba1dfba1986498142bdce2e5fe2d92401acf136c2e82`  
		Last Modified: Fri, 17 Jan 2025 03:10:06 GMT  
		Size: 21.3 MB (21303864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0b43ebf5168b463eec3f98a035bb526d262c7ea182a4512d55af1403efb938`  
		Last Modified: Fri, 17 Jan 2025 03:10:07 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9c775d2142f922fee9a01cd1a263b620904b5742c972910af90e7648c88d3568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5a4e42c5ba363bc8aef3cb74e50dab63c9734c25f86d36792612a546031595`

```dockerfile
```

-	Layers:
	-	`sha256:ecb34284584c52d63e44745705b82df95475a84099839e3c14388a6214ea5f01`  
		Last Modified: Fri, 17 Jan 2025 03:10:05 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:46448a2b08fe5a5504d5f1691183d0fc974fdcfa3b17884c071bc93726c19a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149829070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e0f743e506c55a8233123a5803840a26c7e9f78903b01aee2dd8554580f7ba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98031a3690358e9e338c7b900ff223767ca20fe8d3581d723971bb5d3e97df6e`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 8.1 MB (8074417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c05adf332c68788c150e330500d99375063fb5fccac4eca47664fef925fe6`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05df1af7190779d81ae1d2a2f6bab0f116cd0911eaf925ea3b7c88d84e4dca`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.8 MB (17795742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373537e5e27b254a2e83716ef135b83be0eaffa0fbb7dd7e588802f57c22952f`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.1 MB (17106465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8781806a16e281a8c480f7f429497d259f378f76366f5b8a2047861a9a0eb`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 17.6 MB (17649723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd429dc70fde0e965c93f4ea2aa21344379a0f8461e5e8fb3a260e92129bfbd7`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1709b08f9705b3f6af9978783f2fb732992ff039699fdbc0a842595dbcb3bf9`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d18f467488432eff104e17eebdd3b73776125d5155413e82a70fac1ad2d50de`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eb3998a0993954da71d972744c4ceafe57b9e96dcb75f4d7626277df3d4176`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 7.0 MB (6981841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b5a025a6a9bf0b06bba2fe135db13911e1dcf31474e69df77b00520bbd3191`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 97.8 KB (97784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0743b347437f8517c3560af97d8923ca391286f17acbe0558f46b28c8c8c4d2`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49595e55dbff2fe86a9c4da769bc6a7679b3da9c2279eed30873af6bb678e195`  
		Last Modified: Fri, 17 Jan 2025 02:28:29 GMT  
		Size: 54.0 MB (53952083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3849eac5f1cf6d7788301e473e712d6bf6d77e0e01c3829c96b4dec4acf623d8`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb83a6536a87f2c86efa17f506102254efe83bcb5e283b31a0db94d18505dde5`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3982d96f5df89ee494fa458304355e30ef199bf1f1eda6c8b3dd607ca23d13`  
		Last Modified: Fri, 17 Jan 2025 03:27:30 GMT  
		Size: 1.0 MB (1014204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2b21cd3eb15dce210b7517a6be34965beddec2dc6e9384736e6bb97cc71618`  
		Last Modified: Fri, 17 Jan 2025 03:27:30 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4956e53894609bd8273c577579d49372b1b3f24cd142be4357a8b0e4873b2f90`  
		Last Modified: Fri, 17 Jan 2025 03:27:30 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5cc90ddeee38314b0dceef56e97746323daddce4a63b1dcfa6183891f64d39`  
		Last Modified: Fri, 17 Jan 2025 03:27:47 GMT  
		Size: 23.2 MB (23155160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889d5be2190a9406c5b1b3356b8b527176fc46f76cb5d40192b120061af4949f`  
		Last Modified: Fri, 17 Jan 2025 03:27:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:60876bd91d54cb65a601c27c85c7d8eda74c6a2f025325d12829c4f0173616a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7259e4a52601951b094f318099af2a7f82d03f417f9a37fe03194189522e619f`

```dockerfile
```

-	Layers:
	-	`sha256:1b563391abe23859090df83bb0dd41ef65f19bc25be6210520c59171a5564c22`  
		Last Modified: Fri, 17 Jan 2025 03:27:28 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:45b80efde6892498e1160c3be8eb7cc67732863caac98d2a79af24398ff1c106
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
$ docker pull docker@sha256:328fee4531eccdcfe52b61ba73c849a649cacad29fba1a4129c95b40e0f2196c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133867713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b300b8cdc5f2ac4f108ecdd418f3ea30e35b4ee1018ff818ca39dd3f0bc7aadd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db0ef5f6406167c28a55dbfc0fbbd527a8e8ee10b1ed0053a74bb5847f467b`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 8.1 MB (8060096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd2617d81eedcf635e1fd94dc905266de252ae0d642c05465bb5c57e7b9e5b0`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e4c1fa9475c483015ff35cb0ca5fae973e6192bd7d355b798024cc3f6436c`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18849459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af4884fbc706fb37435cc7859f05891c18eaec536721e17e5a97361694520c3`  
		Last Modified: Fri, 17 Jan 2025 01:27:17 GMT  
		Size: 18.8 MB (18798866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851762183788567546d15646f8ce06871883255ad227fb13b88d2c2e58ef7fa4`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 19.3 MB (19303643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d84c454f28e907e0f1f5996d71027092830cabefb6c3f3a8d0d9fb3b332b9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ada9115c6a1e6e261a5250211382c99910811092b2791e7b32073c01bd5817`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06335ef68f056dd7837956156616452c5087a436b0ddbbc94fcb4493390d9f`  
		Last Modified: Fri, 17 Jan 2025 01:27:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e423b3161e65b5d155f4fee197bb34b95aaaf9034e25661cc942130922d5553f`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 6.7 MB (6733536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8d12927cbc5b132f3d989c2f32cf8fe0e3d4f9136fc784f675b40aa6e2caa5`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 89.4 KB (89425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326df6d9eb79ca016d6f1723d5ca2bced72bd36fd014e852b493a43a6447c10e`  
		Last Modified: Fri, 17 Jan 2025 02:09:21 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa7701ffbf173fdb6f7999d28b78600828e770ef8de8c26f6767ff8d3413253`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 58.4 MB (58383027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40544ceb254c83f9677202983636becd2547551930652c6928a91b62c6b26529`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13647f78c45bebb40dba9ffe52c4bce8371d4edda349c507012fe1300ff50732`  
		Last Modified: Fri, 17 Jan 2025 02:09:22 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:683d1639ff61791a2eae0ec63a422d289dc4e28394eb8e39ccf17b56e1737122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556810057e6ba7d14c45298e2761fef6923333526367bb7e64510b0649dd514e`

```dockerfile
```

-	Layers:
	-	`sha256:18fa62c94f21565d5f5d2b2d15c416dce24b5ac429609729db340cc622a08d00`  
		Last Modified: Fri, 17 Jan 2025 02:09:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:872158a8fc908710ac79c7d0c61287953a6593ef365f7593fbc9ee6d449ca9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124949669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bbc03711f0e14a6963ddb7043e52c2f66782fc50b0319107b2712a9107fc28`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
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
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea778430c11317962e3aa40444717aa8dc546fc65595ea9fd6e73d36310902f`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 17.4 MB (17448787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea230caf38f20e83e44f4dc9f84ff4fb52580e6d973dd8ecd2952cd36ad2a21`  
		Last Modified: Fri, 17 Jan 2025 01:27:49 GMT  
		Size: 18.1 MB (18112354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97006a84267c6bca594ceb4a5bf26d607f5bdef93912e07f6e846be4422b1c`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e59e6b008d5c5752b4a7993bd0b52b1db7dc2dfa774314f4f775cc22afa320`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89fe821a62ed4869930b04fc18ac60cf2bda17c09431466d8459ccc0c3549e2`  
		Last Modified: Fri, 17 Jan 2025 01:27:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fe55d9784a2a762c0d6ed72664929cdf9284a3a888e3089d5e9220628c6b45`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 7.0 MB (7041413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d364c50ad8b6c6c862e3e6daa1c4cf0a6e8c8433c8a71cffd144f766f0e4fb23`  
		Last Modified: Fri, 17 Jan 2025 02:11:06 GMT  
		Size: 89.1 KB (89085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0620df6bfe0a1bc90f013a4bb494501716e787d271b7bc5969ecbc24b43756`  
		Last Modified: Fri, 17 Jan 2025 02:11:06 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bd936df8e147b648aa1a39d212c1624e064452a47059063133cd6adf29f7c7`  
		Last Modified: Fri, 17 Jan 2025 02:11:08 GMT  
		Size: 54.0 MB (54047054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966301da011cd0c70e74a358f99db4b9f43762dd18ed38f53665e9a24e880c4b`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b29247ae6bfe40191a231dba9717f4ca4bf21ec2c13c3606f0ace4b34eb7c43`  
		Last Modified: Fri, 17 Jan 2025 02:11:07 GMT  
		Size: 3.3 KB (3267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:dd0a36256908be42678ad2890166b0e84a6246797662f2b93f3cd6f24ab68906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9af519ad2f15c502e5c17cfd4e3767beadd551d1851f350066b158eb41c6913`

```dockerfile
```

-	Layers:
	-	`sha256:ce130b032bac1fce394cc92324e72573e50caf69fdb9c099daad2c98bd8d9a1d`  
		Last Modified: Fri, 17 Jan 2025 02:11:05 GMT  
		Size: 34.8 KB (34764 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:29597558c26c7e456f9d4350b94f208a69114260adc21bdae0619f9a7749c34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64123e8eceb16c151befc29738868d17cd6b828c82a96cc2b46a182f62e48eab`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
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
	-	`sha256:1d1f394b9e9ceefe286b141a6fce91d86072ca709baf5dc4447f3d5a6db9a163`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 17.4 MB (17427588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755932338966055de46ecbdb4e46288f1f52af30c0f57960411eed7bcbc876d0`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 18.1 MB (18099438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215cf40534564c9b7b71ea6e20aa6912ca15008a9c2dd68162c3efe4fc20e65b`  
		Last Modified: Fri, 17 Jan 2025 01:28:02 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb652a32cd1bd43600fe45d89a2455ab0b882887bfabe0664dc9eb749e932a1`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe784566335013d539f74a4e2e151368fe7ddd75a3583e15b1cbafc6eca14a`  
		Last Modified: Fri, 17 Jan 2025 01:28:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cd34d15034bf9fbabde6b6c4ec8bbfe56b0ee1dad07a86eef7f6d83a4829e5`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 6.4 MB (6367554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049bb15c92b4ba59ad113b753dc6305190eb3111a77ec5b86b8ca81c7dbc59f2`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 85.2 KB (85236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefdea776978b937e65e37c006d81238b97221fac666606609e7569cc915f005`  
		Last Modified: Fri, 17 Jan 2025 02:25:22 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8ab79af5c8f7891f9b4d14518c40aae4efd8acb30339e416de829cf962a8ae`  
		Last Modified: Fri, 17 Jan 2025 02:25:24 GMT  
		Size: 54.0 MB (54047069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4015624859fadb74f8744fab8fe858c4a95b1d5fde6a26c00f709c761fb7908`  
		Last Modified: Fri, 17 Jan 2025 02:25:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935f17568aab4f3b97b7a27a57821ab17388667d24fa04ed2ac2b295bc4217bf`  
		Last Modified: Fri, 17 Jan 2025 02:25:23 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:8fb08780d366a366517f413dc5e7ef73a7f5209ce4924d234dfb98829cba86d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7820bc0b8d0f7ee1b9d6587b10f5355904f51e675ddd0a337e25edb87b5578`

```dockerfile
```

-	Layers:
	-	`sha256:0857811d7117af260dff536135d5b9462e12a604d988f0bbcfa5c98ac94002c1`  
		Last Modified: Fri, 17 Jan 2025 02:25:20 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:be6a2bf3869c0b2ce79cbea0de54fc0151be9915cb61572b8fee8ae231380fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125658359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98a7305162cf56e40d783f72a96aafbe29862ec4cf094baab60b961b874e8a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98031a3690358e9e338c7b900ff223767ca20fe8d3581d723971bb5d3e97df6e`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 8.1 MB (8074417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c05adf332c68788c150e330500d99375063fb5fccac4eca47664fef925fe6`  
		Last Modified: Fri, 17 Jan 2025 01:27:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05df1af7190779d81ae1d2a2f6bab0f116cd0911eaf925ea3b7c88d84e4dca`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.8 MB (17795742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373537e5e27b254a2e83716ef135b83be0eaffa0fbb7dd7e588802f57c22952f`  
		Last Modified: Fri, 17 Jan 2025 01:27:31 GMT  
		Size: 17.1 MB (17106465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8781806a16e281a8c480f7f429497d259f378f76366f5b8a2047861a9a0eb`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 17.6 MB (17649723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd429dc70fde0e965c93f4ea2aa21344379a0f8461e5e8fb3a260e92129bfbd7`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1709b08f9705b3f6af9978783f2fb732992ff039699fdbc0a842595dbcb3bf9`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d18f467488432eff104e17eebdd3b73776125d5155413e82a70fac1ad2d50de`  
		Last Modified: Fri, 17 Jan 2025 01:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eb3998a0993954da71d972744c4ceafe57b9e96dcb75f4d7626277df3d4176`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 7.0 MB (6981841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b5a025a6a9bf0b06bba2fe135db13911e1dcf31474e69df77b00520bbd3191`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 97.8 KB (97784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0743b347437f8517c3560af97d8923ca391286f17acbe0558f46b28c8c8c4d2`  
		Last Modified: Fri, 17 Jan 2025 02:28:26 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49595e55dbff2fe86a9c4da769bc6a7679b3da9c2279eed30873af6bb678e195`  
		Last Modified: Fri, 17 Jan 2025 02:28:29 GMT  
		Size: 54.0 MB (53952083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3849eac5f1cf6d7788301e473e712d6bf6d77e0e01c3829c96b4dec4acf623d8`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb83a6536a87f2c86efa17f506102254efe83bcb5e283b31a0db94d18505dde5`  
		Last Modified: Fri, 17 Jan 2025 02:28:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:66c420a8f09f46b8c9153ce490d112d23b47a11ae227e02b316ba27641ad742e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83edc878bc62dd15adedb843a231f657257baa90509166b729e8665157592cd7`

```dockerfile
```

-	Layers:
	-	`sha256:60f641b6e35d2698c4ef8617324030bdddce902f61a5ed2f117f633f27b92da8`  
		Last Modified: Fri, 17 Jan 2025 02:28:25 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:147774e53a5cba9011ba41fc0a6031a0fe2a38be3ea00ada24c7c986bfe3e895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `docker:windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:1ddbeca1f26cfd027cd80d7c22a37038dc7a5b749a4cc162893d982e25611f9e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2321733461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa6fd542e3201d9417d1c00e4e8e4ea67053d989ef8279153b1c3c1a73390dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 17 Jan 2025 01:32:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 17 Jan 2025 01:32:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 17 Jan 2025 01:32:29 GMT
ENV DOCKER_VERSION=27.5.0
# Fri, 17 Jan 2025 01:32:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Fri, 17 Jan 2025 01:32:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:32:38 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Fri, 17 Jan 2025 01:32:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Fri, 17 Jan 2025 01:32:40 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Fri, 17 Jan 2025 01:32:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:32:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Fri, 17 Jan 2025 01:32:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Fri, 17 Jan 2025 01:32:49 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Fri, 17 Jan 2025 01:32:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a2b5f44002e9945660f33fac78eda870ab26d14af8237ced3f7d6eebafc482`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203a2deeff1a6f93e060d1f072f55c5e625f7a8ba0b5b650ea6a24ec493e906f`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 357.5 KB (357481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892a6f8fa8324bfeb4612f7a42f4557afd5e082b76d6eb091e0de676dc19d26b`  
		Last Modified: Fri, 17 Jan 2025 01:33:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c45ea49c7511c526fac9de55eb8d1ec854cf7c24e175e514d4f76d393a1492f`  
		Last Modified: Fri, 17 Jan 2025 01:33:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e5b7f87ce7df7acc0870faf1a629a49f3f3b7865260274227fe01eb5fbe059`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 19.2 MB (19163659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1792865d58e6d13c7f1f82e4bd2c626a933e6f6a35db76e7a561e7feea4d7313`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc28b08ea10f6f26ceaad44e423332916af104c6c64d5c832f500bc690e15bf`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3b113153c6bc3cc9533ce2cde3d40a1feae4f3c43de591454bc66cabd8b7d6`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab2a02883224978a44c53d67303e6399cfa8291fd4878a7d28d1b9f9c86e0fb`  
		Last Modified: Fri, 17 Jan 2025 01:33:03 GMT  
		Size: 19.6 MB (19646321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9674894f9e36062ebb2d60558e37eb1e25270606e64a963e2154eca16d22a1`  
		Last Modified: Fri, 17 Jan 2025 01:33:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6baac49af4fea3c6c40c4380c6c83141230ecf225b612fef2dcb0860d12bd3`  
		Last Modified: Fri, 17 Jan 2025 01:33:00 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6f04636f816d025e0fcb207436d479348f6902a7b726b00fc0b08c4c91da5`  
		Last Modified: Fri, 17 Jan 2025 01:33:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff25e05ad1368fb78eb59c79e73d3276e7d77771072037ec3e43ca5409067c78`  
		Last Modified: Fri, 17 Jan 2025 01:33:03 GMT  
		Size: 20.2 MB (20169201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:a4691c37ea78600875afbfe9b5f3193ad202961501db79accf2e4169f9b42021
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181529728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1056e0f7366117381694ae8dcdba87d790f109eb17c3d003ef5aef0219256f5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 17 Jan 2025 01:33:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 17 Jan 2025 01:34:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 17 Jan 2025 01:34:31 GMT
ENV DOCKER_VERSION=27.5.0
# Fri, 17 Jan 2025 01:34:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Fri, 17 Jan 2025 01:34:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:34:45 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Fri, 17 Jan 2025 01:34:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Fri, 17 Jan 2025 01:34:46 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Fri, 17 Jan 2025 01:34:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:34:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Fri, 17 Jan 2025 01:34:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Fri, 17 Jan 2025 01:34:58 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Fri, 17 Jan 2025 01:35:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e6274df071a7d5a5db2dfcfdd09b3e5619a6a91cdf7f97ab0e499ce20fbadc`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75379368627062a255445132b6e6f800fa70735daa6088bd9a26716f97d8c20`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 341.5 KB (341471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d991c76af457bbd0d51a6c717c7269b73a45c7241bb22f2ea0a2140d7e5df9b`  
		Last Modified: Fri, 17 Jan 2025 01:35:16 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499d890bbe543c9fa6a376c2cc02860b9d28c3ceb3333573c42123258c044874`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1c11b12baeb8dbd4b7d91eb54b5d14a02ae0cf432615ea004e1e19f8f39c1d`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 19.2 MB (19160387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3235fd67ddd40cdaef5899c144213bba7245b4307f2902f0aebdf497c8d724`  
		Last Modified: Fri, 17 Jan 2025 01:35:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b03c5d4a69994a8004df958ddad06c5afbcc59f276c99989342f8400bf8d7d3`  
		Last Modified: Fri, 17 Jan 2025 01:35:14 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604799b0a87e0da3e79003c6f7f3b8c0ee9f49d2a0fd3da26c55e2d59e5a56ce`  
		Last Modified: Fri, 17 Jan 2025 01:35:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35965d90f9d46033f9e870e8cd2fb5125759d0ab816adacb4c3977e8b124b395`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 19.6 MB (19638065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2795117faa51777ee5591503a846e643112eed007983483a0799b0aba498c98`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e460c490d0afd58b3f2e390983623e89cd4a1f9bafe9b32435fdb41e2c37e99`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54d5078572cf39f63c8f5cc06830bd0716dcc480240b5200491cf747e26c12a`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb52aa115ea25674a9b875dd187041c15e8bd3b155bf96774b70758ad0f61e4`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 20.2 MB (20165876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:3b3e4d8d1726d5fb5d874f245b2d80913ac5431e62e2beed2d21e7966bd16079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:a4691c37ea78600875afbfe9b5f3193ad202961501db79accf2e4169f9b42021
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181529728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1056e0f7366117381694ae8dcdba87d790f109eb17c3d003ef5aef0219256f5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 17 Jan 2025 01:33:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 17 Jan 2025 01:34:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 17 Jan 2025 01:34:31 GMT
ENV DOCKER_VERSION=27.5.0
# Fri, 17 Jan 2025 01:34:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Fri, 17 Jan 2025 01:34:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:34:45 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Fri, 17 Jan 2025 01:34:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Fri, 17 Jan 2025 01:34:46 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Fri, 17 Jan 2025 01:34:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:34:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Fri, 17 Jan 2025 01:34:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Fri, 17 Jan 2025 01:34:58 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Fri, 17 Jan 2025 01:35:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e6274df071a7d5a5db2dfcfdd09b3e5619a6a91cdf7f97ab0e499ce20fbadc`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75379368627062a255445132b6e6f800fa70735daa6088bd9a26716f97d8c20`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 341.5 KB (341471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d991c76af457bbd0d51a6c717c7269b73a45c7241bb22f2ea0a2140d7e5df9b`  
		Last Modified: Fri, 17 Jan 2025 01:35:16 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499d890bbe543c9fa6a376c2cc02860b9d28c3ceb3333573c42123258c044874`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1c11b12baeb8dbd4b7d91eb54b5d14a02ae0cf432615ea004e1e19f8f39c1d`  
		Last Modified: Fri, 17 Jan 2025 01:35:17 GMT  
		Size: 19.2 MB (19160387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3235fd67ddd40cdaef5899c144213bba7245b4307f2902f0aebdf497c8d724`  
		Last Modified: Fri, 17 Jan 2025 01:35:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b03c5d4a69994a8004df958ddad06c5afbcc59f276c99989342f8400bf8d7d3`  
		Last Modified: Fri, 17 Jan 2025 01:35:14 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604799b0a87e0da3e79003c6f7f3b8c0ee9f49d2a0fd3da26c55e2d59e5a56ce`  
		Last Modified: Fri, 17 Jan 2025 01:35:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35965d90f9d46033f9e870e8cd2fb5125759d0ab816adacb4c3977e8b124b395`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 19.6 MB (19638065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2795117faa51777ee5591503a846e643112eed007983483a0799b0aba498c98`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e460c490d0afd58b3f2e390983623e89cd4a1f9bafe9b32435fdb41e2c37e99`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54d5078572cf39f63c8f5cc06830bd0716dcc480240b5200491cf747e26c12a`  
		Last Modified: Fri, 17 Jan 2025 01:35:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb52aa115ea25674a9b875dd187041c15e8bd3b155bf96774b70758ad0f61e4`  
		Last Modified: Fri, 17 Jan 2025 01:35:15 GMT  
		Size: 20.2 MB (20165876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:3bde2a2a6f2192672461cfec2b8264a4927348c274db2b6495e18ce39d141cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:1ddbeca1f26cfd027cd80d7c22a37038dc7a5b749a4cc162893d982e25611f9e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2321733461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa6fd542e3201d9417d1c00e4e8e4ea67053d989ef8279153b1c3c1a73390dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 17 Jan 2025 01:32:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 17 Jan 2025 01:32:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 17 Jan 2025 01:32:29 GMT
ENV DOCKER_VERSION=27.5.0
# Fri, 17 Jan 2025 01:32:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Fri, 17 Jan 2025 01:32:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:32:38 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Fri, 17 Jan 2025 01:32:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Fri, 17 Jan 2025 01:32:40 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Fri, 17 Jan 2025 01:32:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 17 Jan 2025 01:32:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Fri, 17 Jan 2025 01:32:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Fri, 17 Jan 2025 01:32:49 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Fri, 17 Jan 2025 01:32:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a2b5f44002e9945660f33fac78eda870ab26d14af8237ced3f7d6eebafc482`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203a2deeff1a6f93e060d1f072f55c5e625f7a8ba0b5b650ea6a24ec493e906f`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 357.5 KB (357481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892a6f8fa8324bfeb4612f7a42f4557afd5e082b76d6eb091e0de676dc19d26b`  
		Last Modified: Fri, 17 Jan 2025 01:33:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c45ea49c7511c526fac9de55eb8d1ec854cf7c24e175e514d4f76d393a1492f`  
		Last Modified: Fri, 17 Jan 2025 01:33:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e5b7f87ce7df7acc0870faf1a629a49f3f3b7865260274227fe01eb5fbe059`  
		Last Modified: Fri, 17 Jan 2025 01:33:06 GMT  
		Size: 19.2 MB (19163659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1792865d58e6d13c7f1f82e4bd2c626a933e6f6a35db76e7a561e7feea4d7313`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc28b08ea10f6f26ceaad44e423332916af104c6c64d5c832f500bc690e15bf`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3b113153c6bc3cc9533ce2cde3d40a1feae4f3c43de591454bc66cabd8b7d6`  
		Last Modified: Fri, 17 Jan 2025 01:33:02 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab2a02883224978a44c53d67303e6399cfa8291fd4878a7d28d1b9f9c86e0fb`  
		Last Modified: Fri, 17 Jan 2025 01:33:03 GMT  
		Size: 19.6 MB (19646321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9674894f9e36062ebb2d60558e37eb1e25270606e64a963e2154eca16d22a1`  
		Last Modified: Fri, 17 Jan 2025 01:33:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6baac49af4fea3c6c40c4380c6c83141230ecf225b612fef2dcb0860d12bd3`  
		Last Modified: Fri, 17 Jan 2025 01:33:00 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6f04636f816d025e0fcb207436d479348f6902a7b726b00fc0b08c4c91da5`  
		Last Modified: Fri, 17 Jan 2025 01:33:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff25e05ad1368fb78eb59c79e73d3276e7d77771072037ec3e43ca5409067c78`  
		Last Modified: Fri, 17 Jan 2025 01:33:03 GMT  
		Size: 20.2 MB (20169201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
