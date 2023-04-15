## `docker:24-rc-git`

```console
$ docker pull docker@sha256:38c457a41587c990ce64f451534de91e39ab8cd351c2a3ff3143f6baf4dadffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:24-rc-git` - linux; amd64

```console
$ docker pull docker@sha256:d2db3fb2f6fbc3521673deebabd043a2fb61cca3bf3794c25dbba15d4ea1f7a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58349096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa1447af23164b8981ce9b07f5bea79c29ef69b99dfe820bcb4a6c98358c6cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Fri, 14 Apr 2023 17:04:36 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 14 Apr 2023 17:04:36 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Apr 2023 17:04:36 GMT
ENV DOCKER_VERSION=24.0.0-beta.2
# Fri, 14 Apr 2023 17:04:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-24.0.0-beta.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-24.0.0-beta.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-24.0.0-beta.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-24.0.0-beta.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Apr 2023 17:04:36 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Fri, 14 Apr 2023 17:04:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Apr 2023 17:04:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.2
# Fri, 14 Apr 2023 17:04:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-x86_64'; 			sha256='895e20812231543eae9f6b98ef9395327f4f21f1f31fa51fc252d21415802dda'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-armv6'; 			sha256='16a2ce7e9bc45cb864020fb61a4da7425162cb5215ee7c81c48f98b6a7c945c4'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-armv7'; 			sha256='4c8948696831fde2992e82dfcb505c5d6e4a56df9d759cd39a1dee6b6cded1c0'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-aarch64'; 			sha256='fcc2a21588907a7e6d9aa83538f134d2916f7a756cf391e5ce11b9d67bc4aad0'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-ppc64le'; 			sha256='546e0421cda6f0bbedd82efc2d95daf9775ec736ae0c82bcdc051c952eee09cd'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-riscv64'; 			sha256='65824b6aad564debb5ae9f70423f94bf5bbf20062fa4d9d47d2d2bcaf6a822b7'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-s390x'; 			sha256='4fcf6d847203162eb0a698657b98007542047c167188df3c65cca047b4b656c0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Apr 2023 17:04:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Apr 2023 17:04:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Apr 2023 17:04:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Apr 2023 17:04:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Apr 2023 17:04:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Apr 2023 17:04:36 GMT
CMD ["sh"]
# Fri, 14 Apr 2023 17:04:36 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed9ddfd3b8fa49957c18f14a975161f97db10d02990506ab064fef3cd9f06e4`  
		Last Modified: Wed, 29 Mar 2023 18:45:22 GMT  
		Size: 2.1 MB (2063911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788e1ab5616a5765a2b424b3d6f91c26256c1713671000168eee6474fbdeeece`  
		Last Modified: Wed, 29 Mar 2023 18:45:21 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80aff966a25579500dda24ff2db8a52e0b79ff0684ffa639de4852bf43f93dde`  
		Last Modified: Sat, 15 Apr 2023 00:22:10 GMT  
		Size: 16.4 MB (16378264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f9333232b4d54559a107ec7906e8ad105f8b94be454e2be3f028430d300a09`  
		Last Modified: Sat, 15 Apr 2023 00:22:10 GMT  
		Size: 16.0 MB (16001759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9177e01d3b14896cd1429a04736e999e81c84dd0ba5ddcb5e720e21e58bdfb98`  
		Last Modified: Sat, 15 Apr 2023 00:22:10 GMT  
		Size: 16.4 MB (16375108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4efc94832dc4a85c9d41b14135a32ed917fc0f6bde75a2125eb7bd77a482517`  
		Last Modified: Sat, 15 Apr 2023 00:22:07 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0e9023da5192148dc9bf48e8ef3dac9ed65e069698a05331845290f4a5cfbe`  
		Last Modified: Sat, 15 Apr 2023 00:22:07 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950c91304c63e14961fc56081a507280a8e45b8f1a9f52271eec73d188206841`  
		Last Modified: Sat, 15 Apr 2023 00:22:07 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a6716a543007e85aac8961df6bbd7eb48cf896bfabe8cb8450a1d8c6a7c458`  
		Last Modified: Sat, 15 Apr 2023 00:23:14 GMT  
		Size: 4.2 MB (4153667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24-rc-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ff0aa5c05c129923609437178d769f93ea0bd1bb75b1584c4308b6735f73748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54182241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a21c718499cdce9189b77d6380f10faa069d74df8b349ffc6af9bf7badb384f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:18 GMT
ADD file:e51d4089e73ad6dee52b31f0c8059a00c17df6e23f6741fe11b43bd84cc99008 in / 
# Wed, 29 Mar 2023 17:39:18 GMT
CMD ["/bin/sh"]
# Fri, 14 Apr 2023 17:04:36 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 14 Apr 2023 17:04:36 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Apr 2023 17:04:36 GMT
ENV DOCKER_VERSION=24.0.0-beta.2
# Fri, 14 Apr 2023 17:04:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-24.0.0-beta.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-24.0.0-beta.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-24.0.0-beta.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-24.0.0-beta.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Apr 2023 17:04:36 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Fri, 14 Apr 2023 17:04:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Apr 2023 17:04:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.2
# Fri, 14 Apr 2023 17:04:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-x86_64'; 			sha256='895e20812231543eae9f6b98ef9395327f4f21f1f31fa51fc252d21415802dda'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-armv6'; 			sha256='16a2ce7e9bc45cb864020fb61a4da7425162cb5215ee7c81c48f98b6a7c945c4'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-armv7'; 			sha256='4c8948696831fde2992e82dfcb505c5d6e4a56df9d759cd39a1dee6b6cded1c0'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-aarch64'; 			sha256='fcc2a21588907a7e6d9aa83538f134d2916f7a756cf391e5ce11b9d67bc4aad0'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-ppc64le'; 			sha256='546e0421cda6f0bbedd82efc2d95daf9775ec736ae0c82bcdc051c952eee09cd'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-riscv64'; 			sha256='65824b6aad564debb5ae9f70423f94bf5bbf20062fa4d9d47d2d2bcaf6a822b7'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-s390x'; 			sha256='4fcf6d847203162eb0a698657b98007542047c167188df3c65cca047b4b656c0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Apr 2023 17:04:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Apr 2023 17:04:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Apr 2023 17:04:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Apr 2023 17:04:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Apr 2023 17:04:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Apr 2023 17:04:36 GMT
CMD ["sh"]
# Fri, 14 Apr 2023 17:04:36 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:c41833b44d910632b415cd89a9cdaa4d62c9725dc56c99a7ddadafd6719960f9`  
		Last Modified: Wed, 29 Mar 2023 17:39:44 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6343a5c1782164b247a48071eacb0a74cd75c4c98cac780bb97fad9418a29b7d`  
		Last Modified: Thu, 30 Mar 2023 05:48:09 GMT  
		Size: 2.0 MB (2036542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb3fc37985f8c4b7d19deedc94fa0ae9a2dc0d4eb4d0fa64f081da502505fd9`  
		Last Modified: Thu, 30 Mar 2023 05:48:08 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4caa46b127228c48e02e8afe59d68505ca6ee611eb12d0e8b6001c00b2b3374f`  
		Last Modified: Sat, 15 Apr 2023 00:41:33 GMT  
		Size: 15.4 MB (15414634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1af90fe0f3f3426ab1d135c8af9b555943603a9c91a7056a0ed6b8bed06a4c`  
		Last Modified: Sat, 15 Apr 2023 00:41:31 GMT  
		Size: 14.4 MB (14441525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5333df8b4b425fdb18ee31d31994dcb49236880eb5c75b4529a7142a368a220e`  
		Last Modified: Sat, 15 Apr 2023 00:41:31 GMT  
		Size: 14.8 MB (14830399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a9c1692aac44b2cbf9d16e755939556207b8e9b708561360b954f4eefaa920`  
		Last Modified: Sat, 15 Apr 2023 00:41:30 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08def7479b5f9efb5f8d5099f07dfbd001725296a762d61aaf1cd781aee0e2f9`  
		Last Modified: Sat, 15 Apr 2023 00:41:29 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e998bd5b284ea227104e5c1f8651613b5e702c1f566832d9edbf4d5305c7b6`  
		Last Modified: Sat, 15 Apr 2023 00:41:29 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc994581a2c73eee2181bb90ffc0ff2efd4f0a935ad7a6c674b9dc4f40bb64f`  
		Last Modified: Sat, 15 Apr 2023 00:42:27 GMT  
		Size: 4.2 MB (4195462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
