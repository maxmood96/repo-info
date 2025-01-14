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
$ docker pull docker@sha256:3c8fb358b82767a38189e54a89a2ba8d71109f0a17efa87fd009ef8283c46df6
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
$ docker pull docker@sha256:49e6ff5ed3f0137c76b051de305780c16f03b9bd17fec1244808194c9e823b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133457249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0ad917400429d6dea8ffbfb4937b3319f86da6ba149904d9a6ed3de27ed40c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9da8d98be9c497538e046636271095d60600736b8b98dd17d89b85cf6750a8f`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 8.1 MB (8058734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4386589b6f3f3d4248a89850307f7fce69767219761e159ae96376e95133648c`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a489f3b5fec0148d769933a6c683cf67788489232797ba6b97cedc28fba6e83`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 18.7 MB (18669947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098516bf325695b24ce2974045b3ddb5dcdb829015737c0bed7a538be5456ee1`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 18.8 MB (18798865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5bc19395419c3a98f4744b34640d249289415e1edb1e030bf6a58333628592`  
		Last Modified: Thu, 09 Jan 2025 22:28:46 GMT  
		Size: 19.3 MB (19308702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9611a6289157d3d5da09d21f919439c1d7f75f52c4f1c86ee4935487625980c6`  
		Last Modified: Thu, 09 Jan 2025 22:28:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380e7224928097502689c0c3e6dd922dbca5bceb3e5e249123e5b0ce9d13ecde`  
		Last Modified: Thu, 09 Jan 2025 22:28:46 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc6c2a895485e0e9ccb5a3268ffe8ca41f9b3ef6e932337b94f7591126ae90f`  
		Last Modified: Thu, 09 Jan 2025 22:28:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccd10a0d08c0066160d5b279905caebe908957991b637d7293112c10f9254a6`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 6.7 MB (6733477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4e953c13592b855fe5ac2c004028573ca254b3b449c693253578413529b596`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 89.4 KB (89423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf11bfad06271553522156c7166b33e0624501d3119499ef1f46a9d203dc51c3`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fa1d5b8c62c41eb58aeb44f3d2802853db92ca56374ec46745e1ad274a660e`  
		Last Modified: Thu, 09 Jan 2025 23:09:51 GMT  
		Size: 58.1 MB (58148440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1922b615ab4786237b943630fce1b166e2d302351e86e3119f4ae440f7b7905`  
		Last Modified: Thu, 09 Jan 2025 23:09:51 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b317a0873086e41961b65278ad4f6754bd4f730f99945c89f43bb766f5a491d8`  
		Last Modified: Thu, 09 Jan 2025 23:09:51 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:cc1d4784142745c9b47911162f779031f55fc37b7eda97a59f41955920e24a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94905195960a1412761e9794cf2ecd9e83058b3550a91fa562a0a652c558748`

```dockerfile
```

-	Layers:
	-	`sha256:2675d6a7be39c97d9c9690e58c9765ec5bca8b3e2b9e5c3fb868b17da42f207f`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v6

```console
$ docker pull docker@sha256:1f43d24f4b7e21e4b8ec633437279807fac93d6da1d8c1034219ce24d3166c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124584943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac030345b438a7667a295dd56d5c7abc875bd22d1eb08553b257069de82d4a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
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
	-	`sha256:cf73d7cc46a3267dcec3cfc7f304f1abf870c9ecbd6d90f397551be5eff00ae6`  
		Last Modified: Wed, 08 Jan 2025 18:20:41 GMT  
		Size: 16.7 MB (16706472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c7eea2794b482866fb44247a621611bd3105b4f590ec047a41cac4d623e08f`  
		Last Modified: Wed, 08 Jan 2025 18:20:41 GMT  
		Size: 17.4 MB (17448777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16db69aa77862f611701d543dad7e67909f47fcd5d9a9574b9f97a11ba983d29`  
		Last Modified: Thu, 09 Jan 2025 22:30:31 GMT  
		Size: 18.1 MB (18117040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc79f3781d43c0acb2321b1a5716529ab8dd5ef7077e18b0c58a7671854782d`  
		Last Modified: Thu, 09 Jan 2025 22:30:30 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0c94e4fa8de6f36d61b3f90d7d24a03d4c0adcf54276f3abd0226ed166a03e`  
		Last Modified: Thu, 09 Jan 2025 22:30:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9240b077258b7ccef62b5cb88015fe3861991b7dbb7e3205cc5bdb5b0e9e62a`  
		Last Modified: Thu, 09 Jan 2025 22:30:30 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4320f12f1df4243ec5345fea61730e028969bc9c2e48db250684f019bbc71204`  
		Last Modified: Thu, 09 Jan 2025 23:09:43 GMT  
		Size: 7.0 MB (7041225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136ce7681116932314215ea74a5c2a1ec992dcb2806b22a8adb1ad624d1ace6c`  
		Last Modified: Thu, 09 Jan 2025 23:09:42 GMT  
		Size: 89.1 KB (89081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede844aa6bf08e33cbf33b8ab3d54a83218ada675b1e41dcc27dc06c15770f1e`  
		Last Modified: Thu, 09 Jan 2025 23:09:42 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b84dba6d364e19485ec2c81348af1224c45bf5d5d14f699ceb37e3a5a0603e`  
		Last Modified: Thu, 09 Jan 2025 23:09:44 GMT  
		Size: 53.8 MB (53837600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d54dd5266f2a390068c556eb150d4af862281da4aac8d5ea4b283aee2a78af5`  
		Last Modified: Thu, 09 Jan 2025 23:09:43 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3861e2840ecc26375f926f01a8d3eac81da62f6cb2b6e253a6b618333de650be`  
		Last Modified: Thu, 09 Jan 2025 23:09:43 GMT  
		Size: 3.3 KB (3267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:df2dac21f9fd059948ecd5332d14a694d17dcdf7a81cd945b0cb17ff3af8289e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f5f1dd987e3f8758b1531674eb3bd13f84ec122a17691372a7ffe3b93300fe`

```dockerfile
```

-	Layers:
	-	`sha256:44a65346f729ddd7e3c711f15bfc80de482b0a9bc76a38a130411c8049b6372d`  
		Last Modified: Thu, 09 Jan 2025 23:09:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v7

```console
$ docker pull docker@sha256:6c2e036e5e3571aefcfe6cc0ef1dec1ea8ad723a6b68692c17c778588bcb3280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122910186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b1979896efc6f276834731288c136dfcec5c72d40df0380f41303601316421`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
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
	-	`sha256:b346517794cfce1f41b95c705ae9e23769f0eead55b0e45aa310726d624d7e36`  
		Last Modified: Thu, 09 Jan 2025 22:31:30 GMT  
		Size: 16.7 MB (16694613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8af6fe42dd3bd1002a36a0678d7433d5bc1c9b65222d55d1be8f669b50d50ad`  
		Last Modified: Thu, 09 Jan 2025 22:31:30 GMT  
		Size: 17.4 MB (17427581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435b00e153eefddcfb5674d73a4be8017ab0cbee851a5bd11e33016e9b8b8fcc`  
		Last Modified: Thu, 09 Jan 2025 22:31:30 GMT  
		Size: 18.1 MB (18098994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823050d528d8277f11b4566a452e8b76b5e7d7097577342b3d85675aa1f28`  
		Last Modified: Thu, 09 Jan 2025 22:31:29 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fba272fee8435a6f01afdef863fc92b288e2e33bb5d72e633c48abeb1c9967`  
		Last Modified: Thu, 09 Jan 2025 22:31:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4a813131a303def688ad87697fb38ee2b0db911fc22611c905ded3e13d49c4`  
		Last Modified: Thu, 09 Jan 2025 22:31:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa0618922e6709169133b10f595ba8793b03f956a1c7d131890749d66bd336b`  
		Last Modified: Thu, 09 Jan 2025 23:09:55 GMT  
		Size: 6.4 MB (6367220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0a7426d34ab170c52bd4868bf7b90982d98d298f325aba23a37262ee806418`  
		Last Modified: Thu, 09 Jan 2025 23:09:54 GMT  
		Size: 85.2 KB (85224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc89450f6e7f80827ca9f053ec7083fa5e47f3c10f571ce54b8040407058b90c`  
		Last Modified: Thu, 09 Jan 2025 23:09:54 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443963719d80b474f394eb3661e099fd0571d87e95d7d197e87543e1e4366769`  
		Last Modified: Thu, 09 Jan 2025 23:09:56 GMT  
		Size: 53.8 MB (53837561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf03937475f71182a6a712879c07c398b3f9c57b1e0de7af4132cfdea614103`  
		Last Modified: Thu, 09 Jan 2025 23:09:55 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71964f6ba278659ffb392cbd74eb102105929fb5003906d8cf4d49b8a13eff32`  
		Last Modified: Thu, 09 Jan 2025 23:09:55 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:537d0bfd92a4fd1d6a1762140e72d9296020996bd4286ac948043a25512c71c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3f3f3334c8bbb35e6980553891309aa4b5e829d2b3cf9600a7d799d46f6154`

```dockerfile
```

-	Layers:
	-	`sha256:5d7cc935cb72609d8dda009220f97c687934bca9466138209cf43e28b4ae0c23`  
		Last Modified: Thu, 09 Jan 2025 23:09:54 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e39c2cc3c90814aab0b980fbe31a46c46ccd326a31a954aec10b08e17a00f636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125270256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85d4f06cded869b75594119c992d1934951663e005b7b0fbfd21c6ccc18a544`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3528552267cec0f9e2dee7d372df3bbea6255a3ca1a18ba3e58e5cfd106d15e1`  
		Last Modified: Thu, 09 Jan 2025 22:29:23 GMT  
		Size: 8.1 MB (8073134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4781719ef357b2c136f17ff57b79d601b4058a8861d68048cf902106cf3ae9d`  
		Last Modified: Thu, 09 Jan 2025 22:29:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4866b03f4ce1c603a6809790707aae8972781d4ff1b1090b3960153b3abec1e0`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.6 MB (17619398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d036bb2a7049761d033d283b4bc752d8e2d6e25b9ea4bf4329e6a7055ad82e`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.1 MB (17106450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4fa20503c91c2405741c5b1d40f5567a7c641a4624b6c0693716eb0fa6752e`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.7 MB (17653961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f999290013a7bee6f7b09186deee9dc98564604594aac128b7293ef882edfd34`  
		Last Modified: Thu, 09 Jan 2025 22:29:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dca40438acce378f07676329455acd2969680d9ceeeee33d5f34cb1f06c2f4`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730c1436b4a8c8addd307436381ccbe5d3d3adf57e2b67228ea624046c0f4997`  
		Last Modified: Thu, 09 Jan 2025 22:29:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aed778d4d37e95ff4fef9353934ac33be3d14475532284512418c3c7e8802ea`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 7.0 MB (6981951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2357ac4e3b4ca2ae4efd996c265963976e946d8abe41868260f6fc228d6e6cc4`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 97.8 KB (97785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f2dd98d7754adf87dda19dcbdb3a884046d0c27693b4d9c3465c4ae77eca5c`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af42edc6d44256189864a2f5cf56c06590a42e61aeb9f18a2c453de7841076b0`  
		Last Modified: Thu, 09 Jan 2025 23:09:59 GMT  
		Size: 53.7 MB (53737271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518ad24d587855579d9d75a11a4e2b7e0c347114c536d13580a4ea61bde47f9`  
		Last Modified: Thu, 09 Jan 2025 23:09:58 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbdc874d308be16b20915161093ad9bf64226aace0cc1e4a6c39989bc8b42e8`  
		Last Modified: Thu, 09 Jan 2025 23:09:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:3c55cbc4001fb31954e54c34ad17b6c51d156dec418ed2d5227cde645a42dd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae631f8a48e90d1da91e6ad880706bd056becca1725a0b75bcb80783f4aba81`

```dockerfile
```

-	Layers:
	-	`sha256:3a2a24b3e925024d6bde4094ebc288eba2297cf6906eda280f8e1e4735abed3a`  
		Last Modified: Thu, 09 Jan 2025 23:09:56 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-cli`

```console
$ docker pull docker@sha256:77484994bf967c63acbaf60b16491ca18ceb4c5895b4d63d4a25a92d1a496984
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
$ docker pull docker@sha256:079cb70986454a74835b387f76c7aac60261ea12110335cb4a6de4f0c2cfafca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68654583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118ba116e4cc60717257588cf15e365499e33eae2c96f3591484acd65f52d902`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-x86_64'; 			sha256='6ef48e4bf25fbf1f1ad50c43b797cc24e12e4cde29765076b4145e09e35f5713'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv6'; 			sha256='8f415a76ad62ff621b26b37a94841ee0d4480862d8da55320c1c8fc9db4d8359'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv7'; 			sha256='64314c73a7d34e4a8b9dad87bab857304fb60b0293703d02be436893e1c37f33'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-aarch64'; 			sha256='d1a04a3eb7fd738cc78e518d179a03adb9fe531ee422b8a14bdccf36d654b73a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-ppc64le'; 			sha256='23bddc8119bce6c0eeef1461bc0526291d60de9042b28780012033ba4082090e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-riscv64'; 			sha256='c4bac574a2123938de4ef410e7cef92d079abe266298c93257cbcc4e17134184'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-s390x'; 			sha256='6c0c7d9b6119f68b3dcbf816cf9e5782eb7cea8d2433f8a51b95a41276241e18'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2147a509bdeadcb92898e60247f4658852a925a4962e0e29a2d28fcfe83e81`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 8.1 MB (8058755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386023837c56d9b33f3b3c560d987a4d0afffaa2025b6bdb05dbb812ba5fd84d`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ec2a25f188dfb7b2d0d15b2f51239ab8694502bca535fd3c2ceccb359fd868`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 18.8 MB (18849469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47c11d47744bce1446bbff20430a7058587389836041cbda659967ba94b3653`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 18.8 MB (18798855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e324137ff7d6aef2c4fe2746097ee8c2ccfc69735be66123a60f1d9286e99c`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 19.3 MB (19303637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae739ff5a469e4fc30b28a279acac08ee7a9c6f40cee72753bf1cde14f2ea88`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c082b27e013c5d92e5f5698a5eb8564358982c6a8fcd01667c5e16e05499363`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1341245cb0ac938576ee4968bde808b58406e6dc5bad00b169e1584bd79a37`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0834e294409cfea3b7383723da66c834024db808b8f4eb540634fbeb35bd3554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8adc850415b3d1dc2eff9e582890566fe2d56c76cb9ad1d841bca8b83d1275`

```dockerfile
```

-	Layers:
	-	`sha256:e1482745bc132620b8f783302f61bde33791e940048e70d192e1b98b15b225ef`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:39401ed362b2c67e9ac62f3e5710570ab18e024cfc5f565aa517d3094afff38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63766331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2cf88b9b43fcd7963f15edfb83fe97afd5fdb4a84c0c9550747fef06027b2f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-x86_64'; 			sha256='6ef48e4bf25fbf1f1ad50c43b797cc24e12e4cde29765076b4145e09e35f5713'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv6'; 			sha256='8f415a76ad62ff621b26b37a94841ee0d4480862d8da55320c1c8fc9db4d8359'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv7'; 			sha256='64314c73a7d34e4a8b9dad87bab857304fb60b0293703d02be436893e1c37f33'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-aarch64'; 			sha256='d1a04a3eb7fd738cc78e518d179a03adb9fe531ee422b8a14bdccf36d654b73a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-ppc64le'; 			sha256='23bddc8119bce6c0eeef1461bc0526291d60de9042b28780012033ba4082090e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-riscv64'; 			sha256='c4bac574a2123938de4ef410e7cef92d079abe266298c93257cbcc4e17134184'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-s390x'; 			sha256='6c0c7d9b6119f68b3dcbf816cf9e5782eb7cea8d2433f8a51b95a41276241e18'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:b5efa4ecc356aa3f967cf3252f33f35689d69748ad15f6ab382dfbc77e53db68`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 18.1 MB (18112377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8980aece4ef386b0d4c63fa11ec664751daa90f6c5144d7ee6983e0f66a321b`  
		Last Modified: Tue, 14 Jan 2025 01:36:24 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999f06d4f41595fc49c1bbb9b00b3cd4f91965126bb974d09c572be01729d08b`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8b82c0cdef43fe4b7645f72f8fe205f6a146384aa0b8c2e73839234796ffc0`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2b97a1b68497256fc60402e3f5abdb7fb6ab5225d56c1fc671133f2e941c5062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2440854a0cd314cf190b2a6a09c7df59ee4e688a46b9c67324944a7cee09901`

```dockerfile
```

-	Layers:
	-	`sha256:4691173ba00bf555533f59934544855695b5d6d51bba5d12e6194b963a43d6a4`  
		Last Modified: Tue, 14 Jan 2025 01:36:24 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:5e71e6f4cd87cadb9d0f89cbeb32a7687ee1e49f84c428f371c3c33d65ca1254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62614380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eae7261d9a104837a54d4a9ba6a157b650b261e83424ef011bdfe7c14a47a27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 18:50:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Jan 2025 18:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Jan 2025 18:50:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Jan 2025 18:50:16 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 08 Jan 2025 18:50:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Jan 2025 18:50:16 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 08 Jan 2025 18:50:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Jan 2025 18:50:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 08 Jan 2025 18:50:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Jan 2025 18:50:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Jan 2025 18:50:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 18:50:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Jan 2025 18:50:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Jan 2025 18:50:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Jan 2025 18:50:16 GMT
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
	-	`sha256:b346517794cfce1f41b95c705ae9e23769f0eead55b0e45aa310726d624d7e36`  
		Last Modified: Thu, 09 Jan 2025 22:31:30 GMT  
		Size: 16.7 MB (16694613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8af6fe42dd3bd1002a36a0678d7433d5bc1c9b65222d55d1be8f669b50d50ad`  
		Last Modified: Thu, 09 Jan 2025 22:31:30 GMT  
		Size: 17.4 MB (17427581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435b00e153eefddcfb5674d73a4be8017ab0cbee851a5bd11e33016e9b8b8fcc`  
		Last Modified: Thu, 09 Jan 2025 22:31:30 GMT  
		Size: 18.1 MB (18098994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823050d528d8277f11b4566a452e8b76b5e7d7097577342b3d85675aa1f28`  
		Last Modified: Thu, 09 Jan 2025 22:31:29 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fba272fee8435a6f01afdef863fc92b288e2e33bb5d72e633c48abeb1c9967`  
		Last Modified: Thu, 09 Jan 2025 22:31:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4a813131a303def688ad87697fb38ee2b0db911fc22611c905ded3e13d49c4`  
		Last Modified: Thu, 09 Jan 2025 22:31:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:cb6dd5588f0d803d295eed89ded056f5735647bfc9589719d79a64463bb1026d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f060462a83aae9ea7f421874df7e391e459030d30bdf354941fe07ac344be092`

```dockerfile
```

-	Layers:
	-	`sha256:f4c1a16de2a45d8d90746fee23d460d04552b46abb5be4ff308f197dc56d4850`  
		Last Modified: Thu, 09 Jan 2025 22:31:29 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c50766834094413ee0950a29b198399229423316f3fc981748adcec98e9ab775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64619543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62380b06f7e73d08c2f8cc69cf22e68b8b0964d4e943cd7902edebf72bdb8861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-x86_64'; 			sha256='6ef48e4bf25fbf1f1ad50c43b797cc24e12e4cde29765076b4145e09e35f5713'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv6'; 			sha256='8f415a76ad62ff621b26b37a94841ee0d4480862d8da55320c1c8fc9db4d8359'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv7'; 			sha256='64314c73a7d34e4a8b9dad87bab857304fb60b0293703d02be436893e1c37f33'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-aarch64'; 			sha256='d1a04a3eb7fd738cc78e518d179a03adb9fe531ee422b8a14bdccf36d654b73a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-ppc64le'; 			sha256='23bddc8119bce6c0eeef1461bc0526291d60de9042b28780012033ba4082090e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-riscv64'; 			sha256='c4bac574a2123938de4ef410e7cef92d079abe266298c93257cbcc4e17134184'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-s390x'; 			sha256='6c0c7d9b6119f68b3dcbf816cf9e5782eb7cea8d2433f8a51b95a41276241e18'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43785ac1a9e530c3cf3f5502efdd8eb2ca0fe74ce2e9dacfcf49cc1cd44ff5b`  
		Last Modified: Tue, 14 Jan 2025 01:40:05 GMT  
		Size: 8.1 MB (8073121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443e45b7ebe0d6fed7d323b8c918357ccec700454ec81770dd307b744905bef2`  
		Last Modified: Tue, 14 Jan 2025 01:40:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1042953f4da92c640616f959f1c17179c50b5bcbb6bdc9f894f38b4278d5db46`  
		Last Modified: Tue, 14 Jan 2025 01:40:05 GMT  
		Size: 17.8 MB (17795750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595709626d52a6ebd1b0e6f2f42977b3d1eb93f23dc20f0fcff5189182226760`  
		Last Modified: Tue, 14 Jan 2025 01:40:05 GMT  
		Size: 17.1 MB (17106450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748acb43c50f1bb7dbea6130ec9107d0f49825c28b2980022cab395526b50be`  
		Last Modified: Tue, 14 Jan 2025 01:40:08 GMT  
		Size: 17.6 MB (17649713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1870e6ecb9e9730d191ac6aa59e5347eebf36c4df5f1c731a00f2cd2d8f504cf`  
		Last Modified: Tue, 14 Jan 2025 01:40:06 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728bbf9b069189d2d739494cb11a3a541b0f53c1e6432d25588228efc0061360`  
		Last Modified: Tue, 14 Jan 2025 01:40:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0dce1ac1b31cc57ce7e0e566085cadacde994d75882f409fd806190989973c`  
		Last Modified: Tue, 14 Jan 2025 01:40:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:aa5987741b6bbf500dfd9175af5800e5d87ba69bba7bb90c4696491570a18d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084c240dfaf22b97381310758a9c28cce3af37c241e02dc7457710416ed68324`

```dockerfile
```

-	Layers:
	-	`sha256:37e6330f383c6a94d354a35890b299d12ffd73c15f1b5691ea42a5bf6bd7c1c6`  
		Last Modified: Tue, 14 Jan 2025 01:40:04 GMT  
		Size: 38.3 KB (38321 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind`

```console
$ docker pull docker@sha256:3c8fb358b82767a38189e54a89a2ba8d71109f0a17efa87fd009ef8283c46df6
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
$ docker pull docker@sha256:49e6ff5ed3f0137c76b051de305780c16f03b9bd17fec1244808194c9e823b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133457249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0ad917400429d6dea8ffbfb4937b3319f86da6ba149904d9a6ed3de27ed40c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9da8d98be9c497538e046636271095d60600736b8b98dd17d89b85cf6750a8f`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 8.1 MB (8058734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4386589b6f3f3d4248a89850307f7fce69767219761e159ae96376e95133648c`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a489f3b5fec0148d769933a6c683cf67788489232797ba6b97cedc28fba6e83`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 18.7 MB (18669947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098516bf325695b24ce2974045b3ddb5dcdb829015737c0bed7a538be5456ee1`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 18.8 MB (18798865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5bc19395419c3a98f4744b34640d249289415e1edb1e030bf6a58333628592`  
		Last Modified: Thu, 09 Jan 2025 22:28:46 GMT  
		Size: 19.3 MB (19308702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9611a6289157d3d5da09d21f919439c1d7f75f52c4f1c86ee4935487625980c6`  
		Last Modified: Thu, 09 Jan 2025 22:28:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380e7224928097502689c0c3e6dd922dbca5bceb3e5e249123e5b0ce9d13ecde`  
		Last Modified: Thu, 09 Jan 2025 22:28:46 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc6c2a895485e0e9ccb5a3268ffe8ca41f9b3ef6e932337b94f7591126ae90f`  
		Last Modified: Thu, 09 Jan 2025 22:28:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccd10a0d08c0066160d5b279905caebe908957991b637d7293112c10f9254a6`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 6.7 MB (6733477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4e953c13592b855fe5ac2c004028573ca254b3b449c693253578413529b596`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 89.4 KB (89423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf11bfad06271553522156c7166b33e0624501d3119499ef1f46a9d203dc51c3`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fa1d5b8c62c41eb58aeb44f3d2802853db92ca56374ec46745e1ad274a660e`  
		Last Modified: Thu, 09 Jan 2025 23:09:51 GMT  
		Size: 58.1 MB (58148440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1922b615ab4786237b943630fce1b166e2d302351e86e3119f4ae440f7b7905`  
		Last Modified: Thu, 09 Jan 2025 23:09:51 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b317a0873086e41961b65278ad4f6754bd4f730f99945c89f43bb766f5a491d8`  
		Last Modified: Thu, 09 Jan 2025 23:09:51 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:cc1d4784142745c9b47911162f779031f55fc37b7eda97a59f41955920e24a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94905195960a1412761e9794cf2ecd9e83058b3550a91fa562a0a652c558748`

```dockerfile
```

-	Layers:
	-	`sha256:2675d6a7be39c97d9c9690e58c9765ec5bca8b3e2b9e5c3fb868b17da42f207f`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:1f43d24f4b7e21e4b8ec633437279807fac93d6da1d8c1034219ce24d3166c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124584943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac030345b438a7667a295dd56d5c7abc875bd22d1eb08553b257069de82d4a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
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
	-	`sha256:cf73d7cc46a3267dcec3cfc7f304f1abf870c9ecbd6d90f397551be5eff00ae6`  
		Last Modified: Wed, 08 Jan 2025 18:20:41 GMT  
		Size: 16.7 MB (16706472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c7eea2794b482866fb44247a621611bd3105b4f590ec047a41cac4d623e08f`  
		Last Modified: Wed, 08 Jan 2025 18:20:41 GMT  
		Size: 17.4 MB (17448777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16db69aa77862f611701d543dad7e67909f47fcd5d9a9574b9f97a11ba983d29`  
		Last Modified: Thu, 09 Jan 2025 22:30:31 GMT  
		Size: 18.1 MB (18117040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc79f3781d43c0acb2321b1a5716529ab8dd5ef7077e18b0c58a7671854782d`  
		Last Modified: Thu, 09 Jan 2025 22:30:30 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0c94e4fa8de6f36d61b3f90d7d24a03d4c0adcf54276f3abd0226ed166a03e`  
		Last Modified: Thu, 09 Jan 2025 22:30:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9240b077258b7ccef62b5cb88015fe3861991b7dbb7e3205cc5bdb5b0e9e62a`  
		Last Modified: Thu, 09 Jan 2025 22:30:30 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4320f12f1df4243ec5345fea61730e028969bc9c2e48db250684f019bbc71204`  
		Last Modified: Thu, 09 Jan 2025 23:09:43 GMT  
		Size: 7.0 MB (7041225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136ce7681116932314215ea74a5c2a1ec992dcb2806b22a8adb1ad624d1ace6c`  
		Last Modified: Thu, 09 Jan 2025 23:09:42 GMT  
		Size: 89.1 KB (89081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede844aa6bf08e33cbf33b8ab3d54a83218ada675b1e41dcc27dc06c15770f1e`  
		Last Modified: Thu, 09 Jan 2025 23:09:42 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b84dba6d364e19485ec2c81348af1224c45bf5d5d14f699ceb37e3a5a0603e`  
		Last Modified: Thu, 09 Jan 2025 23:09:44 GMT  
		Size: 53.8 MB (53837600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d54dd5266f2a390068c556eb150d4af862281da4aac8d5ea4b283aee2a78af5`  
		Last Modified: Thu, 09 Jan 2025 23:09:43 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3861e2840ecc26375f926f01a8d3eac81da62f6cb2b6e253a6b618333de650be`  
		Last Modified: Thu, 09 Jan 2025 23:09:43 GMT  
		Size: 3.3 KB (3267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:df2dac21f9fd059948ecd5332d14a694d17dcdf7a81cd945b0cb17ff3af8289e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f5f1dd987e3f8758b1531674eb3bd13f84ec122a17691372a7ffe3b93300fe`

```dockerfile
```

-	Layers:
	-	`sha256:44a65346f729ddd7e3c711f15bfc80de482b0a9bc76a38a130411c8049b6372d`  
		Last Modified: Thu, 09 Jan 2025 23:09:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:6c2e036e5e3571aefcfe6cc0ef1dec1ea8ad723a6b68692c17c778588bcb3280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122910186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b1979896efc6f276834731288c136dfcec5c72d40df0380f41303601316421`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
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
	-	`sha256:b346517794cfce1f41b95c705ae9e23769f0eead55b0e45aa310726d624d7e36`  
		Last Modified: Thu, 09 Jan 2025 22:31:30 GMT  
		Size: 16.7 MB (16694613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8af6fe42dd3bd1002a36a0678d7433d5bc1c9b65222d55d1be8f669b50d50ad`  
		Last Modified: Thu, 09 Jan 2025 22:31:30 GMT  
		Size: 17.4 MB (17427581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435b00e153eefddcfb5674d73a4be8017ab0cbee851a5bd11e33016e9b8b8fcc`  
		Last Modified: Thu, 09 Jan 2025 22:31:30 GMT  
		Size: 18.1 MB (18098994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823050d528d8277f11b4566a452e8b76b5e7d7097577342b3d85675aa1f28`  
		Last Modified: Thu, 09 Jan 2025 22:31:29 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fba272fee8435a6f01afdef863fc92b288e2e33bb5d72e633c48abeb1c9967`  
		Last Modified: Thu, 09 Jan 2025 22:31:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4a813131a303def688ad87697fb38ee2b0db911fc22611c905ded3e13d49c4`  
		Last Modified: Thu, 09 Jan 2025 22:31:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa0618922e6709169133b10f595ba8793b03f956a1c7d131890749d66bd336b`  
		Last Modified: Thu, 09 Jan 2025 23:09:55 GMT  
		Size: 6.4 MB (6367220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0a7426d34ab170c52bd4868bf7b90982d98d298f325aba23a37262ee806418`  
		Last Modified: Thu, 09 Jan 2025 23:09:54 GMT  
		Size: 85.2 KB (85224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc89450f6e7f80827ca9f053ec7083fa5e47f3c10f571ce54b8040407058b90c`  
		Last Modified: Thu, 09 Jan 2025 23:09:54 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443963719d80b474f394eb3661e099fd0571d87e95d7d197e87543e1e4366769`  
		Last Modified: Thu, 09 Jan 2025 23:09:56 GMT  
		Size: 53.8 MB (53837561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf03937475f71182a6a712879c07c398b3f9c57b1e0de7af4132cfdea614103`  
		Last Modified: Thu, 09 Jan 2025 23:09:55 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71964f6ba278659ffb392cbd74eb102105929fb5003906d8cf4d49b8a13eff32`  
		Last Modified: Thu, 09 Jan 2025 23:09:55 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:537d0bfd92a4fd1d6a1762140e72d9296020996bd4286ac948043a25512c71c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3f3f3334c8bbb35e6980553891309aa4b5e829d2b3cf9600a7d799d46f6154`

```dockerfile
```

-	Layers:
	-	`sha256:5d7cc935cb72609d8dda009220f97c687934bca9466138209cf43e28b4ae0c23`  
		Last Modified: Thu, 09 Jan 2025 23:09:54 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e39c2cc3c90814aab0b980fbe31a46c46ccd326a31a954aec10b08e17a00f636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125270256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85d4f06cded869b75594119c992d1934951663e005b7b0fbfd21c6ccc18a544`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3528552267cec0f9e2dee7d372df3bbea6255a3ca1a18ba3e58e5cfd106d15e1`  
		Last Modified: Thu, 09 Jan 2025 22:29:23 GMT  
		Size: 8.1 MB (8073134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4781719ef357b2c136f17ff57b79d601b4058a8861d68048cf902106cf3ae9d`  
		Last Modified: Thu, 09 Jan 2025 22:29:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4866b03f4ce1c603a6809790707aae8972781d4ff1b1090b3960153b3abec1e0`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.6 MB (17619398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d036bb2a7049761d033d283b4bc752d8e2d6e25b9ea4bf4329e6a7055ad82e`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.1 MB (17106450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4fa20503c91c2405741c5b1d40f5567a7c641a4624b6c0693716eb0fa6752e`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.7 MB (17653961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f999290013a7bee6f7b09186deee9dc98564604594aac128b7293ef882edfd34`  
		Last Modified: Thu, 09 Jan 2025 22:29:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dca40438acce378f07676329455acd2969680d9ceeeee33d5f34cb1f06c2f4`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730c1436b4a8c8addd307436381ccbe5d3d3adf57e2b67228ea624046c0f4997`  
		Last Modified: Thu, 09 Jan 2025 22:29:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aed778d4d37e95ff4fef9353934ac33be3d14475532284512418c3c7e8802ea`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 7.0 MB (6981951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2357ac4e3b4ca2ae4efd996c265963976e946d8abe41868260f6fc228d6e6cc4`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 97.8 KB (97785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f2dd98d7754adf87dda19dcbdb3a884046d0c27693b4d9c3465c4ae77eca5c`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af42edc6d44256189864a2f5cf56c06590a42e61aeb9f18a2c453de7841076b0`  
		Last Modified: Thu, 09 Jan 2025 23:09:59 GMT  
		Size: 53.7 MB (53737271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518ad24d587855579d9d75a11a4e2b7e0c347114c536d13580a4ea61bde47f9`  
		Last Modified: Thu, 09 Jan 2025 23:09:58 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbdc874d308be16b20915161093ad9bf64226aace0cc1e4a6c39989bc8b42e8`  
		Last Modified: Thu, 09 Jan 2025 23:09:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3c55cbc4001fb31954e54c34ad17b6c51d156dec418ed2d5227cde645a42dd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae631f8a48e90d1da91e6ad880706bd056becca1725a0b75bcb80783f4aba81`

```dockerfile
```

-	Layers:
	-	`sha256:3a2a24b3e925024d6bde4094ebc288eba2297cf6906eda280f8e1e4735abed3a`  
		Last Modified: Thu, 09 Jan 2025 23:09:56 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:3e770a24d3b2b21cfe6bf4f163a3989369235d2e26d47da14e719df3d5539dda
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:7c17ce13c8e0d7d22974ac948f6e11199b70ad2a7161443daba306d989c6833a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155749030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6dc42df64f885d426d42c6985a30d33978f9c04f3bd748919a851b6eec8d81e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD []
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
USER rootless
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9da8d98be9c497538e046636271095d60600736b8b98dd17d89b85cf6750a8f`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 8.1 MB (8058734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4386589b6f3f3d4248a89850307f7fce69767219761e159ae96376e95133648c`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a489f3b5fec0148d769933a6c683cf67788489232797ba6b97cedc28fba6e83`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 18.7 MB (18669947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098516bf325695b24ce2974045b3ddb5dcdb829015737c0bed7a538be5456ee1`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 18.8 MB (18798865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5bc19395419c3a98f4744b34640d249289415e1edb1e030bf6a58333628592`  
		Last Modified: Thu, 09 Jan 2025 22:28:46 GMT  
		Size: 19.3 MB (19308702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9611a6289157d3d5da09d21f919439c1d7f75f52c4f1c86ee4935487625980c6`  
		Last Modified: Thu, 09 Jan 2025 22:28:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380e7224928097502689c0c3e6dd922dbca5bceb3e5e249123e5b0ce9d13ecde`  
		Last Modified: Thu, 09 Jan 2025 22:28:46 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc6c2a895485e0e9ccb5a3268ffe8ca41f9b3ef6e932337b94f7591126ae90f`  
		Last Modified: Thu, 09 Jan 2025 22:28:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccd10a0d08c0066160d5b279905caebe908957991b637d7293112c10f9254a6`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 6.7 MB (6733477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4e953c13592b855fe5ac2c004028573ca254b3b449c693253578413529b596`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 89.4 KB (89423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf11bfad06271553522156c7166b33e0624501d3119499ef1f46a9d203dc51c3`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fa1d5b8c62c41eb58aeb44f3d2802853db92ca56374ec46745e1ad274a660e`  
		Last Modified: Thu, 09 Jan 2025 23:09:51 GMT  
		Size: 58.1 MB (58148440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1922b615ab4786237b943630fce1b166e2d302351e86e3119f4ae440f7b7905`  
		Last Modified: Thu, 09 Jan 2025 23:09:51 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b317a0873086e41961b65278ad4f6754bd4f730f99945c89f43bb766f5a491d8`  
		Last Modified: Thu, 09 Jan 2025 23:09:51 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db5e91f12b0771939beaf1d2267459f2493824d96a199c6f2cfc2e9e1ad2b20`  
		Last Modified: Fri, 10 Jan 2025 00:07:37 GMT  
		Size: 986.6 KB (986560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f3c2a2ccc5c1c0c6b9a8bffbb7ad2f411aa048317f413b2e763c21a397d559`  
		Last Modified: Fri, 10 Jan 2025 00:07:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdccb280e79d0701bb90ad2b947a87729d781ade93dbcb32c8638605f70de0e`  
		Last Modified: Fri, 10 Jan 2025 00:07:37 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cac4f2399f9cc3df49b5713e7ed0dfd23d6612dc071a97e1b11451237ec954`  
		Last Modified: Fri, 10 Jan 2025 00:07:38 GMT  
		Size: 21.3 MB (21303870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73584c7d6ffa77bc341da6b601de589dbb3bc90094dc1506ca7221c18f545976`  
		Last Modified: Fri, 10 Jan 2025 00:07:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a00de156e44b0944a7125426ca4e91c3d3090763debd7d047cf7eda4a39dca87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79936c5c0e560b15b0aad0c8835b9075dd3c50c7fec4f31458eb36228987a1cb`

```dockerfile
```

-	Layers:
	-	`sha256:eadc9d4056786a4ec1c155b1f08ce83af47fd3975f0deedd2ff41384e0bc788e`  
		Last Modified: Fri, 10 Jan 2025 00:07:37 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8877919584cc9a4577906c6c60656e7c44b7c8dae3b65f8d7b74acd9b8947ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149440959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b3ab72d35f78cfb25f15813532542dc016c0f9fd7889844e68ba6df769a39b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD []
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
USER rootless
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3528552267cec0f9e2dee7d372df3bbea6255a3ca1a18ba3e58e5cfd106d15e1`  
		Last Modified: Thu, 09 Jan 2025 22:29:23 GMT  
		Size: 8.1 MB (8073134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4781719ef357b2c136f17ff57b79d601b4058a8861d68048cf902106cf3ae9d`  
		Last Modified: Thu, 09 Jan 2025 22:29:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4866b03f4ce1c603a6809790707aae8972781d4ff1b1090b3960153b3abec1e0`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.6 MB (17619398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d036bb2a7049761d033d283b4bc752d8e2d6e25b9ea4bf4329e6a7055ad82e`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.1 MB (17106450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4fa20503c91c2405741c5b1d40f5567a7c641a4624b6c0693716eb0fa6752e`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.7 MB (17653961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f999290013a7bee6f7b09186deee9dc98564604594aac128b7293ef882edfd34`  
		Last Modified: Thu, 09 Jan 2025 22:29:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dca40438acce378f07676329455acd2969680d9ceeeee33d5f34cb1f06c2f4`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730c1436b4a8c8addd307436381ccbe5d3d3adf57e2b67228ea624046c0f4997`  
		Last Modified: Thu, 09 Jan 2025 22:29:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aed778d4d37e95ff4fef9353934ac33be3d14475532284512418c3c7e8802ea`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 7.0 MB (6981951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2357ac4e3b4ca2ae4efd996c265963976e946d8abe41868260f6fc228d6e6cc4`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 97.8 KB (97785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f2dd98d7754adf87dda19dcbdb3a884046d0c27693b4d9c3465c4ae77eca5c`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af42edc6d44256189864a2f5cf56c06590a42e61aeb9f18a2c453de7841076b0`  
		Last Modified: Thu, 09 Jan 2025 23:09:59 GMT  
		Size: 53.7 MB (53737271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518ad24d587855579d9d75a11a4e2b7e0c347114c536d13580a4ea61bde47f9`  
		Last Modified: Thu, 09 Jan 2025 23:09:58 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbdc874d308be16b20915161093ad9bf64226aace0cc1e4a6c39989bc8b42e8`  
		Last Modified: Thu, 09 Jan 2025 23:09:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fb49e0358a6dcd8f454c229f2e58043c238bd1c31bf2592d90ccf2c54f4e51`  
		Last Modified: Fri, 10 Jan 2025 00:07:30 GMT  
		Size: 1.0 MB (1014210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439b04567bec34e568e7ccb361a72f63a1d46f4d92ecb655b923adc811884224`  
		Last Modified: Fri, 10 Jan 2025 00:07:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914c5eaa7edf15934269fdc326ef1f67b1143f22258e44663c95398675d41f63`  
		Last Modified: Fri, 10 Jan 2025 00:07:29 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b68b3535056a1cc8be40c353f77739f156a5090082cc6be776be14d05d2caa1`  
		Last Modified: Fri, 10 Jan 2025 00:07:30 GMT  
		Size: 23.2 MB (23155143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f44128077eafee533110d4ac4367e5385cabd2739d3546d5c3d1dec4178ae04`  
		Last Modified: Fri, 10 Jan 2025 00:07:30 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3f6f181021a43b59a102e93c0b8ef6e94e8d5f579a9cfc058dccda16ea356cda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58fb060b226c196a27de2c0ef71eb8106443bf7c6124ee1de21d08359d8fb72d`

```dockerfile
```

-	Layers:
	-	`sha256:254aaf99f8db72b2d239c240a4ed5a914197c55e50a316ddee0c09a4ba50cfe8`  
		Last Modified: Fri, 10 Jan 2025 00:07:29 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:a284c7d6870c4e3d5b1aebd1c58f5a505069a7b0329e978b08abf17513aa7a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:c5cd74a023e7faacafb41c44c2747e96c7876beafafde01fb2492784ca74dff0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2313128368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e61f7f6c4cab2dac3a38e28d586ddb278c5d38b92d47ab9d0589d0f8f2c812d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Tue, 14 Jan 2025 01:33:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 01:34:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 01:34:08 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 01:34:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 01:34:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 01:34:30 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 01:34:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 01:34:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 01:34:40 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 01:34:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b9a42b9ecd66f4d789ad699e16330906d9d369d20469828c662fefe12b02e8`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba018976cff219cd6191a11bfc55504ef36738be82baeb71ffc74b2313dd1a9b`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 357.0 KB (356994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b23dc261c6430fb422dc75b6af8a9222a66dce9202b6dd146d0489236423f3`  
		Last Modified: Tue, 14 Jan 2025 01:34:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ac7c6042d38723e1b4633b555e3fcb9ee7c9a2f2551df07d9fa1de8c8f2a08`  
		Last Modified: Tue, 14 Jan 2025 01:34:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67545a67f1de16e949e21b129bbea57c410284aedc8db5faee026b21c95c944e`  
		Last Modified: Tue, 14 Jan 2025 01:34:57 GMT  
		Size: 19.1 MB (19131320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd02d7c050fc6cdf708efdead243164770cabd577abe8a18db6f288f696ff7b8`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c748dabad2a30c59b0159fa58b3472240315a9ec2f64376d5d0381386a2f97`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ecbbb0ec3c3d976a78844e335b33c792dc71f07c2a7e93f8ee679fb504d98e`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b5b5bfffbb0f5a83a7d094b25d599051fdc8dbf1b50d0c5aea1d591ed0299e`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 19.6 MB (19615409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fa2ea051bffbfc1e545845e1eb270495068cb06e93f8ac57231c31ff4cfd03`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d7751f4c9a5b340fdf6ba7576146996238741661e6cf1a7b2fb461ed4016b1`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7201c016b89daaeb208563dfb1a7e997838e81cd51529341002ee3cb0ae426`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45fcce664eafbed1944672cd2d9447505f859b1fd823dbc7f6e0ffa88ecae7f`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 20.1 MB (20139389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:2412f304f0e829b89301d917174de78b373338e7deea7159f4fa1eb71edd3587
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073619759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b2cc3864ebb611e04f866a8a0df76a2db44807df698f694805d7551cf967ea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 14 Jan 2025 01:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 01:34:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 01:34:10 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 01:34:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 01:34:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:28 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 01:34:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:44 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 01:34:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 01:34:45 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 01:34:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425357308f56dd3b281b2556d37baf9db8f8c3b130904a33ffddde5099320a0d`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6b7c3304749381530c4553df1e4cb56b49ac5ff3f306da88d1927e5c867e2b`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 473.9 KB (473861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd751bf8d052b9254190cd7a90b0ec77465de52b18d8a606b27a9e15c9382172`  
		Last Modified: Tue, 14 Jan 2025 01:35:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fed29470c12c566ce347f7982db8e7c38ca9ffec02fac952816378c3542277`  
		Last Modified: Tue, 14 Jan 2025 01:35:04 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298ed1e5eae2c63f4534bfc920d12710d8df9fd7bddeb178169cc5088f915f6a`  
		Last Modified: Tue, 14 Jan 2025 01:35:06 GMT  
		Size: 19.2 MB (19158530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77dabf7d51887079f09f01958ce57b98a262584e91145268ede9528e71cb4f`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec1d3f15655b584105f5d69418e8450904e56e40f6cc740597d32a24dcf0bd2`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0eff69a154ff66b03dcb32f76f86f5bcc6788eec3b8ee4fe571137d404737f`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9896f36188aaf843315e328e9c93add995fb259b42bfab34c209cc8eb2e2234e`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 19.6 MB (19644525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51c5a778e0da9ab6bb36815596910deefa3d1fbcf6c94a55941da25028dffd7`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b7e381ec9896eca8879369b9e71b4be2e219dedfba7772c47aeef95758f4a0`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6bc972d567de2d4dee7559d75cad49ba3b40a07349d26d5f8efcb2b841824eb`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e1e3140e894e79b619265107b247afff926e38dcbfec4fb75bc065e22d82ca`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 20.2 MB (20160932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:a23e84498a9a98c2b1a9dfa3b48a38c116831491c2fcc91c024c3bec41047eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:2412f304f0e829b89301d917174de78b373338e7deea7159f4fa1eb71edd3587
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073619759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b2cc3864ebb611e04f866a8a0df76a2db44807df698f694805d7551cf967ea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 14 Jan 2025 01:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 01:34:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 01:34:10 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 01:34:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 01:34:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:28 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 01:34:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:44 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 01:34:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 01:34:45 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 01:34:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425357308f56dd3b281b2556d37baf9db8f8c3b130904a33ffddde5099320a0d`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6b7c3304749381530c4553df1e4cb56b49ac5ff3f306da88d1927e5c867e2b`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 473.9 KB (473861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd751bf8d052b9254190cd7a90b0ec77465de52b18d8a606b27a9e15c9382172`  
		Last Modified: Tue, 14 Jan 2025 01:35:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fed29470c12c566ce347f7982db8e7c38ca9ffec02fac952816378c3542277`  
		Last Modified: Tue, 14 Jan 2025 01:35:04 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298ed1e5eae2c63f4534bfc920d12710d8df9fd7bddeb178169cc5088f915f6a`  
		Last Modified: Tue, 14 Jan 2025 01:35:06 GMT  
		Size: 19.2 MB (19158530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77dabf7d51887079f09f01958ce57b98a262584e91145268ede9528e71cb4f`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec1d3f15655b584105f5d69418e8450904e56e40f6cc740597d32a24dcf0bd2`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0eff69a154ff66b03dcb32f76f86f5bcc6788eec3b8ee4fe571137d404737f`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9896f36188aaf843315e328e9c93add995fb259b42bfab34c209cc8eb2e2234e`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 19.6 MB (19644525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51c5a778e0da9ab6bb36815596910deefa3d1fbcf6c94a55941da25028dffd7`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b7e381ec9896eca8879369b9e71b4be2e219dedfba7772c47aeef95758f4a0`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6bc972d567de2d4dee7559d75cad49ba3b40a07349d26d5f8efcb2b841824eb`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e1e3140e894e79b619265107b247afff926e38dcbfec4fb75bc065e22d82ca`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 20.2 MB (20160932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:6550e15f54a41601f5bf6cc07cda68d35cf115561478d97cc87dfdca2b7e8df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:c5cd74a023e7faacafb41c44c2747e96c7876beafafde01fb2492784ca74dff0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2313128368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e61f7f6c4cab2dac3a38e28d586ddb278c5d38b92d47ab9d0589d0f8f2c812d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Tue, 14 Jan 2025 01:33:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 01:34:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 01:34:08 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 01:34:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 01:34:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 01:34:30 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 01:34:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 01:34:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 01:34:40 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 01:34:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b9a42b9ecd66f4d789ad699e16330906d9d369d20469828c662fefe12b02e8`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba018976cff219cd6191a11bfc55504ef36738be82baeb71ffc74b2313dd1a9b`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 357.0 KB (356994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b23dc261c6430fb422dc75b6af8a9222a66dce9202b6dd146d0489236423f3`  
		Last Modified: Tue, 14 Jan 2025 01:34:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ac7c6042d38723e1b4633b555e3fcb9ee7c9a2f2551df07d9fa1de8c8f2a08`  
		Last Modified: Tue, 14 Jan 2025 01:34:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67545a67f1de16e949e21b129bbea57c410284aedc8db5faee026b21c95c944e`  
		Last Modified: Tue, 14 Jan 2025 01:34:57 GMT  
		Size: 19.1 MB (19131320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd02d7c050fc6cdf708efdead243164770cabd577abe8a18db6f288f696ff7b8`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c748dabad2a30c59b0159fa58b3472240315a9ec2f64376d5d0381386a2f97`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ecbbb0ec3c3d976a78844e335b33c792dc71f07c2a7e93f8ee679fb504d98e`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b5b5bfffbb0f5a83a7d094b25d599051fdc8dbf1b50d0c5aea1d591ed0299e`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 19.6 MB (19615409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fa2ea051bffbfc1e545845e1eb270495068cb06e93f8ac57231c31ff4cfd03`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d7751f4c9a5b340fdf6ba7576146996238741661e6cf1a7b2fb461ed4016b1`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7201c016b89daaeb208563dfb1a7e997838e81cd51529341002ee3cb0ae426`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45fcce664eafbed1944672cd2d9447505f859b1fd823dbc7f6e0ffa88ecae7f`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 20.1 MB (20139389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:27.5-cli`

```console
$ docker pull docker@sha256:7ac99be316eb5b5d57fab11916ec42ccd009878608f5d732654bd4ba90996824
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.5-cli` - linux; amd64

```console
$ docker pull docker@sha256:079cb70986454a74835b387f76c7aac60261ea12110335cb4a6de4f0c2cfafca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68654583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118ba116e4cc60717257588cf15e365499e33eae2c96f3591484acd65f52d902`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-x86_64'; 			sha256='6ef48e4bf25fbf1f1ad50c43b797cc24e12e4cde29765076b4145e09e35f5713'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv6'; 			sha256='8f415a76ad62ff621b26b37a94841ee0d4480862d8da55320c1c8fc9db4d8359'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv7'; 			sha256='64314c73a7d34e4a8b9dad87bab857304fb60b0293703d02be436893e1c37f33'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-aarch64'; 			sha256='d1a04a3eb7fd738cc78e518d179a03adb9fe531ee422b8a14bdccf36d654b73a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-ppc64le'; 			sha256='23bddc8119bce6c0eeef1461bc0526291d60de9042b28780012033ba4082090e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-riscv64'; 			sha256='c4bac574a2123938de4ef410e7cef92d079abe266298c93257cbcc4e17134184'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-s390x'; 			sha256='6c0c7d9b6119f68b3dcbf816cf9e5782eb7cea8d2433f8a51b95a41276241e18'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2147a509bdeadcb92898e60247f4658852a925a4962e0e29a2d28fcfe83e81`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 8.1 MB (8058755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386023837c56d9b33f3b3c560d987a4d0afffaa2025b6bdb05dbb812ba5fd84d`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ec2a25f188dfb7b2d0d15b2f51239ab8694502bca535fd3c2ceccb359fd868`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 18.8 MB (18849469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47c11d47744bce1446bbff20430a7058587389836041cbda659967ba94b3653`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 18.8 MB (18798855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e324137ff7d6aef2c4fe2746097ee8c2ccfc69735be66123a60f1d9286e99c`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 19.3 MB (19303637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae739ff5a469e4fc30b28a279acac08ee7a9c6f40cee72753bf1cde14f2ea88`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c082b27e013c5d92e5f5698a5eb8564358982c6a8fcd01667c5e16e05499363`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1341245cb0ac938576ee4968bde808b58406e6dc5bad00b169e1584bd79a37`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0834e294409cfea3b7383723da66c834024db808b8f4eb540634fbeb35bd3554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8adc850415b3d1dc2eff9e582890566fe2d56c76cb9ad1d841bca8b83d1275`

```dockerfile
```

-	Layers:
	-	`sha256:e1482745bc132620b8f783302f61bde33791e940048e70d192e1b98b15b225ef`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:39401ed362b2c67e9ac62f3e5710570ab18e024cfc5f565aa517d3094afff38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63766331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2cf88b9b43fcd7963f15edfb83fe97afd5fdb4a84c0c9550747fef06027b2f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-x86_64'; 			sha256='6ef48e4bf25fbf1f1ad50c43b797cc24e12e4cde29765076b4145e09e35f5713'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv6'; 			sha256='8f415a76ad62ff621b26b37a94841ee0d4480862d8da55320c1c8fc9db4d8359'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv7'; 			sha256='64314c73a7d34e4a8b9dad87bab857304fb60b0293703d02be436893e1c37f33'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-aarch64'; 			sha256='d1a04a3eb7fd738cc78e518d179a03adb9fe531ee422b8a14bdccf36d654b73a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-ppc64le'; 			sha256='23bddc8119bce6c0eeef1461bc0526291d60de9042b28780012033ba4082090e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-riscv64'; 			sha256='c4bac574a2123938de4ef410e7cef92d079abe266298c93257cbcc4e17134184'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-s390x'; 			sha256='6c0c7d9b6119f68b3dcbf816cf9e5782eb7cea8d2433f8a51b95a41276241e18'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:b5efa4ecc356aa3f967cf3252f33f35689d69748ad15f6ab382dfbc77e53db68`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 18.1 MB (18112377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8980aece4ef386b0d4c63fa11ec664751daa90f6c5144d7ee6983e0f66a321b`  
		Last Modified: Tue, 14 Jan 2025 01:36:24 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999f06d4f41595fc49c1bbb9b00b3cd4f91965126bb974d09c572be01729d08b`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8b82c0cdef43fe4b7645f72f8fe205f6a146384aa0b8c2e73839234796ffc0`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2b97a1b68497256fc60402e3f5abdb7fb6ab5225d56c1fc671133f2e941c5062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2440854a0cd314cf190b2a6a09c7df59ee4e688a46b9c67324944a7cee09901`

```dockerfile
```

-	Layers:
	-	`sha256:4691173ba00bf555533f59934544855695b5d6d51bba5d12e6194b963a43d6a4`  
		Last Modified: Tue, 14 Jan 2025 01:36:24 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c50766834094413ee0950a29b198399229423316f3fc981748adcec98e9ab775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64619543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62380b06f7e73d08c2f8cc69cf22e68b8b0964d4e943cd7902edebf72bdb8861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-x86_64'; 			sha256='6ef48e4bf25fbf1f1ad50c43b797cc24e12e4cde29765076b4145e09e35f5713'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv6'; 			sha256='8f415a76ad62ff621b26b37a94841ee0d4480862d8da55320c1c8fc9db4d8359'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv7'; 			sha256='64314c73a7d34e4a8b9dad87bab857304fb60b0293703d02be436893e1c37f33'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-aarch64'; 			sha256='d1a04a3eb7fd738cc78e518d179a03adb9fe531ee422b8a14bdccf36d654b73a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-ppc64le'; 			sha256='23bddc8119bce6c0eeef1461bc0526291d60de9042b28780012033ba4082090e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-riscv64'; 			sha256='c4bac574a2123938de4ef410e7cef92d079abe266298c93257cbcc4e17134184'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-s390x'; 			sha256='6c0c7d9b6119f68b3dcbf816cf9e5782eb7cea8d2433f8a51b95a41276241e18'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43785ac1a9e530c3cf3f5502efdd8eb2ca0fe74ce2e9dacfcf49cc1cd44ff5b`  
		Last Modified: Tue, 14 Jan 2025 01:40:05 GMT  
		Size: 8.1 MB (8073121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443e45b7ebe0d6fed7d323b8c918357ccec700454ec81770dd307b744905bef2`  
		Last Modified: Tue, 14 Jan 2025 01:40:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1042953f4da92c640616f959f1c17179c50b5bcbb6bdc9f894f38b4278d5db46`  
		Last Modified: Tue, 14 Jan 2025 01:40:05 GMT  
		Size: 17.8 MB (17795750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595709626d52a6ebd1b0e6f2f42977b3d1eb93f23dc20f0fcff5189182226760`  
		Last Modified: Tue, 14 Jan 2025 01:40:05 GMT  
		Size: 17.1 MB (17106450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748acb43c50f1bb7dbea6130ec9107d0f49825c28b2980022cab395526b50be`  
		Last Modified: Tue, 14 Jan 2025 01:40:08 GMT  
		Size: 17.6 MB (17649713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1870e6ecb9e9730d191ac6aa59e5347eebf36c4df5f1c731a00f2cd2d8f504cf`  
		Last Modified: Tue, 14 Jan 2025 01:40:06 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728bbf9b069189d2d739494cb11a3a541b0f53c1e6432d25588228efc0061360`  
		Last Modified: Tue, 14 Jan 2025 01:40:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0dce1ac1b31cc57ce7e0e566085cadacde994d75882f409fd806190989973c`  
		Last Modified: Tue, 14 Jan 2025 01:40:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:aa5987741b6bbf500dfd9175af5800e5d87ba69bba7bb90c4696491570a18d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084c240dfaf22b97381310758a9c28cce3af37c241e02dc7457710416ed68324`

```dockerfile
```

-	Layers:
	-	`sha256:37e6330f383c6a94d354a35890b299d12ffd73c15f1b5691ea42a5bf6bd7c1c6`  
		Last Modified: Tue, 14 Jan 2025 01:40:04 GMT  
		Size: 38.3 KB (38321 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5-dind`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:27.5-dind-rootless`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:27.5-windowsservercore`

```console
$ docker pull docker@sha256:a284c7d6870c4e3d5b1aebd1c58f5a505069a7b0329e978b08abf17513aa7a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `docker:27.5-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:c5cd74a023e7faacafb41c44c2747e96c7876beafafde01fb2492784ca74dff0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2313128368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e61f7f6c4cab2dac3a38e28d586ddb278c5d38b92d47ab9d0589d0f8f2c812d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Tue, 14 Jan 2025 01:33:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 01:34:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 01:34:08 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 01:34:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 01:34:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 01:34:30 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 01:34:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 01:34:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 01:34:40 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 01:34:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b9a42b9ecd66f4d789ad699e16330906d9d369d20469828c662fefe12b02e8`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba018976cff219cd6191a11bfc55504ef36738be82baeb71ffc74b2313dd1a9b`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 357.0 KB (356994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b23dc261c6430fb422dc75b6af8a9222a66dce9202b6dd146d0489236423f3`  
		Last Modified: Tue, 14 Jan 2025 01:34:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ac7c6042d38723e1b4633b555e3fcb9ee7c9a2f2551df07d9fa1de8c8f2a08`  
		Last Modified: Tue, 14 Jan 2025 01:34:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67545a67f1de16e949e21b129bbea57c410284aedc8db5faee026b21c95c944e`  
		Last Modified: Tue, 14 Jan 2025 01:34:57 GMT  
		Size: 19.1 MB (19131320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd02d7c050fc6cdf708efdead243164770cabd577abe8a18db6f288f696ff7b8`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c748dabad2a30c59b0159fa58b3472240315a9ec2f64376d5d0381386a2f97`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ecbbb0ec3c3d976a78844e335b33c792dc71f07c2a7e93f8ee679fb504d98e`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b5b5bfffbb0f5a83a7d094b25d599051fdc8dbf1b50d0c5aea1d591ed0299e`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 19.6 MB (19615409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fa2ea051bffbfc1e545845e1eb270495068cb06e93f8ac57231c31ff4cfd03`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d7751f4c9a5b340fdf6ba7576146996238741661e6cf1a7b2fb461ed4016b1`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7201c016b89daaeb208563dfb1a7e997838e81cd51529341002ee3cb0ae426`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45fcce664eafbed1944672cd2d9447505f859b1fd823dbc7f6e0ffa88ecae7f`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 20.1 MB (20139389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.5-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:2412f304f0e829b89301d917174de78b373338e7deea7159f4fa1eb71edd3587
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073619759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b2cc3864ebb611e04f866a8a0df76a2db44807df698f694805d7551cf967ea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 14 Jan 2025 01:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 01:34:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 01:34:10 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 01:34:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 01:34:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:28 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 01:34:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:44 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 01:34:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 01:34:45 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 01:34:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425357308f56dd3b281b2556d37baf9db8f8c3b130904a33ffddde5099320a0d`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6b7c3304749381530c4553df1e4cb56b49ac5ff3f306da88d1927e5c867e2b`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 473.9 KB (473861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd751bf8d052b9254190cd7a90b0ec77465de52b18d8a606b27a9e15c9382172`  
		Last Modified: Tue, 14 Jan 2025 01:35:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fed29470c12c566ce347f7982db8e7c38ca9ffec02fac952816378c3542277`  
		Last Modified: Tue, 14 Jan 2025 01:35:04 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298ed1e5eae2c63f4534bfc920d12710d8df9fd7bddeb178169cc5088f915f6a`  
		Last Modified: Tue, 14 Jan 2025 01:35:06 GMT  
		Size: 19.2 MB (19158530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77dabf7d51887079f09f01958ce57b98a262584e91145268ede9528e71cb4f`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec1d3f15655b584105f5d69418e8450904e56e40f6cc740597d32a24dcf0bd2`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0eff69a154ff66b03dcb32f76f86f5bcc6788eec3b8ee4fe571137d404737f`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9896f36188aaf843315e328e9c93add995fb259b42bfab34c209cc8eb2e2234e`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 19.6 MB (19644525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51c5a778e0da9ab6bb36815596910deefa3d1fbcf6c94a55941da25028dffd7`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b7e381ec9896eca8879369b9e71b4be2e219dedfba7772c47aeef95758f4a0`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6bc972d567de2d4dee7559d75cad49ba3b40a07349d26d5f8efcb2b841824eb`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e1e3140e894e79b619265107b247afff926e38dcbfec4fb75bc065e22d82ca`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 20.2 MB (20160932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5-windowsservercore-1809`

```console
$ docker pull docker@sha256:a23e84498a9a98c2b1a9dfa3b48a38c116831491c2fcc91c024c3bec41047eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `docker:27.5-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:2412f304f0e829b89301d917174de78b373338e7deea7159f4fa1eb71edd3587
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073619759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b2cc3864ebb611e04f866a8a0df76a2db44807df698f694805d7551cf967ea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 14 Jan 2025 01:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 01:34:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 01:34:10 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 01:34:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 01:34:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:28 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 01:34:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:44 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 01:34:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 01:34:45 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 01:34:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425357308f56dd3b281b2556d37baf9db8f8c3b130904a33ffddde5099320a0d`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6b7c3304749381530c4553df1e4cb56b49ac5ff3f306da88d1927e5c867e2b`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 473.9 KB (473861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd751bf8d052b9254190cd7a90b0ec77465de52b18d8a606b27a9e15c9382172`  
		Last Modified: Tue, 14 Jan 2025 01:35:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fed29470c12c566ce347f7982db8e7c38ca9ffec02fac952816378c3542277`  
		Last Modified: Tue, 14 Jan 2025 01:35:04 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298ed1e5eae2c63f4534bfc920d12710d8df9fd7bddeb178169cc5088f915f6a`  
		Last Modified: Tue, 14 Jan 2025 01:35:06 GMT  
		Size: 19.2 MB (19158530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77dabf7d51887079f09f01958ce57b98a262584e91145268ede9528e71cb4f`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec1d3f15655b584105f5d69418e8450904e56e40f6cc740597d32a24dcf0bd2`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0eff69a154ff66b03dcb32f76f86f5bcc6788eec3b8ee4fe571137d404737f`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9896f36188aaf843315e328e9c93add995fb259b42bfab34c209cc8eb2e2234e`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 19.6 MB (19644525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51c5a778e0da9ab6bb36815596910deefa3d1fbcf6c94a55941da25028dffd7`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b7e381ec9896eca8879369b9e71b4be2e219dedfba7772c47aeef95758f4a0`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6bc972d567de2d4dee7559d75cad49ba3b40a07349d26d5f8efcb2b841824eb`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e1e3140e894e79b619265107b247afff926e38dcbfec4fb75bc065e22d82ca`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 20.2 MB (20160932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:6550e15f54a41601f5bf6cc07cda68d35cf115561478d97cc87dfdca2b7e8df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `docker:27.5-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:c5cd74a023e7faacafb41c44c2747e96c7876beafafde01fb2492784ca74dff0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2313128368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e61f7f6c4cab2dac3a38e28d586ddb278c5d38b92d47ab9d0589d0f8f2c812d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Tue, 14 Jan 2025 01:33:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 01:34:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 01:34:08 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 01:34:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 01:34:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 01:34:30 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 01:34:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 01:34:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 01:34:40 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 01:34:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b9a42b9ecd66f4d789ad699e16330906d9d369d20469828c662fefe12b02e8`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba018976cff219cd6191a11bfc55504ef36738be82baeb71ffc74b2313dd1a9b`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 357.0 KB (356994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b23dc261c6430fb422dc75b6af8a9222a66dce9202b6dd146d0489236423f3`  
		Last Modified: Tue, 14 Jan 2025 01:34:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ac7c6042d38723e1b4633b555e3fcb9ee7c9a2f2551df07d9fa1de8c8f2a08`  
		Last Modified: Tue, 14 Jan 2025 01:34:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67545a67f1de16e949e21b129bbea57c410284aedc8db5faee026b21c95c944e`  
		Last Modified: Tue, 14 Jan 2025 01:34:57 GMT  
		Size: 19.1 MB (19131320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd02d7c050fc6cdf708efdead243164770cabd577abe8a18db6f288f696ff7b8`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c748dabad2a30c59b0159fa58b3472240315a9ec2f64376d5d0381386a2f97`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ecbbb0ec3c3d976a78844e335b33c792dc71f07c2a7e93f8ee679fb504d98e`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b5b5bfffbb0f5a83a7d094b25d599051fdc8dbf1b50d0c5aea1d591ed0299e`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 19.6 MB (19615409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fa2ea051bffbfc1e545845e1eb270495068cb06e93f8ac57231c31ff4cfd03`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d7751f4c9a5b340fdf6ba7576146996238741661e6cf1a7b2fb461ed4016b1`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7201c016b89daaeb208563dfb1a7e997838e81cd51529341002ee3cb0ae426`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45fcce664eafbed1944672cd2d9447505f859b1fd823dbc7f6e0ffa88ecae7f`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 20.1 MB (20139389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5.0`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:27.5.0-alpine3.21`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:27.5.0-cli`

```console
$ docker pull docker@sha256:60407342059ffa73d3ca74c7fd8a5273efc94a6035d7cff6f4c8123e30ce34a4
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
$ docker pull docker@sha256:079cb70986454a74835b387f76c7aac60261ea12110335cb4a6de4f0c2cfafca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68654583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118ba116e4cc60717257588cf15e365499e33eae2c96f3591484acd65f52d902`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-x86_64'; 			sha256='6ef48e4bf25fbf1f1ad50c43b797cc24e12e4cde29765076b4145e09e35f5713'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv6'; 			sha256='8f415a76ad62ff621b26b37a94841ee0d4480862d8da55320c1c8fc9db4d8359'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv7'; 			sha256='64314c73a7d34e4a8b9dad87bab857304fb60b0293703d02be436893e1c37f33'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-aarch64'; 			sha256='d1a04a3eb7fd738cc78e518d179a03adb9fe531ee422b8a14bdccf36d654b73a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-ppc64le'; 			sha256='23bddc8119bce6c0eeef1461bc0526291d60de9042b28780012033ba4082090e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-riscv64'; 			sha256='c4bac574a2123938de4ef410e7cef92d079abe266298c93257cbcc4e17134184'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-s390x'; 			sha256='6c0c7d9b6119f68b3dcbf816cf9e5782eb7cea8d2433f8a51b95a41276241e18'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2147a509bdeadcb92898e60247f4658852a925a4962e0e29a2d28fcfe83e81`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 8.1 MB (8058755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386023837c56d9b33f3b3c560d987a4d0afffaa2025b6bdb05dbb812ba5fd84d`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ec2a25f188dfb7b2d0d15b2f51239ab8694502bca535fd3c2ceccb359fd868`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 18.8 MB (18849469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47c11d47744bce1446bbff20430a7058587389836041cbda659967ba94b3653`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 18.8 MB (18798855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e324137ff7d6aef2c4fe2746097ee8c2ccfc69735be66123a60f1d9286e99c`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 19.3 MB (19303637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae739ff5a469e4fc30b28a279acac08ee7a9c6f40cee72753bf1cde14f2ea88`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c082b27e013c5d92e5f5698a5eb8564358982c6a8fcd01667c5e16e05499363`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1341245cb0ac938576ee4968bde808b58406e6dc5bad00b169e1584bd79a37`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0834e294409cfea3b7383723da66c834024db808b8f4eb540634fbeb35bd3554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8adc850415b3d1dc2eff9e582890566fe2d56c76cb9ad1d841bca8b83d1275`

```dockerfile
```

-	Layers:
	-	`sha256:e1482745bc132620b8f783302f61bde33791e940048e70d192e1b98b15b225ef`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:39401ed362b2c67e9ac62f3e5710570ab18e024cfc5f565aa517d3094afff38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63766331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2cf88b9b43fcd7963f15edfb83fe97afd5fdb4a84c0c9550747fef06027b2f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-x86_64'; 			sha256='6ef48e4bf25fbf1f1ad50c43b797cc24e12e4cde29765076b4145e09e35f5713'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv6'; 			sha256='8f415a76ad62ff621b26b37a94841ee0d4480862d8da55320c1c8fc9db4d8359'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv7'; 			sha256='64314c73a7d34e4a8b9dad87bab857304fb60b0293703d02be436893e1c37f33'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-aarch64'; 			sha256='d1a04a3eb7fd738cc78e518d179a03adb9fe531ee422b8a14bdccf36d654b73a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-ppc64le'; 			sha256='23bddc8119bce6c0eeef1461bc0526291d60de9042b28780012033ba4082090e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-riscv64'; 			sha256='c4bac574a2123938de4ef410e7cef92d079abe266298c93257cbcc4e17134184'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-s390x'; 			sha256='6c0c7d9b6119f68b3dcbf816cf9e5782eb7cea8d2433f8a51b95a41276241e18'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:b5efa4ecc356aa3f967cf3252f33f35689d69748ad15f6ab382dfbc77e53db68`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 18.1 MB (18112377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8980aece4ef386b0d4c63fa11ec664751daa90f6c5144d7ee6983e0f66a321b`  
		Last Modified: Tue, 14 Jan 2025 01:36:24 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999f06d4f41595fc49c1bbb9b00b3cd4f91965126bb974d09c572be01729d08b`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8b82c0cdef43fe4b7645f72f8fe205f6a146384aa0b8c2e73839234796ffc0`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2b97a1b68497256fc60402e3f5abdb7fb6ab5225d56c1fc671133f2e941c5062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2440854a0cd314cf190b2a6a09c7df59ee4e688a46b9c67324944a7cee09901`

```dockerfile
```

-	Layers:
	-	`sha256:4691173ba00bf555533f59934544855695b5d6d51bba5d12e6194b963a43d6a4`  
		Last Modified: Tue, 14 Jan 2025 01:36:24 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:23923b350de3a2507ee862e801af31acba737fa860a838f5a8e6c7a20056484a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62776091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a313bc642a94a003db6f292d37ce38f797f24997e6dbb16cc41da224f9b81349`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-x86_64'; 			sha256='6ef48e4bf25fbf1f1ad50c43b797cc24e12e4cde29765076b4145e09e35f5713'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv6'; 			sha256='8f415a76ad62ff621b26b37a94841ee0d4480862d8da55320c1c8fc9db4d8359'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv7'; 			sha256='64314c73a7d34e4a8b9dad87bab857304fb60b0293703d02be436893e1c37f33'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-aarch64'; 			sha256='d1a04a3eb7fd738cc78e518d179a03adb9fe531ee422b8a14bdccf36d654b73a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-ppc64le'; 			sha256='23bddc8119bce6c0eeef1461bc0526291d60de9042b28780012033ba4082090e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-riscv64'; 			sha256='c4bac574a2123938de4ef410e7cef92d079abe266298c93257cbcc4e17134184'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-s390x'; 			sha256='6c0c7d9b6119f68b3dcbf816cf9e5782eb7cea8d2433f8a51b95a41276241e18'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:f2df6afa274a12165455efa57585f14851edbe3c8431e611e4aa514c2301b5ae`  
		Last Modified: Tue, 14 Jan 2025 01:40:41 GMT  
		Size: 16.9 MB (16855866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01eb77069da975cd16e756769bced234ed0f0ce04114d17b4fff3f3961ff7fdb`  
		Last Modified: Tue, 14 Jan 2025 01:40:41 GMT  
		Size: 17.4 MB (17427588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2b0f6d3c6a29b62407828319989bf534854431cdf5cc37dfbf8f4265ee109e`  
		Last Modified: Tue, 14 Jan 2025 01:40:41 GMT  
		Size: 18.1 MB (18099444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb58313a02889661a0827edac2479fe14f136f072f9455c7401f027b731565`  
		Last Modified: Tue, 14 Jan 2025 01:40:40 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a31c7f92732acfb2da6e4003cc0236067eeebca4fdb7fd0578439be93bf221`  
		Last Modified: Tue, 14 Jan 2025 01:40:41 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744ae77c3140a38213a1adbd7f5730687718b7d1174559a578dd21556d5fbc70`  
		Last Modified: Tue, 14 Jan 2025 01:40:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:208152349647b5817d0e8732f0d0dbc10072a46f8ef4336fa213a63fc8a33202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156dfbb0c501116bdacec71b4b366939a77df27332590e0dbc91663289b12c2c`

```dockerfile
```

-	Layers:
	-	`sha256:1acab073d9634576b42209cc73006115c1a4fb59cb51d376758c181229c3ee6f`  
		Last Modified: Tue, 14 Jan 2025 01:40:39 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c50766834094413ee0950a29b198399229423316f3fc981748adcec98e9ab775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64619543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62380b06f7e73d08c2f8cc69cf22e68b8b0964d4e943cd7902edebf72bdb8861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-x86_64'; 			sha256='6ef48e4bf25fbf1f1ad50c43b797cc24e12e4cde29765076b4145e09e35f5713'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv6'; 			sha256='8f415a76ad62ff621b26b37a94841ee0d4480862d8da55320c1c8fc9db4d8359'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv7'; 			sha256='64314c73a7d34e4a8b9dad87bab857304fb60b0293703d02be436893e1c37f33'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-aarch64'; 			sha256='d1a04a3eb7fd738cc78e518d179a03adb9fe531ee422b8a14bdccf36d654b73a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-ppc64le'; 			sha256='23bddc8119bce6c0eeef1461bc0526291d60de9042b28780012033ba4082090e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-riscv64'; 			sha256='c4bac574a2123938de4ef410e7cef92d079abe266298c93257cbcc4e17134184'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-s390x'; 			sha256='6c0c7d9b6119f68b3dcbf816cf9e5782eb7cea8d2433f8a51b95a41276241e18'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43785ac1a9e530c3cf3f5502efdd8eb2ca0fe74ce2e9dacfcf49cc1cd44ff5b`  
		Last Modified: Tue, 14 Jan 2025 01:40:05 GMT  
		Size: 8.1 MB (8073121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443e45b7ebe0d6fed7d323b8c918357ccec700454ec81770dd307b744905bef2`  
		Last Modified: Tue, 14 Jan 2025 01:40:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1042953f4da92c640616f959f1c17179c50b5bcbb6bdc9f894f38b4278d5db46`  
		Last Modified: Tue, 14 Jan 2025 01:40:05 GMT  
		Size: 17.8 MB (17795750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595709626d52a6ebd1b0e6f2f42977b3d1eb93f23dc20f0fcff5189182226760`  
		Last Modified: Tue, 14 Jan 2025 01:40:05 GMT  
		Size: 17.1 MB (17106450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748acb43c50f1bb7dbea6130ec9107d0f49825c28b2980022cab395526b50be`  
		Last Modified: Tue, 14 Jan 2025 01:40:08 GMT  
		Size: 17.6 MB (17649713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1870e6ecb9e9730d191ac6aa59e5347eebf36c4df5f1c731a00f2cd2d8f504cf`  
		Last Modified: Tue, 14 Jan 2025 01:40:06 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728bbf9b069189d2d739494cb11a3a541b0f53c1e6432d25588228efc0061360`  
		Last Modified: Tue, 14 Jan 2025 01:40:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0dce1ac1b31cc57ce7e0e566085cadacde994d75882f409fd806190989973c`  
		Last Modified: Tue, 14 Jan 2025 01:40:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:aa5987741b6bbf500dfd9175af5800e5d87ba69bba7bb90c4696491570a18d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084c240dfaf22b97381310758a9c28cce3af37c241e02dc7457710416ed68324`

```dockerfile
```

-	Layers:
	-	`sha256:37e6330f383c6a94d354a35890b299d12ffd73c15f1b5691ea42a5bf6bd7c1c6`  
		Last Modified: Tue, 14 Jan 2025 01:40:04 GMT  
		Size: 38.3 KB (38321 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5.0-cli-alpine3.21`

```console
$ docker pull docker@sha256:60407342059ffa73d3ca74c7fd8a5273efc94a6035d7cff6f4c8123e30ce34a4
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
$ docker pull docker@sha256:079cb70986454a74835b387f76c7aac60261ea12110335cb4a6de4f0c2cfafca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68654583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118ba116e4cc60717257588cf15e365499e33eae2c96f3591484acd65f52d902`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-x86_64'; 			sha256='6ef48e4bf25fbf1f1ad50c43b797cc24e12e4cde29765076b4145e09e35f5713'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv6'; 			sha256='8f415a76ad62ff621b26b37a94841ee0d4480862d8da55320c1c8fc9db4d8359'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv7'; 			sha256='64314c73a7d34e4a8b9dad87bab857304fb60b0293703d02be436893e1c37f33'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-aarch64'; 			sha256='d1a04a3eb7fd738cc78e518d179a03adb9fe531ee422b8a14bdccf36d654b73a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-ppc64le'; 			sha256='23bddc8119bce6c0eeef1461bc0526291d60de9042b28780012033ba4082090e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-riscv64'; 			sha256='c4bac574a2123938de4ef410e7cef92d079abe266298c93257cbcc4e17134184'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-s390x'; 			sha256='6c0c7d9b6119f68b3dcbf816cf9e5782eb7cea8d2433f8a51b95a41276241e18'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2147a509bdeadcb92898e60247f4658852a925a4962e0e29a2d28fcfe83e81`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 8.1 MB (8058755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386023837c56d9b33f3b3c560d987a4d0afffaa2025b6bdb05dbb812ba5fd84d`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ec2a25f188dfb7b2d0d15b2f51239ab8694502bca535fd3c2ceccb359fd868`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 18.8 MB (18849469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47c11d47744bce1446bbff20430a7058587389836041cbda659967ba94b3653`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 18.8 MB (18798855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e324137ff7d6aef2c4fe2746097ee8c2ccfc69735be66123a60f1d9286e99c`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 19.3 MB (19303637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae739ff5a469e4fc30b28a279acac08ee7a9c6f40cee72753bf1cde14f2ea88`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c082b27e013c5d92e5f5698a5eb8564358982c6a8fcd01667c5e16e05499363`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1341245cb0ac938576ee4968bde808b58406e6dc5bad00b169e1584bd79a37`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:0834e294409cfea3b7383723da66c834024db808b8f4eb540634fbeb35bd3554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8adc850415b3d1dc2eff9e582890566fe2d56c76cb9ad1d841bca8b83d1275`

```dockerfile
```

-	Layers:
	-	`sha256:e1482745bc132620b8f783302f61bde33791e940048e70d192e1b98b15b225ef`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-cli-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:39401ed362b2c67e9ac62f3e5710570ab18e024cfc5f565aa517d3094afff38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63766331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2cf88b9b43fcd7963f15edfb83fe97afd5fdb4a84c0c9550747fef06027b2f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-x86_64'; 			sha256='6ef48e4bf25fbf1f1ad50c43b797cc24e12e4cde29765076b4145e09e35f5713'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv6'; 			sha256='8f415a76ad62ff621b26b37a94841ee0d4480862d8da55320c1c8fc9db4d8359'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv7'; 			sha256='64314c73a7d34e4a8b9dad87bab857304fb60b0293703d02be436893e1c37f33'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-aarch64'; 			sha256='d1a04a3eb7fd738cc78e518d179a03adb9fe531ee422b8a14bdccf36d654b73a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-ppc64le'; 			sha256='23bddc8119bce6c0eeef1461bc0526291d60de9042b28780012033ba4082090e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-riscv64'; 			sha256='c4bac574a2123938de4ef410e7cef92d079abe266298c93257cbcc4e17134184'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-s390x'; 			sha256='6c0c7d9b6119f68b3dcbf816cf9e5782eb7cea8d2433f8a51b95a41276241e18'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:b5efa4ecc356aa3f967cf3252f33f35689d69748ad15f6ab382dfbc77e53db68`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 18.1 MB (18112377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8980aece4ef386b0d4c63fa11ec664751daa90f6c5144d7ee6983e0f66a321b`  
		Last Modified: Tue, 14 Jan 2025 01:36:24 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999f06d4f41595fc49c1bbb9b00b3cd4f91965126bb974d09c572be01729d08b`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8b82c0cdef43fe4b7645f72f8fe205f6a146384aa0b8c2e73839234796ffc0`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:2b97a1b68497256fc60402e3f5abdb7fb6ab5225d56c1fc671133f2e941c5062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2440854a0cd314cf190b2a6a09c7df59ee4e688a46b9c67324944a7cee09901`

```dockerfile
```

-	Layers:
	-	`sha256:4691173ba00bf555533f59934544855695b5d6d51bba5d12e6194b963a43d6a4`  
		Last Modified: Tue, 14 Jan 2025 01:36:24 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-cli-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:23923b350de3a2507ee862e801af31acba737fa860a838f5a8e6c7a20056484a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62776091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a313bc642a94a003db6f292d37ce38f797f24997e6dbb16cc41da224f9b81349`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-x86_64'; 			sha256='6ef48e4bf25fbf1f1ad50c43b797cc24e12e4cde29765076b4145e09e35f5713'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv6'; 			sha256='8f415a76ad62ff621b26b37a94841ee0d4480862d8da55320c1c8fc9db4d8359'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv7'; 			sha256='64314c73a7d34e4a8b9dad87bab857304fb60b0293703d02be436893e1c37f33'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-aarch64'; 			sha256='d1a04a3eb7fd738cc78e518d179a03adb9fe531ee422b8a14bdccf36d654b73a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-ppc64le'; 			sha256='23bddc8119bce6c0eeef1461bc0526291d60de9042b28780012033ba4082090e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-riscv64'; 			sha256='c4bac574a2123938de4ef410e7cef92d079abe266298c93257cbcc4e17134184'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-s390x'; 			sha256='6c0c7d9b6119f68b3dcbf816cf9e5782eb7cea8d2433f8a51b95a41276241e18'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:f2df6afa274a12165455efa57585f14851edbe3c8431e611e4aa514c2301b5ae`  
		Last Modified: Tue, 14 Jan 2025 01:40:41 GMT  
		Size: 16.9 MB (16855866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01eb77069da975cd16e756769bced234ed0f0ce04114d17b4fff3f3961ff7fdb`  
		Last Modified: Tue, 14 Jan 2025 01:40:41 GMT  
		Size: 17.4 MB (17427588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2b0f6d3c6a29b62407828319989bf534854431cdf5cc37dfbf8f4265ee109e`  
		Last Modified: Tue, 14 Jan 2025 01:40:41 GMT  
		Size: 18.1 MB (18099444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb58313a02889661a0827edac2479fe14f136f072f9455c7401f027b731565`  
		Last Modified: Tue, 14 Jan 2025 01:40:40 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a31c7f92732acfb2da6e4003cc0236067eeebca4fdb7fd0578439be93bf221`  
		Last Modified: Tue, 14 Jan 2025 01:40:41 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744ae77c3140a38213a1adbd7f5730687718b7d1174559a578dd21556d5fbc70`  
		Last Modified: Tue, 14 Jan 2025 01:40:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:208152349647b5817d0e8732f0d0dbc10072a46f8ef4336fa213a63fc8a33202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156dfbb0c501116bdacec71b4b366939a77df27332590e0dbc91663289b12c2c`

```dockerfile
```

-	Layers:
	-	`sha256:1acab073d9634576b42209cc73006115c1a4fb59cb51d376758c181229c3ee6f`  
		Last Modified: Tue, 14 Jan 2025 01:40:39 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-cli-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c50766834094413ee0950a29b198399229423316f3fc981748adcec98e9ab775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64619543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62380b06f7e73d08c2f8cc69cf22e68b8b0964d4e943cd7902edebf72bdb8861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-x86_64'; 			sha256='6ef48e4bf25fbf1f1ad50c43b797cc24e12e4cde29765076b4145e09e35f5713'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv6'; 			sha256='8f415a76ad62ff621b26b37a94841ee0d4480862d8da55320c1c8fc9db4d8359'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv7'; 			sha256='64314c73a7d34e4a8b9dad87bab857304fb60b0293703d02be436893e1c37f33'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-aarch64'; 			sha256='d1a04a3eb7fd738cc78e518d179a03adb9fe531ee422b8a14bdccf36d654b73a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-ppc64le'; 			sha256='23bddc8119bce6c0eeef1461bc0526291d60de9042b28780012033ba4082090e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-riscv64'; 			sha256='c4bac574a2123938de4ef410e7cef92d079abe266298c93257cbcc4e17134184'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-s390x'; 			sha256='6c0c7d9b6119f68b3dcbf816cf9e5782eb7cea8d2433f8a51b95a41276241e18'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43785ac1a9e530c3cf3f5502efdd8eb2ca0fe74ce2e9dacfcf49cc1cd44ff5b`  
		Last Modified: Tue, 14 Jan 2025 01:40:05 GMT  
		Size: 8.1 MB (8073121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443e45b7ebe0d6fed7d323b8c918357ccec700454ec81770dd307b744905bef2`  
		Last Modified: Tue, 14 Jan 2025 01:40:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1042953f4da92c640616f959f1c17179c50b5bcbb6bdc9f894f38b4278d5db46`  
		Last Modified: Tue, 14 Jan 2025 01:40:05 GMT  
		Size: 17.8 MB (17795750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595709626d52a6ebd1b0e6f2f42977b3d1eb93f23dc20f0fcff5189182226760`  
		Last Modified: Tue, 14 Jan 2025 01:40:05 GMT  
		Size: 17.1 MB (17106450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748acb43c50f1bb7dbea6130ec9107d0f49825c28b2980022cab395526b50be`  
		Last Modified: Tue, 14 Jan 2025 01:40:08 GMT  
		Size: 17.6 MB (17649713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1870e6ecb9e9730d191ac6aa59e5347eebf36c4df5f1c731a00f2cd2d8f504cf`  
		Last Modified: Tue, 14 Jan 2025 01:40:06 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728bbf9b069189d2d739494cb11a3a541b0f53c1e6432d25588228efc0061360`  
		Last Modified: Tue, 14 Jan 2025 01:40:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0dce1ac1b31cc57ce7e0e566085cadacde994d75882f409fd806190989973c`  
		Last Modified: Tue, 14 Jan 2025 01:40:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:aa5987741b6bbf500dfd9175af5800e5d87ba69bba7bb90c4696491570a18d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084c240dfaf22b97381310758a9c28cce3af37c241e02dc7457710416ed68324`

```dockerfile
```

-	Layers:
	-	`sha256:37e6330f383c6a94d354a35890b299d12ffd73c15f1b5691ea42a5bf6bd7c1c6`  
		Last Modified: Tue, 14 Jan 2025 01:40:04 GMT  
		Size: 38.3 KB (38321 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5.0-dind`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:27.5.0-dind-alpine3.21`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:27.5.0-dind-rootless`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:27.5.0-windowsservercore`

```console
$ docker pull docker@sha256:a284c7d6870c4e3d5b1aebd1c58f5a505069a7b0329e978b08abf17513aa7a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `docker:27.5.0-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:c5cd74a023e7faacafb41c44c2747e96c7876beafafde01fb2492784ca74dff0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2313128368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e61f7f6c4cab2dac3a38e28d586ddb278c5d38b92d47ab9d0589d0f8f2c812d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Tue, 14 Jan 2025 01:33:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 01:34:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 01:34:08 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 01:34:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 01:34:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 01:34:30 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 01:34:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 01:34:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 01:34:40 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 01:34:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b9a42b9ecd66f4d789ad699e16330906d9d369d20469828c662fefe12b02e8`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba018976cff219cd6191a11bfc55504ef36738be82baeb71ffc74b2313dd1a9b`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 357.0 KB (356994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b23dc261c6430fb422dc75b6af8a9222a66dce9202b6dd146d0489236423f3`  
		Last Modified: Tue, 14 Jan 2025 01:34:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ac7c6042d38723e1b4633b555e3fcb9ee7c9a2f2551df07d9fa1de8c8f2a08`  
		Last Modified: Tue, 14 Jan 2025 01:34:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67545a67f1de16e949e21b129bbea57c410284aedc8db5faee026b21c95c944e`  
		Last Modified: Tue, 14 Jan 2025 01:34:57 GMT  
		Size: 19.1 MB (19131320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd02d7c050fc6cdf708efdead243164770cabd577abe8a18db6f288f696ff7b8`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c748dabad2a30c59b0159fa58b3472240315a9ec2f64376d5d0381386a2f97`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ecbbb0ec3c3d976a78844e335b33c792dc71f07c2a7e93f8ee679fb504d98e`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b5b5bfffbb0f5a83a7d094b25d599051fdc8dbf1b50d0c5aea1d591ed0299e`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 19.6 MB (19615409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fa2ea051bffbfc1e545845e1eb270495068cb06e93f8ac57231c31ff4cfd03`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d7751f4c9a5b340fdf6ba7576146996238741661e6cf1a7b2fb461ed4016b1`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7201c016b89daaeb208563dfb1a7e997838e81cd51529341002ee3cb0ae426`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45fcce664eafbed1944672cd2d9447505f859b1fd823dbc7f6e0ffa88ecae7f`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 20.1 MB (20139389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.5.0-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:2412f304f0e829b89301d917174de78b373338e7deea7159f4fa1eb71edd3587
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073619759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b2cc3864ebb611e04f866a8a0df76a2db44807df698f694805d7551cf967ea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 14 Jan 2025 01:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 01:34:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 01:34:10 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 01:34:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 01:34:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:28 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 01:34:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:44 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 01:34:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 01:34:45 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 01:34:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425357308f56dd3b281b2556d37baf9db8f8c3b130904a33ffddde5099320a0d`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6b7c3304749381530c4553df1e4cb56b49ac5ff3f306da88d1927e5c867e2b`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 473.9 KB (473861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd751bf8d052b9254190cd7a90b0ec77465de52b18d8a606b27a9e15c9382172`  
		Last Modified: Tue, 14 Jan 2025 01:35:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fed29470c12c566ce347f7982db8e7c38ca9ffec02fac952816378c3542277`  
		Last Modified: Tue, 14 Jan 2025 01:35:04 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298ed1e5eae2c63f4534bfc920d12710d8df9fd7bddeb178169cc5088f915f6a`  
		Last Modified: Tue, 14 Jan 2025 01:35:06 GMT  
		Size: 19.2 MB (19158530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77dabf7d51887079f09f01958ce57b98a262584e91145268ede9528e71cb4f`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec1d3f15655b584105f5d69418e8450904e56e40f6cc740597d32a24dcf0bd2`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0eff69a154ff66b03dcb32f76f86f5bcc6788eec3b8ee4fe571137d404737f`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9896f36188aaf843315e328e9c93add995fb259b42bfab34c209cc8eb2e2234e`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 19.6 MB (19644525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51c5a778e0da9ab6bb36815596910deefa3d1fbcf6c94a55941da25028dffd7`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b7e381ec9896eca8879369b9e71b4be2e219dedfba7772c47aeef95758f4a0`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6bc972d567de2d4dee7559d75cad49ba3b40a07349d26d5f8efcb2b841824eb`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e1e3140e894e79b619265107b247afff926e38dcbfec4fb75bc065e22d82ca`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 20.2 MB (20160932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:a23e84498a9a98c2b1a9dfa3b48a38c116831491c2fcc91c024c3bec41047eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `docker:27.5.0-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:2412f304f0e829b89301d917174de78b373338e7deea7159f4fa1eb71edd3587
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073619759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b2cc3864ebb611e04f866a8a0df76a2db44807df698f694805d7551cf967ea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 14 Jan 2025 01:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 01:34:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 01:34:10 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 01:34:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 01:34:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:28 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 01:34:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:44 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 01:34:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 01:34:45 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 01:34:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425357308f56dd3b281b2556d37baf9db8f8c3b130904a33ffddde5099320a0d`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6b7c3304749381530c4553df1e4cb56b49ac5ff3f306da88d1927e5c867e2b`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 473.9 KB (473861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd751bf8d052b9254190cd7a90b0ec77465de52b18d8a606b27a9e15c9382172`  
		Last Modified: Tue, 14 Jan 2025 01:35:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fed29470c12c566ce347f7982db8e7c38ca9ffec02fac952816378c3542277`  
		Last Modified: Tue, 14 Jan 2025 01:35:04 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298ed1e5eae2c63f4534bfc920d12710d8df9fd7bddeb178169cc5088f915f6a`  
		Last Modified: Tue, 14 Jan 2025 01:35:06 GMT  
		Size: 19.2 MB (19158530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77dabf7d51887079f09f01958ce57b98a262584e91145268ede9528e71cb4f`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec1d3f15655b584105f5d69418e8450904e56e40f6cc740597d32a24dcf0bd2`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0eff69a154ff66b03dcb32f76f86f5bcc6788eec3b8ee4fe571137d404737f`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9896f36188aaf843315e328e9c93add995fb259b42bfab34c209cc8eb2e2234e`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 19.6 MB (19644525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51c5a778e0da9ab6bb36815596910deefa3d1fbcf6c94a55941da25028dffd7`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b7e381ec9896eca8879369b9e71b4be2e219dedfba7772c47aeef95758f4a0`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6bc972d567de2d4dee7559d75cad49ba3b40a07349d26d5f8efcb2b841824eb`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e1e3140e894e79b619265107b247afff926e38dcbfec4fb75bc065e22d82ca`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 20.2 MB (20160932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:6550e15f54a41601f5bf6cc07cda68d35cf115561478d97cc87dfdca2b7e8df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `docker:27.5.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:c5cd74a023e7faacafb41c44c2747e96c7876beafafde01fb2492784ca74dff0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2313128368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e61f7f6c4cab2dac3a38e28d586ddb278c5d38b92d47ab9d0589d0f8f2c812d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Tue, 14 Jan 2025 01:33:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 01:34:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 01:34:08 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 01:34:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 01:34:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 01:34:30 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 01:34:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 01:34:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 01:34:40 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 01:34:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b9a42b9ecd66f4d789ad699e16330906d9d369d20469828c662fefe12b02e8`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba018976cff219cd6191a11bfc55504ef36738be82baeb71ffc74b2313dd1a9b`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 357.0 KB (356994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b23dc261c6430fb422dc75b6af8a9222a66dce9202b6dd146d0489236423f3`  
		Last Modified: Tue, 14 Jan 2025 01:34:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ac7c6042d38723e1b4633b555e3fcb9ee7c9a2f2551df07d9fa1de8c8f2a08`  
		Last Modified: Tue, 14 Jan 2025 01:34:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67545a67f1de16e949e21b129bbea57c410284aedc8db5faee026b21c95c944e`  
		Last Modified: Tue, 14 Jan 2025 01:34:57 GMT  
		Size: 19.1 MB (19131320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd02d7c050fc6cdf708efdead243164770cabd577abe8a18db6f288f696ff7b8`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c748dabad2a30c59b0159fa58b3472240315a9ec2f64376d5d0381386a2f97`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ecbbb0ec3c3d976a78844e335b33c792dc71f07c2a7e93f8ee679fb504d98e`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b5b5bfffbb0f5a83a7d094b25d599051fdc8dbf1b50d0c5aea1d591ed0299e`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 19.6 MB (19615409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fa2ea051bffbfc1e545845e1eb270495068cb06e93f8ac57231c31ff4cfd03`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d7751f4c9a5b340fdf6ba7576146996238741661e6cf1a7b2fb461ed4016b1`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7201c016b89daaeb208563dfb1a7e997838e81cd51529341002ee3cb0ae426`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45fcce664eafbed1944672cd2d9447505f859b1fd823dbc7f6e0ffa88ecae7f`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 20.1 MB (20139389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:60407342059ffa73d3ca74c7fd8a5273efc94a6035d7cff6f4c8123e30ce34a4
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
$ docker pull docker@sha256:079cb70986454a74835b387f76c7aac60261ea12110335cb4a6de4f0c2cfafca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68654583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118ba116e4cc60717257588cf15e365499e33eae2c96f3591484acd65f52d902`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-x86_64'; 			sha256='6ef48e4bf25fbf1f1ad50c43b797cc24e12e4cde29765076b4145e09e35f5713'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv6'; 			sha256='8f415a76ad62ff621b26b37a94841ee0d4480862d8da55320c1c8fc9db4d8359'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv7'; 			sha256='64314c73a7d34e4a8b9dad87bab857304fb60b0293703d02be436893e1c37f33'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-aarch64'; 			sha256='d1a04a3eb7fd738cc78e518d179a03adb9fe531ee422b8a14bdccf36d654b73a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-ppc64le'; 			sha256='23bddc8119bce6c0eeef1461bc0526291d60de9042b28780012033ba4082090e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-riscv64'; 			sha256='c4bac574a2123938de4ef410e7cef92d079abe266298c93257cbcc4e17134184'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-s390x'; 			sha256='6c0c7d9b6119f68b3dcbf816cf9e5782eb7cea8d2433f8a51b95a41276241e18'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2147a509bdeadcb92898e60247f4658852a925a4962e0e29a2d28fcfe83e81`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 8.1 MB (8058755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386023837c56d9b33f3b3c560d987a4d0afffaa2025b6bdb05dbb812ba5fd84d`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ec2a25f188dfb7b2d0d15b2f51239ab8694502bca535fd3c2ceccb359fd868`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 18.8 MB (18849469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47c11d47744bce1446bbff20430a7058587389836041cbda659967ba94b3653`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 18.8 MB (18798855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e324137ff7d6aef2c4fe2746097ee8c2ccfc69735be66123a60f1d9286e99c`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 19.3 MB (19303637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae739ff5a469e4fc30b28a279acac08ee7a9c6f40cee72753bf1cde14f2ea88`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c082b27e013c5d92e5f5698a5eb8564358982c6a8fcd01667c5e16e05499363`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1341245cb0ac938576ee4968bde808b58406e6dc5bad00b169e1584bd79a37`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:0834e294409cfea3b7383723da66c834024db808b8f4eb540634fbeb35bd3554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8adc850415b3d1dc2eff9e582890566fe2d56c76cb9ad1d841bca8b83d1275`

```dockerfile
```

-	Layers:
	-	`sha256:e1482745bc132620b8f783302f61bde33791e940048e70d192e1b98b15b225ef`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:39401ed362b2c67e9ac62f3e5710570ab18e024cfc5f565aa517d3094afff38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63766331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2cf88b9b43fcd7963f15edfb83fe97afd5fdb4a84c0c9550747fef06027b2f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-x86_64'; 			sha256='6ef48e4bf25fbf1f1ad50c43b797cc24e12e4cde29765076b4145e09e35f5713'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv6'; 			sha256='8f415a76ad62ff621b26b37a94841ee0d4480862d8da55320c1c8fc9db4d8359'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv7'; 			sha256='64314c73a7d34e4a8b9dad87bab857304fb60b0293703d02be436893e1c37f33'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-aarch64'; 			sha256='d1a04a3eb7fd738cc78e518d179a03adb9fe531ee422b8a14bdccf36d654b73a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-ppc64le'; 			sha256='23bddc8119bce6c0eeef1461bc0526291d60de9042b28780012033ba4082090e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-riscv64'; 			sha256='c4bac574a2123938de4ef410e7cef92d079abe266298c93257cbcc4e17134184'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-s390x'; 			sha256='6c0c7d9b6119f68b3dcbf816cf9e5782eb7cea8d2433f8a51b95a41276241e18'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:b5efa4ecc356aa3f967cf3252f33f35689d69748ad15f6ab382dfbc77e53db68`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 18.1 MB (18112377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8980aece4ef386b0d4c63fa11ec664751daa90f6c5144d7ee6983e0f66a321b`  
		Last Modified: Tue, 14 Jan 2025 01:36:24 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999f06d4f41595fc49c1bbb9b00b3cd4f91965126bb974d09c572be01729d08b`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8b82c0cdef43fe4b7645f72f8fe205f6a146384aa0b8c2e73839234796ffc0`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:2b97a1b68497256fc60402e3f5abdb7fb6ab5225d56c1fc671133f2e941c5062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2440854a0cd314cf190b2a6a09c7df59ee4e688a46b9c67324944a7cee09901`

```dockerfile
```

-	Layers:
	-	`sha256:4691173ba00bf555533f59934544855695b5d6d51bba5d12e6194b963a43d6a4`  
		Last Modified: Tue, 14 Jan 2025 01:36:24 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:23923b350de3a2507ee862e801af31acba737fa860a838f5a8e6c7a20056484a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62776091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a313bc642a94a003db6f292d37ce38f797f24997e6dbb16cc41da224f9b81349`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-x86_64'; 			sha256='6ef48e4bf25fbf1f1ad50c43b797cc24e12e4cde29765076b4145e09e35f5713'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv6'; 			sha256='8f415a76ad62ff621b26b37a94841ee0d4480862d8da55320c1c8fc9db4d8359'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv7'; 			sha256='64314c73a7d34e4a8b9dad87bab857304fb60b0293703d02be436893e1c37f33'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-aarch64'; 			sha256='d1a04a3eb7fd738cc78e518d179a03adb9fe531ee422b8a14bdccf36d654b73a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-ppc64le'; 			sha256='23bddc8119bce6c0eeef1461bc0526291d60de9042b28780012033ba4082090e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-riscv64'; 			sha256='c4bac574a2123938de4ef410e7cef92d079abe266298c93257cbcc4e17134184'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-s390x'; 			sha256='6c0c7d9b6119f68b3dcbf816cf9e5782eb7cea8d2433f8a51b95a41276241e18'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:f2df6afa274a12165455efa57585f14851edbe3c8431e611e4aa514c2301b5ae`  
		Last Modified: Tue, 14 Jan 2025 01:40:41 GMT  
		Size: 16.9 MB (16855866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01eb77069da975cd16e756769bced234ed0f0ce04114d17b4fff3f3961ff7fdb`  
		Last Modified: Tue, 14 Jan 2025 01:40:41 GMT  
		Size: 17.4 MB (17427588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2b0f6d3c6a29b62407828319989bf534854431cdf5cc37dfbf8f4265ee109e`  
		Last Modified: Tue, 14 Jan 2025 01:40:41 GMT  
		Size: 18.1 MB (18099444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb58313a02889661a0827edac2479fe14f136f072f9455c7401f027b731565`  
		Last Modified: Tue, 14 Jan 2025 01:40:40 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a31c7f92732acfb2da6e4003cc0236067eeebca4fdb7fd0578439be93bf221`  
		Last Modified: Tue, 14 Jan 2025 01:40:41 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744ae77c3140a38213a1adbd7f5730687718b7d1174559a578dd21556d5fbc70`  
		Last Modified: Tue, 14 Jan 2025 01:40:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:208152349647b5817d0e8732f0d0dbc10072a46f8ef4336fa213a63fc8a33202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156dfbb0c501116bdacec71b4b366939a77df27332590e0dbc91663289b12c2c`

```dockerfile
```

-	Layers:
	-	`sha256:1acab073d9634576b42209cc73006115c1a4fb59cb51d376758c181229c3ee6f`  
		Last Modified: Tue, 14 Jan 2025 01:40:39 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c50766834094413ee0950a29b198399229423316f3fc981748adcec98e9ab775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64619543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62380b06f7e73d08c2f8cc69cf22e68b8b0964d4e943cd7902edebf72bdb8861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-x86_64'; 			sha256='6ef48e4bf25fbf1f1ad50c43b797cc24e12e4cde29765076b4145e09e35f5713'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv6'; 			sha256='8f415a76ad62ff621b26b37a94841ee0d4480862d8da55320c1c8fc9db4d8359'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv7'; 			sha256='64314c73a7d34e4a8b9dad87bab857304fb60b0293703d02be436893e1c37f33'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-aarch64'; 			sha256='d1a04a3eb7fd738cc78e518d179a03adb9fe531ee422b8a14bdccf36d654b73a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-ppc64le'; 			sha256='23bddc8119bce6c0eeef1461bc0526291d60de9042b28780012033ba4082090e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-riscv64'; 			sha256='c4bac574a2123938de4ef410e7cef92d079abe266298c93257cbcc4e17134184'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-s390x'; 			sha256='6c0c7d9b6119f68b3dcbf816cf9e5782eb7cea8d2433f8a51b95a41276241e18'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43785ac1a9e530c3cf3f5502efdd8eb2ca0fe74ce2e9dacfcf49cc1cd44ff5b`  
		Last Modified: Tue, 14 Jan 2025 01:40:05 GMT  
		Size: 8.1 MB (8073121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443e45b7ebe0d6fed7d323b8c918357ccec700454ec81770dd307b744905bef2`  
		Last Modified: Tue, 14 Jan 2025 01:40:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1042953f4da92c640616f959f1c17179c50b5bcbb6bdc9f894f38b4278d5db46`  
		Last Modified: Tue, 14 Jan 2025 01:40:05 GMT  
		Size: 17.8 MB (17795750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595709626d52a6ebd1b0e6f2f42977b3d1eb93f23dc20f0fcff5189182226760`  
		Last Modified: Tue, 14 Jan 2025 01:40:05 GMT  
		Size: 17.1 MB (17106450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748acb43c50f1bb7dbea6130ec9107d0f49825c28b2980022cab395526b50be`  
		Last Modified: Tue, 14 Jan 2025 01:40:08 GMT  
		Size: 17.6 MB (17649713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1870e6ecb9e9730d191ac6aa59e5347eebf36c4df5f1c731a00f2cd2d8f504cf`  
		Last Modified: Tue, 14 Jan 2025 01:40:06 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728bbf9b069189d2d739494cb11a3a541b0f53c1e6432d25588228efc0061360`  
		Last Modified: Tue, 14 Jan 2025 01:40:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0dce1ac1b31cc57ce7e0e566085cadacde994d75882f409fd806190989973c`  
		Last Modified: Tue, 14 Jan 2025 01:40:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:aa5987741b6bbf500dfd9175af5800e5d87ba69bba7bb90c4696491570a18d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084c240dfaf22b97381310758a9c28cce3af37c241e02dc7457710416ed68324`

```dockerfile
```

-	Layers:
	-	`sha256:37e6330f383c6a94d354a35890b299d12ffd73c15f1b5691ea42a5bf6bd7c1c6`  
		Last Modified: Tue, 14 Jan 2025 01:40:04 GMT  
		Size: 38.3 KB (38321 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:3c8fb358b82767a38189e54a89a2ba8d71109f0a17efa87fd009ef8283c46df6
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
$ docker pull docker@sha256:49e6ff5ed3f0137c76b051de305780c16f03b9bd17fec1244808194c9e823b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133457249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0ad917400429d6dea8ffbfb4937b3319f86da6ba149904d9a6ed3de27ed40c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9da8d98be9c497538e046636271095d60600736b8b98dd17d89b85cf6750a8f`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 8.1 MB (8058734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4386589b6f3f3d4248a89850307f7fce69767219761e159ae96376e95133648c`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a489f3b5fec0148d769933a6c683cf67788489232797ba6b97cedc28fba6e83`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 18.7 MB (18669947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098516bf325695b24ce2974045b3ddb5dcdb829015737c0bed7a538be5456ee1`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 18.8 MB (18798865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5bc19395419c3a98f4744b34640d249289415e1edb1e030bf6a58333628592`  
		Last Modified: Thu, 09 Jan 2025 22:28:46 GMT  
		Size: 19.3 MB (19308702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9611a6289157d3d5da09d21f919439c1d7f75f52c4f1c86ee4935487625980c6`  
		Last Modified: Thu, 09 Jan 2025 22:28:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380e7224928097502689c0c3e6dd922dbca5bceb3e5e249123e5b0ce9d13ecde`  
		Last Modified: Thu, 09 Jan 2025 22:28:46 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc6c2a895485e0e9ccb5a3268ffe8ca41f9b3ef6e932337b94f7591126ae90f`  
		Last Modified: Thu, 09 Jan 2025 22:28:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccd10a0d08c0066160d5b279905caebe908957991b637d7293112c10f9254a6`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 6.7 MB (6733477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4e953c13592b855fe5ac2c004028573ca254b3b449c693253578413529b596`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 89.4 KB (89423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf11bfad06271553522156c7166b33e0624501d3119499ef1f46a9d203dc51c3`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fa1d5b8c62c41eb58aeb44f3d2802853db92ca56374ec46745e1ad274a660e`  
		Last Modified: Thu, 09 Jan 2025 23:09:51 GMT  
		Size: 58.1 MB (58148440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1922b615ab4786237b943630fce1b166e2d302351e86e3119f4ae440f7b7905`  
		Last Modified: Thu, 09 Jan 2025 23:09:51 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b317a0873086e41961b65278ad4f6754bd4f730f99945c89f43bb766f5a491d8`  
		Last Modified: Thu, 09 Jan 2025 23:09:51 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:cc1d4784142745c9b47911162f779031f55fc37b7eda97a59f41955920e24a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94905195960a1412761e9794cf2ecd9e83058b3550a91fa562a0a652c558748`

```dockerfile
```

-	Layers:
	-	`sha256:2675d6a7be39c97d9c9690e58c9765ec5bca8b3e2b9e5c3fb868b17da42f207f`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:1f43d24f4b7e21e4b8ec633437279807fac93d6da1d8c1034219ce24d3166c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124584943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac030345b438a7667a295dd56d5c7abc875bd22d1eb08553b257069de82d4a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
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
	-	`sha256:cf73d7cc46a3267dcec3cfc7f304f1abf870c9ecbd6d90f397551be5eff00ae6`  
		Last Modified: Wed, 08 Jan 2025 18:20:41 GMT  
		Size: 16.7 MB (16706472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c7eea2794b482866fb44247a621611bd3105b4f590ec047a41cac4d623e08f`  
		Last Modified: Wed, 08 Jan 2025 18:20:41 GMT  
		Size: 17.4 MB (17448777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16db69aa77862f611701d543dad7e67909f47fcd5d9a9574b9f97a11ba983d29`  
		Last Modified: Thu, 09 Jan 2025 22:30:31 GMT  
		Size: 18.1 MB (18117040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc79f3781d43c0acb2321b1a5716529ab8dd5ef7077e18b0c58a7671854782d`  
		Last Modified: Thu, 09 Jan 2025 22:30:30 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0c94e4fa8de6f36d61b3f90d7d24a03d4c0adcf54276f3abd0226ed166a03e`  
		Last Modified: Thu, 09 Jan 2025 22:30:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9240b077258b7ccef62b5cb88015fe3861991b7dbb7e3205cc5bdb5b0e9e62a`  
		Last Modified: Thu, 09 Jan 2025 22:30:30 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4320f12f1df4243ec5345fea61730e028969bc9c2e48db250684f019bbc71204`  
		Last Modified: Thu, 09 Jan 2025 23:09:43 GMT  
		Size: 7.0 MB (7041225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136ce7681116932314215ea74a5c2a1ec992dcb2806b22a8adb1ad624d1ace6c`  
		Last Modified: Thu, 09 Jan 2025 23:09:42 GMT  
		Size: 89.1 KB (89081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede844aa6bf08e33cbf33b8ab3d54a83218ada675b1e41dcc27dc06c15770f1e`  
		Last Modified: Thu, 09 Jan 2025 23:09:42 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b84dba6d364e19485ec2c81348af1224c45bf5d5d14f699ceb37e3a5a0603e`  
		Last Modified: Thu, 09 Jan 2025 23:09:44 GMT  
		Size: 53.8 MB (53837600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d54dd5266f2a390068c556eb150d4af862281da4aac8d5ea4b283aee2a78af5`  
		Last Modified: Thu, 09 Jan 2025 23:09:43 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3861e2840ecc26375f926f01a8d3eac81da62f6cb2b6e253a6b618333de650be`  
		Last Modified: Thu, 09 Jan 2025 23:09:43 GMT  
		Size: 3.3 KB (3267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:df2dac21f9fd059948ecd5332d14a694d17dcdf7a81cd945b0cb17ff3af8289e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f5f1dd987e3f8758b1531674eb3bd13f84ec122a17691372a7ffe3b93300fe`

```dockerfile
```

-	Layers:
	-	`sha256:44a65346f729ddd7e3c711f15bfc80de482b0a9bc76a38a130411c8049b6372d`  
		Last Modified: Thu, 09 Jan 2025 23:09:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:6c2e036e5e3571aefcfe6cc0ef1dec1ea8ad723a6b68692c17c778588bcb3280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122910186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b1979896efc6f276834731288c136dfcec5c72d40df0380f41303601316421`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
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
	-	`sha256:b346517794cfce1f41b95c705ae9e23769f0eead55b0e45aa310726d624d7e36`  
		Last Modified: Thu, 09 Jan 2025 22:31:30 GMT  
		Size: 16.7 MB (16694613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8af6fe42dd3bd1002a36a0678d7433d5bc1c9b65222d55d1be8f669b50d50ad`  
		Last Modified: Thu, 09 Jan 2025 22:31:30 GMT  
		Size: 17.4 MB (17427581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435b00e153eefddcfb5674d73a4be8017ab0cbee851a5bd11e33016e9b8b8fcc`  
		Last Modified: Thu, 09 Jan 2025 22:31:30 GMT  
		Size: 18.1 MB (18098994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823050d528d8277f11b4566a452e8b76b5e7d7097577342b3d85675aa1f28`  
		Last Modified: Thu, 09 Jan 2025 22:31:29 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fba272fee8435a6f01afdef863fc92b288e2e33bb5d72e633c48abeb1c9967`  
		Last Modified: Thu, 09 Jan 2025 22:31:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4a813131a303def688ad87697fb38ee2b0db911fc22611c905ded3e13d49c4`  
		Last Modified: Thu, 09 Jan 2025 22:31:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa0618922e6709169133b10f595ba8793b03f956a1c7d131890749d66bd336b`  
		Last Modified: Thu, 09 Jan 2025 23:09:55 GMT  
		Size: 6.4 MB (6367220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0a7426d34ab170c52bd4868bf7b90982d98d298f325aba23a37262ee806418`  
		Last Modified: Thu, 09 Jan 2025 23:09:54 GMT  
		Size: 85.2 KB (85224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc89450f6e7f80827ca9f053ec7083fa5e47f3c10f571ce54b8040407058b90c`  
		Last Modified: Thu, 09 Jan 2025 23:09:54 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443963719d80b474f394eb3661e099fd0571d87e95d7d197e87543e1e4366769`  
		Last Modified: Thu, 09 Jan 2025 23:09:56 GMT  
		Size: 53.8 MB (53837561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf03937475f71182a6a712879c07c398b3f9c57b1e0de7af4132cfdea614103`  
		Last Modified: Thu, 09 Jan 2025 23:09:55 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71964f6ba278659ffb392cbd74eb102105929fb5003906d8cf4d49b8a13eff32`  
		Last Modified: Thu, 09 Jan 2025 23:09:55 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:537d0bfd92a4fd1d6a1762140e72d9296020996bd4286ac948043a25512c71c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3f3f3334c8bbb35e6980553891309aa4b5e829d2b3cf9600a7d799d46f6154`

```dockerfile
```

-	Layers:
	-	`sha256:5d7cc935cb72609d8dda009220f97c687934bca9466138209cf43e28b4ae0c23`  
		Last Modified: Thu, 09 Jan 2025 23:09:54 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e39c2cc3c90814aab0b980fbe31a46c46ccd326a31a954aec10b08e17a00f636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125270256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85d4f06cded869b75594119c992d1934951663e005b7b0fbfd21c6ccc18a544`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3528552267cec0f9e2dee7d372df3bbea6255a3ca1a18ba3e58e5cfd106d15e1`  
		Last Modified: Thu, 09 Jan 2025 22:29:23 GMT  
		Size: 8.1 MB (8073134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4781719ef357b2c136f17ff57b79d601b4058a8861d68048cf902106cf3ae9d`  
		Last Modified: Thu, 09 Jan 2025 22:29:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4866b03f4ce1c603a6809790707aae8972781d4ff1b1090b3960153b3abec1e0`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.6 MB (17619398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d036bb2a7049761d033d283b4bc752d8e2d6e25b9ea4bf4329e6a7055ad82e`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.1 MB (17106450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4fa20503c91c2405741c5b1d40f5567a7c641a4624b6c0693716eb0fa6752e`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.7 MB (17653961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f999290013a7bee6f7b09186deee9dc98564604594aac128b7293ef882edfd34`  
		Last Modified: Thu, 09 Jan 2025 22:29:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dca40438acce378f07676329455acd2969680d9ceeeee33d5f34cb1f06c2f4`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730c1436b4a8c8addd307436381ccbe5d3d3adf57e2b67228ea624046c0f4997`  
		Last Modified: Thu, 09 Jan 2025 22:29:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aed778d4d37e95ff4fef9353934ac33be3d14475532284512418c3c7e8802ea`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 7.0 MB (6981951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2357ac4e3b4ca2ae4efd996c265963976e946d8abe41868260f6fc228d6e6cc4`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 97.8 KB (97785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f2dd98d7754adf87dda19dcbdb3a884046d0c27693b4d9c3465c4ae77eca5c`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af42edc6d44256189864a2f5cf56c06590a42e61aeb9f18a2c453de7841076b0`  
		Last Modified: Thu, 09 Jan 2025 23:09:59 GMT  
		Size: 53.7 MB (53737271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518ad24d587855579d9d75a11a4e2b7e0c347114c536d13580a4ea61bde47f9`  
		Last Modified: Thu, 09 Jan 2025 23:09:58 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbdc874d308be16b20915161093ad9bf64226aace0cc1e4a6c39989bc8b42e8`  
		Last Modified: Thu, 09 Jan 2025 23:09:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:3c55cbc4001fb31954e54c34ad17b6c51d156dec418ed2d5227cde645a42dd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae631f8a48e90d1da91e6ad880706bd056becca1725a0b75bcb80783f4aba81`

```dockerfile
```

-	Layers:
	-	`sha256:3a2a24b3e925024d6bde4094ebc288eba2297cf6906eda280f8e1e4735abed3a`  
		Last Modified: Thu, 09 Jan 2025 23:09:56 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:3e770a24d3b2b21cfe6bf4f163a3989369235d2e26d47da14e719df3d5539dda
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:7c17ce13c8e0d7d22974ac948f6e11199b70ad2a7161443daba306d989c6833a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155749030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6dc42df64f885d426d42c6985a30d33978f9c04f3bd748919a851b6eec8d81e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD []
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
USER rootless
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9da8d98be9c497538e046636271095d60600736b8b98dd17d89b85cf6750a8f`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 8.1 MB (8058734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4386589b6f3f3d4248a89850307f7fce69767219761e159ae96376e95133648c`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a489f3b5fec0148d769933a6c683cf67788489232797ba6b97cedc28fba6e83`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 18.7 MB (18669947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098516bf325695b24ce2974045b3ddb5dcdb829015737c0bed7a538be5456ee1`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 18.8 MB (18798865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5bc19395419c3a98f4744b34640d249289415e1edb1e030bf6a58333628592`  
		Last Modified: Thu, 09 Jan 2025 22:28:46 GMT  
		Size: 19.3 MB (19308702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9611a6289157d3d5da09d21f919439c1d7f75f52c4f1c86ee4935487625980c6`  
		Last Modified: Thu, 09 Jan 2025 22:28:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380e7224928097502689c0c3e6dd922dbca5bceb3e5e249123e5b0ce9d13ecde`  
		Last Modified: Thu, 09 Jan 2025 22:28:46 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc6c2a895485e0e9ccb5a3268ffe8ca41f9b3ef6e932337b94f7591126ae90f`  
		Last Modified: Thu, 09 Jan 2025 22:28:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccd10a0d08c0066160d5b279905caebe908957991b637d7293112c10f9254a6`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 6.7 MB (6733477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4e953c13592b855fe5ac2c004028573ca254b3b449c693253578413529b596`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 89.4 KB (89423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf11bfad06271553522156c7166b33e0624501d3119499ef1f46a9d203dc51c3`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fa1d5b8c62c41eb58aeb44f3d2802853db92ca56374ec46745e1ad274a660e`  
		Last Modified: Thu, 09 Jan 2025 23:09:51 GMT  
		Size: 58.1 MB (58148440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1922b615ab4786237b943630fce1b166e2d302351e86e3119f4ae440f7b7905`  
		Last Modified: Thu, 09 Jan 2025 23:09:51 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b317a0873086e41961b65278ad4f6754bd4f730f99945c89f43bb766f5a491d8`  
		Last Modified: Thu, 09 Jan 2025 23:09:51 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db5e91f12b0771939beaf1d2267459f2493824d96a199c6f2cfc2e9e1ad2b20`  
		Last Modified: Fri, 10 Jan 2025 00:07:37 GMT  
		Size: 986.6 KB (986560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f3c2a2ccc5c1c0c6b9a8bffbb7ad2f411aa048317f413b2e763c21a397d559`  
		Last Modified: Fri, 10 Jan 2025 00:07:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdccb280e79d0701bb90ad2b947a87729d781ade93dbcb32c8638605f70de0e`  
		Last Modified: Fri, 10 Jan 2025 00:07:37 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cac4f2399f9cc3df49b5713e7ed0dfd23d6612dc071a97e1b11451237ec954`  
		Last Modified: Fri, 10 Jan 2025 00:07:38 GMT  
		Size: 21.3 MB (21303870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73584c7d6ffa77bc341da6b601de589dbb3bc90094dc1506ca7221c18f545976`  
		Last Modified: Fri, 10 Jan 2025 00:07:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a00de156e44b0944a7125426ca4e91c3d3090763debd7d047cf7eda4a39dca87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79936c5c0e560b15b0aad0c8835b9075dd3c50c7fec4f31458eb36228987a1cb`

```dockerfile
```

-	Layers:
	-	`sha256:eadc9d4056786a4ec1c155b1f08ce83af47fd3975f0deedd2ff41384e0bc788e`  
		Last Modified: Fri, 10 Jan 2025 00:07:37 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8877919584cc9a4577906c6c60656e7c44b7c8dae3b65f8d7b74acd9b8947ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149440959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b3ab72d35f78cfb25f15813532542dc016c0f9fd7889844e68ba6df769a39b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD []
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
USER rootless
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3528552267cec0f9e2dee7d372df3bbea6255a3ca1a18ba3e58e5cfd106d15e1`  
		Last Modified: Thu, 09 Jan 2025 22:29:23 GMT  
		Size: 8.1 MB (8073134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4781719ef357b2c136f17ff57b79d601b4058a8861d68048cf902106cf3ae9d`  
		Last Modified: Thu, 09 Jan 2025 22:29:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4866b03f4ce1c603a6809790707aae8972781d4ff1b1090b3960153b3abec1e0`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.6 MB (17619398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d036bb2a7049761d033d283b4bc752d8e2d6e25b9ea4bf4329e6a7055ad82e`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.1 MB (17106450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4fa20503c91c2405741c5b1d40f5567a7c641a4624b6c0693716eb0fa6752e`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.7 MB (17653961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f999290013a7bee6f7b09186deee9dc98564604594aac128b7293ef882edfd34`  
		Last Modified: Thu, 09 Jan 2025 22:29:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dca40438acce378f07676329455acd2969680d9ceeeee33d5f34cb1f06c2f4`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730c1436b4a8c8addd307436381ccbe5d3d3adf57e2b67228ea624046c0f4997`  
		Last Modified: Thu, 09 Jan 2025 22:29:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aed778d4d37e95ff4fef9353934ac33be3d14475532284512418c3c7e8802ea`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 7.0 MB (6981951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2357ac4e3b4ca2ae4efd996c265963976e946d8abe41868260f6fc228d6e6cc4`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 97.8 KB (97785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f2dd98d7754adf87dda19dcbdb3a884046d0c27693b4d9c3465c4ae77eca5c`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af42edc6d44256189864a2f5cf56c06590a42e61aeb9f18a2c453de7841076b0`  
		Last Modified: Thu, 09 Jan 2025 23:09:59 GMT  
		Size: 53.7 MB (53737271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518ad24d587855579d9d75a11a4e2b7e0c347114c536d13580a4ea61bde47f9`  
		Last Modified: Thu, 09 Jan 2025 23:09:58 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbdc874d308be16b20915161093ad9bf64226aace0cc1e4a6c39989bc8b42e8`  
		Last Modified: Thu, 09 Jan 2025 23:09:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fb49e0358a6dcd8f454c229f2e58043c238bd1c31bf2592d90ccf2c54f4e51`  
		Last Modified: Fri, 10 Jan 2025 00:07:30 GMT  
		Size: 1.0 MB (1014210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439b04567bec34e568e7ccb361a72f63a1d46f4d92ecb655b923adc811884224`  
		Last Modified: Fri, 10 Jan 2025 00:07:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914c5eaa7edf15934269fdc326ef1f67b1143f22258e44663c95398675d41f63`  
		Last Modified: Fri, 10 Jan 2025 00:07:29 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b68b3535056a1cc8be40c353f77739f156a5090082cc6be776be14d05d2caa1`  
		Last Modified: Fri, 10 Jan 2025 00:07:30 GMT  
		Size: 23.2 MB (23155143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f44128077eafee533110d4ac4367e5385cabd2739d3546d5c3d1dec4178ae04`  
		Last Modified: Fri, 10 Jan 2025 00:07:30 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3f6f181021a43b59a102e93c0b8ef6e94e8d5f579a9cfc058dccda16ea356cda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58fb060b226c196a27de2c0ef71eb8106443bf7c6124ee1de21d08359d8fb72d`

```dockerfile
```

-	Layers:
	-	`sha256:254aaf99f8db72b2d239c240a4ed5a914197c55e50a316ddee0c09a4ba50cfe8`  
		Last Modified: Fri, 10 Jan 2025 00:07:29 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:3c8fb358b82767a38189e54a89a2ba8d71109f0a17efa87fd009ef8283c46df6
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
$ docker pull docker@sha256:49e6ff5ed3f0137c76b051de305780c16f03b9bd17fec1244808194c9e823b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133457249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0ad917400429d6dea8ffbfb4937b3319f86da6ba149904d9a6ed3de27ed40c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD []
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9da8d98be9c497538e046636271095d60600736b8b98dd17d89b85cf6750a8f`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 8.1 MB (8058734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4386589b6f3f3d4248a89850307f7fce69767219761e159ae96376e95133648c`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a489f3b5fec0148d769933a6c683cf67788489232797ba6b97cedc28fba6e83`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 18.7 MB (18669947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098516bf325695b24ce2974045b3ddb5dcdb829015737c0bed7a538be5456ee1`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 18.8 MB (18798865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5bc19395419c3a98f4744b34640d249289415e1edb1e030bf6a58333628592`  
		Last Modified: Thu, 09 Jan 2025 22:28:46 GMT  
		Size: 19.3 MB (19308702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9611a6289157d3d5da09d21f919439c1d7f75f52c4f1c86ee4935487625980c6`  
		Last Modified: Thu, 09 Jan 2025 22:28:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380e7224928097502689c0c3e6dd922dbca5bceb3e5e249123e5b0ce9d13ecde`  
		Last Modified: Thu, 09 Jan 2025 22:28:46 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc6c2a895485e0e9ccb5a3268ffe8ca41f9b3ef6e932337b94f7591126ae90f`  
		Last Modified: Thu, 09 Jan 2025 22:28:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccd10a0d08c0066160d5b279905caebe908957991b637d7293112c10f9254a6`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 6.7 MB (6733477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4e953c13592b855fe5ac2c004028573ca254b3b449c693253578413529b596`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 89.4 KB (89423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf11bfad06271553522156c7166b33e0624501d3119499ef1f46a9d203dc51c3`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fa1d5b8c62c41eb58aeb44f3d2802853db92ca56374ec46745e1ad274a660e`  
		Last Modified: Thu, 09 Jan 2025 23:09:51 GMT  
		Size: 58.1 MB (58148440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1922b615ab4786237b943630fce1b166e2d302351e86e3119f4ae440f7b7905`  
		Last Modified: Thu, 09 Jan 2025 23:09:51 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b317a0873086e41961b65278ad4f6754bd4f730f99945c89f43bb766f5a491d8`  
		Last Modified: Thu, 09 Jan 2025 23:09:51 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:cc1d4784142745c9b47911162f779031f55fc37b7eda97a59f41955920e24a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94905195960a1412761e9794cf2ecd9e83058b3550a91fa562a0a652c558748`

```dockerfile
```

-	Layers:
	-	`sha256:2675d6a7be39c97d9c9690e58c9765ec5bca8b3e2b9e5c3fb868b17da42f207f`  
		Last Modified: Thu, 09 Jan 2025 23:09:50 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:1f43d24f4b7e21e4b8ec633437279807fac93d6da1d8c1034219ce24d3166c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124584943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac030345b438a7667a295dd56d5c7abc875bd22d1eb08553b257069de82d4a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
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
	-	`sha256:cf73d7cc46a3267dcec3cfc7f304f1abf870c9ecbd6d90f397551be5eff00ae6`  
		Last Modified: Wed, 08 Jan 2025 18:20:41 GMT  
		Size: 16.7 MB (16706472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c7eea2794b482866fb44247a621611bd3105b4f590ec047a41cac4d623e08f`  
		Last Modified: Wed, 08 Jan 2025 18:20:41 GMT  
		Size: 17.4 MB (17448777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16db69aa77862f611701d543dad7e67909f47fcd5d9a9574b9f97a11ba983d29`  
		Last Modified: Thu, 09 Jan 2025 22:30:31 GMT  
		Size: 18.1 MB (18117040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc79f3781d43c0acb2321b1a5716529ab8dd5ef7077e18b0c58a7671854782d`  
		Last Modified: Thu, 09 Jan 2025 22:30:30 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0c94e4fa8de6f36d61b3f90d7d24a03d4c0adcf54276f3abd0226ed166a03e`  
		Last Modified: Thu, 09 Jan 2025 22:30:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9240b077258b7ccef62b5cb88015fe3861991b7dbb7e3205cc5bdb5b0e9e62a`  
		Last Modified: Thu, 09 Jan 2025 22:30:30 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4320f12f1df4243ec5345fea61730e028969bc9c2e48db250684f019bbc71204`  
		Last Modified: Thu, 09 Jan 2025 23:09:43 GMT  
		Size: 7.0 MB (7041225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136ce7681116932314215ea74a5c2a1ec992dcb2806b22a8adb1ad624d1ace6c`  
		Last Modified: Thu, 09 Jan 2025 23:09:42 GMT  
		Size: 89.1 KB (89081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede844aa6bf08e33cbf33b8ab3d54a83218ada675b1e41dcc27dc06c15770f1e`  
		Last Modified: Thu, 09 Jan 2025 23:09:42 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b84dba6d364e19485ec2c81348af1224c45bf5d5d14f699ceb37e3a5a0603e`  
		Last Modified: Thu, 09 Jan 2025 23:09:44 GMT  
		Size: 53.8 MB (53837600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d54dd5266f2a390068c556eb150d4af862281da4aac8d5ea4b283aee2a78af5`  
		Last Modified: Thu, 09 Jan 2025 23:09:43 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3861e2840ecc26375f926f01a8d3eac81da62f6cb2b6e253a6b618333de650be`  
		Last Modified: Thu, 09 Jan 2025 23:09:43 GMT  
		Size: 3.3 KB (3267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:df2dac21f9fd059948ecd5332d14a694d17dcdf7a81cd945b0cb17ff3af8289e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f5f1dd987e3f8758b1531674eb3bd13f84ec122a17691372a7ffe3b93300fe`

```dockerfile
```

-	Layers:
	-	`sha256:44a65346f729ddd7e3c711f15bfc80de482b0a9bc76a38a130411c8049b6372d`  
		Last Modified: Thu, 09 Jan 2025 23:09:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:6c2e036e5e3571aefcfe6cc0ef1dec1ea8ad723a6b68692c17c778588bcb3280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122910186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b1979896efc6f276834731288c136dfcec5c72d40df0380f41303601316421`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
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
	-	`sha256:b346517794cfce1f41b95c705ae9e23769f0eead55b0e45aa310726d624d7e36`  
		Last Modified: Thu, 09 Jan 2025 22:31:30 GMT  
		Size: 16.7 MB (16694613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8af6fe42dd3bd1002a36a0678d7433d5bc1c9b65222d55d1be8f669b50d50ad`  
		Last Modified: Thu, 09 Jan 2025 22:31:30 GMT  
		Size: 17.4 MB (17427581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435b00e153eefddcfb5674d73a4be8017ab0cbee851a5bd11e33016e9b8b8fcc`  
		Last Modified: Thu, 09 Jan 2025 22:31:30 GMT  
		Size: 18.1 MB (18098994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823050d528d8277f11b4566a452e8b76b5e7d7097577342b3d85675aa1f28`  
		Last Modified: Thu, 09 Jan 2025 22:31:29 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fba272fee8435a6f01afdef863fc92b288e2e33bb5d72e633c48abeb1c9967`  
		Last Modified: Thu, 09 Jan 2025 22:31:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4a813131a303def688ad87697fb38ee2b0db911fc22611c905ded3e13d49c4`  
		Last Modified: Thu, 09 Jan 2025 22:31:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa0618922e6709169133b10f595ba8793b03f956a1c7d131890749d66bd336b`  
		Last Modified: Thu, 09 Jan 2025 23:09:55 GMT  
		Size: 6.4 MB (6367220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0a7426d34ab170c52bd4868bf7b90982d98d298f325aba23a37262ee806418`  
		Last Modified: Thu, 09 Jan 2025 23:09:54 GMT  
		Size: 85.2 KB (85224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc89450f6e7f80827ca9f053ec7083fa5e47f3c10f571ce54b8040407058b90c`  
		Last Modified: Thu, 09 Jan 2025 23:09:54 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443963719d80b474f394eb3661e099fd0571d87e95d7d197e87543e1e4366769`  
		Last Modified: Thu, 09 Jan 2025 23:09:56 GMT  
		Size: 53.8 MB (53837561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf03937475f71182a6a712879c07c398b3f9c57b1e0de7af4132cfdea614103`  
		Last Modified: Thu, 09 Jan 2025 23:09:55 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71964f6ba278659ffb392cbd74eb102105929fb5003906d8cf4d49b8a13eff32`  
		Last Modified: Thu, 09 Jan 2025 23:09:55 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:537d0bfd92a4fd1d6a1762140e72d9296020996bd4286ac948043a25512c71c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3f3f3334c8bbb35e6980553891309aa4b5e829d2b3cf9600a7d799d46f6154`

```dockerfile
```

-	Layers:
	-	`sha256:5d7cc935cb72609d8dda009220f97c687934bca9466138209cf43e28b4ae0c23`  
		Last Modified: Thu, 09 Jan 2025 23:09:54 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e39c2cc3c90814aab0b980fbe31a46c46ccd326a31a954aec10b08e17a00f636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125270256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85d4f06cded869b75594119c992d1934951663e005b7b0fbfd21c6ccc18a544`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3528552267cec0f9e2dee7d372df3bbea6255a3ca1a18ba3e58e5cfd106d15e1`  
		Last Modified: Thu, 09 Jan 2025 22:29:23 GMT  
		Size: 8.1 MB (8073134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4781719ef357b2c136f17ff57b79d601b4058a8861d68048cf902106cf3ae9d`  
		Last Modified: Thu, 09 Jan 2025 22:29:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4866b03f4ce1c603a6809790707aae8972781d4ff1b1090b3960153b3abec1e0`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.6 MB (17619398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d036bb2a7049761d033d283b4bc752d8e2d6e25b9ea4bf4329e6a7055ad82e`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.1 MB (17106450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4fa20503c91c2405741c5b1d40f5567a7c641a4624b6c0693716eb0fa6752e`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.7 MB (17653961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f999290013a7bee6f7b09186deee9dc98564604594aac128b7293ef882edfd34`  
		Last Modified: Thu, 09 Jan 2025 22:29:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dca40438acce378f07676329455acd2969680d9ceeeee33d5f34cb1f06c2f4`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730c1436b4a8c8addd307436381ccbe5d3d3adf57e2b67228ea624046c0f4997`  
		Last Modified: Thu, 09 Jan 2025 22:29:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aed778d4d37e95ff4fef9353934ac33be3d14475532284512418c3c7e8802ea`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 7.0 MB (6981951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2357ac4e3b4ca2ae4efd996c265963976e946d8abe41868260f6fc228d6e6cc4`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 97.8 KB (97785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f2dd98d7754adf87dda19dcbdb3a884046d0c27693b4d9c3465c4ae77eca5c`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af42edc6d44256189864a2f5cf56c06590a42e61aeb9f18a2c453de7841076b0`  
		Last Modified: Thu, 09 Jan 2025 23:09:59 GMT  
		Size: 53.7 MB (53737271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518ad24d587855579d9d75a11a4e2b7e0c347114c536d13580a4ea61bde47f9`  
		Last Modified: Thu, 09 Jan 2025 23:09:58 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbdc874d308be16b20915161093ad9bf64226aace0cc1e4a6c39989bc8b42e8`  
		Last Modified: Thu, 09 Jan 2025 23:09:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:3c55cbc4001fb31954e54c34ad17b6c51d156dec418ed2d5227cde645a42dd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae631f8a48e90d1da91e6ad880706bd056becca1725a0b75bcb80783f4aba81`

```dockerfile
```

-	Layers:
	-	`sha256:3a2a24b3e925024d6bde4094ebc288eba2297cf6906eda280f8e1e4735abed3a`  
		Last Modified: Thu, 09 Jan 2025 23:09:56 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:a284c7d6870c4e3d5b1aebd1c58f5a505069a7b0329e978b08abf17513aa7a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:c5cd74a023e7faacafb41c44c2747e96c7876beafafde01fb2492784ca74dff0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2313128368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e61f7f6c4cab2dac3a38e28d586ddb278c5d38b92d47ab9d0589d0f8f2c812d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Tue, 14 Jan 2025 01:33:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 01:34:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 01:34:08 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 01:34:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 01:34:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 01:34:30 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 01:34:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 01:34:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 01:34:40 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 01:34:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b9a42b9ecd66f4d789ad699e16330906d9d369d20469828c662fefe12b02e8`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba018976cff219cd6191a11bfc55504ef36738be82baeb71ffc74b2313dd1a9b`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 357.0 KB (356994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b23dc261c6430fb422dc75b6af8a9222a66dce9202b6dd146d0489236423f3`  
		Last Modified: Tue, 14 Jan 2025 01:34:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ac7c6042d38723e1b4633b555e3fcb9ee7c9a2f2551df07d9fa1de8c8f2a08`  
		Last Modified: Tue, 14 Jan 2025 01:34:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67545a67f1de16e949e21b129bbea57c410284aedc8db5faee026b21c95c944e`  
		Last Modified: Tue, 14 Jan 2025 01:34:57 GMT  
		Size: 19.1 MB (19131320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd02d7c050fc6cdf708efdead243164770cabd577abe8a18db6f288f696ff7b8`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c748dabad2a30c59b0159fa58b3472240315a9ec2f64376d5d0381386a2f97`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ecbbb0ec3c3d976a78844e335b33c792dc71f07c2a7e93f8ee679fb504d98e`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b5b5bfffbb0f5a83a7d094b25d599051fdc8dbf1b50d0c5aea1d591ed0299e`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 19.6 MB (19615409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fa2ea051bffbfc1e545845e1eb270495068cb06e93f8ac57231c31ff4cfd03`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d7751f4c9a5b340fdf6ba7576146996238741661e6cf1a7b2fb461ed4016b1`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7201c016b89daaeb208563dfb1a7e997838e81cd51529341002ee3cb0ae426`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45fcce664eafbed1944672cd2d9447505f859b1fd823dbc7f6e0ffa88ecae7f`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 20.1 MB (20139389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:2412f304f0e829b89301d917174de78b373338e7deea7159f4fa1eb71edd3587
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073619759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b2cc3864ebb611e04f866a8a0df76a2db44807df698f694805d7551cf967ea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 14 Jan 2025 01:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 01:34:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 01:34:10 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 01:34:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 01:34:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:28 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 01:34:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:44 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 01:34:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 01:34:45 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 01:34:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425357308f56dd3b281b2556d37baf9db8f8c3b130904a33ffddde5099320a0d`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6b7c3304749381530c4553df1e4cb56b49ac5ff3f306da88d1927e5c867e2b`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 473.9 KB (473861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd751bf8d052b9254190cd7a90b0ec77465de52b18d8a606b27a9e15c9382172`  
		Last Modified: Tue, 14 Jan 2025 01:35:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fed29470c12c566ce347f7982db8e7c38ca9ffec02fac952816378c3542277`  
		Last Modified: Tue, 14 Jan 2025 01:35:04 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298ed1e5eae2c63f4534bfc920d12710d8df9fd7bddeb178169cc5088f915f6a`  
		Last Modified: Tue, 14 Jan 2025 01:35:06 GMT  
		Size: 19.2 MB (19158530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77dabf7d51887079f09f01958ce57b98a262584e91145268ede9528e71cb4f`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec1d3f15655b584105f5d69418e8450904e56e40f6cc740597d32a24dcf0bd2`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0eff69a154ff66b03dcb32f76f86f5bcc6788eec3b8ee4fe571137d404737f`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9896f36188aaf843315e328e9c93add995fb259b42bfab34c209cc8eb2e2234e`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 19.6 MB (19644525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51c5a778e0da9ab6bb36815596910deefa3d1fbcf6c94a55941da25028dffd7`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b7e381ec9896eca8879369b9e71b4be2e219dedfba7772c47aeef95758f4a0`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6bc972d567de2d4dee7559d75cad49ba3b40a07349d26d5f8efcb2b841824eb`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e1e3140e894e79b619265107b247afff926e38dcbfec4fb75bc065e22d82ca`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 20.2 MB (20160932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:a23e84498a9a98c2b1a9dfa3b48a38c116831491c2fcc91c024c3bec41047eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:2412f304f0e829b89301d917174de78b373338e7deea7159f4fa1eb71edd3587
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073619759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b2cc3864ebb611e04f866a8a0df76a2db44807df698f694805d7551cf967ea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Tue, 14 Jan 2025 01:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 01:34:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 01:34:10 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 01:34:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 01:34:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:28 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 01:34:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:44 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 01:34:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 01:34:45 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 01:34:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425357308f56dd3b281b2556d37baf9db8f8c3b130904a33ffddde5099320a0d`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6b7c3304749381530c4553df1e4cb56b49ac5ff3f306da88d1927e5c867e2b`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 473.9 KB (473861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd751bf8d052b9254190cd7a90b0ec77465de52b18d8a606b27a9e15c9382172`  
		Last Modified: Tue, 14 Jan 2025 01:35:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fed29470c12c566ce347f7982db8e7c38ca9ffec02fac952816378c3542277`  
		Last Modified: Tue, 14 Jan 2025 01:35:04 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298ed1e5eae2c63f4534bfc920d12710d8df9fd7bddeb178169cc5088f915f6a`  
		Last Modified: Tue, 14 Jan 2025 01:35:06 GMT  
		Size: 19.2 MB (19158530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77dabf7d51887079f09f01958ce57b98a262584e91145268ede9528e71cb4f`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec1d3f15655b584105f5d69418e8450904e56e40f6cc740597d32a24dcf0bd2`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0eff69a154ff66b03dcb32f76f86f5bcc6788eec3b8ee4fe571137d404737f`  
		Last Modified: Tue, 14 Jan 2025 01:35:03 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9896f36188aaf843315e328e9c93add995fb259b42bfab34c209cc8eb2e2234e`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 19.6 MB (19644525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51c5a778e0da9ab6bb36815596910deefa3d1fbcf6c94a55941da25028dffd7`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b7e381ec9896eca8879369b9e71b4be2e219dedfba7772c47aeef95758f4a0`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6bc972d567de2d4dee7559d75cad49ba3b40a07349d26d5f8efcb2b841824eb`  
		Last Modified: Tue, 14 Jan 2025 01:35:02 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e1e3140e894e79b619265107b247afff926e38dcbfec4fb75bc065e22d82ca`  
		Last Modified: Tue, 14 Jan 2025 01:35:05 GMT  
		Size: 20.2 MB (20160932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:6550e15f54a41601f5bf6cc07cda68d35cf115561478d97cc87dfdca2b7e8df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:c5cd74a023e7faacafb41c44c2747e96c7876beafafde01fb2492784ca74dff0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2313128368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e61f7f6c4cab2dac3a38e28d586ddb278c5d38b92d47ab9d0589d0f8f2c812d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Tue, 14 Jan 2025 01:33:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 01:34:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 01:34:08 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 01:34:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 01:34:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 01:34:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 01:34:30 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 01:34:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 01:34:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 01:34:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 01:34:40 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 01:34:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b9a42b9ecd66f4d789ad699e16330906d9d369d20469828c662fefe12b02e8`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba018976cff219cd6191a11bfc55504ef36738be82baeb71ffc74b2313dd1a9b`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 357.0 KB (356994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b23dc261c6430fb422dc75b6af8a9222a66dce9202b6dd146d0489236423f3`  
		Last Modified: Tue, 14 Jan 2025 01:34:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ac7c6042d38723e1b4633b555e3fcb9ee7c9a2f2551df07d9fa1de8c8f2a08`  
		Last Modified: Tue, 14 Jan 2025 01:34:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67545a67f1de16e949e21b129bbea57c410284aedc8db5faee026b21c95c944e`  
		Last Modified: Tue, 14 Jan 2025 01:34:57 GMT  
		Size: 19.1 MB (19131320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd02d7c050fc6cdf708efdead243164770cabd577abe8a18db6f288f696ff7b8`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c748dabad2a30c59b0159fa58b3472240315a9ec2f64376d5d0381386a2f97`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ecbbb0ec3c3d976a78844e335b33c792dc71f07c2a7e93f8ee679fb504d98e`  
		Last Modified: Tue, 14 Jan 2025 01:34:54 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b5b5bfffbb0f5a83a7d094b25d599051fdc8dbf1b50d0c5aea1d591ed0299e`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 19.6 MB (19615409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fa2ea051bffbfc1e545845e1eb270495068cb06e93f8ac57231c31ff4cfd03`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d7751f4c9a5b340fdf6ba7576146996238741661e6cf1a7b2fb461ed4016b1`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7201c016b89daaeb208563dfb1a7e997838e81cd51529341002ee3cb0ae426`  
		Last Modified: Tue, 14 Jan 2025 01:34:53 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45fcce664eafbed1944672cd2d9447505f859b1fd823dbc7f6e0ffa88ecae7f`  
		Last Modified: Tue, 14 Jan 2025 01:34:56 GMT  
		Size: 20.1 MB (20139389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
