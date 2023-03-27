## `docker:20-dind`

```console
$ docker pull docker@sha256:8d66608acd78f5c686b0364ecc2e4ba3abfe8b2cc1cd89bcc04ccac4c2dcf026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:ff435720b140a25fc2c320026cf9aaa0ce03bc88ef8810f02d5963ac7465a796
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111661536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac7ccac7fa711d43530ecc282bf6497abd5ff9d0f8fb392e0fcae63a9ba655b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Tue, 07 Mar 2023 19:40:30 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 07 Mar 2023 19:40:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Mon, 27 Mar 2023 22:23:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.2
# Mon, 27 Mar 2023 22:23:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-x86_64'; 			sha256='895e20812231543eae9f6b98ef9395327f4f21f1f31fa51fc252d21415802dda'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-armv6'; 			sha256='16a2ce7e9bc45cb864020fb61a4da7425162cb5215ee7c81c48f98b6a7c945c4'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-armv7'; 			sha256='4c8948696831fde2992e82dfcb505c5d6e4a56df9d759cd39a1dee6b6cded1c0'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-aarch64'; 			sha256='fcc2a21588907a7e6d9aa83538f134d2916f7a756cf391e5ce11b9d67bc4aad0'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-ppc64le'; 			sha256='546e0421cda6f0bbedd82efc2d95daf9775ec736ae0c82bcdc051c952eee09cd'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-riscv64'; 			sha256='65824b6aad564debb5ae9f70423f94bf5bbf20062fa4d9d47d2d2bcaf6a822b7'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-s390x'; 			sha256='4fcf6d847203162eb0a698657b98007542047c167188df3c65cca047b4b656c0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Mar 2023 22:23:35 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Mar 2023 22:23:35 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Mar 2023 22:23:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Mar 2023 22:23:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Mar 2023 22:23:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Mar 2023 22:23:36 GMT
CMD ["sh"]
# Mon, 27 Mar 2023 22:23:40 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 27 Mar 2023 22:23:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 27 Mar 2023 22:23:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Mon, 27 Mar 2023 22:23:45 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 27 Mar 2023 22:23:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 27 Mar 2023 22:23:46 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Mon, 27 Mar 2023 22:23:46 GMT
VOLUME [/var/lib/docker]
# Mon, 27 Mar 2023 22:23:46 GMT
EXPOSE 2375 2376
# Mon, 27 Mar 2023 22:23:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 27 Mar 2023 22:23:46 GMT
CMD []
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4927f75f31364ad04a4dc42dfc39fee8d641e4d89462d798a6af390b45daeff1`  
		Last Modified: Tue, 07 Mar 2023 19:43:08 GMT  
		Size: 16.0 MB (16001695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a113e01fff05ebe6cb2dfc010becf0c13771abd21c9e972d94d7787d76429e`  
		Last Modified: Mon, 27 Mar 2023 22:25:42 GMT  
		Size: 16.4 MB (16375135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d1dbef1a7beea6bde68ba6b2881045193ca8977b6cf87bcef9eaa7b56e3297`  
		Last Modified: Mon, 27 Mar 2023 22:25:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd233bdcf675bc100477c7eda72c0efe30bd76ab37907e1fa6c4c9b3339a99f`  
		Last Modified: Mon, 27 Mar 2023 22:25:39 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e9984e16c72651d2e0a02026dafc949e3641104c1d79758a612ad1605fd13f`  
		Last Modified: Mon, 27 Mar 2023 22:25:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207bf7bd3968af5a10f6a7eca580eaa7490e3e0d3d6ac949ea059ded1c457c52`  
		Last Modified: Mon, 27 Mar 2023 22:26:02 GMT  
		Size: 6.8 MB (6839095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e083bdff2c3cb5e54c6e2fc09eaf15b75f68f60f17ee6257d1f03f8a8539c84b`  
		Last Modified: Mon, 27 Mar 2023 22:26:01 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9ebdaaed271b9928fd55b219bd140d35da6904e07602a4c74caec594b3ad10`  
		Last Modified: Mon, 27 Mar 2023 22:26:09 GMT  
		Size: 53.0 MB (53016624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d92b7af34f6f354780dd8ee41f2b3544a72bebb90f1cea3ab13abb34cf1aeaf`  
		Last Modified: Mon, 27 Mar 2023 22:26:01 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5428e3481132734c3cdb80de2c5b17b0dcbde5a59e3fda0a4fbdd8da35f3c73d`  
		Last Modified: Mon, 27 Mar 2023 22:26:01 GMT  
		Size: 2.8 KB (2827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:af009f3a1dc2370d0c857914a6f734d7e6ed1de715adc2ea3ab48a12e52c22f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102992914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cdfc41d053e71b41af16f0327f5f464e8b22838e7f41e1bfd9bef1c65cbce2c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Tue, 07 Mar 2023 19:42:24 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 07 Mar 2023 19:42:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Mon, 27 Mar 2023 22:42:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.2
# Mon, 27 Mar 2023 22:42:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-x86_64'; 			sha256='895e20812231543eae9f6b98ef9395327f4f21f1f31fa51fc252d21415802dda'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-armv6'; 			sha256='16a2ce7e9bc45cb864020fb61a4da7425162cb5215ee7c81c48f98b6a7c945c4'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-armv7'; 			sha256='4c8948696831fde2992e82dfcb505c5d6e4a56df9d759cd39a1dee6b6cded1c0'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-aarch64'; 			sha256='fcc2a21588907a7e6d9aa83538f134d2916f7a756cf391e5ce11b9d67bc4aad0'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-ppc64le'; 			sha256='546e0421cda6f0bbedd82efc2d95daf9775ec736ae0c82bcdc051c952eee09cd'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-riscv64'; 			sha256='65824b6aad564debb5ae9f70423f94bf5bbf20062fa4d9d47d2d2bcaf6a822b7'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-s390x'; 			sha256='4fcf6d847203162eb0a698657b98007542047c167188df3c65cca047b4b656c0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Mar 2023 22:42:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Mar 2023 22:42:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Mar 2023 22:42:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Mar 2023 22:42:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Mar 2023 22:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Mar 2023 22:42:15 GMT
CMD ["sh"]
# Mon, 27 Mar 2023 22:42:20 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 27 Mar 2023 22:42:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 27 Mar 2023 22:42:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Mon, 27 Mar 2023 22:42:25 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 27 Mar 2023 22:42:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 27 Mar 2023 22:42:25 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Mon, 27 Mar 2023 22:42:25 GMT
VOLUME [/var/lib/docker]
# Mon, 27 Mar 2023 22:42:26 GMT
EXPOSE 2375 2376
# Mon, 27 Mar 2023 22:42:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 27 Mar 2023 22:42:26 GMT
CMD []
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0b5e8fb705e85176b3e83174bd85f70a7b1cb78f26717f945d058641c64572`  
		Last Modified: Tue, 07 Mar 2023 19:45:01 GMT  
		Size: 14.4 MB (14441448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e360a08db5514042e5c464d5f4bf36f3ef6858ec34875620823ba341ba17fad8`  
		Last Modified: Mon, 27 Mar 2023 22:44:13 GMT  
		Size: 14.8 MB (14830342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cc9b577bb7b3dd63e1c5afc5e7fdb163a2de17dc9d1b4b858ee42b080b2f81`  
		Last Modified: Mon, 27 Mar 2023 22:44:11 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6a9b3956214582fb93f5581da9dfa07a2356a9a190a53de4290e115c9e9c8c`  
		Last Modified: Mon, 27 Mar 2023 22:44:11 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b26bf6fb2770cba254711b3d69cf0dd7625a1ea0cdf4389c171c8d25c57d5f9`  
		Last Modified: Mon, 27 Mar 2023 22:44:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995d0e92df4dc8ed818f128bb433f20bc1c0e1344cc19383d9bf551b7f92be25`  
		Last Modified: Mon, 27 Mar 2023 22:44:33 GMT  
		Size: 7.0 MB (6992904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf34576ee307828784320347804cb27107562d3fbd364610cdad2c1d6755f506`  
		Last Modified: Mon, 27 Mar 2023 22:44:31 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8277d756bf44f759b97af987926e7a9b8fcc142f6421f09f757a5e52573fe7`  
		Last Modified: Mon, 27 Mar 2023 22:44:37 GMT  
		Size: 48.7 MB (48680430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31e2f4bac58ae3764c8688daf75b8b7ef94b60dbdd93793be133b3037611e6b`  
		Last Modified: Mon, 27 Mar 2023 22:44:32 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f3bc8491faec403c73e61ce1703095ba543a565cefcd1868e1f4b5642d7127`  
		Last Modified: Mon, 27 Mar 2023 22:44:32 GMT  
		Size: 2.8 KB (2825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
