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
$ docker pull docker@sha256:cbde039f51b3d85366f59fe2e97cdaf329a6eef076b79a9afb9f9568d04d0767
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
$ docker pull docker@sha256:36b7c405e8884e399ac3c7c63f3f61b065a94b62e0b915e62db4d0de3a0aa0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133866334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef043a7d033c06edb878336aba69dc08a2340456f7dc1c2f80a75a362a7f28a8`
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
	-	`sha256:01ede50c7df8b73c8a3ac91fb3bb36978c76e031bb46b82aa12fa72fada06402`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 6.7 MB (6733496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d285c3782350dd5f9e9ba3ffdca6909b3a357f12e4e0aa69f6509f071fbcfbe3`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 89.4 KB (89420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23e2f46c920045fd9af6784bbff05014d36f9150a63b66c744172d76be81c4`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dca5dcdd0a1de285b0723f6c07453eb8ad4c4e39c1d4685a5921590a3228e6`  
		Last Modified: Tue, 14 Jan 2025 02:16:02 GMT  
		Size: 58.4 MB (58383043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88a905ff3d6fd8eeb1a0e9a4da76911f3121664e953d721c866942a7926851a`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76253b0cea165b9074f6b67ca91b09076bb938e59f417391480e5db39bdf1a9`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:e37c8bd01854ac13fcaa41da9fb226c89c8238bef5a9de4787c9dd0cd07938c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88d598c27af9d5b832d3315a7aabddf36261d15c0e4eb374faf85a8590e65c`

```dockerfile
```

-	Layers:
	-	`sha256:56e2c5d5c223aaa11d450a30736bb729d576e219338fd7ffc0de44d4849a78b0`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v6

```console
$ docker pull docker@sha256:9d7a7eeddee151b3a91d4187569b2bfed0bc15418e0a5f6cb964ad1bc5c00d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124949459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257951f363b47b171f00cddf758ba9666b0e34a357a010eb907440a2634cdeb3`
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
	-	`sha256:846cdf8016994cf55c03364ec088d83836cd9124c4feadfdc1a290c0db052ea1`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 7.0 MB (7041193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105e956e17649a3bfc6e14bb6b91440fae0386c90f0a79b4ef0af00a6633a337`  
		Last Modified: Tue, 14 Jan 2025 02:15:17 GMT  
		Size: 89.1 KB (89081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec413a996e6897217d8210770f776246e893b515e1c89145e412f0d0f0cb2a4`  
		Last Modified: Tue, 14 Jan 2025 02:15:17 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03338e4032fbada969eec48dc2c2fee01ed7adf78828bc6d40c04ab9507583d`  
		Last Modified: Tue, 14 Jan 2025 02:15:20 GMT  
		Size: 54.0 MB (54047058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e723cb52bcf30c84558d4ccac188f71c03b8891058ff95be8152022690f21f4f`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5282e780179a5e7e90adcb73980f2f9f70231fef1447fbd149a1bc5c64706`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:8689bdb9c541bab78f9dd1908957878caf8f25c1253d8bce06cdafe62c1144fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c90fd3c8b21ca316ab44ec447e5562c65bf0a586cb80772ee7a88783c272e86`

```dockerfile
```

-	Layers:
	-	`sha256:f42d1ce12c955562a797d5229e156021010cb89d2612a09a3c8038db1e71759b`  
		Last Modified: Tue, 14 Jan 2025 02:15:16 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v7

```console
$ docker pull docker@sha256:5999a9ff7ae4b7bfd9ffbdc09f506554ad45cf038a06735ee5bf8f4319855ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05426371377f59be4857cbf89178a0f3786fe20bc74bc05b8177a8ed9053ff4`
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
	-	`sha256:e3a7347c9e2b4172d426277de5d40fe3125e0c6b4f9c9b1b210c2190c24f71a6`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 6.4 MB (6367075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170816e95ac1cab8fd3486637652d489c9eb3aec9613c3b50d432b9080a822bc`  
		Last Modified: Tue, 14 Jan 2025 02:20:08 GMT  
		Size: 85.2 KB (85226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45751052d07b0cc92dd9bbbb7d3b61c9e7c35c0f7cebfb423551d2bd9b9f5756`  
		Last Modified: Tue, 14 Jan 2025 02:20:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6227cd6b9897a9ed931bc5860ced54ff59f31642da0ab188c39197dc19cad0fe`  
		Last Modified: Tue, 14 Jan 2025 02:20:10 GMT  
		Size: 54.0 MB (54047052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73cbf2e0a446e5961fdd597ab7cf88eeb26bf806635c7d184ab9675ddad4374`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d10838d3f481fcdee3e8625d0e55d29fc7d9679f071020833f3730f57d9d83`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:037c2c83a82e85230be44bdef44cb3b1d52a2e22d058a5de3aceca56e7159130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0386c303557c0cf65db0f5960ebf6b90f8eaa30c74ffe08cb4c55633a6579454`

```dockerfile
```

-	Layers:
	-	`sha256:941354ab8739c4685b3ec8524f7ba8d6f80ed7d2dc31d182e3d796aff9179e45`  
		Last Modified: Tue, 14 Jan 2025 02:20:07 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ebe06ac52e509d7503408f503c85e7184638d3a39f9da87aa8d7435ebabedef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125657212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a08754d01aa0993ff2b714b092fc20d4c49c6f2b4a2e353e59b54bc19c896af`
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
	-	`sha256:bd25f3cb55cedc28ef3ec15976f2b429e5e24e2f2ec8cf36bbaaa7e6c87c994e`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 7.0 MB (6981981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d49b3e3cd0572d2d1fd7020a8df0ff5fe6bc2b0011ddd9eaf8cc24628779ef9`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 97.8 KB (97789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3200f3c13982eac3851a0c9e87c77fbfe96425bc74c4a9a4db3897a614a1a1`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff187bc55eaede3054ec4ae2f34a0780ccd3306daca06b661e97b61a08d7e413`  
		Last Modified: Tue, 14 Jan 2025 02:26:10 GMT  
		Size: 54.0 MB (53952110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee3e8d3d62aa9df8772f783716c898cf08d668f5759aa735966330e4b3540bc`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f568e54dc452c5a82c30e4b27b6d23ae4813b3aec42ddd31a56a9df635a8af58`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:71af01ec9968269e01302b3e5c567694d917a9ff9193f8a336de02c0adfcba6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25642e7f3a9ac8e5eddd583a6b68a8f2802dc2ae11098c5b85bc08b4de76b0fb`

```dockerfile
```

-	Layers:
	-	`sha256:20cf12060b8c0aa852adbbf7cd68171cb42ed9361a70dfc9558418ec756eb3f6`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-cli`

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

### `docker:27-cli` - unknown; unknown

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
$ docker pull docker@sha256:cbde039f51b3d85366f59fe2e97cdaf329a6eef076b79a9afb9f9568d04d0767
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
$ docker pull docker@sha256:36b7c405e8884e399ac3c7c63f3f61b065a94b62e0b915e62db4d0de3a0aa0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133866334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef043a7d033c06edb878336aba69dc08a2340456f7dc1c2f80a75a362a7f28a8`
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
	-	`sha256:01ede50c7df8b73c8a3ac91fb3bb36978c76e031bb46b82aa12fa72fada06402`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 6.7 MB (6733496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d285c3782350dd5f9e9ba3ffdca6909b3a357f12e4e0aa69f6509f071fbcfbe3`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 89.4 KB (89420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23e2f46c920045fd9af6784bbff05014d36f9150a63b66c744172d76be81c4`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dca5dcdd0a1de285b0723f6c07453eb8ad4c4e39c1d4685a5921590a3228e6`  
		Last Modified: Tue, 14 Jan 2025 02:16:02 GMT  
		Size: 58.4 MB (58383043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88a905ff3d6fd8eeb1a0e9a4da76911f3121664e953d721c866942a7926851a`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76253b0cea165b9074f6b67ca91b09076bb938e59f417391480e5db39bdf1a9`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e37c8bd01854ac13fcaa41da9fb226c89c8238bef5a9de4787c9dd0cd07938c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88d598c27af9d5b832d3315a7aabddf36261d15c0e4eb374faf85a8590e65c`

```dockerfile
```

-	Layers:
	-	`sha256:56e2c5d5c223aaa11d450a30736bb729d576e219338fd7ffc0de44d4849a78b0`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:9d7a7eeddee151b3a91d4187569b2bfed0bc15418e0a5f6cb964ad1bc5c00d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124949459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257951f363b47b171f00cddf758ba9666b0e34a357a010eb907440a2634cdeb3`
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
	-	`sha256:846cdf8016994cf55c03364ec088d83836cd9124c4feadfdc1a290c0db052ea1`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 7.0 MB (7041193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105e956e17649a3bfc6e14bb6b91440fae0386c90f0a79b4ef0af00a6633a337`  
		Last Modified: Tue, 14 Jan 2025 02:15:17 GMT  
		Size: 89.1 KB (89081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec413a996e6897217d8210770f776246e893b515e1c89145e412f0d0f0cb2a4`  
		Last Modified: Tue, 14 Jan 2025 02:15:17 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03338e4032fbada969eec48dc2c2fee01ed7adf78828bc6d40c04ab9507583d`  
		Last Modified: Tue, 14 Jan 2025 02:15:20 GMT  
		Size: 54.0 MB (54047058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e723cb52bcf30c84558d4ccac188f71c03b8891058ff95be8152022690f21f4f`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5282e780179a5e7e90adcb73980f2f9f70231fef1447fbd149a1bc5c64706`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8689bdb9c541bab78f9dd1908957878caf8f25c1253d8bce06cdafe62c1144fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c90fd3c8b21ca316ab44ec447e5562c65bf0a586cb80772ee7a88783c272e86`

```dockerfile
```

-	Layers:
	-	`sha256:f42d1ce12c955562a797d5229e156021010cb89d2612a09a3c8038db1e71759b`  
		Last Modified: Tue, 14 Jan 2025 02:15:16 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:5999a9ff7ae4b7bfd9ffbdc09f506554ad45cf038a06735ee5bf8f4319855ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05426371377f59be4857cbf89178a0f3786fe20bc74bc05b8177a8ed9053ff4`
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
	-	`sha256:e3a7347c9e2b4172d426277de5d40fe3125e0c6b4f9c9b1b210c2190c24f71a6`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 6.4 MB (6367075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170816e95ac1cab8fd3486637652d489c9eb3aec9613c3b50d432b9080a822bc`  
		Last Modified: Tue, 14 Jan 2025 02:20:08 GMT  
		Size: 85.2 KB (85226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45751052d07b0cc92dd9bbbb7d3b61c9e7c35c0f7cebfb423551d2bd9b9f5756`  
		Last Modified: Tue, 14 Jan 2025 02:20:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6227cd6b9897a9ed931bc5860ced54ff59f31642da0ab188c39197dc19cad0fe`  
		Last Modified: Tue, 14 Jan 2025 02:20:10 GMT  
		Size: 54.0 MB (54047052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73cbf2e0a446e5961fdd597ab7cf88eeb26bf806635c7d184ab9675ddad4374`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d10838d3f481fcdee3e8625d0e55d29fc7d9679f071020833f3730f57d9d83`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:037c2c83a82e85230be44bdef44cb3b1d52a2e22d058a5de3aceca56e7159130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0386c303557c0cf65db0f5960ebf6b90f8eaa30c74ffe08cb4c55633a6579454`

```dockerfile
```

-	Layers:
	-	`sha256:941354ab8739c4685b3ec8524f7ba8d6f80ed7d2dc31d182e3d796aff9179e45`  
		Last Modified: Tue, 14 Jan 2025 02:20:07 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ebe06ac52e509d7503408f503c85e7184638d3a39f9da87aa8d7435ebabedef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125657212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a08754d01aa0993ff2b714b092fc20d4c49c6f2b4a2e353e59b54bc19c896af`
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
	-	`sha256:bd25f3cb55cedc28ef3ec15976f2b429e5e24e2f2ec8cf36bbaaa7e6c87c994e`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 7.0 MB (6981981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d49b3e3cd0572d2d1fd7020a8df0ff5fe6bc2b0011ddd9eaf8cc24628779ef9`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 97.8 KB (97789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3200f3c13982eac3851a0c9e87c77fbfe96425bc74c4a9a4db3897a614a1a1`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff187bc55eaede3054ec4ae2f34a0780ccd3306daca06b661e97b61a08d7e413`  
		Last Modified: Tue, 14 Jan 2025 02:26:10 GMT  
		Size: 54.0 MB (53952110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee3e8d3d62aa9df8772f783716c898cf08d668f5759aa735966330e4b3540bc`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f568e54dc452c5a82c30e4b27b6d23ae4813b3aec42ddd31a56a9df635a8af58`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:71af01ec9968269e01302b3e5c567694d917a9ff9193f8a336de02c0adfcba6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25642e7f3a9ac8e5eddd583a6b68a8f2802dc2ae11098c5b85bc08b4de76b0fb`

```dockerfile
```

-	Layers:
	-	`sha256:20cf12060b8c0aa852adbbf7cd68171cb42ed9361a70dfc9558418ec756eb3f6`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:219cd9ce4727ea072f68cff017caa11fd7719835fa252f4b1fbc1ce77a4ab203
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9a103862e4648fbcaf52c07bb8ef33db59ee46cbc1eedbc4cbdd10fc4af9788e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156158115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d95700034e28d044add69f30a925b41f26152ee4130b7e8081ca8bda098f95`
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
	-	`sha256:01ede50c7df8b73c8a3ac91fb3bb36978c76e031bb46b82aa12fa72fada06402`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 6.7 MB (6733496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d285c3782350dd5f9e9ba3ffdca6909b3a357f12e4e0aa69f6509f071fbcfbe3`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 89.4 KB (89420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23e2f46c920045fd9af6784bbff05014d36f9150a63b66c744172d76be81c4`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dca5dcdd0a1de285b0723f6c07453eb8ad4c4e39c1d4685a5921590a3228e6`  
		Last Modified: Tue, 14 Jan 2025 02:16:02 GMT  
		Size: 58.4 MB (58383043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88a905ff3d6fd8eeb1a0e9a4da76911f3121664e953d721c866942a7926851a`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76253b0cea165b9074f6b67ca91b09076bb938e59f417391480e5db39bdf1a9`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f935cb48b813bca67e3f4262bc998f10d445daf1ae1c2fe167bea1c7063459`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 986.6 KB (986564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a49473459905f4e8055629a7c6a93f3cef28430740f4a7460d66c31cebe219`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725ab53ec019a57158824c067b8d7c5d4aac14cac54bd82d929c6b3643929400`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a04e34cc60c0c247d0c4340ff8367878b45b1d4eb32445d48706d1c75078bab`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 21.3 MB (21303868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07647e8159772a3be30c90e3f36bcc2cc9575cd8e107a75a5dd202b40e50ec84`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f2bac0bc675c790fd6442f9801b8e048cf22f413d496faaac7d7d98f65e8775f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a58d67e13b913de17a6cef81562735d1cd54b387aeb9bd8393ebedaee21bac8`

```dockerfile
```

-	Layers:
	-	`sha256:9e2e64133b433d854e70c47e94e568307f6e6a9d22ba7f98ac3e92a3860b6b70`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 30.6 KB (30617 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fe693adc6e1b262dd846e29f8f1f3e52d17839c598c6a9669541aee1390252e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149827921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f807d6de5ec469882013150c9395841dbefd2c5462aa50d31078f831014dd37b`
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
	-	`sha256:bd25f3cb55cedc28ef3ec15976f2b429e5e24e2f2ec8cf36bbaaa7e6c87c994e`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 7.0 MB (6981981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d49b3e3cd0572d2d1fd7020a8df0ff5fe6bc2b0011ddd9eaf8cc24628779ef9`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 97.8 KB (97789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3200f3c13982eac3851a0c9e87c77fbfe96425bc74c4a9a4db3897a614a1a1`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff187bc55eaede3054ec4ae2f34a0780ccd3306daca06b661e97b61a08d7e413`  
		Last Modified: Tue, 14 Jan 2025 02:26:10 GMT  
		Size: 54.0 MB (53952110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee3e8d3d62aa9df8772f783716c898cf08d668f5759aa735966330e4b3540bc`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f568e54dc452c5a82c30e4b27b6d23ae4813b3aec42ddd31a56a9df635a8af58`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a5b110e56f5def4ad57fe3b856b02e8cab49cc738b90c12d2d19c32da7d926`  
		Last Modified: Tue, 14 Jan 2025 13:08:45 GMT  
		Size: 1.0 MB (1014216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1b2aa8218cdd3765ecb7535d1cbfa89c18b85f2826ce1a033776a41f717b0a`  
		Last Modified: Tue, 14 Jan 2025 13:08:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef861fa84a514bb8446c6f52f373f06c448d3b145269e425c1478b9beaac650`  
		Last Modified: Tue, 14 Jan 2025 13:08:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420511f545246aa0d29d9ba63a0499d1f16e94dfe4aee78152f490772e5669`  
		Last Modified: Tue, 14 Jan 2025 13:08:46 GMT  
		Size: 23.2 MB (23155143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276b9bb32935b77cea19ba047d02d2195aad318d0625bef649d08ee9f85faca8`  
		Last Modified: Tue, 14 Jan 2025 13:08:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:36f161acc3a7aa93dfc002353a682c22393105e860ddff634da0d448d639be2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf8ff57c5b5817496db05260da18bcaba486563fab91628bf1a1e58482bcb6e`

```dockerfile
```

-	Layers:
	-	`sha256:73c16f25635b347a54bad4a273bb8614886e4af8e24067871dc9f20867d2bd00`  
		Last Modified: Tue, 14 Jan 2025 13:08:45 GMT  
		Size: 30.8 KB (30787 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:3dc453c179e8242a7449e4f8028145e010292915e3230b76aae64d82b49486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:65abbf8e57dc9b9317388e7635b591c02a450877d39a6776468c9329c6f0b244
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2321679678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5d69e1dda4a11c5d64215052395e362481548cde33a8d6a4be0b4b125f4b53`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:30:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:30:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 23:30:49 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 23:30:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 23:30:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:31:00 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 23:31:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 23:31:01 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 23:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:31:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 23:31:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 23:31:11 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 23:31:20 GMT
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
	-	`sha256:7e42393aec052ef4ad419b20811d5f8f1f4cef5ae7d1b6da49d51a64a7bded4a`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273b7e9f3e3d8546b60d078c2152236a9749ecd2ce4b8677348fe2d97b5798be`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 341.3 KB (341285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cbb7d5116a553e19e688cc78072e8b1eb29afb0b5be4644ed522bf083acd3f`  
		Last Modified: Tue, 14 Jan 2025 23:31:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bfc86e47da2a329fa916e619f50b1572e090a406c11b35b6235548d8bc52ee`  
		Last Modified: Tue, 14 Jan 2025 23:31:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3634f4abc247a49927973cdf069a2717f0053ec34fae55d8f7014967864fb`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 19.1 MB (19149523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36028f38b9d36c2624a31329c881064c7c9b02472ec1aecfb6924bd39ef2450`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0cfd1d3174eb2bbbce2d334d4fd0e90cdd7ca8747f146ef6da5a8cf8e937a3`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834b9a7619d4a8f64af8850acc540189ba984e6f829cde434c43eaa00ac13251`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde3f31a6ef2d6c5cb116f4c7246bdcf8ed9a39ac3ea376b13832a9a90df8d63`  
		Last Modified: Tue, 14 Jan 2025 23:31:27 GMT  
		Size: 19.6 MB (19634023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7331fb5fa54eb509667e318fef4224b22e7267a8b01ab08320597309a61cc9`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41addc9937b80bc18e288c60f1f057cce9b501761a6c845a8a385dca9084663e`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752c051f71c979cefbe564869be494631945a5cd1aad02a5904c2715b12c51b0`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dff165c12cf41f3471c535f13b2fefdaf7f686d0bc74b8372caf2d7dbb7a08f`  
		Last Modified: Tue, 14 Jan 2025 23:31:27 GMT  
		Size: 20.2 MB (20158014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:e623df1460d3ebcb3ad8073621cc95b69f52df75ca8d0ab278177ef2085183d4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181418375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edf4c3deefe7cfd0ff52fd0d9d60c10b8e24d2facaaff9e581b0bed9b8c7cdc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:37:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:38:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 23:38:50 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 23:38:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 23:39:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:04 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 23:39:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 23:39:05 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 23:39:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 23:39:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 23:39:15 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 23:39:22 GMT
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
	-	`sha256:ace576e2b330b24c982543035820a2ecbea8fa58428209b788c8dbc34fe43f5e`  
		Last Modified: Tue, 14 Jan 2025 23:39:28 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d288a76c5d5ee64affc87ec0d46e06ebb6326b17068f33a5792bf7f16641fe84`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 316.6 KB (316613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d7033573b703663b78be30fbeb8df368a1408341870dee01f3801334d22fdf`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200e4ef96719afb123d542fba348a35d1e6b8c7ea5da1d183af90ff0537d8adf`  
		Last Modified: Tue, 14 Jan 2025 23:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0f7834de3577810e21557605584283e758ff40eae06e414866571f6c2e16df`  
		Last Modified: Tue, 14 Jan 2025 23:39:29 GMT  
		Size: 19.1 MB (19132926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cc1331cde43f073663e2b9396edd7ccac0f5309292d4f046cbe985d4402471`  
		Last Modified: Tue, 14 Jan 2025 23:39:26 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff86dabfa389add56b99fda4a391700fa18ff5756120341345a47f98a2802312`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8192f34e31a6709287fc3944570a104c942154cde3b91498b2afc544cf1bde`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3253d8429e17a419d9f3970970cec0e25ea529d22e9b1f46d68195ccd2ddf9`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 19.6 MB (19607700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb691e1b2ced8da219bfba3fd2da38afd59e2d41d524d5f93ff610894aab74c`  
		Last Modified: Tue, 14 Jan 2025 23:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37177f635ff92a20fc9c2edee74a5d7fef05bac391f1261da856a52900a7d2f`  
		Last Modified: Tue, 14 Jan 2025 23:39:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e7ed4e2f131f942a5e8a2b6add2e3585ef60fff72094fffe47b43c98ff50f5`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c0912a92c0e5091e90b6472cd2d2c89be81d415d84cc5426d62c54b147fdd1`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 20.1 MB (20137257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:fd008b6841d28c3f235332ce741282e625c4b9909c55ac89eba81a4efe37e611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:e623df1460d3ebcb3ad8073621cc95b69f52df75ca8d0ab278177ef2085183d4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181418375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edf4c3deefe7cfd0ff52fd0d9d60c10b8e24d2facaaff9e581b0bed9b8c7cdc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:37:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:38:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 23:38:50 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 23:38:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 23:39:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:04 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 23:39:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 23:39:05 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 23:39:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 23:39:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 23:39:15 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 23:39:22 GMT
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
	-	`sha256:ace576e2b330b24c982543035820a2ecbea8fa58428209b788c8dbc34fe43f5e`  
		Last Modified: Tue, 14 Jan 2025 23:39:28 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d288a76c5d5ee64affc87ec0d46e06ebb6326b17068f33a5792bf7f16641fe84`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 316.6 KB (316613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d7033573b703663b78be30fbeb8df368a1408341870dee01f3801334d22fdf`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200e4ef96719afb123d542fba348a35d1e6b8c7ea5da1d183af90ff0537d8adf`  
		Last Modified: Tue, 14 Jan 2025 23:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0f7834de3577810e21557605584283e758ff40eae06e414866571f6c2e16df`  
		Last Modified: Tue, 14 Jan 2025 23:39:29 GMT  
		Size: 19.1 MB (19132926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cc1331cde43f073663e2b9396edd7ccac0f5309292d4f046cbe985d4402471`  
		Last Modified: Tue, 14 Jan 2025 23:39:26 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff86dabfa389add56b99fda4a391700fa18ff5756120341345a47f98a2802312`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8192f34e31a6709287fc3944570a104c942154cde3b91498b2afc544cf1bde`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3253d8429e17a419d9f3970970cec0e25ea529d22e9b1f46d68195ccd2ddf9`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 19.6 MB (19607700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb691e1b2ced8da219bfba3fd2da38afd59e2d41d524d5f93ff610894aab74c`  
		Last Modified: Tue, 14 Jan 2025 23:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37177f635ff92a20fc9c2edee74a5d7fef05bac391f1261da856a52900a7d2f`  
		Last Modified: Tue, 14 Jan 2025 23:39:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e7ed4e2f131f942a5e8a2b6add2e3585ef60fff72094fffe47b43c98ff50f5`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c0912a92c0e5091e90b6472cd2d2c89be81d415d84cc5426d62c54b147fdd1`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 20.1 MB (20137257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:74d0de74839599456a874f19aee0058bfba7a13d7a8049272594f2e69a1ff72b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:65abbf8e57dc9b9317388e7635b591c02a450877d39a6776468c9329c6f0b244
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2321679678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5d69e1dda4a11c5d64215052395e362481548cde33a8d6a4be0b4b125f4b53`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:30:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:30:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 23:30:49 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 23:30:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 23:30:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:31:00 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 23:31:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 23:31:01 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 23:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:31:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 23:31:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 23:31:11 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 23:31:20 GMT
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
	-	`sha256:7e42393aec052ef4ad419b20811d5f8f1f4cef5ae7d1b6da49d51a64a7bded4a`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273b7e9f3e3d8546b60d078c2152236a9749ecd2ce4b8677348fe2d97b5798be`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 341.3 KB (341285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cbb7d5116a553e19e688cc78072e8b1eb29afb0b5be4644ed522bf083acd3f`  
		Last Modified: Tue, 14 Jan 2025 23:31:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bfc86e47da2a329fa916e619f50b1572e090a406c11b35b6235548d8bc52ee`  
		Last Modified: Tue, 14 Jan 2025 23:31:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3634f4abc247a49927973cdf069a2717f0053ec34fae55d8f7014967864fb`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 19.1 MB (19149523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36028f38b9d36c2624a31329c881064c7c9b02472ec1aecfb6924bd39ef2450`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0cfd1d3174eb2bbbce2d334d4fd0e90cdd7ca8747f146ef6da5a8cf8e937a3`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834b9a7619d4a8f64af8850acc540189ba984e6f829cde434c43eaa00ac13251`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde3f31a6ef2d6c5cb116f4c7246bdcf8ed9a39ac3ea376b13832a9a90df8d63`  
		Last Modified: Tue, 14 Jan 2025 23:31:27 GMT  
		Size: 19.6 MB (19634023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7331fb5fa54eb509667e318fef4224b22e7267a8b01ab08320597309a61cc9`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41addc9937b80bc18e288c60f1f057cce9b501761a6c845a8a385dca9084663e`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752c051f71c979cefbe564869be494631945a5cd1aad02a5904c2715b12c51b0`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dff165c12cf41f3471c535f13b2fefdaf7f686d0bc74b8372caf2d7dbb7a08f`  
		Last Modified: Tue, 14 Jan 2025 23:31:27 GMT  
		Size: 20.2 MB (20158014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5`

```console
$ docker pull docker@sha256:cbde039f51b3d85366f59fe2e97cdaf329a6eef076b79a9afb9f9568d04d0767
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
$ docker pull docker@sha256:36b7c405e8884e399ac3c7c63f3f61b065a94b62e0b915e62db4d0de3a0aa0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133866334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef043a7d033c06edb878336aba69dc08a2340456f7dc1c2f80a75a362a7f28a8`
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
	-	`sha256:01ede50c7df8b73c8a3ac91fb3bb36978c76e031bb46b82aa12fa72fada06402`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 6.7 MB (6733496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d285c3782350dd5f9e9ba3ffdca6909b3a357f12e4e0aa69f6509f071fbcfbe3`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 89.4 KB (89420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23e2f46c920045fd9af6784bbff05014d36f9150a63b66c744172d76be81c4`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dca5dcdd0a1de285b0723f6c07453eb8ad4c4e39c1d4685a5921590a3228e6`  
		Last Modified: Tue, 14 Jan 2025 02:16:02 GMT  
		Size: 58.4 MB (58383043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88a905ff3d6fd8eeb1a0e9a4da76911f3121664e953d721c866942a7926851a`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76253b0cea165b9074f6b67ca91b09076bb938e59f417391480e5db39bdf1a9`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5` - unknown; unknown

```console
$ docker pull docker@sha256:e37c8bd01854ac13fcaa41da9fb226c89c8238bef5a9de4787c9dd0cd07938c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88d598c27af9d5b832d3315a7aabddf36261d15c0e4eb374faf85a8590e65c`

```dockerfile
```

-	Layers:
	-	`sha256:56e2c5d5c223aaa11d450a30736bb729d576e219338fd7ffc0de44d4849a78b0`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5` - linux; arm variant v6

```console
$ docker pull docker@sha256:9d7a7eeddee151b3a91d4187569b2bfed0bc15418e0a5f6cb964ad1bc5c00d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124949459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257951f363b47b171f00cddf758ba9666b0e34a357a010eb907440a2634cdeb3`
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
	-	`sha256:846cdf8016994cf55c03364ec088d83836cd9124c4feadfdc1a290c0db052ea1`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 7.0 MB (7041193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105e956e17649a3bfc6e14bb6b91440fae0386c90f0a79b4ef0af00a6633a337`  
		Last Modified: Tue, 14 Jan 2025 02:15:17 GMT  
		Size: 89.1 KB (89081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec413a996e6897217d8210770f776246e893b515e1c89145e412f0d0f0cb2a4`  
		Last Modified: Tue, 14 Jan 2025 02:15:17 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03338e4032fbada969eec48dc2c2fee01ed7adf78828bc6d40c04ab9507583d`  
		Last Modified: Tue, 14 Jan 2025 02:15:20 GMT  
		Size: 54.0 MB (54047058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e723cb52bcf30c84558d4ccac188f71c03b8891058ff95be8152022690f21f4f`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5282e780179a5e7e90adcb73980f2f9f70231fef1447fbd149a1bc5c64706`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5` - unknown; unknown

```console
$ docker pull docker@sha256:8689bdb9c541bab78f9dd1908957878caf8f25c1253d8bce06cdafe62c1144fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c90fd3c8b21ca316ab44ec447e5562c65bf0a586cb80772ee7a88783c272e86`

```dockerfile
```

-	Layers:
	-	`sha256:f42d1ce12c955562a797d5229e156021010cb89d2612a09a3c8038db1e71759b`  
		Last Modified: Tue, 14 Jan 2025 02:15:16 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5` - linux; arm variant v7

```console
$ docker pull docker@sha256:5999a9ff7ae4b7bfd9ffbdc09f506554ad45cf038a06735ee5bf8f4319855ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05426371377f59be4857cbf89178a0f3786fe20bc74bc05b8177a8ed9053ff4`
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
	-	`sha256:e3a7347c9e2b4172d426277de5d40fe3125e0c6b4f9c9b1b210c2190c24f71a6`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 6.4 MB (6367075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170816e95ac1cab8fd3486637652d489c9eb3aec9613c3b50d432b9080a822bc`  
		Last Modified: Tue, 14 Jan 2025 02:20:08 GMT  
		Size: 85.2 KB (85226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45751052d07b0cc92dd9bbbb7d3b61c9e7c35c0f7cebfb423551d2bd9b9f5756`  
		Last Modified: Tue, 14 Jan 2025 02:20:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6227cd6b9897a9ed931bc5860ced54ff59f31642da0ab188c39197dc19cad0fe`  
		Last Modified: Tue, 14 Jan 2025 02:20:10 GMT  
		Size: 54.0 MB (54047052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73cbf2e0a446e5961fdd597ab7cf88eeb26bf806635c7d184ab9675ddad4374`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d10838d3f481fcdee3e8625d0e55d29fc7d9679f071020833f3730f57d9d83`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5` - unknown; unknown

```console
$ docker pull docker@sha256:037c2c83a82e85230be44bdef44cb3b1d52a2e22d058a5de3aceca56e7159130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0386c303557c0cf65db0f5960ebf6b90f8eaa30c74ffe08cb4c55633a6579454`

```dockerfile
```

-	Layers:
	-	`sha256:941354ab8739c4685b3ec8524f7ba8d6f80ed7d2dc31d182e3d796aff9179e45`  
		Last Modified: Tue, 14 Jan 2025 02:20:07 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ebe06ac52e509d7503408f503c85e7184638d3a39f9da87aa8d7435ebabedef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125657212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a08754d01aa0993ff2b714b092fc20d4c49c6f2b4a2e353e59b54bc19c896af`
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
	-	`sha256:bd25f3cb55cedc28ef3ec15976f2b429e5e24e2f2ec8cf36bbaaa7e6c87c994e`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 7.0 MB (6981981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d49b3e3cd0572d2d1fd7020a8df0ff5fe6bc2b0011ddd9eaf8cc24628779ef9`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 97.8 KB (97789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3200f3c13982eac3851a0c9e87c77fbfe96425bc74c4a9a4db3897a614a1a1`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff187bc55eaede3054ec4ae2f34a0780ccd3306daca06b661e97b61a08d7e413`  
		Last Modified: Tue, 14 Jan 2025 02:26:10 GMT  
		Size: 54.0 MB (53952110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee3e8d3d62aa9df8772f783716c898cf08d668f5759aa735966330e4b3540bc`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f568e54dc452c5a82c30e4b27b6d23ae4813b3aec42ddd31a56a9df635a8af58`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5` - unknown; unknown

```console
$ docker pull docker@sha256:71af01ec9968269e01302b3e5c567694d917a9ff9193f8a336de02c0adfcba6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25642e7f3a9ac8e5eddd583a6b68a8f2802dc2ae11098c5b85bc08b4de76b0fb`

```dockerfile
```

-	Layers:
	-	`sha256:20cf12060b8c0aa852adbbf7cd68171cb42ed9361a70dfc9558418ec756eb3f6`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5-cli`

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

### `docker:27.5-cli` - linux; arm variant v7

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

### `docker:27.5-cli` - unknown; unknown

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
$ docker pull docker@sha256:cbde039f51b3d85366f59fe2e97cdaf329a6eef076b79a9afb9f9568d04d0767
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
$ docker pull docker@sha256:36b7c405e8884e399ac3c7c63f3f61b065a94b62e0b915e62db4d0de3a0aa0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133866334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef043a7d033c06edb878336aba69dc08a2340456f7dc1c2f80a75a362a7f28a8`
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
	-	`sha256:01ede50c7df8b73c8a3ac91fb3bb36978c76e031bb46b82aa12fa72fada06402`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 6.7 MB (6733496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d285c3782350dd5f9e9ba3ffdca6909b3a357f12e4e0aa69f6509f071fbcfbe3`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 89.4 KB (89420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23e2f46c920045fd9af6784bbff05014d36f9150a63b66c744172d76be81c4`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dca5dcdd0a1de285b0723f6c07453eb8ad4c4e39c1d4685a5921590a3228e6`  
		Last Modified: Tue, 14 Jan 2025 02:16:02 GMT  
		Size: 58.4 MB (58383043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88a905ff3d6fd8eeb1a0e9a4da76911f3121664e953d721c866942a7926851a`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76253b0cea165b9074f6b67ca91b09076bb938e59f417391480e5db39bdf1a9`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e37c8bd01854ac13fcaa41da9fb226c89c8238bef5a9de4787c9dd0cd07938c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88d598c27af9d5b832d3315a7aabddf36261d15c0e4eb374faf85a8590e65c`

```dockerfile
```

-	Layers:
	-	`sha256:56e2c5d5c223aaa11d450a30736bb729d576e219338fd7ffc0de44d4849a78b0`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:9d7a7eeddee151b3a91d4187569b2bfed0bc15418e0a5f6cb964ad1bc5c00d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124949459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257951f363b47b171f00cddf758ba9666b0e34a357a010eb907440a2634cdeb3`
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
	-	`sha256:846cdf8016994cf55c03364ec088d83836cd9124c4feadfdc1a290c0db052ea1`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 7.0 MB (7041193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105e956e17649a3bfc6e14bb6b91440fae0386c90f0a79b4ef0af00a6633a337`  
		Last Modified: Tue, 14 Jan 2025 02:15:17 GMT  
		Size: 89.1 KB (89081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec413a996e6897217d8210770f776246e893b515e1c89145e412f0d0f0cb2a4`  
		Last Modified: Tue, 14 Jan 2025 02:15:17 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03338e4032fbada969eec48dc2c2fee01ed7adf78828bc6d40c04ab9507583d`  
		Last Modified: Tue, 14 Jan 2025 02:15:20 GMT  
		Size: 54.0 MB (54047058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e723cb52bcf30c84558d4ccac188f71c03b8891058ff95be8152022690f21f4f`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5282e780179a5e7e90adcb73980f2f9f70231fef1447fbd149a1bc5c64706`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8689bdb9c541bab78f9dd1908957878caf8f25c1253d8bce06cdafe62c1144fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c90fd3c8b21ca316ab44ec447e5562c65bf0a586cb80772ee7a88783c272e86`

```dockerfile
```

-	Layers:
	-	`sha256:f42d1ce12c955562a797d5229e156021010cb89d2612a09a3c8038db1e71759b`  
		Last Modified: Tue, 14 Jan 2025 02:15:16 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:5999a9ff7ae4b7bfd9ffbdc09f506554ad45cf038a06735ee5bf8f4319855ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05426371377f59be4857cbf89178a0f3786fe20bc74bc05b8177a8ed9053ff4`
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
	-	`sha256:e3a7347c9e2b4172d426277de5d40fe3125e0c6b4f9c9b1b210c2190c24f71a6`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 6.4 MB (6367075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170816e95ac1cab8fd3486637652d489c9eb3aec9613c3b50d432b9080a822bc`  
		Last Modified: Tue, 14 Jan 2025 02:20:08 GMT  
		Size: 85.2 KB (85226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45751052d07b0cc92dd9bbbb7d3b61c9e7c35c0f7cebfb423551d2bd9b9f5756`  
		Last Modified: Tue, 14 Jan 2025 02:20:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6227cd6b9897a9ed931bc5860ced54ff59f31642da0ab188c39197dc19cad0fe`  
		Last Modified: Tue, 14 Jan 2025 02:20:10 GMT  
		Size: 54.0 MB (54047052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73cbf2e0a446e5961fdd597ab7cf88eeb26bf806635c7d184ab9675ddad4374`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d10838d3f481fcdee3e8625d0e55d29fc7d9679f071020833f3730f57d9d83`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:037c2c83a82e85230be44bdef44cb3b1d52a2e22d058a5de3aceca56e7159130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0386c303557c0cf65db0f5960ebf6b90f8eaa30c74ffe08cb4c55633a6579454`

```dockerfile
```

-	Layers:
	-	`sha256:941354ab8739c4685b3ec8524f7ba8d6f80ed7d2dc31d182e3d796aff9179e45`  
		Last Modified: Tue, 14 Jan 2025 02:20:07 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ebe06ac52e509d7503408f503c85e7184638d3a39f9da87aa8d7435ebabedef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125657212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a08754d01aa0993ff2b714b092fc20d4c49c6f2b4a2e353e59b54bc19c896af`
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
	-	`sha256:bd25f3cb55cedc28ef3ec15976f2b429e5e24e2f2ec8cf36bbaaa7e6c87c994e`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 7.0 MB (6981981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d49b3e3cd0572d2d1fd7020a8df0ff5fe6bc2b0011ddd9eaf8cc24628779ef9`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 97.8 KB (97789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3200f3c13982eac3851a0c9e87c77fbfe96425bc74c4a9a4db3897a614a1a1`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff187bc55eaede3054ec4ae2f34a0780ccd3306daca06b661e97b61a08d7e413`  
		Last Modified: Tue, 14 Jan 2025 02:26:10 GMT  
		Size: 54.0 MB (53952110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee3e8d3d62aa9df8772f783716c898cf08d668f5759aa735966330e4b3540bc`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f568e54dc452c5a82c30e4b27b6d23ae4813b3aec42ddd31a56a9df635a8af58`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:71af01ec9968269e01302b3e5c567694d917a9ff9193f8a336de02c0adfcba6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25642e7f3a9ac8e5eddd583a6b68a8f2802dc2ae11098c5b85bc08b4de76b0fb`

```dockerfile
```

-	Layers:
	-	`sha256:20cf12060b8c0aa852adbbf7cd68171cb42ed9361a70dfc9558418ec756eb3f6`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5-dind-rootless`

```console
$ docker pull docker@sha256:219cd9ce4727ea072f68cff017caa11fd7719835fa252f4b1fbc1ce77a4ab203
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.5-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9a103862e4648fbcaf52c07bb8ef33db59ee46cbc1eedbc4cbdd10fc4af9788e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156158115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d95700034e28d044add69f30a925b41f26152ee4130b7e8081ca8bda098f95`
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
	-	`sha256:01ede50c7df8b73c8a3ac91fb3bb36978c76e031bb46b82aa12fa72fada06402`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 6.7 MB (6733496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d285c3782350dd5f9e9ba3ffdca6909b3a357f12e4e0aa69f6509f071fbcfbe3`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 89.4 KB (89420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23e2f46c920045fd9af6784bbff05014d36f9150a63b66c744172d76be81c4`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dca5dcdd0a1de285b0723f6c07453eb8ad4c4e39c1d4685a5921590a3228e6`  
		Last Modified: Tue, 14 Jan 2025 02:16:02 GMT  
		Size: 58.4 MB (58383043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88a905ff3d6fd8eeb1a0e9a4da76911f3121664e953d721c866942a7926851a`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76253b0cea165b9074f6b67ca91b09076bb938e59f417391480e5db39bdf1a9`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f935cb48b813bca67e3f4262bc998f10d445daf1ae1c2fe167bea1c7063459`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 986.6 KB (986564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a49473459905f4e8055629a7c6a93f3cef28430740f4a7460d66c31cebe219`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725ab53ec019a57158824c067b8d7c5d4aac14cac54bd82d929c6b3643929400`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a04e34cc60c0c247d0c4340ff8367878b45b1d4eb32445d48706d1c75078bab`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 21.3 MB (21303868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07647e8159772a3be30c90e3f36bcc2cc9575cd8e107a75a5dd202b40e50ec84`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f2bac0bc675c790fd6442f9801b8e048cf22f413d496faaac7d7d98f65e8775f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a58d67e13b913de17a6cef81562735d1cd54b387aeb9bd8393ebedaee21bac8`

```dockerfile
```

-	Layers:
	-	`sha256:9e2e64133b433d854e70c47e94e568307f6e6a9d22ba7f98ac3e92a3860b6b70`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 30.6 KB (30617 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fe693adc6e1b262dd846e29f8f1f3e52d17839c598c6a9669541aee1390252e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149827921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f807d6de5ec469882013150c9395841dbefd2c5462aa50d31078f831014dd37b`
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
	-	`sha256:bd25f3cb55cedc28ef3ec15976f2b429e5e24e2f2ec8cf36bbaaa7e6c87c994e`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 7.0 MB (6981981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d49b3e3cd0572d2d1fd7020a8df0ff5fe6bc2b0011ddd9eaf8cc24628779ef9`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 97.8 KB (97789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3200f3c13982eac3851a0c9e87c77fbfe96425bc74c4a9a4db3897a614a1a1`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff187bc55eaede3054ec4ae2f34a0780ccd3306daca06b661e97b61a08d7e413`  
		Last Modified: Tue, 14 Jan 2025 02:26:10 GMT  
		Size: 54.0 MB (53952110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee3e8d3d62aa9df8772f783716c898cf08d668f5759aa735966330e4b3540bc`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f568e54dc452c5a82c30e4b27b6d23ae4813b3aec42ddd31a56a9df635a8af58`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a5b110e56f5def4ad57fe3b856b02e8cab49cc738b90c12d2d19c32da7d926`  
		Last Modified: Tue, 14 Jan 2025 13:08:45 GMT  
		Size: 1.0 MB (1014216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1b2aa8218cdd3765ecb7535d1cbfa89c18b85f2826ce1a033776a41f717b0a`  
		Last Modified: Tue, 14 Jan 2025 13:08:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef861fa84a514bb8446c6f52f373f06c448d3b145269e425c1478b9beaac650`  
		Last Modified: Tue, 14 Jan 2025 13:08:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420511f545246aa0d29d9ba63a0499d1f16e94dfe4aee78152f490772e5669`  
		Last Modified: Tue, 14 Jan 2025 13:08:46 GMT  
		Size: 23.2 MB (23155143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276b9bb32935b77cea19ba047d02d2195aad318d0625bef649d08ee9f85faca8`  
		Last Modified: Tue, 14 Jan 2025 13:08:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:36f161acc3a7aa93dfc002353a682c22393105e860ddff634da0d448d639be2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf8ff57c5b5817496db05260da18bcaba486563fab91628bf1a1e58482bcb6e`

```dockerfile
```

-	Layers:
	-	`sha256:73c16f25635b347a54bad4a273bb8614886e4af8e24067871dc9f20867d2bd00`  
		Last Modified: Tue, 14 Jan 2025 13:08:45 GMT  
		Size: 30.8 KB (30787 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5-windowsservercore`

```console
$ docker pull docker@sha256:3dc453c179e8242a7449e4f8028145e010292915e3230b76aae64d82b49486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `docker:27.5-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:65abbf8e57dc9b9317388e7635b591c02a450877d39a6776468c9329c6f0b244
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2321679678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5d69e1dda4a11c5d64215052395e362481548cde33a8d6a4be0b4b125f4b53`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:30:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:30:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 23:30:49 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 23:30:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 23:30:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:31:00 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 23:31:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 23:31:01 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 23:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:31:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 23:31:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 23:31:11 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 23:31:20 GMT
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
	-	`sha256:7e42393aec052ef4ad419b20811d5f8f1f4cef5ae7d1b6da49d51a64a7bded4a`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273b7e9f3e3d8546b60d078c2152236a9749ecd2ce4b8677348fe2d97b5798be`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 341.3 KB (341285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cbb7d5116a553e19e688cc78072e8b1eb29afb0b5be4644ed522bf083acd3f`  
		Last Modified: Tue, 14 Jan 2025 23:31:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bfc86e47da2a329fa916e619f50b1572e090a406c11b35b6235548d8bc52ee`  
		Last Modified: Tue, 14 Jan 2025 23:31:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3634f4abc247a49927973cdf069a2717f0053ec34fae55d8f7014967864fb`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 19.1 MB (19149523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36028f38b9d36c2624a31329c881064c7c9b02472ec1aecfb6924bd39ef2450`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0cfd1d3174eb2bbbce2d334d4fd0e90cdd7ca8747f146ef6da5a8cf8e937a3`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834b9a7619d4a8f64af8850acc540189ba984e6f829cde434c43eaa00ac13251`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde3f31a6ef2d6c5cb116f4c7246bdcf8ed9a39ac3ea376b13832a9a90df8d63`  
		Last Modified: Tue, 14 Jan 2025 23:31:27 GMT  
		Size: 19.6 MB (19634023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7331fb5fa54eb509667e318fef4224b22e7267a8b01ab08320597309a61cc9`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41addc9937b80bc18e288c60f1f057cce9b501761a6c845a8a385dca9084663e`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752c051f71c979cefbe564869be494631945a5cd1aad02a5904c2715b12c51b0`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dff165c12cf41f3471c535f13b2fefdaf7f686d0bc74b8372caf2d7dbb7a08f`  
		Last Modified: Tue, 14 Jan 2025 23:31:27 GMT  
		Size: 20.2 MB (20158014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.5-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:e623df1460d3ebcb3ad8073621cc95b69f52df75ca8d0ab278177ef2085183d4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181418375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edf4c3deefe7cfd0ff52fd0d9d60c10b8e24d2facaaff9e581b0bed9b8c7cdc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:37:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:38:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 23:38:50 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 23:38:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 23:39:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:04 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 23:39:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 23:39:05 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 23:39:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 23:39:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 23:39:15 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 23:39:22 GMT
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
	-	`sha256:ace576e2b330b24c982543035820a2ecbea8fa58428209b788c8dbc34fe43f5e`  
		Last Modified: Tue, 14 Jan 2025 23:39:28 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d288a76c5d5ee64affc87ec0d46e06ebb6326b17068f33a5792bf7f16641fe84`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 316.6 KB (316613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d7033573b703663b78be30fbeb8df368a1408341870dee01f3801334d22fdf`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200e4ef96719afb123d542fba348a35d1e6b8c7ea5da1d183af90ff0537d8adf`  
		Last Modified: Tue, 14 Jan 2025 23:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0f7834de3577810e21557605584283e758ff40eae06e414866571f6c2e16df`  
		Last Modified: Tue, 14 Jan 2025 23:39:29 GMT  
		Size: 19.1 MB (19132926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cc1331cde43f073663e2b9396edd7ccac0f5309292d4f046cbe985d4402471`  
		Last Modified: Tue, 14 Jan 2025 23:39:26 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff86dabfa389add56b99fda4a391700fa18ff5756120341345a47f98a2802312`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8192f34e31a6709287fc3944570a104c942154cde3b91498b2afc544cf1bde`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3253d8429e17a419d9f3970970cec0e25ea529d22e9b1f46d68195ccd2ddf9`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 19.6 MB (19607700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb691e1b2ced8da219bfba3fd2da38afd59e2d41d524d5f93ff610894aab74c`  
		Last Modified: Tue, 14 Jan 2025 23:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37177f635ff92a20fc9c2edee74a5d7fef05bac391f1261da856a52900a7d2f`  
		Last Modified: Tue, 14 Jan 2025 23:39:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e7ed4e2f131f942a5e8a2b6add2e3585ef60fff72094fffe47b43c98ff50f5`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c0912a92c0e5091e90b6472cd2d2c89be81d415d84cc5426d62c54b147fdd1`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 20.1 MB (20137257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5-windowsservercore-1809`

```console
$ docker pull docker@sha256:fd008b6841d28c3f235332ce741282e625c4b9909c55ac89eba81a4efe37e611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `docker:27.5-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:e623df1460d3ebcb3ad8073621cc95b69f52df75ca8d0ab278177ef2085183d4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181418375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edf4c3deefe7cfd0ff52fd0d9d60c10b8e24d2facaaff9e581b0bed9b8c7cdc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:37:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:38:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 23:38:50 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 23:38:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 23:39:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:04 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 23:39:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 23:39:05 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 23:39:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 23:39:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 23:39:15 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 23:39:22 GMT
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
	-	`sha256:ace576e2b330b24c982543035820a2ecbea8fa58428209b788c8dbc34fe43f5e`  
		Last Modified: Tue, 14 Jan 2025 23:39:28 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d288a76c5d5ee64affc87ec0d46e06ebb6326b17068f33a5792bf7f16641fe84`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 316.6 KB (316613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d7033573b703663b78be30fbeb8df368a1408341870dee01f3801334d22fdf`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200e4ef96719afb123d542fba348a35d1e6b8c7ea5da1d183af90ff0537d8adf`  
		Last Modified: Tue, 14 Jan 2025 23:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0f7834de3577810e21557605584283e758ff40eae06e414866571f6c2e16df`  
		Last Modified: Tue, 14 Jan 2025 23:39:29 GMT  
		Size: 19.1 MB (19132926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cc1331cde43f073663e2b9396edd7ccac0f5309292d4f046cbe985d4402471`  
		Last Modified: Tue, 14 Jan 2025 23:39:26 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff86dabfa389add56b99fda4a391700fa18ff5756120341345a47f98a2802312`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8192f34e31a6709287fc3944570a104c942154cde3b91498b2afc544cf1bde`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3253d8429e17a419d9f3970970cec0e25ea529d22e9b1f46d68195ccd2ddf9`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 19.6 MB (19607700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb691e1b2ced8da219bfba3fd2da38afd59e2d41d524d5f93ff610894aab74c`  
		Last Modified: Tue, 14 Jan 2025 23:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37177f635ff92a20fc9c2edee74a5d7fef05bac391f1261da856a52900a7d2f`  
		Last Modified: Tue, 14 Jan 2025 23:39:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e7ed4e2f131f942a5e8a2b6add2e3585ef60fff72094fffe47b43c98ff50f5`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c0912a92c0e5091e90b6472cd2d2c89be81d415d84cc5426d62c54b147fdd1`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 20.1 MB (20137257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:74d0de74839599456a874f19aee0058bfba7a13d7a8049272594f2e69a1ff72b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `docker:27.5-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:65abbf8e57dc9b9317388e7635b591c02a450877d39a6776468c9329c6f0b244
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2321679678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5d69e1dda4a11c5d64215052395e362481548cde33a8d6a4be0b4b125f4b53`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:30:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:30:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 23:30:49 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 23:30:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 23:30:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:31:00 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 23:31:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 23:31:01 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 23:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:31:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 23:31:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 23:31:11 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 23:31:20 GMT
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
	-	`sha256:7e42393aec052ef4ad419b20811d5f8f1f4cef5ae7d1b6da49d51a64a7bded4a`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273b7e9f3e3d8546b60d078c2152236a9749ecd2ce4b8677348fe2d97b5798be`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 341.3 KB (341285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cbb7d5116a553e19e688cc78072e8b1eb29afb0b5be4644ed522bf083acd3f`  
		Last Modified: Tue, 14 Jan 2025 23:31:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bfc86e47da2a329fa916e619f50b1572e090a406c11b35b6235548d8bc52ee`  
		Last Modified: Tue, 14 Jan 2025 23:31:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3634f4abc247a49927973cdf069a2717f0053ec34fae55d8f7014967864fb`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 19.1 MB (19149523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36028f38b9d36c2624a31329c881064c7c9b02472ec1aecfb6924bd39ef2450`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0cfd1d3174eb2bbbce2d334d4fd0e90cdd7ca8747f146ef6da5a8cf8e937a3`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834b9a7619d4a8f64af8850acc540189ba984e6f829cde434c43eaa00ac13251`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde3f31a6ef2d6c5cb116f4c7246bdcf8ed9a39ac3ea376b13832a9a90df8d63`  
		Last Modified: Tue, 14 Jan 2025 23:31:27 GMT  
		Size: 19.6 MB (19634023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7331fb5fa54eb509667e318fef4224b22e7267a8b01ab08320597309a61cc9`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41addc9937b80bc18e288c60f1f057cce9b501761a6c845a8a385dca9084663e`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752c051f71c979cefbe564869be494631945a5cd1aad02a5904c2715b12c51b0`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dff165c12cf41f3471c535f13b2fefdaf7f686d0bc74b8372caf2d7dbb7a08f`  
		Last Modified: Tue, 14 Jan 2025 23:31:27 GMT  
		Size: 20.2 MB (20158014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5.0`

```console
$ docker pull docker@sha256:cbde039f51b3d85366f59fe2e97cdaf329a6eef076b79a9afb9f9568d04d0767
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
$ docker pull docker@sha256:36b7c405e8884e399ac3c7c63f3f61b065a94b62e0b915e62db4d0de3a0aa0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133866334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef043a7d033c06edb878336aba69dc08a2340456f7dc1c2f80a75a362a7f28a8`
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
	-	`sha256:01ede50c7df8b73c8a3ac91fb3bb36978c76e031bb46b82aa12fa72fada06402`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 6.7 MB (6733496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d285c3782350dd5f9e9ba3ffdca6909b3a357f12e4e0aa69f6509f071fbcfbe3`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 89.4 KB (89420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23e2f46c920045fd9af6784bbff05014d36f9150a63b66c744172d76be81c4`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dca5dcdd0a1de285b0723f6c07453eb8ad4c4e39c1d4685a5921590a3228e6`  
		Last Modified: Tue, 14 Jan 2025 02:16:02 GMT  
		Size: 58.4 MB (58383043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88a905ff3d6fd8eeb1a0e9a4da76911f3121664e953d721c866942a7926851a`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76253b0cea165b9074f6b67ca91b09076bb938e59f417391480e5db39bdf1a9`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0` - unknown; unknown

```console
$ docker pull docker@sha256:e37c8bd01854ac13fcaa41da9fb226c89c8238bef5a9de4787c9dd0cd07938c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88d598c27af9d5b832d3315a7aabddf36261d15c0e4eb374faf85a8590e65c`

```dockerfile
```

-	Layers:
	-	`sha256:56e2c5d5c223aaa11d450a30736bb729d576e219338fd7ffc0de44d4849a78b0`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0` - linux; arm variant v6

```console
$ docker pull docker@sha256:9d7a7eeddee151b3a91d4187569b2bfed0bc15418e0a5f6cb964ad1bc5c00d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124949459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257951f363b47b171f00cddf758ba9666b0e34a357a010eb907440a2634cdeb3`
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
	-	`sha256:846cdf8016994cf55c03364ec088d83836cd9124c4feadfdc1a290c0db052ea1`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 7.0 MB (7041193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105e956e17649a3bfc6e14bb6b91440fae0386c90f0a79b4ef0af00a6633a337`  
		Last Modified: Tue, 14 Jan 2025 02:15:17 GMT  
		Size: 89.1 KB (89081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec413a996e6897217d8210770f776246e893b515e1c89145e412f0d0f0cb2a4`  
		Last Modified: Tue, 14 Jan 2025 02:15:17 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03338e4032fbada969eec48dc2c2fee01ed7adf78828bc6d40c04ab9507583d`  
		Last Modified: Tue, 14 Jan 2025 02:15:20 GMT  
		Size: 54.0 MB (54047058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e723cb52bcf30c84558d4ccac188f71c03b8891058ff95be8152022690f21f4f`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5282e780179a5e7e90adcb73980f2f9f70231fef1447fbd149a1bc5c64706`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0` - unknown; unknown

```console
$ docker pull docker@sha256:8689bdb9c541bab78f9dd1908957878caf8f25c1253d8bce06cdafe62c1144fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c90fd3c8b21ca316ab44ec447e5562c65bf0a586cb80772ee7a88783c272e86`

```dockerfile
```

-	Layers:
	-	`sha256:f42d1ce12c955562a797d5229e156021010cb89d2612a09a3c8038db1e71759b`  
		Last Modified: Tue, 14 Jan 2025 02:15:16 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0` - linux; arm variant v7

```console
$ docker pull docker@sha256:5999a9ff7ae4b7bfd9ffbdc09f506554ad45cf038a06735ee5bf8f4319855ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05426371377f59be4857cbf89178a0f3786fe20bc74bc05b8177a8ed9053ff4`
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
	-	`sha256:e3a7347c9e2b4172d426277de5d40fe3125e0c6b4f9c9b1b210c2190c24f71a6`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 6.4 MB (6367075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170816e95ac1cab8fd3486637652d489c9eb3aec9613c3b50d432b9080a822bc`  
		Last Modified: Tue, 14 Jan 2025 02:20:08 GMT  
		Size: 85.2 KB (85226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45751052d07b0cc92dd9bbbb7d3b61c9e7c35c0f7cebfb423551d2bd9b9f5756`  
		Last Modified: Tue, 14 Jan 2025 02:20:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6227cd6b9897a9ed931bc5860ced54ff59f31642da0ab188c39197dc19cad0fe`  
		Last Modified: Tue, 14 Jan 2025 02:20:10 GMT  
		Size: 54.0 MB (54047052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73cbf2e0a446e5961fdd597ab7cf88eeb26bf806635c7d184ab9675ddad4374`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d10838d3f481fcdee3e8625d0e55d29fc7d9679f071020833f3730f57d9d83`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0` - unknown; unknown

```console
$ docker pull docker@sha256:037c2c83a82e85230be44bdef44cb3b1d52a2e22d058a5de3aceca56e7159130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0386c303557c0cf65db0f5960ebf6b90f8eaa30c74ffe08cb4c55633a6579454`

```dockerfile
```

-	Layers:
	-	`sha256:941354ab8739c4685b3ec8524f7ba8d6f80ed7d2dc31d182e3d796aff9179e45`  
		Last Modified: Tue, 14 Jan 2025 02:20:07 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ebe06ac52e509d7503408f503c85e7184638d3a39f9da87aa8d7435ebabedef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125657212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a08754d01aa0993ff2b714b092fc20d4c49c6f2b4a2e353e59b54bc19c896af`
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
	-	`sha256:bd25f3cb55cedc28ef3ec15976f2b429e5e24e2f2ec8cf36bbaaa7e6c87c994e`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 7.0 MB (6981981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d49b3e3cd0572d2d1fd7020a8df0ff5fe6bc2b0011ddd9eaf8cc24628779ef9`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 97.8 KB (97789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3200f3c13982eac3851a0c9e87c77fbfe96425bc74c4a9a4db3897a614a1a1`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff187bc55eaede3054ec4ae2f34a0780ccd3306daca06b661e97b61a08d7e413`  
		Last Modified: Tue, 14 Jan 2025 02:26:10 GMT  
		Size: 54.0 MB (53952110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee3e8d3d62aa9df8772f783716c898cf08d668f5759aa735966330e4b3540bc`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f568e54dc452c5a82c30e4b27b6d23ae4813b3aec42ddd31a56a9df635a8af58`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0` - unknown; unknown

```console
$ docker pull docker@sha256:71af01ec9968269e01302b3e5c567694d917a9ff9193f8a336de02c0adfcba6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25642e7f3a9ac8e5eddd583a6b68a8f2802dc2ae11098c5b85bc08b4de76b0fb`

```dockerfile
```

-	Layers:
	-	`sha256:20cf12060b8c0aa852adbbf7cd68171cb42ed9361a70dfc9558418ec756eb3f6`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5.0-alpine3.21`

```console
$ docker pull docker@sha256:cbde039f51b3d85366f59fe2e97cdaf329a6eef076b79a9afb9f9568d04d0767
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
$ docker pull docker@sha256:36b7c405e8884e399ac3c7c63f3f61b065a94b62e0b915e62db4d0de3a0aa0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133866334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef043a7d033c06edb878336aba69dc08a2340456f7dc1c2f80a75a362a7f28a8`
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
	-	`sha256:01ede50c7df8b73c8a3ac91fb3bb36978c76e031bb46b82aa12fa72fada06402`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 6.7 MB (6733496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d285c3782350dd5f9e9ba3ffdca6909b3a357f12e4e0aa69f6509f071fbcfbe3`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 89.4 KB (89420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23e2f46c920045fd9af6784bbff05014d36f9150a63b66c744172d76be81c4`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dca5dcdd0a1de285b0723f6c07453eb8ad4c4e39c1d4685a5921590a3228e6`  
		Last Modified: Tue, 14 Jan 2025 02:16:02 GMT  
		Size: 58.4 MB (58383043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88a905ff3d6fd8eeb1a0e9a4da76911f3121664e953d721c866942a7926851a`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76253b0cea165b9074f6b67ca91b09076bb938e59f417391480e5db39bdf1a9`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:e37c8bd01854ac13fcaa41da9fb226c89c8238bef5a9de4787c9dd0cd07938c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88d598c27af9d5b832d3315a7aabddf36261d15c0e4eb374faf85a8590e65c`

```dockerfile
```

-	Layers:
	-	`sha256:56e2c5d5c223aaa11d450a30736bb729d576e219338fd7ffc0de44d4849a78b0`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:9d7a7eeddee151b3a91d4187569b2bfed0bc15418e0a5f6cb964ad1bc5c00d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124949459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257951f363b47b171f00cddf758ba9666b0e34a357a010eb907440a2634cdeb3`
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
	-	`sha256:846cdf8016994cf55c03364ec088d83836cd9124c4feadfdc1a290c0db052ea1`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 7.0 MB (7041193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105e956e17649a3bfc6e14bb6b91440fae0386c90f0a79b4ef0af00a6633a337`  
		Last Modified: Tue, 14 Jan 2025 02:15:17 GMT  
		Size: 89.1 KB (89081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec413a996e6897217d8210770f776246e893b515e1c89145e412f0d0f0cb2a4`  
		Last Modified: Tue, 14 Jan 2025 02:15:17 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03338e4032fbada969eec48dc2c2fee01ed7adf78828bc6d40c04ab9507583d`  
		Last Modified: Tue, 14 Jan 2025 02:15:20 GMT  
		Size: 54.0 MB (54047058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e723cb52bcf30c84558d4ccac188f71c03b8891058ff95be8152022690f21f4f`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5282e780179a5e7e90adcb73980f2f9f70231fef1447fbd149a1bc5c64706`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:8689bdb9c541bab78f9dd1908957878caf8f25c1253d8bce06cdafe62c1144fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c90fd3c8b21ca316ab44ec447e5562c65bf0a586cb80772ee7a88783c272e86`

```dockerfile
```

-	Layers:
	-	`sha256:f42d1ce12c955562a797d5229e156021010cb89d2612a09a3c8038db1e71759b`  
		Last Modified: Tue, 14 Jan 2025 02:15:16 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:5999a9ff7ae4b7bfd9ffbdc09f506554ad45cf038a06735ee5bf8f4319855ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05426371377f59be4857cbf89178a0f3786fe20bc74bc05b8177a8ed9053ff4`
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
	-	`sha256:e3a7347c9e2b4172d426277de5d40fe3125e0c6b4f9c9b1b210c2190c24f71a6`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 6.4 MB (6367075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170816e95ac1cab8fd3486637652d489c9eb3aec9613c3b50d432b9080a822bc`  
		Last Modified: Tue, 14 Jan 2025 02:20:08 GMT  
		Size: 85.2 KB (85226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45751052d07b0cc92dd9bbbb7d3b61c9e7c35c0f7cebfb423551d2bd9b9f5756`  
		Last Modified: Tue, 14 Jan 2025 02:20:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6227cd6b9897a9ed931bc5860ced54ff59f31642da0ab188c39197dc19cad0fe`  
		Last Modified: Tue, 14 Jan 2025 02:20:10 GMT  
		Size: 54.0 MB (54047052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73cbf2e0a446e5961fdd597ab7cf88eeb26bf806635c7d184ab9675ddad4374`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d10838d3f481fcdee3e8625d0e55d29fc7d9679f071020833f3730f57d9d83`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:037c2c83a82e85230be44bdef44cb3b1d52a2e22d058a5de3aceca56e7159130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0386c303557c0cf65db0f5960ebf6b90f8eaa30c74ffe08cb4c55633a6579454`

```dockerfile
```

-	Layers:
	-	`sha256:941354ab8739c4685b3ec8524f7ba8d6f80ed7d2dc31d182e3d796aff9179e45`  
		Last Modified: Tue, 14 Jan 2025 02:20:07 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ebe06ac52e509d7503408f503c85e7184638d3a39f9da87aa8d7435ebabedef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125657212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a08754d01aa0993ff2b714b092fc20d4c49c6f2b4a2e353e59b54bc19c896af`
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
	-	`sha256:bd25f3cb55cedc28ef3ec15976f2b429e5e24e2f2ec8cf36bbaaa7e6c87c994e`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 7.0 MB (6981981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d49b3e3cd0572d2d1fd7020a8df0ff5fe6bc2b0011ddd9eaf8cc24628779ef9`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 97.8 KB (97789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3200f3c13982eac3851a0c9e87c77fbfe96425bc74c4a9a4db3897a614a1a1`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff187bc55eaede3054ec4ae2f34a0780ccd3306daca06b661e97b61a08d7e413`  
		Last Modified: Tue, 14 Jan 2025 02:26:10 GMT  
		Size: 54.0 MB (53952110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee3e8d3d62aa9df8772f783716c898cf08d668f5759aa735966330e4b3540bc`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f568e54dc452c5a82c30e4b27b6d23ae4813b3aec42ddd31a56a9df635a8af58`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:71af01ec9968269e01302b3e5c567694d917a9ff9193f8a336de02c0adfcba6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25642e7f3a9ac8e5eddd583a6b68a8f2802dc2ae11098c5b85bc08b4de76b0fb`

```dockerfile
```

-	Layers:
	-	`sha256:20cf12060b8c0aa852adbbf7cd68171cb42ed9361a70dfc9558418ec756eb3f6`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull docker@sha256:cbde039f51b3d85366f59fe2e97cdaf329a6eef076b79a9afb9f9568d04d0767
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
$ docker pull docker@sha256:36b7c405e8884e399ac3c7c63f3f61b065a94b62e0b915e62db4d0de3a0aa0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133866334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef043a7d033c06edb878336aba69dc08a2340456f7dc1c2f80a75a362a7f28a8`
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
	-	`sha256:01ede50c7df8b73c8a3ac91fb3bb36978c76e031bb46b82aa12fa72fada06402`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 6.7 MB (6733496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d285c3782350dd5f9e9ba3ffdca6909b3a357f12e4e0aa69f6509f071fbcfbe3`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 89.4 KB (89420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23e2f46c920045fd9af6784bbff05014d36f9150a63b66c744172d76be81c4`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dca5dcdd0a1de285b0723f6c07453eb8ad4c4e39c1d4685a5921590a3228e6`  
		Last Modified: Tue, 14 Jan 2025 02:16:02 GMT  
		Size: 58.4 MB (58383043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88a905ff3d6fd8eeb1a0e9a4da76911f3121664e953d721c866942a7926851a`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76253b0cea165b9074f6b67ca91b09076bb938e59f417391480e5db39bdf1a9`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e37c8bd01854ac13fcaa41da9fb226c89c8238bef5a9de4787c9dd0cd07938c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88d598c27af9d5b832d3315a7aabddf36261d15c0e4eb374faf85a8590e65c`

```dockerfile
```

-	Layers:
	-	`sha256:56e2c5d5c223aaa11d450a30736bb729d576e219338fd7ffc0de44d4849a78b0`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:9d7a7eeddee151b3a91d4187569b2bfed0bc15418e0a5f6cb964ad1bc5c00d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124949459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257951f363b47b171f00cddf758ba9666b0e34a357a010eb907440a2634cdeb3`
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
	-	`sha256:846cdf8016994cf55c03364ec088d83836cd9124c4feadfdc1a290c0db052ea1`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 7.0 MB (7041193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105e956e17649a3bfc6e14bb6b91440fae0386c90f0a79b4ef0af00a6633a337`  
		Last Modified: Tue, 14 Jan 2025 02:15:17 GMT  
		Size: 89.1 KB (89081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec413a996e6897217d8210770f776246e893b515e1c89145e412f0d0f0cb2a4`  
		Last Modified: Tue, 14 Jan 2025 02:15:17 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03338e4032fbada969eec48dc2c2fee01ed7adf78828bc6d40c04ab9507583d`  
		Last Modified: Tue, 14 Jan 2025 02:15:20 GMT  
		Size: 54.0 MB (54047058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e723cb52bcf30c84558d4ccac188f71c03b8891058ff95be8152022690f21f4f`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5282e780179a5e7e90adcb73980f2f9f70231fef1447fbd149a1bc5c64706`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8689bdb9c541bab78f9dd1908957878caf8f25c1253d8bce06cdafe62c1144fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c90fd3c8b21ca316ab44ec447e5562c65bf0a586cb80772ee7a88783c272e86`

```dockerfile
```

-	Layers:
	-	`sha256:f42d1ce12c955562a797d5229e156021010cb89d2612a09a3c8038db1e71759b`  
		Last Modified: Tue, 14 Jan 2025 02:15:16 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:5999a9ff7ae4b7bfd9ffbdc09f506554ad45cf038a06735ee5bf8f4319855ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05426371377f59be4857cbf89178a0f3786fe20bc74bc05b8177a8ed9053ff4`
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
	-	`sha256:e3a7347c9e2b4172d426277de5d40fe3125e0c6b4f9c9b1b210c2190c24f71a6`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 6.4 MB (6367075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170816e95ac1cab8fd3486637652d489c9eb3aec9613c3b50d432b9080a822bc`  
		Last Modified: Tue, 14 Jan 2025 02:20:08 GMT  
		Size: 85.2 KB (85226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45751052d07b0cc92dd9bbbb7d3b61c9e7c35c0f7cebfb423551d2bd9b9f5756`  
		Last Modified: Tue, 14 Jan 2025 02:20:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6227cd6b9897a9ed931bc5860ced54ff59f31642da0ab188c39197dc19cad0fe`  
		Last Modified: Tue, 14 Jan 2025 02:20:10 GMT  
		Size: 54.0 MB (54047052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73cbf2e0a446e5961fdd597ab7cf88eeb26bf806635c7d184ab9675ddad4374`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d10838d3f481fcdee3e8625d0e55d29fc7d9679f071020833f3730f57d9d83`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:037c2c83a82e85230be44bdef44cb3b1d52a2e22d058a5de3aceca56e7159130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0386c303557c0cf65db0f5960ebf6b90f8eaa30c74ffe08cb4c55633a6579454`

```dockerfile
```

-	Layers:
	-	`sha256:941354ab8739c4685b3ec8524f7ba8d6f80ed7d2dc31d182e3d796aff9179e45`  
		Last Modified: Tue, 14 Jan 2025 02:20:07 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ebe06ac52e509d7503408f503c85e7184638d3a39f9da87aa8d7435ebabedef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125657212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a08754d01aa0993ff2b714b092fc20d4c49c6f2b4a2e353e59b54bc19c896af`
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
	-	`sha256:bd25f3cb55cedc28ef3ec15976f2b429e5e24e2f2ec8cf36bbaaa7e6c87c994e`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 7.0 MB (6981981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d49b3e3cd0572d2d1fd7020a8df0ff5fe6bc2b0011ddd9eaf8cc24628779ef9`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 97.8 KB (97789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3200f3c13982eac3851a0c9e87c77fbfe96425bc74c4a9a4db3897a614a1a1`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff187bc55eaede3054ec4ae2f34a0780ccd3306daca06b661e97b61a08d7e413`  
		Last Modified: Tue, 14 Jan 2025 02:26:10 GMT  
		Size: 54.0 MB (53952110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee3e8d3d62aa9df8772f783716c898cf08d668f5759aa735966330e4b3540bc`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f568e54dc452c5a82c30e4b27b6d23ae4813b3aec42ddd31a56a9df635a8af58`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:71af01ec9968269e01302b3e5c567694d917a9ff9193f8a336de02c0adfcba6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25642e7f3a9ac8e5eddd583a6b68a8f2802dc2ae11098c5b85bc08b4de76b0fb`

```dockerfile
```

-	Layers:
	-	`sha256:20cf12060b8c0aa852adbbf7cd68171cb42ed9361a70dfc9558418ec756eb3f6`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5.0-dind-alpine3.21`

```console
$ docker pull docker@sha256:cbde039f51b3d85366f59fe2e97cdaf329a6eef076b79a9afb9f9568d04d0767
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
$ docker pull docker@sha256:36b7c405e8884e399ac3c7c63f3f61b065a94b62e0b915e62db4d0de3a0aa0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133866334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef043a7d033c06edb878336aba69dc08a2340456f7dc1c2f80a75a362a7f28a8`
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
	-	`sha256:01ede50c7df8b73c8a3ac91fb3bb36978c76e031bb46b82aa12fa72fada06402`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 6.7 MB (6733496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d285c3782350dd5f9e9ba3ffdca6909b3a357f12e4e0aa69f6509f071fbcfbe3`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 89.4 KB (89420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23e2f46c920045fd9af6784bbff05014d36f9150a63b66c744172d76be81c4`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dca5dcdd0a1de285b0723f6c07453eb8ad4c4e39c1d4685a5921590a3228e6`  
		Last Modified: Tue, 14 Jan 2025 02:16:02 GMT  
		Size: 58.4 MB (58383043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88a905ff3d6fd8eeb1a0e9a4da76911f3121664e953d721c866942a7926851a`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76253b0cea165b9074f6b67ca91b09076bb938e59f417391480e5db39bdf1a9`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:e37c8bd01854ac13fcaa41da9fb226c89c8238bef5a9de4787c9dd0cd07938c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88d598c27af9d5b832d3315a7aabddf36261d15c0e4eb374faf85a8590e65c`

```dockerfile
```

-	Layers:
	-	`sha256:56e2c5d5c223aaa11d450a30736bb729d576e219338fd7ffc0de44d4849a78b0`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-dind-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:9d7a7eeddee151b3a91d4187569b2bfed0bc15418e0a5f6cb964ad1bc5c00d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124949459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257951f363b47b171f00cddf758ba9666b0e34a357a010eb907440a2634cdeb3`
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
	-	`sha256:846cdf8016994cf55c03364ec088d83836cd9124c4feadfdc1a290c0db052ea1`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 7.0 MB (7041193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105e956e17649a3bfc6e14bb6b91440fae0386c90f0a79b4ef0af00a6633a337`  
		Last Modified: Tue, 14 Jan 2025 02:15:17 GMT  
		Size: 89.1 KB (89081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec413a996e6897217d8210770f776246e893b515e1c89145e412f0d0f0cb2a4`  
		Last Modified: Tue, 14 Jan 2025 02:15:17 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03338e4032fbada969eec48dc2c2fee01ed7adf78828bc6d40c04ab9507583d`  
		Last Modified: Tue, 14 Jan 2025 02:15:20 GMT  
		Size: 54.0 MB (54047058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e723cb52bcf30c84558d4ccac188f71c03b8891058ff95be8152022690f21f4f`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5282e780179a5e7e90adcb73980f2f9f70231fef1447fbd149a1bc5c64706`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:8689bdb9c541bab78f9dd1908957878caf8f25c1253d8bce06cdafe62c1144fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c90fd3c8b21ca316ab44ec447e5562c65bf0a586cb80772ee7a88783c272e86`

```dockerfile
```

-	Layers:
	-	`sha256:f42d1ce12c955562a797d5229e156021010cb89d2612a09a3c8038db1e71759b`  
		Last Modified: Tue, 14 Jan 2025 02:15:16 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-dind-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:5999a9ff7ae4b7bfd9ffbdc09f506554ad45cf038a06735ee5bf8f4319855ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05426371377f59be4857cbf89178a0f3786fe20bc74bc05b8177a8ed9053ff4`
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
	-	`sha256:e3a7347c9e2b4172d426277de5d40fe3125e0c6b4f9c9b1b210c2190c24f71a6`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 6.4 MB (6367075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170816e95ac1cab8fd3486637652d489c9eb3aec9613c3b50d432b9080a822bc`  
		Last Modified: Tue, 14 Jan 2025 02:20:08 GMT  
		Size: 85.2 KB (85226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45751052d07b0cc92dd9bbbb7d3b61c9e7c35c0f7cebfb423551d2bd9b9f5756`  
		Last Modified: Tue, 14 Jan 2025 02:20:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6227cd6b9897a9ed931bc5860ced54ff59f31642da0ab188c39197dc19cad0fe`  
		Last Modified: Tue, 14 Jan 2025 02:20:10 GMT  
		Size: 54.0 MB (54047052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73cbf2e0a446e5961fdd597ab7cf88eeb26bf806635c7d184ab9675ddad4374`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d10838d3f481fcdee3e8625d0e55d29fc7d9679f071020833f3730f57d9d83`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:037c2c83a82e85230be44bdef44cb3b1d52a2e22d058a5de3aceca56e7159130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0386c303557c0cf65db0f5960ebf6b90f8eaa30c74ffe08cb4c55633a6579454`

```dockerfile
```

-	Layers:
	-	`sha256:941354ab8739c4685b3ec8524f7ba8d6f80ed7d2dc31d182e3d796aff9179e45`  
		Last Modified: Tue, 14 Jan 2025 02:20:07 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-dind-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ebe06ac52e509d7503408f503c85e7184638d3a39f9da87aa8d7435ebabedef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125657212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a08754d01aa0993ff2b714b092fc20d4c49c6f2b4a2e353e59b54bc19c896af`
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
	-	`sha256:bd25f3cb55cedc28ef3ec15976f2b429e5e24e2f2ec8cf36bbaaa7e6c87c994e`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 7.0 MB (6981981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d49b3e3cd0572d2d1fd7020a8df0ff5fe6bc2b0011ddd9eaf8cc24628779ef9`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 97.8 KB (97789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3200f3c13982eac3851a0c9e87c77fbfe96425bc74c4a9a4db3897a614a1a1`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff187bc55eaede3054ec4ae2f34a0780ccd3306daca06b661e97b61a08d7e413`  
		Last Modified: Tue, 14 Jan 2025 02:26:10 GMT  
		Size: 54.0 MB (53952110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee3e8d3d62aa9df8772f783716c898cf08d668f5759aa735966330e4b3540bc`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f568e54dc452c5a82c30e4b27b6d23ae4813b3aec42ddd31a56a9df635a8af58`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:71af01ec9968269e01302b3e5c567694d917a9ff9193f8a336de02c0adfcba6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25642e7f3a9ac8e5eddd583a6b68a8f2802dc2ae11098c5b85bc08b4de76b0fb`

```dockerfile
```

-	Layers:
	-	`sha256:20cf12060b8c0aa852adbbf7cd68171cb42ed9361a70dfc9558418ec756eb3f6`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5.0-dind-rootless`

```console
$ docker pull docker@sha256:219cd9ce4727ea072f68cff017caa11fd7719835fa252f4b1fbc1ce77a4ab203
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.5.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9a103862e4648fbcaf52c07bb8ef33db59ee46cbc1eedbc4cbdd10fc4af9788e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156158115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d95700034e28d044add69f30a925b41f26152ee4130b7e8081ca8bda098f95`
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
	-	`sha256:01ede50c7df8b73c8a3ac91fb3bb36978c76e031bb46b82aa12fa72fada06402`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 6.7 MB (6733496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d285c3782350dd5f9e9ba3ffdca6909b3a357f12e4e0aa69f6509f071fbcfbe3`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 89.4 KB (89420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23e2f46c920045fd9af6784bbff05014d36f9150a63b66c744172d76be81c4`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dca5dcdd0a1de285b0723f6c07453eb8ad4c4e39c1d4685a5921590a3228e6`  
		Last Modified: Tue, 14 Jan 2025 02:16:02 GMT  
		Size: 58.4 MB (58383043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88a905ff3d6fd8eeb1a0e9a4da76911f3121664e953d721c866942a7926851a`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76253b0cea165b9074f6b67ca91b09076bb938e59f417391480e5db39bdf1a9`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f935cb48b813bca67e3f4262bc998f10d445daf1ae1c2fe167bea1c7063459`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 986.6 KB (986564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a49473459905f4e8055629a7c6a93f3cef28430740f4a7460d66c31cebe219`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725ab53ec019a57158824c067b8d7c5d4aac14cac54bd82d929c6b3643929400`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a04e34cc60c0c247d0c4340ff8367878b45b1d4eb32445d48706d1c75078bab`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 21.3 MB (21303868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07647e8159772a3be30c90e3f36bcc2cc9575cd8e107a75a5dd202b40e50ec84`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f2bac0bc675c790fd6442f9801b8e048cf22f413d496faaac7d7d98f65e8775f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a58d67e13b913de17a6cef81562735d1cd54b387aeb9bd8393ebedaee21bac8`

```dockerfile
```

-	Layers:
	-	`sha256:9e2e64133b433d854e70c47e94e568307f6e6a9d22ba7f98ac3e92a3860b6b70`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 30.6 KB (30617 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.5.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fe693adc6e1b262dd846e29f8f1f3e52d17839c598c6a9669541aee1390252e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149827921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f807d6de5ec469882013150c9395841dbefd2c5462aa50d31078f831014dd37b`
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
	-	`sha256:bd25f3cb55cedc28ef3ec15976f2b429e5e24e2f2ec8cf36bbaaa7e6c87c994e`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 7.0 MB (6981981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d49b3e3cd0572d2d1fd7020a8df0ff5fe6bc2b0011ddd9eaf8cc24628779ef9`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 97.8 KB (97789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3200f3c13982eac3851a0c9e87c77fbfe96425bc74c4a9a4db3897a614a1a1`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff187bc55eaede3054ec4ae2f34a0780ccd3306daca06b661e97b61a08d7e413`  
		Last Modified: Tue, 14 Jan 2025 02:26:10 GMT  
		Size: 54.0 MB (53952110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee3e8d3d62aa9df8772f783716c898cf08d668f5759aa735966330e4b3540bc`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f568e54dc452c5a82c30e4b27b6d23ae4813b3aec42ddd31a56a9df635a8af58`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a5b110e56f5def4ad57fe3b856b02e8cab49cc738b90c12d2d19c32da7d926`  
		Last Modified: Tue, 14 Jan 2025 13:08:45 GMT  
		Size: 1.0 MB (1014216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1b2aa8218cdd3765ecb7535d1cbfa89c18b85f2826ce1a033776a41f717b0a`  
		Last Modified: Tue, 14 Jan 2025 13:08:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef861fa84a514bb8446c6f52f373f06c448d3b145269e425c1478b9beaac650`  
		Last Modified: Tue, 14 Jan 2025 13:08:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420511f545246aa0d29d9ba63a0499d1f16e94dfe4aee78152f490772e5669`  
		Last Modified: Tue, 14 Jan 2025 13:08:46 GMT  
		Size: 23.2 MB (23155143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276b9bb32935b77cea19ba047d02d2195aad318d0625bef649d08ee9f85faca8`  
		Last Modified: Tue, 14 Jan 2025 13:08:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.5.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:36f161acc3a7aa93dfc002353a682c22393105e860ddff634da0d448d639be2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf8ff57c5b5817496db05260da18bcaba486563fab91628bf1a1e58482bcb6e`

```dockerfile
```

-	Layers:
	-	`sha256:73c16f25635b347a54bad4a273bb8614886e4af8e24067871dc9f20867d2bd00`  
		Last Modified: Tue, 14 Jan 2025 13:08:45 GMT  
		Size: 30.8 KB (30787 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.5.0-windowsservercore`

```console
$ docker pull docker@sha256:3dc453c179e8242a7449e4f8028145e010292915e3230b76aae64d82b49486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `docker:27.5.0-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:65abbf8e57dc9b9317388e7635b591c02a450877d39a6776468c9329c6f0b244
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2321679678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5d69e1dda4a11c5d64215052395e362481548cde33a8d6a4be0b4b125f4b53`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:30:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:30:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 23:30:49 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 23:30:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 23:30:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:31:00 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 23:31:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 23:31:01 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 23:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:31:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 23:31:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 23:31:11 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 23:31:20 GMT
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
	-	`sha256:7e42393aec052ef4ad419b20811d5f8f1f4cef5ae7d1b6da49d51a64a7bded4a`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273b7e9f3e3d8546b60d078c2152236a9749ecd2ce4b8677348fe2d97b5798be`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 341.3 KB (341285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cbb7d5116a553e19e688cc78072e8b1eb29afb0b5be4644ed522bf083acd3f`  
		Last Modified: Tue, 14 Jan 2025 23:31:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bfc86e47da2a329fa916e619f50b1572e090a406c11b35b6235548d8bc52ee`  
		Last Modified: Tue, 14 Jan 2025 23:31:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3634f4abc247a49927973cdf069a2717f0053ec34fae55d8f7014967864fb`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 19.1 MB (19149523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36028f38b9d36c2624a31329c881064c7c9b02472ec1aecfb6924bd39ef2450`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0cfd1d3174eb2bbbce2d334d4fd0e90cdd7ca8747f146ef6da5a8cf8e937a3`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834b9a7619d4a8f64af8850acc540189ba984e6f829cde434c43eaa00ac13251`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde3f31a6ef2d6c5cb116f4c7246bdcf8ed9a39ac3ea376b13832a9a90df8d63`  
		Last Modified: Tue, 14 Jan 2025 23:31:27 GMT  
		Size: 19.6 MB (19634023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7331fb5fa54eb509667e318fef4224b22e7267a8b01ab08320597309a61cc9`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41addc9937b80bc18e288c60f1f057cce9b501761a6c845a8a385dca9084663e`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752c051f71c979cefbe564869be494631945a5cd1aad02a5904c2715b12c51b0`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dff165c12cf41f3471c535f13b2fefdaf7f686d0bc74b8372caf2d7dbb7a08f`  
		Last Modified: Tue, 14 Jan 2025 23:31:27 GMT  
		Size: 20.2 MB (20158014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.5.0-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:e623df1460d3ebcb3ad8073621cc95b69f52df75ca8d0ab278177ef2085183d4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181418375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edf4c3deefe7cfd0ff52fd0d9d60c10b8e24d2facaaff9e581b0bed9b8c7cdc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:37:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:38:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 23:38:50 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 23:38:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 23:39:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:04 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 23:39:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 23:39:05 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 23:39:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 23:39:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 23:39:15 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 23:39:22 GMT
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
	-	`sha256:ace576e2b330b24c982543035820a2ecbea8fa58428209b788c8dbc34fe43f5e`  
		Last Modified: Tue, 14 Jan 2025 23:39:28 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d288a76c5d5ee64affc87ec0d46e06ebb6326b17068f33a5792bf7f16641fe84`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 316.6 KB (316613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d7033573b703663b78be30fbeb8df368a1408341870dee01f3801334d22fdf`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200e4ef96719afb123d542fba348a35d1e6b8c7ea5da1d183af90ff0537d8adf`  
		Last Modified: Tue, 14 Jan 2025 23:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0f7834de3577810e21557605584283e758ff40eae06e414866571f6c2e16df`  
		Last Modified: Tue, 14 Jan 2025 23:39:29 GMT  
		Size: 19.1 MB (19132926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cc1331cde43f073663e2b9396edd7ccac0f5309292d4f046cbe985d4402471`  
		Last Modified: Tue, 14 Jan 2025 23:39:26 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff86dabfa389add56b99fda4a391700fa18ff5756120341345a47f98a2802312`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8192f34e31a6709287fc3944570a104c942154cde3b91498b2afc544cf1bde`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3253d8429e17a419d9f3970970cec0e25ea529d22e9b1f46d68195ccd2ddf9`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 19.6 MB (19607700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb691e1b2ced8da219bfba3fd2da38afd59e2d41d524d5f93ff610894aab74c`  
		Last Modified: Tue, 14 Jan 2025 23:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37177f635ff92a20fc9c2edee74a5d7fef05bac391f1261da856a52900a7d2f`  
		Last Modified: Tue, 14 Jan 2025 23:39:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e7ed4e2f131f942a5e8a2b6add2e3585ef60fff72094fffe47b43c98ff50f5`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c0912a92c0e5091e90b6472cd2d2c89be81d415d84cc5426d62c54b147fdd1`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 20.1 MB (20137257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:fd008b6841d28c3f235332ce741282e625c4b9909c55ac89eba81a4efe37e611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `docker:27.5.0-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:e623df1460d3ebcb3ad8073621cc95b69f52df75ca8d0ab278177ef2085183d4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181418375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edf4c3deefe7cfd0ff52fd0d9d60c10b8e24d2facaaff9e581b0bed9b8c7cdc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:37:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:38:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 23:38:50 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 23:38:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 23:39:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:04 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 23:39:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 23:39:05 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 23:39:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 23:39:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 23:39:15 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 23:39:22 GMT
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
	-	`sha256:ace576e2b330b24c982543035820a2ecbea8fa58428209b788c8dbc34fe43f5e`  
		Last Modified: Tue, 14 Jan 2025 23:39:28 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d288a76c5d5ee64affc87ec0d46e06ebb6326b17068f33a5792bf7f16641fe84`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 316.6 KB (316613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d7033573b703663b78be30fbeb8df368a1408341870dee01f3801334d22fdf`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200e4ef96719afb123d542fba348a35d1e6b8c7ea5da1d183af90ff0537d8adf`  
		Last Modified: Tue, 14 Jan 2025 23:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0f7834de3577810e21557605584283e758ff40eae06e414866571f6c2e16df`  
		Last Modified: Tue, 14 Jan 2025 23:39:29 GMT  
		Size: 19.1 MB (19132926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cc1331cde43f073663e2b9396edd7ccac0f5309292d4f046cbe985d4402471`  
		Last Modified: Tue, 14 Jan 2025 23:39:26 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff86dabfa389add56b99fda4a391700fa18ff5756120341345a47f98a2802312`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8192f34e31a6709287fc3944570a104c942154cde3b91498b2afc544cf1bde`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3253d8429e17a419d9f3970970cec0e25ea529d22e9b1f46d68195ccd2ddf9`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 19.6 MB (19607700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb691e1b2ced8da219bfba3fd2da38afd59e2d41d524d5f93ff610894aab74c`  
		Last Modified: Tue, 14 Jan 2025 23:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37177f635ff92a20fc9c2edee74a5d7fef05bac391f1261da856a52900a7d2f`  
		Last Modified: Tue, 14 Jan 2025 23:39:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e7ed4e2f131f942a5e8a2b6add2e3585ef60fff72094fffe47b43c98ff50f5`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c0912a92c0e5091e90b6472cd2d2c89be81d415d84cc5426d62c54b147fdd1`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 20.1 MB (20137257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.5.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:74d0de74839599456a874f19aee0058bfba7a13d7a8049272594f2e69a1ff72b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `docker:27.5.0-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:65abbf8e57dc9b9317388e7635b591c02a450877d39a6776468c9329c6f0b244
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2321679678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5d69e1dda4a11c5d64215052395e362481548cde33a8d6a4be0b4b125f4b53`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:30:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:30:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 23:30:49 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 23:30:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 23:30:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:31:00 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 23:31:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 23:31:01 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 23:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:31:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 23:31:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 23:31:11 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 23:31:20 GMT
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
	-	`sha256:7e42393aec052ef4ad419b20811d5f8f1f4cef5ae7d1b6da49d51a64a7bded4a`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273b7e9f3e3d8546b60d078c2152236a9749ecd2ce4b8677348fe2d97b5798be`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 341.3 KB (341285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cbb7d5116a553e19e688cc78072e8b1eb29afb0b5be4644ed522bf083acd3f`  
		Last Modified: Tue, 14 Jan 2025 23:31:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bfc86e47da2a329fa916e619f50b1572e090a406c11b35b6235548d8bc52ee`  
		Last Modified: Tue, 14 Jan 2025 23:31:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3634f4abc247a49927973cdf069a2717f0053ec34fae55d8f7014967864fb`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 19.1 MB (19149523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36028f38b9d36c2624a31329c881064c7c9b02472ec1aecfb6924bd39ef2450`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0cfd1d3174eb2bbbce2d334d4fd0e90cdd7ca8747f146ef6da5a8cf8e937a3`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834b9a7619d4a8f64af8850acc540189ba984e6f829cde434c43eaa00ac13251`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde3f31a6ef2d6c5cb116f4c7246bdcf8ed9a39ac3ea376b13832a9a90df8d63`  
		Last Modified: Tue, 14 Jan 2025 23:31:27 GMT  
		Size: 19.6 MB (19634023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7331fb5fa54eb509667e318fef4224b22e7267a8b01ab08320597309a61cc9`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41addc9937b80bc18e288c60f1f057cce9b501761a6c845a8a385dca9084663e`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752c051f71c979cefbe564869be494631945a5cd1aad02a5904c2715b12c51b0`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dff165c12cf41f3471c535f13b2fefdaf7f686d0bc74b8372caf2d7dbb7a08f`  
		Last Modified: Tue, 14 Jan 2025 23:31:27 GMT  
		Size: 20.2 MB (20158014 bytes)  
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
$ docker pull docker@sha256:cbde039f51b3d85366f59fe2e97cdaf329a6eef076b79a9afb9f9568d04d0767
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
$ docker pull docker@sha256:36b7c405e8884e399ac3c7c63f3f61b065a94b62e0b915e62db4d0de3a0aa0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133866334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef043a7d033c06edb878336aba69dc08a2340456f7dc1c2f80a75a362a7f28a8`
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
	-	`sha256:01ede50c7df8b73c8a3ac91fb3bb36978c76e031bb46b82aa12fa72fada06402`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 6.7 MB (6733496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d285c3782350dd5f9e9ba3ffdca6909b3a357f12e4e0aa69f6509f071fbcfbe3`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 89.4 KB (89420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23e2f46c920045fd9af6784bbff05014d36f9150a63b66c744172d76be81c4`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dca5dcdd0a1de285b0723f6c07453eb8ad4c4e39c1d4685a5921590a3228e6`  
		Last Modified: Tue, 14 Jan 2025 02:16:02 GMT  
		Size: 58.4 MB (58383043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88a905ff3d6fd8eeb1a0e9a4da76911f3121664e953d721c866942a7926851a`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76253b0cea165b9074f6b67ca91b09076bb938e59f417391480e5db39bdf1a9`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:e37c8bd01854ac13fcaa41da9fb226c89c8238bef5a9de4787c9dd0cd07938c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88d598c27af9d5b832d3315a7aabddf36261d15c0e4eb374faf85a8590e65c`

```dockerfile
```

-	Layers:
	-	`sha256:56e2c5d5c223aaa11d450a30736bb729d576e219338fd7ffc0de44d4849a78b0`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:9d7a7eeddee151b3a91d4187569b2bfed0bc15418e0a5f6cb964ad1bc5c00d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124949459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257951f363b47b171f00cddf758ba9666b0e34a357a010eb907440a2634cdeb3`
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
	-	`sha256:846cdf8016994cf55c03364ec088d83836cd9124c4feadfdc1a290c0db052ea1`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 7.0 MB (7041193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105e956e17649a3bfc6e14bb6b91440fae0386c90f0a79b4ef0af00a6633a337`  
		Last Modified: Tue, 14 Jan 2025 02:15:17 GMT  
		Size: 89.1 KB (89081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec413a996e6897217d8210770f776246e893b515e1c89145e412f0d0f0cb2a4`  
		Last Modified: Tue, 14 Jan 2025 02:15:17 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03338e4032fbada969eec48dc2c2fee01ed7adf78828bc6d40c04ab9507583d`  
		Last Modified: Tue, 14 Jan 2025 02:15:20 GMT  
		Size: 54.0 MB (54047058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e723cb52bcf30c84558d4ccac188f71c03b8891058ff95be8152022690f21f4f`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5282e780179a5e7e90adcb73980f2f9f70231fef1447fbd149a1bc5c64706`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:8689bdb9c541bab78f9dd1908957878caf8f25c1253d8bce06cdafe62c1144fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c90fd3c8b21ca316ab44ec447e5562c65bf0a586cb80772ee7a88783c272e86`

```dockerfile
```

-	Layers:
	-	`sha256:f42d1ce12c955562a797d5229e156021010cb89d2612a09a3c8038db1e71759b`  
		Last Modified: Tue, 14 Jan 2025 02:15:16 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:5999a9ff7ae4b7bfd9ffbdc09f506554ad45cf038a06735ee5bf8f4319855ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05426371377f59be4857cbf89178a0f3786fe20bc74bc05b8177a8ed9053ff4`
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
	-	`sha256:e3a7347c9e2b4172d426277de5d40fe3125e0c6b4f9c9b1b210c2190c24f71a6`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 6.4 MB (6367075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170816e95ac1cab8fd3486637652d489c9eb3aec9613c3b50d432b9080a822bc`  
		Last Modified: Tue, 14 Jan 2025 02:20:08 GMT  
		Size: 85.2 KB (85226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45751052d07b0cc92dd9bbbb7d3b61c9e7c35c0f7cebfb423551d2bd9b9f5756`  
		Last Modified: Tue, 14 Jan 2025 02:20:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6227cd6b9897a9ed931bc5860ced54ff59f31642da0ab188c39197dc19cad0fe`  
		Last Modified: Tue, 14 Jan 2025 02:20:10 GMT  
		Size: 54.0 MB (54047052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73cbf2e0a446e5961fdd597ab7cf88eeb26bf806635c7d184ab9675ddad4374`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d10838d3f481fcdee3e8625d0e55d29fc7d9679f071020833f3730f57d9d83`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:037c2c83a82e85230be44bdef44cb3b1d52a2e22d058a5de3aceca56e7159130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0386c303557c0cf65db0f5960ebf6b90f8eaa30c74ffe08cb4c55633a6579454`

```dockerfile
```

-	Layers:
	-	`sha256:941354ab8739c4685b3ec8524f7ba8d6f80ed7d2dc31d182e3d796aff9179e45`  
		Last Modified: Tue, 14 Jan 2025 02:20:07 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ebe06ac52e509d7503408f503c85e7184638d3a39f9da87aa8d7435ebabedef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125657212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a08754d01aa0993ff2b714b092fc20d4c49c6f2b4a2e353e59b54bc19c896af`
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
	-	`sha256:bd25f3cb55cedc28ef3ec15976f2b429e5e24e2f2ec8cf36bbaaa7e6c87c994e`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 7.0 MB (6981981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d49b3e3cd0572d2d1fd7020a8df0ff5fe6bc2b0011ddd9eaf8cc24628779ef9`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 97.8 KB (97789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3200f3c13982eac3851a0c9e87c77fbfe96425bc74c4a9a4db3897a614a1a1`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff187bc55eaede3054ec4ae2f34a0780ccd3306daca06b661e97b61a08d7e413`  
		Last Modified: Tue, 14 Jan 2025 02:26:10 GMT  
		Size: 54.0 MB (53952110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee3e8d3d62aa9df8772f783716c898cf08d668f5759aa735966330e4b3540bc`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f568e54dc452c5a82c30e4b27b6d23ae4813b3aec42ddd31a56a9df635a8af58`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:71af01ec9968269e01302b3e5c567694d917a9ff9193f8a336de02c0adfcba6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25642e7f3a9ac8e5eddd583a6b68a8f2802dc2ae11098c5b85bc08b4de76b0fb`

```dockerfile
```

-	Layers:
	-	`sha256:20cf12060b8c0aa852adbbf7cd68171cb42ed9361a70dfc9558418ec756eb3f6`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:219cd9ce4727ea072f68cff017caa11fd7719835fa252f4b1fbc1ce77a4ab203
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9a103862e4648fbcaf52c07bb8ef33db59ee46cbc1eedbc4cbdd10fc4af9788e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156158115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d95700034e28d044add69f30a925b41f26152ee4130b7e8081ca8bda098f95`
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
	-	`sha256:01ede50c7df8b73c8a3ac91fb3bb36978c76e031bb46b82aa12fa72fada06402`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 6.7 MB (6733496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d285c3782350dd5f9e9ba3ffdca6909b3a357f12e4e0aa69f6509f071fbcfbe3`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 89.4 KB (89420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23e2f46c920045fd9af6784bbff05014d36f9150a63b66c744172d76be81c4`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dca5dcdd0a1de285b0723f6c07453eb8ad4c4e39c1d4685a5921590a3228e6`  
		Last Modified: Tue, 14 Jan 2025 02:16:02 GMT  
		Size: 58.4 MB (58383043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88a905ff3d6fd8eeb1a0e9a4da76911f3121664e953d721c866942a7926851a`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76253b0cea165b9074f6b67ca91b09076bb938e59f417391480e5db39bdf1a9`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f935cb48b813bca67e3f4262bc998f10d445daf1ae1c2fe167bea1c7063459`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 986.6 KB (986564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a49473459905f4e8055629a7c6a93f3cef28430740f4a7460d66c31cebe219`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725ab53ec019a57158824c067b8d7c5d4aac14cac54bd82d929c6b3643929400`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a04e34cc60c0c247d0c4340ff8367878b45b1d4eb32445d48706d1c75078bab`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 21.3 MB (21303868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07647e8159772a3be30c90e3f36bcc2cc9575cd8e107a75a5dd202b40e50ec84`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f2bac0bc675c790fd6442f9801b8e048cf22f413d496faaac7d7d98f65e8775f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a58d67e13b913de17a6cef81562735d1cd54b387aeb9bd8393ebedaee21bac8`

```dockerfile
```

-	Layers:
	-	`sha256:9e2e64133b433d854e70c47e94e568307f6e6a9d22ba7f98ac3e92a3860b6b70`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 30.6 KB (30617 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fe693adc6e1b262dd846e29f8f1f3e52d17839c598c6a9669541aee1390252e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149827921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f807d6de5ec469882013150c9395841dbefd2c5462aa50d31078f831014dd37b`
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
	-	`sha256:bd25f3cb55cedc28ef3ec15976f2b429e5e24e2f2ec8cf36bbaaa7e6c87c994e`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 7.0 MB (6981981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d49b3e3cd0572d2d1fd7020a8df0ff5fe6bc2b0011ddd9eaf8cc24628779ef9`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 97.8 KB (97789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3200f3c13982eac3851a0c9e87c77fbfe96425bc74c4a9a4db3897a614a1a1`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff187bc55eaede3054ec4ae2f34a0780ccd3306daca06b661e97b61a08d7e413`  
		Last Modified: Tue, 14 Jan 2025 02:26:10 GMT  
		Size: 54.0 MB (53952110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee3e8d3d62aa9df8772f783716c898cf08d668f5759aa735966330e4b3540bc`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f568e54dc452c5a82c30e4b27b6d23ae4813b3aec42ddd31a56a9df635a8af58`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a5b110e56f5def4ad57fe3b856b02e8cab49cc738b90c12d2d19c32da7d926`  
		Last Modified: Tue, 14 Jan 2025 13:08:45 GMT  
		Size: 1.0 MB (1014216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1b2aa8218cdd3765ecb7535d1cbfa89c18b85f2826ce1a033776a41f717b0a`  
		Last Modified: Tue, 14 Jan 2025 13:08:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef861fa84a514bb8446c6f52f373f06c448d3b145269e425c1478b9beaac650`  
		Last Modified: Tue, 14 Jan 2025 13:08:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb420511f545246aa0d29d9ba63a0499d1f16e94dfe4aee78152f490772e5669`  
		Last Modified: Tue, 14 Jan 2025 13:08:46 GMT  
		Size: 23.2 MB (23155143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276b9bb32935b77cea19ba047d02d2195aad318d0625bef649d08ee9f85faca8`  
		Last Modified: Tue, 14 Jan 2025 13:08:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:36f161acc3a7aa93dfc002353a682c22393105e860ddff634da0d448d639be2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf8ff57c5b5817496db05260da18bcaba486563fab91628bf1a1e58482bcb6e`

```dockerfile
```

-	Layers:
	-	`sha256:73c16f25635b347a54bad4a273bb8614886e4af8e24067871dc9f20867d2bd00`  
		Last Modified: Tue, 14 Jan 2025 13:08:45 GMT  
		Size: 30.8 KB (30787 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:cbde039f51b3d85366f59fe2e97cdaf329a6eef076b79a9afb9f9568d04d0767
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
$ docker pull docker@sha256:36b7c405e8884e399ac3c7c63f3f61b065a94b62e0b915e62db4d0de3a0aa0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133866334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef043a7d033c06edb878336aba69dc08a2340456f7dc1c2f80a75a362a7f28a8`
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
	-	`sha256:01ede50c7df8b73c8a3ac91fb3bb36978c76e031bb46b82aa12fa72fada06402`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 6.7 MB (6733496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d285c3782350dd5f9e9ba3ffdca6909b3a357f12e4e0aa69f6509f071fbcfbe3`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 89.4 KB (89420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23e2f46c920045fd9af6784bbff05014d36f9150a63b66c744172d76be81c4`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dca5dcdd0a1de285b0723f6c07453eb8ad4c4e39c1d4685a5921590a3228e6`  
		Last Modified: Tue, 14 Jan 2025 02:16:02 GMT  
		Size: 58.4 MB (58383043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88a905ff3d6fd8eeb1a0e9a4da76911f3121664e953d721c866942a7926851a`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76253b0cea165b9074f6b67ca91b09076bb938e59f417391480e5db39bdf1a9`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:e37c8bd01854ac13fcaa41da9fb226c89c8238bef5a9de4787c9dd0cd07938c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88d598c27af9d5b832d3315a7aabddf36261d15c0e4eb374faf85a8590e65c`

```dockerfile
```

-	Layers:
	-	`sha256:56e2c5d5c223aaa11d450a30736bb729d576e219338fd7ffc0de44d4849a78b0`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:9d7a7eeddee151b3a91d4187569b2bfed0bc15418e0a5f6cb964ad1bc5c00d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124949459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257951f363b47b171f00cddf758ba9666b0e34a357a010eb907440a2634cdeb3`
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
	-	`sha256:846cdf8016994cf55c03364ec088d83836cd9124c4feadfdc1a290c0db052ea1`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 7.0 MB (7041193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105e956e17649a3bfc6e14bb6b91440fae0386c90f0a79b4ef0af00a6633a337`  
		Last Modified: Tue, 14 Jan 2025 02:15:17 GMT  
		Size: 89.1 KB (89081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec413a996e6897217d8210770f776246e893b515e1c89145e412f0d0f0cb2a4`  
		Last Modified: Tue, 14 Jan 2025 02:15:17 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03338e4032fbada969eec48dc2c2fee01ed7adf78828bc6d40c04ab9507583d`  
		Last Modified: Tue, 14 Jan 2025 02:15:20 GMT  
		Size: 54.0 MB (54047058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e723cb52bcf30c84558d4ccac188f71c03b8891058ff95be8152022690f21f4f`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5282e780179a5e7e90adcb73980f2f9f70231fef1447fbd149a1bc5c64706`  
		Last Modified: Tue, 14 Jan 2025 02:15:18 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:8689bdb9c541bab78f9dd1908957878caf8f25c1253d8bce06cdafe62c1144fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c90fd3c8b21ca316ab44ec447e5562c65bf0a586cb80772ee7a88783c272e86`

```dockerfile
```

-	Layers:
	-	`sha256:f42d1ce12c955562a797d5229e156021010cb89d2612a09a3c8038db1e71759b`  
		Last Modified: Tue, 14 Jan 2025 02:15:16 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:5999a9ff7ae4b7bfd9ffbdc09f506554ad45cf038a06735ee5bf8f4319855ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123281242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05426371377f59be4857cbf89178a0f3786fe20bc74bc05b8177a8ed9053ff4`
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
	-	`sha256:e3a7347c9e2b4172d426277de5d40fe3125e0c6b4f9c9b1b210c2190c24f71a6`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 6.4 MB (6367075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170816e95ac1cab8fd3486637652d489c9eb3aec9613c3b50d432b9080a822bc`  
		Last Modified: Tue, 14 Jan 2025 02:20:08 GMT  
		Size: 85.2 KB (85226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45751052d07b0cc92dd9bbbb7d3b61c9e7c35c0f7cebfb423551d2bd9b9f5756`  
		Last Modified: Tue, 14 Jan 2025 02:20:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6227cd6b9897a9ed931bc5860ced54ff59f31642da0ab188c39197dc19cad0fe`  
		Last Modified: Tue, 14 Jan 2025 02:20:10 GMT  
		Size: 54.0 MB (54047052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73cbf2e0a446e5961fdd597ab7cf88eeb26bf806635c7d184ab9675ddad4374`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d10838d3f481fcdee3e8625d0e55d29fc7d9679f071020833f3730f57d9d83`  
		Last Modified: Tue, 14 Jan 2025 02:20:09 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:037c2c83a82e85230be44bdef44cb3b1d52a2e22d058a5de3aceca56e7159130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0386c303557c0cf65db0f5960ebf6b90f8eaa30c74ffe08cb4c55633a6579454`

```dockerfile
```

-	Layers:
	-	`sha256:941354ab8739c4685b3ec8524f7ba8d6f80ed7d2dc31d182e3d796aff9179e45`  
		Last Modified: Tue, 14 Jan 2025 02:20:07 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ebe06ac52e509d7503408f503c85e7184638d3a39f9da87aa8d7435ebabedef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125657212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a08754d01aa0993ff2b714b092fc20d4c49c6f2b4a2e353e59b54bc19c896af`
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
	-	`sha256:bd25f3cb55cedc28ef3ec15976f2b429e5e24e2f2ec8cf36bbaaa7e6c87c994e`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 7.0 MB (6981981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d49b3e3cd0572d2d1fd7020a8df0ff5fe6bc2b0011ddd9eaf8cc24628779ef9`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 97.8 KB (97789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3200f3c13982eac3851a0c9e87c77fbfe96425bc74c4a9a4db3897a614a1a1`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff187bc55eaede3054ec4ae2f34a0780ccd3306daca06b661e97b61a08d7e413`  
		Last Modified: Tue, 14 Jan 2025 02:26:10 GMT  
		Size: 54.0 MB (53952110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee3e8d3d62aa9df8772f783716c898cf08d668f5759aa735966330e4b3540bc`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f568e54dc452c5a82c30e4b27b6d23ae4813b3aec42ddd31a56a9df635a8af58`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:71af01ec9968269e01302b3e5c567694d917a9ff9193f8a336de02c0adfcba6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25642e7f3a9ac8e5eddd583a6b68a8f2802dc2ae11098c5b85bc08b4de76b0fb`

```dockerfile
```

-	Layers:
	-	`sha256:20cf12060b8c0aa852adbbf7cd68171cb42ed9361a70dfc9558418ec756eb3f6`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:3dc453c179e8242a7449e4f8028145e010292915e3230b76aae64d82b49486e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `docker:windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:65abbf8e57dc9b9317388e7635b591c02a450877d39a6776468c9329c6f0b244
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2321679678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5d69e1dda4a11c5d64215052395e362481548cde33a8d6a4be0b4b125f4b53`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:30:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:30:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 23:30:49 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 23:30:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 23:30:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:31:00 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 23:31:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 23:31:01 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 23:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:31:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 23:31:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 23:31:11 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 23:31:20 GMT
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
	-	`sha256:7e42393aec052ef4ad419b20811d5f8f1f4cef5ae7d1b6da49d51a64a7bded4a`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273b7e9f3e3d8546b60d078c2152236a9749ecd2ce4b8677348fe2d97b5798be`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 341.3 KB (341285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cbb7d5116a553e19e688cc78072e8b1eb29afb0b5be4644ed522bf083acd3f`  
		Last Modified: Tue, 14 Jan 2025 23:31:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bfc86e47da2a329fa916e619f50b1572e090a406c11b35b6235548d8bc52ee`  
		Last Modified: Tue, 14 Jan 2025 23:31:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3634f4abc247a49927973cdf069a2717f0053ec34fae55d8f7014967864fb`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 19.1 MB (19149523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36028f38b9d36c2624a31329c881064c7c9b02472ec1aecfb6924bd39ef2450`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0cfd1d3174eb2bbbce2d334d4fd0e90cdd7ca8747f146ef6da5a8cf8e937a3`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834b9a7619d4a8f64af8850acc540189ba984e6f829cde434c43eaa00ac13251`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde3f31a6ef2d6c5cb116f4c7246bdcf8ed9a39ac3ea376b13832a9a90df8d63`  
		Last Modified: Tue, 14 Jan 2025 23:31:27 GMT  
		Size: 19.6 MB (19634023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7331fb5fa54eb509667e318fef4224b22e7267a8b01ab08320597309a61cc9`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41addc9937b80bc18e288c60f1f057cce9b501761a6c845a8a385dca9084663e`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752c051f71c979cefbe564869be494631945a5cd1aad02a5904c2715b12c51b0`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dff165c12cf41f3471c535f13b2fefdaf7f686d0bc74b8372caf2d7dbb7a08f`  
		Last Modified: Tue, 14 Jan 2025 23:31:27 GMT  
		Size: 20.2 MB (20158014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:e623df1460d3ebcb3ad8073621cc95b69f52df75ca8d0ab278177ef2085183d4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181418375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edf4c3deefe7cfd0ff52fd0d9d60c10b8e24d2facaaff9e581b0bed9b8c7cdc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:37:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:38:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 23:38:50 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 23:38:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 23:39:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:04 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 23:39:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 23:39:05 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 23:39:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 23:39:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 23:39:15 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 23:39:22 GMT
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
	-	`sha256:ace576e2b330b24c982543035820a2ecbea8fa58428209b788c8dbc34fe43f5e`  
		Last Modified: Tue, 14 Jan 2025 23:39:28 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d288a76c5d5ee64affc87ec0d46e06ebb6326b17068f33a5792bf7f16641fe84`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 316.6 KB (316613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d7033573b703663b78be30fbeb8df368a1408341870dee01f3801334d22fdf`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200e4ef96719afb123d542fba348a35d1e6b8c7ea5da1d183af90ff0537d8adf`  
		Last Modified: Tue, 14 Jan 2025 23:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0f7834de3577810e21557605584283e758ff40eae06e414866571f6c2e16df`  
		Last Modified: Tue, 14 Jan 2025 23:39:29 GMT  
		Size: 19.1 MB (19132926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cc1331cde43f073663e2b9396edd7ccac0f5309292d4f046cbe985d4402471`  
		Last Modified: Tue, 14 Jan 2025 23:39:26 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff86dabfa389add56b99fda4a391700fa18ff5756120341345a47f98a2802312`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8192f34e31a6709287fc3944570a104c942154cde3b91498b2afc544cf1bde`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3253d8429e17a419d9f3970970cec0e25ea529d22e9b1f46d68195ccd2ddf9`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 19.6 MB (19607700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb691e1b2ced8da219bfba3fd2da38afd59e2d41d524d5f93ff610894aab74c`  
		Last Modified: Tue, 14 Jan 2025 23:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37177f635ff92a20fc9c2edee74a5d7fef05bac391f1261da856a52900a7d2f`  
		Last Modified: Tue, 14 Jan 2025 23:39:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e7ed4e2f131f942a5e8a2b6add2e3585ef60fff72094fffe47b43c98ff50f5`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c0912a92c0e5091e90b6472cd2d2c89be81d415d84cc5426d62c54b147fdd1`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 20.1 MB (20137257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:fd008b6841d28c3f235332ce741282e625c4b9909c55ac89eba81a4efe37e611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:e623df1460d3ebcb3ad8073621cc95b69f52df75ca8d0ab278177ef2085183d4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181418375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edf4c3deefe7cfd0ff52fd0d9d60c10b8e24d2facaaff9e581b0bed9b8c7cdc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:37:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:38:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 23:38:50 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 23:38:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 23:39:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:04 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 23:39:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 23:39:05 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 23:39:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 23:39:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 23:39:15 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 23:39:22 GMT
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
	-	`sha256:ace576e2b330b24c982543035820a2ecbea8fa58428209b788c8dbc34fe43f5e`  
		Last Modified: Tue, 14 Jan 2025 23:39:28 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d288a76c5d5ee64affc87ec0d46e06ebb6326b17068f33a5792bf7f16641fe84`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 316.6 KB (316613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d7033573b703663b78be30fbeb8df368a1408341870dee01f3801334d22fdf`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200e4ef96719afb123d542fba348a35d1e6b8c7ea5da1d183af90ff0537d8adf`  
		Last Modified: Tue, 14 Jan 2025 23:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0f7834de3577810e21557605584283e758ff40eae06e414866571f6c2e16df`  
		Last Modified: Tue, 14 Jan 2025 23:39:29 GMT  
		Size: 19.1 MB (19132926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cc1331cde43f073663e2b9396edd7ccac0f5309292d4f046cbe985d4402471`  
		Last Modified: Tue, 14 Jan 2025 23:39:26 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff86dabfa389add56b99fda4a391700fa18ff5756120341345a47f98a2802312`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8192f34e31a6709287fc3944570a104c942154cde3b91498b2afc544cf1bde`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3253d8429e17a419d9f3970970cec0e25ea529d22e9b1f46d68195ccd2ddf9`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 19.6 MB (19607700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb691e1b2ced8da219bfba3fd2da38afd59e2d41d524d5f93ff610894aab74c`  
		Last Modified: Tue, 14 Jan 2025 23:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37177f635ff92a20fc9c2edee74a5d7fef05bac391f1261da856a52900a7d2f`  
		Last Modified: Tue, 14 Jan 2025 23:39:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e7ed4e2f131f942a5e8a2b6add2e3585ef60fff72094fffe47b43c98ff50f5`  
		Last Modified: Tue, 14 Jan 2025 23:39:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c0912a92c0e5091e90b6472cd2d2c89be81d415d84cc5426d62c54b147fdd1`  
		Last Modified: Tue, 14 Jan 2025 23:39:27 GMT  
		Size: 20.1 MB (20137257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:74d0de74839599456a874f19aee0058bfba7a13d7a8049272594f2e69a1ff72b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:65abbf8e57dc9b9317388e7635b591c02a450877d39a6776468c9329c6f0b244
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2321679678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5d69e1dda4a11c5d64215052395e362481548cde33a8d6a4be0b4b125f4b53`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:30:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:30:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Jan 2025 23:30:49 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 14 Jan 2025 23:30:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 14 Jan 2025 23:30:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:31:00 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Tue, 14 Jan 2025 23:31:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Tue, 14 Jan 2025 23:31:01 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Tue, 14 Jan 2025 23:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:31:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Tue, 14 Jan 2025 23:31:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-windows-x86_64.exe
# Tue, 14 Jan 2025 23:31:11 GMT
ENV DOCKER_COMPOSE_SHA256=67a0c3ca2fd94c74982917c8bdf54465367fc3a8c0cb17c529eb6525d32b1674
# Tue, 14 Jan 2025 23:31:20 GMT
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
	-	`sha256:7e42393aec052ef4ad419b20811d5f8f1f4cef5ae7d1b6da49d51a64a7bded4a`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273b7e9f3e3d8546b60d078c2152236a9749ecd2ce4b8677348fe2d97b5798be`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 341.3 KB (341285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cbb7d5116a553e19e688cc78072e8b1eb29afb0b5be4644ed522bf083acd3f`  
		Last Modified: Tue, 14 Jan 2025 23:31:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bfc86e47da2a329fa916e619f50b1572e090a406c11b35b6235548d8bc52ee`  
		Last Modified: Tue, 14 Jan 2025 23:31:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3634f4abc247a49927973cdf069a2717f0053ec34fae55d8f7014967864fb`  
		Last Modified: Tue, 14 Jan 2025 23:31:30 GMT  
		Size: 19.1 MB (19149523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36028f38b9d36c2624a31329c881064c7c9b02472ec1aecfb6924bd39ef2450`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0cfd1d3174eb2bbbce2d334d4fd0e90cdd7ca8747f146ef6da5a8cf8e937a3`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834b9a7619d4a8f64af8850acc540189ba984e6f829cde434c43eaa00ac13251`  
		Last Modified: Tue, 14 Jan 2025 23:31:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde3f31a6ef2d6c5cb116f4c7246bdcf8ed9a39ac3ea376b13832a9a90df8d63`  
		Last Modified: Tue, 14 Jan 2025 23:31:27 GMT  
		Size: 19.6 MB (19634023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7331fb5fa54eb509667e318fef4224b22e7267a8b01ab08320597309a61cc9`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41addc9937b80bc18e288c60f1f057cce9b501761a6c845a8a385dca9084663e`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752c051f71c979cefbe564869be494631945a5cd1aad02a5904c2715b12c51b0`  
		Last Modified: Tue, 14 Jan 2025 23:31:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dff165c12cf41f3471c535f13b2fefdaf7f686d0bc74b8372caf2d7dbb7a08f`  
		Last Modified: Tue, 14 Jan 2025 23:31:27 GMT  
		Size: 20.2 MB (20158014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
