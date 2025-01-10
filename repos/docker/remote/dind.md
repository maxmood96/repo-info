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
