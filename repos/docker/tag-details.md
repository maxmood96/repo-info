<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:23`](#docker23)
-	[`docker:23-cli`](#docker23-cli)
-	[`docker:23-dind`](#docker23-dind)
-	[`docker:23-dind-rootless`](#docker23-dind-rootless)
-	[`docker:23-git`](#docker23-git)
-	[`docker:23-windowsservercore`](#docker23-windowsservercore)
-	[`docker:23-windowsservercore-1809`](#docker23-windowsservercore-1809)
-	[`docker:23-windowsservercore-ltsc2022`](#docker23-windowsservercore-ltsc2022)
-	[`docker:23.0`](#docker230)
-	[`docker:23.0-cli`](#docker230-cli)
-	[`docker:23.0-dind`](#docker230-dind)
-	[`docker:23.0-dind-rootless`](#docker230-dind-rootless)
-	[`docker:23.0-git`](#docker230-git)
-	[`docker:23.0-windowsservercore`](#docker230-windowsservercore)
-	[`docker:23.0-windowsservercore-1809`](#docker230-windowsservercore-1809)
-	[`docker:23.0-windowsservercore-ltsc2022`](#docker230-windowsservercore-ltsc2022)
-	[`docker:23.0.6`](#docker2306)
-	[`docker:23.0.6-alpine3.18`](#docker2306-alpine318)
-	[`docker:23.0.6-cli`](#docker2306-cli)
-	[`docker:23.0.6-cli-alpine3.18`](#docker2306-cli-alpine318)
-	[`docker:23.0.6-dind`](#docker2306-dind)
-	[`docker:23.0.6-dind-alpine3.18`](#docker2306-dind-alpine318)
-	[`docker:23.0.6-dind-rootless`](#docker2306-dind-rootless)
-	[`docker:23.0.6-git`](#docker2306-git)
-	[`docker:23.0.6-windowsservercore`](#docker2306-windowsservercore)
-	[`docker:23.0.6-windowsservercore-1809`](#docker2306-windowsservercore-1809)
-	[`docker:23.0.6-windowsservercore-ltsc2022`](#docker2306-windowsservercore-ltsc2022)
-	[`docker:24`](#docker24)
-	[`docker:24-cli`](#docker24-cli)
-	[`docker:24-dind`](#docker24-dind)
-	[`docker:24-dind-rootless`](#docker24-dind-rootless)
-	[`docker:24-git`](#docker24-git)
-	[`docker:24-windowsservercore`](#docker24-windowsservercore)
-	[`docker:24-windowsservercore-1809`](#docker24-windowsservercore-1809)
-	[`docker:24-windowsservercore-ltsc2022`](#docker24-windowsservercore-ltsc2022)
-	[`docker:24.0`](#docker240)
-	[`docker:24.0-cli`](#docker240-cli)
-	[`docker:24.0-dind`](#docker240-dind)
-	[`docker:24.0-dind-rootless`](#docker240-dind-rootless)
-	[`docker:24.0-git`](#docker240-git)
-	[`docker:24.0-windowsservercore`](#docker240-windowsservercore)
-	[`docker:24.0-windowsservercore-1809`](#docker240-windowsservercore-1809)
-	[`docker:24.0-windowsservercore-ltsc2022`](#docker240-windowsservercore-ltsc2022)
-	[`docker:24.0.0`](#docker2400)
-	[`docker:24.0.0-alpine3.18`](#docker2400-alpine318)
-	[`docker:24.0.0-cli`](#docker2400-cli)
-	[`docker:24.0.0-cli-alpine3.18`](#docker2400-cli-alpine318)
-	[`docker:24.0.0-dind`](#docker2400-dind)
-	[`docker:24.0.0-dind-alpine3.18`](#docker2400-dind-alpine318)
-	[`docker:24.0.0-dind-rootless`](#docker2400-dind-rootless)
-	[`docker:24.0.0-git`](#docker2400-git)
-	[`docker:24.0.0-windowsservercore`](#docker2400-windowsservercore)
-	[`docker:24.0.0-windowsservercore-1809`](#docker2400-windowsservercore-1809)
-	[`docker:24.0.0-windowsservercore-ltsc2022`](#docker2400-windowsservercore-ltsc2022)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:git`](#dockergit)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)

## `docker:23`

```console
$ docker pull docker@sha256:d8dfdb733748109806968a94095412310232988a20046ea57fb6d68ccd94036a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23` - linux; amd64

```console
$ docker pull docker@sha256:af8a4eb8e61f87ea50c72057624c1710dd0c6356d74e64465bc01123c7d37795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112738963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4966f34e6de695acc18297ea9b1c513a58c4048554aaaac4f10bf6080be3b32`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 15 May 2023 22:39:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/var/lib/docker]
# Mon, 15 May 2023 22:39:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 15 May 2023 22:39:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 15 May 2023 22:39:50 GMT
CMD []
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058b1c95dcd434f93391bf0ec0c404ae630b363de88563fa9a4a4d3c6889b90`  
		Last Modified: Thu, 11 May 2023 19:25:14 GMT  
		Size: 7.0 MB (7025224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1c4c35af9e9b29cde02d3d5b488ed71b7821d39319354f4aba1a8ae8ace24`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d938c8b2399339aaf8caeefbdc85c8b8dddf7d27d57d8c3d09bf070e0a4374b`  
		Last Modified: Thu, 11 May 2023 19:25:20 GMT  
		Size: 51.7 MB (51657452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2885b54919758712d2ab1b9d1e43574e5fa8d8fe06612e193c876de7d221ea`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3ce26085aa03b6fc712003b8cd4e3675c6975181aca50368e8af84866d7b9e`  
		Last Modified: Tue, 16 May 2023 00:21:06 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6df96d5cb64ef8f5cea2f45a415c388301f852b3cf8ea2d52e085139b6096031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104300688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c967226c69d0fa470b803590a3db4f0d47ca48f4691259861dc5f16904036d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755db036d15ac84998f2eac830ac44d7e439c03ecb38bd242508a0481efc0fc`  
		Last Modified: Thu, 11 May 2023 19:43:32 GMT  
		Size: 15.3 MB (15325101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f85b23db6b3d2bdbfb74d5012a03f03cb9ef9ff1e86bc625be7fd7367750a`  
		Last Modified: Thu, 11 May 2023 19:43:31 GMT  
		Size: 14.4 MB (14441512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c2aaa7ad28f7b2dbb51676ad9d28a8dd94a62c33b7b67360abbdd877825a6`  
		Last Modified: Wed, 17 May 2023 00:05:19 GMT  
		Size: 14.9 MB (14861209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f732bb283cf7f3f4629f8f8fe627fe87c1a816e6b18fb43a474e9a0488ecfb`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef0fa04d98283db2caaecb633a590ebb724d80881afd74ab3a7a0cd65c868c9`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f747c1b4bde6324e1f2a1a5bd574a10060714e43ddb674da4c8c63e6bd817`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18139dccdfd465a21cc50f7973a2aab999e1ea3ce051cac86e9bd41527b53d`  
		Last Modified: Wed, 17 May 2023 00:05:32 GMT  
		Size: 7.2 MB (7245090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c86802d31a079a23a88f2dde8479a6832603e3e1fb4f09cf4b5d99d98fb481`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f890bcd554f3ab2798ec63eea6dae3a81e80b49ebad80afab0ff62f5dafd617`  
		Last Modified: Wed, 17 May 2023 00:05:36 GMT  
		Size: 47.1 MB (47053390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3de5c6d78526ef5a60d99f63b7459b261ef8ce726a8a4e5d04e2a7b6d3c3205`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8e069943ade3caee551dd7560eeb5ea0bfe3688bd6755994395c23b78c4b1a`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 2.8 KB (2795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-cli`

```console
$ docker pull docker@sha256:f76e77bbeba3e7c53693d557c22488ddc7e77664e6e20325c2a37b1d59ef77a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23-cli` - linux; amd64

```console
$ docker pull docker@sha256:3b2d99643c86bfd09e5c2ae0c610a7820b755d71d270949f0b1e7e7ff9836ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54051122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ea5edbac8ee1fa4488a13fcf136fa3eeaff8c92b78ce78993f60a07967de99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:572ed66d449f4425cdac72cf5c26f85bd7d8220b27fddb2f77cba7a50836aa28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49997039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697bbcd3ead6712b704071f9f133f8afffa6bd65db86d186fa601607e3221aa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755db036d15ac84998f2eac830ac44d7e439c03ecb38bd242508a0481efc0fc`  
		Last Modified: Thu, 11 May 2023 19:43:32 GMT  
		Size: 15.3 MB (15325101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f85b23db6b3d2bdbfb74d5012a03f03cb9ef9ff1e86bc625be7fd7367750a`  
		Last Modified: Thu, 11 May 2023 19:43:31 GMT  
		Size: 14.4 MB (14441512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c2aaa7ad28f7b2dbb51676ad9d28a8dd94a62c33b7b67360abbdd877825a6`  
		Last Modified: Wed, 17 May 2023 00:05:19 GMT  
		Size: 14.9 MB (14861209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f732bb283cf7f3f4629f8f8fe627fe87c1a816e6b18fb43a474e9a0488ecfb`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef0fa04d98283db2caaecb633a590ebb724d80881afd74ab3a7a0cd65c868c9`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f747c1b4bde6324e1f2a1a5bd574a10060714e43ddb674da4c8c63e6bd817`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-dind`

```console
$ docker pull docker@sha256:d8dfdb733748109806968a94095412310232988a20046ea57fb6d68ccd94036a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23-dind` - linux; amd64

```console
$ docker pull docker@sha256:af8a4eb8e61f87ea50c72057624c1710dd0c6356d74e64465bc01123c7d37795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112738963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4966f34e6de695acc18297ea9b1c513a58c4048554aaaac4f10bf6080be3b32`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 15 May 2023 22:39:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/var/lib/docker]
# Mon, 15 May 2023 22:39:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 15 May 2023 22:39:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 15 May 2023 22:39:50 GMT
CMD []
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058b1c95dcd434f93391bf0ec0c404ae630b363de88563fa9a4a4d3c6889b90`  
		Last Modified: Thu, 11 May 2023 19:25:14 GMT  
		Size: 7.0 MB (7025224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1c4c35af9e9b29cde02d3d5b488ed71b7821d39319354f4aba1a8ae8ace24`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d938c8b2399339aaf8caeefbdc85c8b8dddf7d27d57d8c3d09bf070e0a4374b`  
		Last Modified: Thu, 11 May 2023 19:25:20 GMT  
		Size: 51.7 MB (51657452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2885b54919758712d2ab1b9d1e43574e5fa8d8fe06612e193c876de7d221ea`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3ce26085aa03b6fc712003b8cd4e3675c6975181aca50368e8af84866d7b9e`  
		Last Modified: Tue, 16 May 2023 00:21:06 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6df96d5cb64ef8f5cea2f45a415c388301f852b3cf8ea2d52e085139b6096031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104300688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c967226c69d0fa470b803590a3db4f0d47ca48f4691259861dc5f16904036d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755db036d15ac84998f2eac830ac44d7e439c03ecb38bd242508a0481efc0fc`  
		Last Modified: Thu, 11 May 2023 19:43:32 GMT  
		Size: 15.3 MB (15325101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f85b23db6b3d2bdbfb74d5012a03f03cb9ef9ff1e86bc625be7fd7367750a`  
		Last Modified: Thu, 11 May 2023 19:43:31 GMT  
		Size: 14.4 MB (14441512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c2aaa7ad28f7b2dbb51676ad9d28a8dd94a62c33b7b67360abbdd877825a6`  
		Last Modified: Wed, 17 May 2023 00:05:19 GMT  
		Size: 14.9 MB (14861209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f732bb283cf7f3f4629f8f8fe627fe87c1a816e6b18fb43a474e9a0488ecfb`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef0fa04d98283db2caaecb633a590ebb724d80881afd74ab3a7a0cd65c868c9`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f747c1b4bde6324e1f2a1a5bd574a10060714e43ddb674da4c8c63e6bd817`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18139dccdfd465a21cc50f7973a2aab999e1ea3ce051cac86e9bd41527b53d`  
		Last Modified: Wed, 17 May 2023 00:05:32 GMT  
		Size: 7.2 MB (7245090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c86802d31a079a23a88f2dde8479a6832603e3e1fb4f09cf4b5d99d98fb481`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f890bcd554f3ab2798ec63eea6dae3a81e80b49ebad80afab0ff62f5dafd617`  
		Last Modified: Wed, 17 May 2023 00:05:36 GMT  
		Size: 47.1 MB (47053390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3de5c6d78526ef5a60d99f63b7459b261ef8ce726a8a4e5d04e2a7b6d3c3205`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8e069943ade3caee551dd7560eeb5ea0bfe3688bd6755994395c23b78c4b1a`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 2.8 KB (2795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-dind-rootless`

```console
$ docker pull docker@sha256:26f0725b027bea7e699c27b411548d2e11560543d03b4301de24cac12f9372db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:3d5b0a0a81a2b8770652468b38847721050af219e94c5711a9a7bc8e8cdc1333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134450185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272062036ead322e794888251164e54b81a1f64cba944eda4f84db8d820accae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 15 May 2023 22:39:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/var/lib/docker]
# Mon, 15 May 2023 22:39:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 15 May 2023 22:39:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 15 May 2023 22:39:50 GMT
CMD []
# Mon, 15 May 2023 22:39:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 15 May 2023 22:39:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058b1c95dcd434f93391bf0ec0c404ae630b363de88563fa9a4a4d3c6889b90`  
		Last Modified: Thu, 11 May 2023 19:25:14 GMT  
		Size: 7.0 MB (7025224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1c4c35af9e9b29cde02d3d5b488ed71b7821d39319354f4aba1a8ae8ace24`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d938c8b2399339aaf8caeefbdc85c8b8dddf7d27d57d8c3d09bf070e0a4374b`  
		Last Modified: Thu, 11 May 2023 19:25:20 GMT  
		Size: 51.7 MB (51657452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2885b54919758712d2ab1b9d1e43574e5fa8d8fe06612e193c876de7d221ea`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3ce26085aa03b6fc712003b8cd4e3675c6975181aca50368e8af84866d7b9e`  
		Last Modified: Tue, 16 May 2023 00:21:06 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98ac734fba950213b5eef3e34a74cfb050771d2dcfb9e09bf8849e430a97171`  
		Last Modified: Tue, 16 May 2023 00:21:32 GMT  
		Size: 1.4 MB (1362380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a2dc52b58512c04b6f21d9013089f46e944d25ee401bf249410fbfee0a386a`  
		Last Modified: Tue, 16 May 2023 00:21:32 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d714531a153f83a639d0577eb97fbabde8a658d045e1a5934d0fdd66e1647e`  
		Last Modified: Tue, 16 May 2023 00:21:32 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d363f0101be8e2f3cf083449298d611caf75351c46d338317982af0bac53317e`  
		Last Modified: Tue, 16 May 2023 00:21:35 GMT  
		Size: 20.3 MB (20347094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9fecae1fab5b25b43bb2d749c2266c981b255b6ab3505f483a58c208da98e4e`  
		Last Modified: Tue, 16 May 2023 00:21:32 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b1c63d3c2d46ccf56935ea78e081c6961e8aff55b19f67b649b290a8f74b7cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127956751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:529cab109e8578d5364ffa8c1460b6f14313ad7cfcd5fd20af761767ca17c53b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 16 May 2023 17:59:38 GMT
USER rootless
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755db036d15ac84998f2eac830ac44d7e439c03ecb38bd242508a0481efc0fc`  
		Last Modified: Thu, 11 May 2023 19:43:32 GMT  
		Size: 15.3 MB (15325101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f85b23db6b3d2bdbfb74d5012a03f03cb9ef9ff1e86bc625be7fd7367750a`  
		Last Modified: Thu, 11 May 2023 19:43:31 GMT  
		Size: 14.4 MB (14441512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c2aaa7ad28f7b2dbb51676ad9d28a8dd94a62c33b7b67360abbdd877825a6`  
		Last Modified: Wed, 17 May 2023 00:05:19 GMT  
		Size: 14.9 MB (14861209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f732bb283cf7f3f4629f8f8fe627fe87c1a816e6b18fb43a474e9a0488ecfb`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef0fa04d98283db2caaecb633a590ebb724d80881afd74ab3a7a0cd65c868c9`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f747c1b4bde6324e1f2a1a5bd574a10060714e43ddb674da4c8c63e6bd817`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18139dccdfd465a21cc50f7973a2aab999e1ea3ce051cac86e9bd41527b53d`  
		Last Modified: Wed, 17 May 2023 00:05:32 GMT  
		Size: 7.2 MB (7245090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c86802d31a079a23a88f2dde8479a6832603e3e1fb4f09cf4b5d99d98fb481`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f890bcd554f3ab2798ec63eea6dae3a81e80b49ebad80afab0ff62f5dafd617`  
		Last Modified: Wed, 17 May 2023 00:05:36 GMT  
		Size: 47.1 MB (47053390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3de5c6d78526ef5a60d99f63b7459b261ef8ce726a8a4e5d04e2a7b6d3c3205`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8e069943ade3caee551dd7560eeb5ea0bfe3688bd6755994395c23b78c4b1a`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 2.8 KB (2795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f403fc6a76be877efebea34e9697fa8940f81bd7930562034d51cbbb16ee7836`  
		Last Modified: Wed, 17 May 2023 00:05:59 GMT  
		Size: 1.4 MB (1413346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d638bdef2674041ed5d4d4540aaf98cc1778c9b56db593a6d62d2f68d16c6dba`  
		Last Modified: Wed, 17 May 2023 00:05:58 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e827686ffa7ac4e0f2de8bf334fc2657f11eb7205ba4c8646b9b1c58e812da`  
		Last Modified: Wed, 17 May 2023 00:05:58 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77316858144b4c941955823a315a78cb335fc7fc0bab38f0bfe28fac673029ad`  
		Last Modified: Wed, 17 May 2023 00:06:03 GMT  
		Size: 22.2 MB (22240980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff39cfa386a5ac16b38135820005cf8ac5d291d71b2078ae17079ecf2eb3fc30`  
		Last Modified: Wed, 17 May 2023 00:05:58 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-git`

```console
$ docker pull docker@sha256:336d51df0ca7e0094a5bc3b72ddaf5ff68f9430e1b511eec7cc82193b6ecfd3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23-git` - linux; amd64

```console
$ docker pull docker@sha256:e0a9ff309d9d4d49f145163565cf50106de9bb15023321d9f6027da8243fba86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117658830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd2153f16eee41cf91fc1f892e613b7acfd0411a50ed24492a54719464d87a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 15 May 2023 22:39:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/var/lib/docker]
# Mon, 15 May 2023 22:39:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 15 May 2023 22:39:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 15 May 2023 22:39:50 GMT
CMD []
# Mon, 15 May 2023 22:39:50 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058b1c95dcd434f93391bf0ec0c404ae630b363de88563fa9a4a4d3c6889b90`  
		Last Modified: Thu, 11 May 2023 19:25:14 GMT  
		Size: 7.0 MB (7025224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1c4c35af9e9b29cde02d3d5b488ed71b7821d39319354f4aba1a8ae8ace24`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d938c8b2399339aaf8caeefbdc85c8b8dddf7d27d57d8c3d09bf070e0a4374b`  
		Last Modified: Thu, 11 May 2023 19:25:20 GMT  
		Size: 51.7 MB (51657452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2885b54919758712d2ab1b9d1e43574e5fa8d8fe06612e193c876de7d221ea`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3ce26085aa03b6fc712003b8cd4e3675c6975181aca50368e8af84866d7b9e`  
		Last Modified: Tue, 16 May 2023 00:21:06 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0eaf8da2ec7a0ad445e808e182a80a080ca992008cce921c5013474d44087e`  
		Last Modified: Tue, 16 May 2023 00:21:51 GMT  
		Size: 4.9 MB (4919867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7960c408821f0ae78825fa1d16ae3c624e622043f6bd22886009b376fc9875af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109312273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d556ee0123586a92b57931a25dfa7f48300f769681dfcd14f6bf84633a9e4092`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755db036d15ac84998f2eac830ac44d7e439c03ecb38bd242508a0481efc0fc`  
		Last Modified: Thu, 11 May 2023 19:43:32 GMT  
		Size: 15.3 MB (15325101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f85b23db6b3d2bdbfb74d5012a03f03cb9ef9ff1e86bc625be7fd7367750a`  
		Last Modified: Thu, 11 May 2023 19:43:31 GMT  
		Size: 14.4 MB (14441512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c2aaa7ad28f7b2dbb51676ad9d28a8dd94a62c33b7b67360abbdd877825a6`  
		Last Modified: Wed, 17 May 2023 00:05:19 GMT  
		Size: 14.9 MB (14861209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f732bb283cf7f3f4629f8f8fe627fe87c1a816e6b18fb43a474e9a0488ecfb`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef0fa04d98283db2caaecb633a590ebb724d80881afd74ab3a7a0cd65c868c9`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f747c1b4bde6324e1f2a1a5bd574a10060714e43ddb674da4c8c63e6bd817`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18139dccdfd465a21cc50f7973a2aab999e1ea3ce051cac86e9bd41527b53d`  
		Last Modified: Wed, 17 May 2023 00:05:32 GMT  
		Size: 7.2 MB (7245090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c86802d31a079a23a88f2dde8479a6832603e3e1fb4f09cf4b5d99d98fb481`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f890bcd554f3ab2798ec63eea6dae3a81e80b49ebad80afab0ff62f5dafd617`  
		Last Modified: Wed, 17 May 2023 00:05:36 GMT  
		Size: 47.1 MB (47053390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3de5c6d78526ef5a60d99f63b7459b261ef8ce726a8a4e5d04e2a7b6d3c3205`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8e069943ade3caee551dd7560eeb5ea0bfe3688bd6755994395c23b78c4b1a`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 2.8 KB (2795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ea70a033aec128fc750a0d6d759753695ba4227b1e7f769d29c65e44121ed2`  
		Last Modified: Wed, 17 May 2023 00:06:15 GMT  
		Size: 5.0 MB (5011585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-windowsservercore`

```console
$ docker pull docker@sha256:5ece48bf73b8c468e9da42e73104a47deb073ce38dff0342c64b8d5fd1c1aac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1726; amd64
	-	windows version 10.0.17763.4377; amd64

### `docker:23-windowsservercore` - windows version 10.0.20348.1726; amd64

```console
$ docker pull docker@sha256:49feec5ed8108d054e24262a0263775b0dea7ea6161420279ead5035f8f7ca2a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1826042174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb39d95d7392898fc2a92fe045c7948e23bac13e88a2771b9628a6fcd00df72`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:13:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 May 2023 03:24:47 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 03:24:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Wed, 10 May 2023 03:25:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:25:32 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 03:25:32 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 10 May 2023 03:25:33 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 10 May 2023 03:25:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:25:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 03:25:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-windows-x86_64.exe
# Wed, 10 May 2023 03:25:59 GMT
ENV DOCKER_COMPOSE_SHA256=556cc1d373503a897ecc2def998a40b2ad1fe27ff049769eb912c7e208772e74
# Wed, 10 May 2023 03:26:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d178a10e123ab9f41a66d7e6d8ffca4aab5fba57cf381f48bc0090f603be2d5`  
		Last Modified: Wed, 10 May 2023 01:45:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94bc80e6c1e6606bc432e9fa1ebc3ed83fe3ceb5a176e0a7b2c8334bf863c53`  
		Last Modified: Wed, 10 May 2023 07:11:29 GMT  
		Size: 446.9 KB (446946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e927fbd88402bacc902c2a4593f281068b2a6657c7f8b4e53ac01f8e636901`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165e88795de1230f78ac3b0186a534bd16fad90474fddb00254443f5440c8c65`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438806a743132696d59ff6500d80c1c45b0742da1613dbde135436ef14f725af`  
		Last Modified: Wed, 10 May 2023 07:12:05 GMT  
		Size: 17.3 MB (17316446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c96495f4df59195a31aba0ef651c79d5519baf34e22333d63d5a8bfe03900b`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f5f979d4f16ed05773444607ec525a26e8c703f03f102d8759e864981d5c82`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d23d10667208a1b8d0f8e33582643dd1c513834082f55a73336deecf2b3e829`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f367dbae07d50a7ea9664467f0f6935dd7ba395cf98c8f7d2e39925ff3f64e`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 16.5 MB (16457754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2158efcafa6303ace2a8d3f0d2442bddd73799341b2a6258c21abd8bd7fcac`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4a3d8cbc64bd1d463e94f091e7177ec22f9f28eb318370cdb0506d93494666`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca474991c2a553554d33df3995317383bfa4ec8b4f4249b931de5a485a27adc`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b95097e5ada96414856478813a948262a40d9c84537402939e98cd82036573`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 16.8 MB (16826864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23-windowsservercore` - windows version 10.0.17763.4377; amd64

```console
$ docker pull docker@sha256:ce1be907c58a74261c54ae870470d5c36ef2f63674c4e4cf8372e83777330ac4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2123136881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136da637bc1dc002acdb31b90bd13bb45820f2e95343006a0e97d66e2e39037b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:16:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 May 2023 03:26:29 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 03:26:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Wed, 10 May 2023 03:27:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:27:42 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 03:27:43 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 10 May 2023 03:27:43 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 10 May 2023 03:28:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:28:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 03:28:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-windows-x86_64.exe
# Wed, 10 May 2023 03:28:55 GMT
ENV DOCKER_COMPOSE_SHA256=556cc1d373503a897ecc2def998a40b2ad1fe27ff049769eb912c7e208772e74
# Wed, 10 May 2023 03:30:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5869a0b27170ed378e5d22763ab388eaf4a9dbd91cb7eaee4cef7d8639a2ff74`  
		Last Modified: Wed, 10 May 2023 07:11:47 GMT  
		Size: 451.5 KB (451506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470efce6095b6077dfd4d6bac6f6e2010f4d5bcdf636e954d0c3e9051baa7a30`  
		Last Modified: Wed, 10 May 2023 07:12:22 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf94d195dbf8bcb75f6433208dda2b0af64c556bf5eed006468d61cccf49971`  
		Last Modified: Wed, 10 May 2023 07:12:22 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f57c72aed2637dc5fc359ff575642812168a390b96d73791c2e00a8aa6c341`  
		Last Modified: Wed, 10 May 2023 07:12:25 GMT  
		Size: 17.3 MB (17330027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3802307c89ea480234035e4a743bf5fcb7af504addfaeeccdae1e83d0286ea03`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf5c7bff562bb1a033d8a2f465437525a829a56113ca6204efed01ecd6ba653`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6608073b14838ddabd4f13d2848b33488d2a7e42d3646245fc6f163e333e551`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412458425ced3171f449f28b8c40912d57931270d9d427efe39dfc669c81baa1`  
		Last Modified: Wed, 10 May 2023 07:12:23 GMT  
		Size: 16.5 MB (16467670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef29bfe39940055963010676df5645f3c05482f819eb0a729b16d43c7bc3af8`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ee6d41023794ee61421888956d914f83fedaedc16321d0aa3d0ac7e1315c25`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adecc2295964edd8cc0fd6feb81e6c3d28e20be1318d1b70c52acac1651a769b`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8302c4a8fb9f7dfb47a9992223517957000b185668adcb36a0e3f24b913406`  
		Last Modified: Wed, 10 May 2023 07:12:23 GMT  
		Size: 16.8 MB (16839833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-windowsservercore-1809`

```console
$ docker pull docker@sha256:3ae378fb4bac1f8f4fd2f950e2e961da4eeec2fa1c4e07394c2d81e3401b4d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `docker:23-windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull docker@sha256:ce1be907c58a74261c54ae870470d5c36ef2f63674c4e4cf8372e83777330ac4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2123136881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136da637bc1dc002acdb31b90bd13bb45820f2e95343006a0e97d66e2e39037b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:16:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 May 2023 03:26:29 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 03:26:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Wed, 10 May 2023 03:27:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:27:42 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 03:27:43 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 10 May 2023 03:27:43 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 10 May 2023 03:28:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:28:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 03:28:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-windows-x86_64.exe
# Wed, 10 May 2023 03:28:55 GMT
ENV DOCKER_COMPOSE_SHA256=556cc1d373503a897ecc2def998a40b2ad1fe27ff049769eb912c7e208772e74
# Wed, 10 May 2023 03:30:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5869a0b27170ed378e5d22763ab388eaf4a9dbd91cb7eaee4cef7d8639a2ff74`  
		Last Modified: Wed, 10 May 2023 07:11:47 GMT  
		Size: 451.5 KB (451506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470efce6095b6077dfd4d6bac6f6e2010f4d5bcdf636e954d0c3e9051baa7a30`  
		Last Modified: Wed, 10 May 2023 07:12:22 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf94d195dbf8bcb75f6433208dda2b0af64c556bf5eed006468d61cccf49971`  
		Last Modified: Wed, 10 May 2023 07:12:22 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f57c72aed2637dc5fc359ff575642812168a390b96d73791c2e00a8aa6c341`  
		Last Modified: Wed, 10 May 2023 07:12:25 GMT  
		Size: 17.3 MB (17330027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3802307c89ea480234035e4a743bf5fcb7af504addfaeeccdae1e83d0286ea03`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf5c7bff562bb1a033d8a2f465437525a829a56113ca6204efed01ecd6ba653`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6608073b14838ddabd4f13d2848b33488d2a7e42d3646245fc6f163e333e551`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412458425ced3171f449f28b8c40912d57931270d9d427efe39dfc669c81baa1`  
		Last Modified: Wed, 10 May 2023 07:12:23 GMT  
		Size: 16.5 MB (16467670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef29bfe39940055963010676df5645f3c05482f819eb0a729b16d43c7bc3af8`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ee6d41023794ee61421888956d914f83fedaedc16321d0aa3d0ac7e1315c25`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adecc2295964edd8cc0fd6feb81e6c3d28e20be1318d1b70c52acac1651a769b`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8302c4a8fb9f7dfb47a9992223517957000b185668adcb36a0e3f24b913406`  
		Last Modified: Wed, 10 May 2023 07:12:23 GMT  
		Size: 16.8 MB (16839833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:146958020dbeb7898c0db7c57aa5753ac981d68e700983b0d2ce745f9438aa6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1726; amd64

### `docker:23-windowsservercore-ltsc2022` - windows version 10.0.20348.1726; amd64

```console
$ docker pull docker@sha256:49feec5ed8108d054e24262a0263775b0dea7ea6161420279ead5035f8f7ca2a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1826042174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb39d95d7392898fc2a92fe045c7948e23bac13e88a2771b9628a6fcd00df72`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:13:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 May 2023 03:24:47 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 03:24:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Wed, 10 May 2023 03:25:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:25:32 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 03:25:32 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 10 May 2023 03:25:33 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 10 May 2023 03:25:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:25:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 03:25:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-windows-x86_64.exe
# Wed, 10 May 2023 03:25:59 GMT
ENV DOCKER_COMPOSE_SHA256=556cc1d373503a897ecc2def998a40b2ad1fe27ff049769eb912c7e208772e74
# Wed, 10 May 2023 03:26:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d178a10e123ab9f41a66d7e6d8ffca4aab5fba57cf381f48bc0090f603be2d5`  
		Last Modified: Wed, 10 May 2023 01:45:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94bc80e6c1e6606bc432e9fa1ebc3ed83fe3ceb5a176e0a7b2c8334bf863c53`  
		Last Modified: Wed, 10 May 2023 07:11:29 GMT  
		Size: 446.9 KB (446946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e927fbd88402bacc902c2a4593f281068b2a6657c7f8b4e53ac01f8e636901`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165e88795de1230f78ac3b0186a534bd16fad90474fddb00254443f5440c8c65`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438806a743132696d59ff6500d80c1c45b0742da1613dbde135436ef14f725af`  
		Last Modified: Wed, 10 May 2023 07:12:05 GMT  
		Size: 17.3 MB (17316446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c96495f4df59195a31aba0ef651c79d5519baf34e22333d63d5a8bfe03900b`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f5f979d4f16ed05773444607ec525a26e8c703f03f102d8759e864981d5c82`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d23d10667208a1b8d0f8e33582643dd1c513834082f55a73336deecf2b3e829`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f367dbae07d50a7ea9664467f0f6935dd7ba395cf98c8f7d2e39925ff3f64e`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 16.5 MB (16457754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2158efcafa6303ace2a8d3f0d2442bddd73799341b2a6258c21abd8bd7fcac`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4a3d8cbc64bd1d463e94f091e7177ec22f9f28eb318370cdb0506d93494666`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca474991c2a553554d33df3995317383bfa4ec8b4f4249b931de5a485a27adc`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b95097e5ada96414856478813a948262a40d9c84537402939e98cd82036573`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 16.8 MB (16826864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0`

```console
$ docker pull docker@sha256:d8dfdb733748109806968a94095412310232988a20046ea57fb6d68ccd94036a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0` - linux; amd64

```console
$ docker pull docker@sha256:af8a4eb8e61f87ea50c72057624c1710dd0c6356d74e64465bc01123c7d37795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112738963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4966f34e6de695acc18297ea9b1c513a58c4048554aaaac4f10bf6080be3b32`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 15 May 2023 22:39:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/var/lib/docker]
# Mon, 15 May 2023 22:39:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 15 May 2023 22:39:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 15 May 2023 22:39:50 GMT
CMD []
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058b1c95dcd434f93391bf0ec0c404ae630b363de88563fa9a4a4d3c6889b90`  
		Last Modified: Thu, 11 May 2023 19:25:14 GMT  
		Size: 7.0 MB (7025224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1c4c35af9e9b29cde02d3d5b488ed71b7821d39319354f4aba1a8ae8ace24`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d938c8b2399339aaf8caeefbdc85c8b8dddf7d27d57d8c3d09bf070e0a4374b`  
		Last Modified: Thu, 11 May 2023 19:25:20 GMT  
		Size: 51.7 MB (51657452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2885b54919758712d2ab1b9d1e43574e5fa8d8fe06612e193c876de7d221ea`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3ce26085aa03b6fc712003b8cd4e3675c6975181aca50368e8af84866d7b9e`  
		Last Modified: Tue, 16 May 2023 00:21:06 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6df96d5cb64ef8f5cea2f45a415c388301f852b3cf8ea2d52e085139b6096031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104300688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c967226c69d0fa470b803590a3db4f0d47ca48f4691259861dc5f16904036d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755db036d15ac84998f2eac830ac44d7e439c03ecb38bd242508a0481efc0fc`  
		Last Modified: Thu, 11 May 2023 19:43:32 GMT  
		Size: 15.3 MB (15325101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f85b23db6b3d2bdbfb74d5012a03f03cb9ef9ff1e86bc625be7fd7367750a`  
		Last Modified: Thu, 11 May 2023 19:43:31 GMT  
		Size: 14.4 MB (14441512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c2aaa7ad28f7b2dbb51676ad9d28a8dd94a62c33b7b67360abbdd877825a6`  
		Last Modified: Wed, 17 May 2023 00:05:19 GMT  
		Size: 14.9 MB (14861209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f732bb283cf7f3f4629f8f8fe627fe87c1a816e6b18fb43a474e9a0488ecfb`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef0fa04d98283db2caaecb633a590ebb724d80881afd74ab3a7a0cd65c868c9`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f747c1b4bde6324e1f2a1a5bd574a10060714e43ddb674da4c8c63e6bd817`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18139dccdfd465a21cc50f7973a2aab999e1ea3ce051cac86e9bd41527b53d`  
		Last Modified: Wed, 17 May 2023 00:05:32 GMT  
		Size: 7.2 MB (7245090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c86802d31a079a23a88f2dde8479a6832603e3e1fb4f09cf4b5d99d98fb481`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f890bcd554f3ab2798ec63eea6dae3a81e80b49ebad80afab0ff62f5dafd617`  
		Last Modified: Wed, 17 May 2023 00:05:36 GMT  
		Size: 47.1 MB (47053390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3de5c6d78526ef5a60d99f63b7459b261ef8ce726a8a4e5d04e2a7b6d3c3205`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8e069943ade3caee551dd7560eeb5ea0bfe3688bd6755994395c23b78c4b1a`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 2.8 KB (2795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-cli`

```console
$ docker pull docker@sha256:f76e77bbeba3e7c53693d557c22488ddc7e77664e6e20325c2a37b1d59ef77a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:3b2d99643c86bfd09e5c2ae0c610a7820b755d71d270949f0b1e7e7ff9836ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54051122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ea5edbac8ee1fa4488a13fcf136fa3eeaff8c92b78ce78993f60a07967de99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:572ed66d449f4425cdac72cf5c26f85bd7d8220b27fddb2f77cba7a50836aa28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49997039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697bbcd3ead6712b704071f9f133f8afffa6bd65db86d186fa601607e3221aa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755db036d15ac84998f2eac830ac44d7e439c03ecb38bd242508a0481efc0fc`  
		Last Modified: Thu, 11 May 2023 19:43:32 GMT  
		Size: 15.3 MB (15325101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f85b23db6b3d2bdbfb74d5012a03f03cb9ef9ff1e86bc625be7fd7367750a`  
		Last Modified: Thu, 11 May 2023 19:43:31 GMT  
		Size: 14.4 MB (14441512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c2aaa7ad28f7b2dbb51676ad9d28a8dd94a62c33b7b67360abbdd877825a6`  
		Last Modified: Wed, 17 May 2023 00:05:19 GMT  
		Size: 14.9 MB (14861209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f732bb283cf7f3f4629f8f8fe627fe87c1a816e6b18fb43a474e9a0488ecfb`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef0fa04d98283db2caaecb633a590ebb724d80881afd74ab3a7a0cd65c868c9`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f747c1b4bde6324e1f2a1a5bd574a10060714e43ddb674da4c8c63e6bd817`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-dind`

```console
$ docker pull docker@sha256:d8dfdb733748109806968a94095412310232988a20046ea57fb6d68ccd94036a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:af8a4eb8e61f87ea50c72057624c1710dd0c6356d74e64465bc01123c7d37795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112738963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4966f34e6de695acc18297ea9b1c513a58c4048554aaaac4f10bf6080be3b32`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 15 May 2023 22:39:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/var/lib/docker]
# Mon, 15 May 2023 22:39:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 15 May 2023 22:39:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 15 May 2023 22:39:50 GMT
CMD []
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058b1c95dcd434f93391bf0ec0c404ae630b363de88563fa9a4a4d3c6889b90`  
		Last Modified: Thu, 11 May 2023 19:25:14 GMT  
		Size: 7.0 MB (7025224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1c4c35af9e9b29cde02d3d5b488ed71b7821d39319354f4aba1a8ae8ace24`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d938c8b2399339aaf8caeefbdc85c8b8dddf7d27d57d8c3d09bf070e0a4374b`  
		Last Modified: Thu, 11 May 2023 19:25:20 GMT  
		Size: 51.7 MB (51657452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2885b54919758712d2ab1b9d1e43574e5fa8d8fe06612e193c876de7d221ea`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3ce26085aa03b6fc712003b8cd4e3675c6975181aca50368e8af84866d7b9e`  
		Last Modified: Tue, 16 May 2023 00:21:06 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6df96d5cb64ef8f5cea2f45a415c388301f852b3cf8ea2d52e085139b6096031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104300688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c967226c69d0fa470b803590a3db4f0d47ca48f4691259861dc5f16904036d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755db036d15ac84998f2eac830ac44d7e439c03ecb38bd242508a0481efc0fc`  
		Last Modified: Thu, 11 May 2023 19:43:32 GMT  
		Size: 15.3 MB (15325101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f85b23db6b3d2bdbfb74d5012a03f03cb9ef9ff1e86bc625be7fd7367750a`  
		Last Modified: Thu, 11 May 2023 19:43:31 GMT  
		Size: 14.4 MB (14441512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c2aaa7ad28f7b2dbb51676ad9d28a8dd94a62c33b7b67360abbdd877825a6`  
		Last Modified: Wed, 17 May 2023 00:05:19 GMT  
		Size: 14.9 MB (14861209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f732bb283cf7f3f4629f8f8fe627fe87c1a816e6b18fb43a474e9a0488ecfb`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef0fa04d98283db2caaecb633a590ebb724d80881afd74ab3a7a0cd65c868c9`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f747c1b4bde6324e1f2a1a5bd574a10060714e43ddb674da4c8c63e6bd817`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18139dccdfd465a21cc50f7973a2aab999e1ea3ce051cac86e9bd41527b53d`  
		Last Modified: Wed, 17 May 2023 00:05:32 GMT  
		Size: 7.2 MB (7245090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c86802d31a079a23a88f2dde8479a6832603e3e1fb4f09cf4b5d99d98fb481`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f890bcd554f3ab2798ec63eea6dae3a81e80b49ebad80afab0ff62f5dafd617`  
		Last Modified: Wed, 17 May 2023 00:05:36 GMT  
		Size: 47.1 MB (47053390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3de5c6d78526ef5a60d99f63b7459b261ef8ce726a8a4e5d04e2a7b6d3c3205`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8e069943ade3caee551dd7560eeb5ea0bfe3688bd6755994395c23b78c4b1a`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 2.8 KB (2795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-dind-rootless`

```console
$ docker pull docker@sha256:26f0725b027bea7e699c27b411548d2e11560543d03b4301de24cac12f9372db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:3d5b0a0a81a2b8770652468b38847721050af219e94c5711a9a7bc8e8cdc1333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134450185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272062036ead322e794888251164e54b81a1f64cba944eda4f84db8d820accae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 15 May 2023 22:39:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/var/lib/docker]
# Mon, 15 May 2023 22:39:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 15 May 2023 22:39:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 15 May 2023 22:39:50 GMT
CMD []
# Mon, 15 May 2023 22:39:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 15 May 2023 22:39:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058b1c95dcd434f93391bf0ec0c404ae630b363de88563fa9a4a4d3c6889b90`  
		Last Modified: Thu, 11 May 2023 19:25:14 GMT  
		Size: 7.0 MB (7025224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1c4c35af9e9b29cde02d3d5b488ed71b7821d39319354f4aba1a8ae8ace24`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d938c8b2399339aaf8caeefbdc85c8b8dddf7d27d57d8c3d09bf070e0a4374b`  
		Last Modified: Thu, 11 May 2023 19:25:20 GMT  
		Size: 51.7 MB (51657452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2885b54919758712d2ab1b9d1e43574e5fa8d8fe06612e193c876de7d221ea`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3ce26085aa03b6fc712003b8cd4e3675c6975181aca50368e8af84866d7b9e`  
		Last Modified: Tue, 16 May 2023 00:21:06 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98ac734fba950213b5eef3e34a74cfb050771d2dcfb9e09bf8849e430a97171`  
		Last Modified: Tue, 16 May 2023 00:21:32 GMT  
		Size: 1.4 MB (1362380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a2dc52b58512c04b6f21d9013089f46e944d25ee401bf249410fbfee0a386a`  
		Last Modified: Tue, 16 May 2023 00:21:32 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d714531a153f83a639d0577eb97fbabde8a658d045e1a5934d0fdd66e1647e`  
		Last Modified: Tue, 16 May 2023 00:21:32 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d363f0101be8e2f3cf083449298d611caf75351c46d338317982af0bac53317e`  
		Last Modified: Tue, 16 May 2023 00:21:35 GMT  
		Size: 20.3 MB (20347094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9fecae1fab5b25b43bb2d749c2266c981b255b6ab3505f483a58c208da98e4e`  
		Last Modified: Tue, 16 May 2023 00:21:32 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b1c63d3c2d46ccf56935ea78e081c6961e8aff55b19f67b649b290a8f74b7cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127956751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:529cab109e8578d5364ffa8c1460b6f14313ad7cfcd5fd20af761767ca17c53b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 16 May 2023 17:59:38 GMT
USER rootless
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755db036d15ac84998f2eac830ac44d7e439c03ecb38bd242508a0481efc0fc`  
		Last Modified: Thu, 11 May 2023 19:43:32 GMT  
		Size: 15.3 MB (15325101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f85b23db6b3d2bdbfb74d5012a03f03cb9ef9ff1e86bc625be7fd7367750a`  
		Last Modified: Thu, 11 May 2023 19:43:31 GMT  
		Size: 14.4 MB (14441512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c2aaa7ad28f7b2dbb51676ad9d28a8dd94a62c33b7b67360abbdd877825a6`  
		Last Modified: Wed, 17 May 2023 00:05:19 GMT  
		Size: 14.9 MB (14861209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f732bb283cf7f3f4629f8f8fe627fe87c1a816e6b18fb43a474e9a0488ecfb`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef0fa04d98283db2caaecb633a590ebb724d80881afd74ab3a7a0cd65c868c9`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f747c1b4bde6324e1f2a1a5bd574a10060714e43ddb674da4c8c63e6bd817`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18139dccdfd465a21cc50f7973a2aab999e1ea3ce051cac86e9bd41527b53d`  
		Last Modified: Wed, 17 May 2023 00:05:32 GMT  
		Size: 7.2 MB (7245090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c86802d31a079a23a88f2dde8479a6832603e3e1fb4f09cf4b5d99d98fb481`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f890bcd554f3ab2798ec63eea6dae3a81e80b49ebad80afab0ff62f5dafd617`  
		Last Modified: Wed, 17 May 2023 00:05:36 GMT  
		Size: 47.1 MB (47053390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3de5c6d78526ef5a60d99f63b7459b261ef8ce726a8a4e5d04e2a7b6d3c3205`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8e069943ade3caee551dd7560eeb5ea0bfe3688bd6755994395c23b78c4b1a`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 2.8 KB (2795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f403fc6a76be877efebea34e9697fa8940f81bd7930562034d51cbbb16ee7836`  
		Last Modified: Wed, 17 May 2023 00:05:59 GMT  
		Size: 1.4 MB (1413346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d638bdef2674041ed5d4d4540aaf98cc1778c9b56db593a6d62d2f68d16c6dba`  
		Last Modified: Wed, 17 May 2023 00:05:58 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e827686ffa7ac4e0f2de8bf334fc2657f11eb7205ba4c8646b9b1c58e812da`  
		Last Modified: Wed, 17 May 2023 00:05:58 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77316858144b4c941955823a315a78cb335fc7fc0bab38f0bfe28fac673029ad`  
		Last Modified: Wed, 17 May 2023 00:06:03 GMT  
		Size: 22.2 MB (22240980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff39cfa386a5ac16b38135820005cf8ac5d291d71b2078ae17079ecf2eb3fc30`  
		Last Modified: Wed, 17 May 2023 00:05:58 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-git`

```console
$ docker pull docker@sha256:336d51df0ca7e0094a5bc3b72ddaf5ff68f9430e1b511eec7cc82193b6ecfd3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0-git` - linux; amd64

```console
$ docker pull docker@sha256:e0a9ff309d9d4d49f145163565cf50106de9bb15023321d9f6027da8243fba86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117658830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd2153f16eee41cf91fc1f892e613b7acfd0411a50ed24492a54719464d87a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 15 May 2023 22:39:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/var/lib/docker]
# Mon, 15 May 2023 22:39:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 15 May 2023 22:39:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 15 May 2023 22:39:50 GMT
CMD []
# Mon, 15 May 2023 22:39:50 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058b1c95dcd434f93391bf0ec0c404ae630b363de88563fa9a4a4d3c6889b90`  
		Last Modified: Thu, 11 May 2023 19:25:14 GMT  
		Size: 7.0 MB (7025224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1c4c35af9e9b29cde02d3d5b488ed71b7821d39319354f4aba1a8ae8ace24`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d938c8b2399339aaf8caeefbdc85c8b8dddf7d27d57d8c3d09bf070e0a4374b`  
		Last Modified: Thu, 11 May 2023 19:25:20 GMT  
		Size: 51.7 MB (51657452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2885b54919758712d2ab1b9d1e43574e5fa8d8fe06612e193c876de7d221ea`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3ce26085aa03b6fc712003b8cd4e3675c6975181aca50368e8af84866d7b9e`  
		Last Modified: Tue, 16 May 2023 00:21:06 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0eaf8da2ec7a0ad445e808e182a80a080ca992008cce921c5013474d44087e`  
		Last Modified: Tue, 16 May 2023 00:21:51 GMT  
		Size: 4.9 MB (4919867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7960c408821f0ae78825fa1d16ae3c624e622043f6bd22886009b376fc9875af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109312273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d556ee0123586a92b57931a25dfa7f48300f769681dfcd14f6bf84633a9e4092`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755db036d15ac84998f2eac830ac44d7e439c03ecb38bd242508a0481efc0fc`  
		Last Modified: Thu, 11 May 2023 19:43:32 GMT  
		Size: 15.3 MB (15325101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f85b23db6b3d2bdbfb74d5012a03f03cb9ef9ff1e86bc625be7fd7367750a`  
		Last Modified: Thu, 11 May 2023 19:43:31 GMT  
		Size: 14.4 MB (14441512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c2aaa7ad28f7b2dbb51676ad9d28a8dd94a62c33b7b67360abbdd877825a6`  
		Last Modified: Wed, 17 May 2023 00:05:19 GMT  
		Size: 14.9 MB (14861209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f732bb283cf7f3f4629f8f8fe627fe87c1a816e6b18fb43a474e9a0488ecfb`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef0fa04d98283db2caaecb633a590ebb724d80881afd74ab3a7a0cd65c868c9`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f747c1b4bde6324e1f2a1a5bd574a10060714e43ddb674da4c8c63e6bd817`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18139dccdfd465a21cc50f7973a2aab999e1ea3ce051cac86e9bd41527b53d`  
		Last Modified: Wed, 17 May 2023 00:05:32 GMT  
		Size: 7.2 MB (7245090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c86802d31a079a23a88f2dde8479a6832603e3e1fb4f09cf4b5d99d98fb481`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f890bcd554f3ab2798ec63eea6dae3a81e80b49ebad80afab0ff62f5dafd617`  
		Last Modified: Wed, 17 May 2023 00:05:36 GMT  
		Size: 47.1 MB (47053390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3de5c6d78526ef5a60d99f63b7459b261ef8ce726a8a4e5d04e2a7b6d3c3205`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8e069943ade3caee551dd7560eeb5ea0bfe3688bd6755994395c23b78c4b1a`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 2.8 KB (2795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ea70a033aec128fc750a0d6d759753695ba4227b1e7f769d29c65e44121ed2`  
		Last Modified: Wed, 17 May 2023 00:06:15 GMT  
		Size: 5.0 MB (5011585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-windowsservercore`

```console
$ docker pull docker@sha256:5ece48bf73b8c468e9da42e73104a47deb073ce38dff0342c64b8d5fd1c1aac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1726; amd64
	-	windows version 10.0.17763.4377; amd64

### `docker:23.0-windowsservercore` - windows version 10.0.20348.1726; amd64

```console
$ docker pull docker@sha256:49feec5ed8108d054e24262a0263775b0dea7ea6161420279ead5035f8f7ca2a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1826042174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb39d95d7392898fc2a92fe045c7948e23bac13e88a2771b9628a6fcd00df72`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:13:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 May 2023 03:24:47 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 03:24:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Wed, 10 May 2023 03:25:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:25:32 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 03:25:32 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 10 May 2023 03:25:33 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 10 May 2023 03:25:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:25:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 03:25:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-windows-x86_64.exe
# Wed, 10 May 2023 03:25:59 GMT
ENV DOCKER_COMPOSE_SHA256=556cc1d373503a897ecc2def998a40b2ad1fe27ff049769eb912c7e208772e74
# Wed, 10 May 2023 03:26:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d178a10e123ab9f41a66d7e6d8ffca4aab5fba57cf381f48bc0090f603be2d5`  
		Last Modified: Wed, 10 May 2023 01:45:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94bc80e6c1e6606bc432e9fa1ebc3ed83fe3ceb5a176e0a7b2c8334bf863c53`  
		Last Modified: Wed, 10 May 2023 07:11:29 GMT  
		Size: 446.9 KB (446946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e927fbd88402bacc902c2a4593f281068b2a6657c7f8b4e53ac01f8e636901`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165e88795de1230f78ac3b0186a534bd16fad90474fddb00254443f5440c8c65`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438806a743132696d59ff6500d80c1c45b0742da1613dbde135436ef14f725af`  
		Last Modified: Wed, 10 May 2023 07:12:05 GMT  
		Size: 17.3 MB (17316446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c96495f4df59195a31aba0ef651c79d5519baf34e22333d63d5a8bfe03900b`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f5f979d4f16ed05773444607ec525a26e8c703f03f102d8759e864981d5c82`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d23d10667208a1b8d0f8e33582643dd1c513834082f55a73336deecf2b3e829`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f367dbae07d50a7ea9664467f0f6935dd7ba395cf98c8f7d2e39925ff3f64e`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 16.5 MB (16457754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2158efcafa6303ace2a8d3f0d2442bddd73799341b2a6258c21abd8bd7fcac`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4a3d8cbc64bd1d463e94f091e7177ec22f9f28eb318370cdb0506d93494666`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca474991c2a553554d33df3995317383bfa4ec8b4f4249b931de5a485a27adc`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b95097e5ada96414856478813a948262a40d9c84537402939e98cd82036573`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 16.8 MB (16826864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0-windowsservercore` - windows version 10.0.17763.4377; amd64

```console
$ docker pull docker@sha256:ce1be907c58a74261c54ae870470d5c36ef2f63674c4e4cf8372e83777330ac4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2123136881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136da637bc1dc002acdb31b90bd13bb45820f2e95343006a0e97d66e2e39037b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:16:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 May 2023 03:26:29 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 03:26:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Wed, 10 May 2023 03:27:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:27:42 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 03:27:43 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 10 May 2023 03:27:43 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 10 May 2023 03:28:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:28:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 03:28:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-windows-x86_64.exe
# Wed, 10 May 2023 03:28:55 GMT
ENV DOCKER_COMPOSE_SHA256=556cc1d373503a897ecc2def998a40b2ad1fe27ff049769eb912c7e208772e74
# Wed, 10 May 2023 03:30:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5869a0b27170ed378e5d22763ab388eaf4a9dbd91cb7eaee4cef7d8639a2ff74`  
		Last Modified: Wed, 10 May 2023 07:11:47 GMT  
		Size: 451.5 KB (451506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470efce6095b6077dfd4d6bac6f6e2010f4d5bcdf636e954d0c3e9051baa7a30`  
		Last Modified: Wed, 10 May 2023 07:12:22 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf94d195dbf8bcb75f6433208dda2b0af64c556bf5eed006468d61cccf49971`  
		Last Modified: Wed, 10 May 2023 07:12:22 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f57c72aed2637dc5fc359ff575642812168a390b96d73791c2e00a8aa6c341`  
		Last Modified: Wed, 10 May 2023 07:12:25 GMT  
		Size: 17.3 MB (17330027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3802307c89ea480234035e4a743bf5fcb7af504addfaeeccdae1e83d0286ea03`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf5c7bff562bb1a033d8a2f465437525a829a56113ca6204efed01ecd6ba653`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6608073b14838ddabd4f13d2848b33488d2a7e42d3646245fc6f163e333e551`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412458425ced3171f449f28b8c40912d57931270d9d427efe39dfc669c81baa1`  
		Last Modified: Wed, 10 May 2023 07:12:23 GMT  
		Size: 16.5 MB (16467670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef29bfe39940055963010676df5645f3c05482f819eb0a729b16d43c7bc3af8`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ee6d41023794ee61421888956d914f83fedaedc16321d0aa3d0ac7e1315c25`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adecc2295964edd8cc0fd6feb81e6c3d28e20be1318d1b70c52acac1651a769b`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8302c4a8fb9f7dfb47a9992223517957000b185668adcb36a0e3f24b913406`  
		Last Modified: Wed, 10 May 2023 07:12:23 GMT  
		Size: 16.8 MB (16839833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:3ae378fb4bac1f8f4fd2f950e2e961da4eeec2fa1c4e07394c2d81e3401b4d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `docker:23.0-windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull docker@sha256:ce1be907c58a74261c54ae870470d5c36ef2f63674c4e4cf8372e83777330ac4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2123136881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136da637bc1dc002acdb31b90bd13bb45820f2e95343006a0e97d66e2e39037b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:16:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 May 2023 03:26:29 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 03:26:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Wed, 10 May 2023 03:27:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:27:42 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 03:27:43 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 10 May 2023 03:27:43 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 10 May 2023 03:28:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:28:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 03:28:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-windows-x86_64.exe
# Wed, 10 May 2023 03:28:55 GMT
ENV DOCKER_COMPOSE_SHA256=556cc1d373503a897ecc2def998a40b2ad1fe27ff049769eb912c7e208772e74
# Wed, 10 May 2023 03:30:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5869a0b27170ed378e5d22763ab388eaf4a9dbd91cb7eaee4cef7d8639a2ff74`  
		Last Modified: Wed, 10 May 2023 07:11:47 GMT  
		Size: 451.5 KB (451506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470efce6095b6077dfd4d6bac6f6e2010f4d5bcdf636e954d0c3e9051baa7a30`  
		Last Modified: Wed, 10 May 2023 07:12:22 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf94d195dbf8bcb75f6433208dda2b0af64c556bf5eed006468d61cccf49971`  
		Last Modified: Wed, 10 May 2023 07:12:22 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f57c72aed2637dc5fc359ff575642812168a390b96d73791c2e00a8aa6c341`  
		Last Modified: Wed, 10 May 2023 07:12:25 GMT  
		Size: 17.3 MB (17330027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3802307c89ea480234035e4a743bf5fcb7af504addfaeeccdae1e83d0286ea03`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf5c7bff562bb1a033d8a2f465437525a829a56113ca6204efed01ecd6ba653`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6608073b14838ddabd4f13d2848b33488d2a7e42d3646245fc6f163e333e551`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412458425ced3171f449f28b8c40912d57931270d9d427efe39dfc669c81baa1`  
		Last Modified: Wed, 10 May 2023 07:12:23 GMT  
		Size: 16.5 MB (16467670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef29bfe39940055963010676df5645f3c05482f819eb0a729b16d43c7bc3af8`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ee6d41023794ee61421888956d914f83fedaedc16321d0aa3d0ac7e1315c25`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adecc2295964edd8cc0fd6feb81e6c3d28e20be1318d1b70c52acac1651a769b`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8302c4a8fb9f7dfb47a9992223517957000b185668adcb36a0e3f24b913406`  
		Last Modified: Wed, 10 May 2023 07:12:23 GMT  
		Size: 16.8 MB (16839833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:146958020dbeb7898c0db7c57aa5753ac981d68e700983b0d2ce745f9438aa6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1726; amd64

### `docker:23.0-windowsservercore-ltsc2022` - windows version 10.0.20348.1726; amd64

```console
$ docker pull docker@sha256:49feec5ed8108d054e24262a0263775b0dea7ea6161420279ead5035f8f7ca2a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1826042174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb39d95d7392898fc2a92fe045c7948e23bac13e88a2771b9628a6fcd00df72`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:13:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 May 2023 03:24:47 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 03:24:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Wed, 10 May 2023 03:25:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:25:32 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 03:25:32 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 10 May 2023 03:25:33 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 10 May 2023 03:25:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:25:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 03:25:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-windows-x86_64.exe
# Wed, 10 May 2023 03:25:59 GMT
ENV DOCKER_COMPOSE_SHA256=556cc1d373503a897ecc2def998a40b2ad1fe27ff049769eb912c7e208772e74
# Wed, 10 May 2023 03:26:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d178a10e123ab9f41a66d7e6d8ffca4aab5fba57cf381f48bc0090f603be2d5`  
		Last Modified: Wed, 10 May 2023 01:45:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94bc80e6c1e6606bc432e9fa1ebc3ed83fe3ceb5a176e0a7b2c8334bf863c53`  
		Last Modified: Wed, 10 May 2023 07:11:29 GMT  
		Size: 446.9 KB (446946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e927fbd88402bacc902c2a4593f281068b2a6657c7f8b4e53ac01f8e636901`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165e88795de1230f78ac3b0186a534bd16fad90474fddb00254443f5440c8c65`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438806a743132696d59ff6500d80c1c45b0742da1613dbde135436ef14f725af`  
		Last Modified: Wed, 10 May 2023 07:12:05 GMT  
		Size: 17.3 MB (17316446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c96495f4df59195a31aba0ef651c79d5519baf34e22333d63d5a8bfe03900b`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f5f979d4f16ed05773444607ec525a26e8c703f03f102d8759e864981d5c82`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d23d10667208a1b8d0f8e33582643dd1c513834082f55a73336deecf2b3e829`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f367dbae07d50a7ea9664467f0f6935dd7ba395cf98c8f7d2e39925ff3f64e`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 16.5 MB (16457754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2158efcafa6303ace2a8d3f0d2442bddd73799341b2a6258c21abd8bd7fcac`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4a3d8cbc64bd1d463e94f091e7177ec22f9f28eb318370cdb0506d93494666`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca474991c2a553554d33df3995317383bfa4ec8b4f4249b931de5a485a27adc`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b95097e5ada96414856478813a948262a40d9c84537402939e98cd82036573`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 16.8 MB (16826864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6`

```console
$ docker pull docker@sha256:d8dfdb733748109806968a94095412310232988a20046ea57fb6d68ccd94036a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.6` - linux; amd64

```console
$ docker pull docker@sha256:af8a4eb8e61f87ea50c72057624c1710dd0c6356d74e64465bc01123c7d37795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112738963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4966f34e6de695acc18297ea9b1c513a58c4048554aaaac4f10bf6080be3b32`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 15 May 2023 22:39:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/var/lib/docker]
# Mon, 15 May 2023 22:39:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 15 May 2023 22:39:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 15 May 2023 22:39:50 GMT
CMD []
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058b1c95dcd434f93391bf0ec0c404ae630b363de88563fa9a4a4d3c6889b90`  
		Last Modified: Thu, 11 May 2023 19:25:14 GMT  
		Size: 7.0 MB (7025224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1c4c35af9e9b29cde02d3d5b488ed71b7821d39319354f4aba1a8ae8ace24`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d938c8b2399339aaf8caeefbdc85c8b8dddf7d27d57d8c3d09bf070e0a4374b`  
		Last Modified: Thu, 11 May 2023 19:25:20 GMT  
		Size: 51.7 MB (51657452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2885b54919758712d2ab1b9d1e43574e5fa8d8fe06612e193c876de7d221ea`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3ce26085aa03b6fc712003b8cd4e3675c6975181aca50368e8af84866d7b9e`  
		Last Modified: Tue, 16 May 2023 00:21:06 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.6` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6df96d5cb64ef8f5cea2f45a415c388301f852b3cf8ea2d52e085139b6096031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104300688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c967226c69d0fa470b803590a3db4f0d47ca48f4691259861dc5f16904036d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755db036d15ac84998f2eac830ac44d7e439c03ecb38bd242508a0481efc0fc`  
		Last Modified: Thu, 11 May 2023 19:43:32 GMT  
		Size: 15.3 MB (15325101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f85b23db6b3d2bdbfb74d5012a03f03cb9ef9ff1e86bc625be7fd7367750a`  
		Last Modified: Thu, 11 May 2023 19:43:31 GMT  
		Size: 14.4 MB (14441512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c2aaa7ad28f7b2dbb51676ad9d28a8dd94a62c33b7b67360abbdd877825a6`  
		Last Modified: Wed, 17 May 2023 00:05:19 GMT  
		Size: 14.9 MB (14861209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f732bb283cf7f3f4629f8f8fe627fe87c1a816e6b18fb43a474e9a0488ecfb`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef0fa04d98283db2caaecb633a590ebb724d80881afd74ab3a7a0cd65c868c9`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f747c1b4bde6324e1f2a1a5bd574a10060714e43ddb674da4c8c63e6bd817`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18139dccdfd465a21cc50f7973a2aab999e1ea3ce051cac86e9bd41527b53d`  
		Last Modified: Wed, 17 May 2023 00:05:32 GMT  
		Size: 7.2 MB (7245090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c86802d31a079a23a88f2dde8479a6832603e3e1fb4f09cf4b5d99d98fb481`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f890bcd554f3ab2798ec63eea6dae3a81e80b49ebad80afab0ff62f5dafd617`  
		Last Modified: Wed, 17 May 2023 00:05:36 GMT  
		Size: 47.1 MB (47053390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3de5c6d78526ef5a60d99f63b7459b261ef8ce726a8a4e5d04e2a7b6d3c3205`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8e069943ade3caee551dd7560eeb5ea0bfe3688bd6755994395c23b78c4b1a`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 2.8 KB (2795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6-alpine3.18`

```console
$ docker pull docker@sha256:d8dfdb733748109806968a94095412310232988a20046ea57fb6d68ccd94036a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.6-alpine3.18` - linux; amd64

```console
$ docker pull docker@sha256:af8a4eb8e61f87ea50c72057624c1710dd0c6356d74e64465bc01123c7d37795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112738963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4966f34e6de695acc18297ea9b1c513a58c4048554aaaac4f10bf6080be3b32`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 15 May 2023 22:39:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/var/lib/docker]
# Mon, 15 May 2023 22:39:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 15 May 2023 22:39:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 15 May 2023 22:39:50 GMT
CMD []
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058b1c95dcd434f93391bf0ec0c404ae630b363de88563fa9a4a4d3c6889b90`  
		Last Modified: Thu, 11 May 2023 19:25:14 GMT  
		Size: 7.0 MB (7025224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1c4c35af9e9b29cde02d3d5b488ed71b7821d39319354f4aba1a8ae8ace24`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d938c8b2399339aaf8caeefbdc85c8b8dddf7d27d57d8c3d09bf070e0a4374b`  
		Last Modified: Thu, 11 May 2023 19:25:20 GMT  
		Size: 51.7 MB (51657452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2885b54919758712d2ab1b9d1e43574e5fa8d8fe06612e193c876de7d221ea`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3ce26085aa03b6fc712003b8cd4e3675c6975181aca50368e8af84866d7b9e`  
		Last Modified: Tue, 16 May 2023 00:21:06 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.6-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6df96d5cb64ef8f5cea2f45a415c388301f852b3cf8ea2d52e085139b6096031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104300688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c967226c69d0fa470b803590a3db4f0d47ca48f4691259861dc5f16904036d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755db036d15ac84998f2eac830ac44d7e439c03ecb38bd242508a0481efc0fc`  
		Last Modified: Thu, 11 May 2023 19:43:32 GMT  
		Size: 15.3 MB (15325101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f85b23db6b3d2bdbfb74d5012a03f03cb9ef9ff1e86bc625be7fd7367750a`  
		Last Modified: Thu, 11 May 2023 19:43:31 GMT  
		Size: 14.4 MB (14441512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c2aaa7ad28f7b2dbb51676ad9d28a8dd94a62c33b7b67360abbdd877825a6`  
		Last Modified: Wed, 17 May 2023 00:05:19 GMT  
		Size: 14.9 MB (14861209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f732bb283cf7f3f4629f8f8fe627fe87c1a816e6b18fb43a474e9a0488ecfb`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef0fa04d98283db2caaecb633a590ebb724d80881afd74ab3a7a0cd65c868c9`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f747c1b4bde6324e1f2a1a5bd574a10060714e43ddb674da4c8c63e6bd817`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18139dccdfd465a21cc50f7973a2aab999e1ea3ce051cac86e9bd41527b53d`  
		Last Modified: Wed, 17 May 2023 00:05:32 GMT  
		Size: 7.2 MB (7245090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c86802d31a079a23a88f2dde8479a6832603e3e1fb4f09cf4b5d99d98fb481`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f890bcd554f3ab2798ec63eea6dae3a81e80b49ebad80afab0ff62f5dafd617`  
		Last Modified: Wed, 17 May 2023 00:05:36 GMT  
		Size: 47.1 MB (47053390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3de5c6d78526ef5a60d99f63b7459b261ef8ce726a8a4e5d04e2a7b6d3c3205`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8e069943ade3caee551dd7560eeb5ea0bfe3688bd6755994395c23b78c4b1a`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 2.8 KB (2795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6-cli`

```console
$ docker pull docker@sha256:f76e77bbeba3e7c53693d557c22488ddc7e77664e6e20325c2a37b1d59ef77a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.6-cli` - linux; amd64

```console
$ docker pull docker@sha256:3b2d99643c86bfd09e5c2ae0c610a7820b755d71d270949f0b1e7e7ff9836ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54051122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ea5edbac8ee1fa4488a13fcf136fa3eeaff8c92b78ce78993f60a07967de99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.6-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:572ed66d449f4425cdac72cf5c26f85bd7d8220b27fddb2f77cba7a50836aa28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49997039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697bbcd3ead6712b704071f9f133f8afffa6bd65db86d186fa601607e3221aa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755db036d15ac84998f2eac830ac44d7e439c03ecb38bd242508a0481efc0fc`  
		Last Modified: Thu, 11 May 2023 19:43:32 GMT  
		Size: 15.3 MB (15325101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f85b23db6b3d2bdbfb74d5012a03f03cb9ef9ff1e86bc625be7fd7367750a`  
		Last Modified: Thu, 11 May 2023 19:43:31 GMT  
		Size: 14.4 MB (14441512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c2aaa7ad28f7b2dbb51676ad9d28a8dd94a62c33b7b67360abbdd877825a6`  
		Last Modified: Wed, 17 May 2023 00:05:19 GMT  
		Size: 14.9 MB (14861209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f732bb283cf7f3f4629f8f8fe627fe87c1a816e6b18fb43a474e9a0488ecfb`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef0fa04d98283db2caaecb633a590ebb724d80881afd74ab3a7a0cd65c868c9`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f747c1b4bde6324e1f2a1a5bd574a10060714e43ddb674da4c8c63e6bd817`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6-cli-alpine3.18`

```console
$ docker pull docker@sha256:f76e77bbeba3e7c53693d557c22488ddc7e77664e6e20325c2a37b1d59ef77a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.6-cli-alpine3.18` - linux; amd64

```console
$ docker pull docker@sha256:3b2d99643c86bfd09e5c2ae0c610a7820b755d71d270949f0b1e7e7ff9836ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54051122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ea5edbac8ee1fa4488a13fcf136fa3eeaff8c92b78ce78993f60a07967de99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.6-cli-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:572ed66d449f4425cdac72cf5c26f85bd7d8220b27fddb2f77cba7a50836aa28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49997039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697bbcd3ead6712b704071f9f133f8afffa6bd65db86d186fa601607e3221aa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755db036d15ac84998f2eac830ac44d7e439c03ecb38bd242508a0481efc0fc`  
		Last Modified: Thu, 11 May 2023 19:43:32 GMT  
		Size: 15.3 MB (15325101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f85b23db6b3d2bdbfb74d5012a03f03cb9ef9ff1e86bc625be7fd7367750a`  
		Last Modified: Thu, 11 May 2023 19:43:31 GMT  
		Size: 14.4 MB (14441512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c2aaa7ad28f7b2dbb51676ad9d28a8dd94a62c33b7b67360abbdd877825a6`  
		Last Modified: Wed, 17 May 2023 00:05:19 GMT  
		Size: 14.9 MB (14861209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f732bb283cf7f3f4629f8f8fe627fe87c1a816e6b18fb43a474e9a0488ecfb`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef0fa04d98283db2caaecb633a590ebb724d80881afd74ab3a7a0cd65c868c9`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f747c1b4bde6324e1f2a1a5bd574a10060714e43ddb674da4c8c63e6bd817`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6-dind`

```console
$ docker pull docker@sha256:d8dfdb733748109806968a94095412310232988a20046ea57fb6d68ccd94036a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.6-dind` - linux; amd64

```console
$ docker pull docker@sha256:af8a4eb8e61f87ea50c72057624c1710dd0c6356d74e64465bc01123c7d37795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112738963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4966f34e6de695acc18297ea9b1c513a58c4048554aaaac4f10bf6080be3b32`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 15 May 2023 22:39:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/var/lib/docker]
# Mon, 15 May 2023 22:39:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 15 May 2023 22:39:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 15 May 2023 22:39:50 GMT
CMD []
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058b1c95dcd434f93391bf0ec0c404ae630b363de88563fa9a4a4d3c6889b90`  
		Last Modified: Thu, 11 May 2023 19:25:14 GMT  
		Size: 7.0 MB (7025224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1c4c35af9e9b29cde02d3d5b488ed71b7821d39319354f4aba1a8ae8ace24`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d938c8b2399339aaf8caeefbdc85c8b8dddf7d27d57d8c3d09bf070e0a4374b`  
		Last Modified: Thu, 11 May 2023 19:25:20 GMT  
		Size: 51.7 MB (51657452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2885b54919758712d2ab1b9d1e43574e5fa8d8fe06612e193c876de7d221ea`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3ce26085aa03b6fc712003b8cd4e3675c6975181aca50368e8af84866d7b9e`  
		Last Modified: Tue, 16 May 2023 00:21:06 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.6-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6df96d5cb64ef8f5cea2f45a415c388301f852b3cf8ea2d52e085139b6096031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104300688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c967226c69d0fa470b803590a3db4f0d47ca48f4691259861dc5f16904036d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755db036d15ac84998f2eac830ac44d7e439c03ecb38bd242508a0481efc0fc`  
		Last Modified: Thu, 11 May 2023 19:43:32 GMT  
		Size: 15.3 MB (15325101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f85b23db6b3d2bdbfb74d5012a03f03cb9ef9ff1e86bc625be7fd7367750a`  
		Last Modified: Thu, 11 May 2023 19:43:31 GMT  
		Size: 14.4 MB (14441512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c2aaa7ad28f7b2dbb51676ad9d28a8dd94a62c33b7b67360abbdd877825a6`  
		Last Modified: Wed, 17 May 2023 00:05:19 GMT  
		Size: 14.9 MB (14861209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f732bb283cf7f3f4629f8f8fe627fe87c1a816e6b18fb43a474e9a0488ecfb`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef0fa04d98283db2caaecb633a590ebb724d80881afd74ab3a7a0cd65c868c9`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f747c1b4bde6324e1f2a1a5bd574a10060714e43ddb674da4c8c63e6bd817`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18139dccdfd465a21cc50f7973a2aab999e1ea3ce051cac86e9bd41527b53d`  
		Last Modified: Wed, 17 May 2023 00:05:32 GMT  
		Size: 7.2 MB (7245090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c86802d31a079a23a88f2dde8479a6832603e3e1fb4f09cf4b5d99d98fb481`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f890bcd554f3ab2798ec63eea6dae3a81e80b49ebad80afab0ff62f5dafd617`  
		Last Modified: Wed, 17 May 2023 00:05:36 GMT  
		Size: 47.1 MB (47053390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3de5c6d78526ef5a60d99f63b7459b261ef8ce726a8a4e5d04e2a7b6d3c3205`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8e069943ade3caee551dd7560eeb5ea0bfe3688bd6755994395c23b78c4b1a`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 2.8 KB (2795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6-dind-alpine3.18`

```console
$ docker pull docker@sha256:d8dfdb733748109806968a94095412310232988a20046ea57fb6d68ccd94036a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.6-dind-alpine3.18` - linux; amd64

```console
$ docker pull docker@sha256:af8a4eb8e61f87ea50c72057624c1710dd0c6356d74e64465bc01123c7d37795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112738963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4966f34e6de695acc18297ea9b1c513a58c4048554aaaac4f10bf6080be3b32`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 15 May 2023 22:39:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/var/lib/docker]
# Mon, 15 May 2023 22:39:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 15 May 2023 22:39:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 15 May 2023 22:39:50 GMT
CMD []
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058b1c95dcd434f93391bf0ec0c404ae630b363de88563fa9a4a4d3c6889b90`  
		Last Modified: Thu, 11 May 2023 19:25:14 GMT  
		Size: 7.0 MB (7025224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1c4c35af9e9b29cde02d3d5b488ed71b7821d39319354f4aba1a8ae8ace24`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d938c8b2399339aaf8caeefbdc85c8b8dddf7d27d57d8c3d09bf070e0a4374b`  
		Last Modified: Thu, 11 May 2023 19:25:20 GMT  
		Size: 51.7 MB (51657452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2885b54919758712d2ab1b9d1e43574e5fa8d8fe06612e193c876de7d221ea`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3ce26085aa03b6fc712003b8cd4e3675c6975181aca50368e8af84866d7b9e`  
		Last Modified: Tue, 16 May 2023 00:21:06 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.6-dind-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6df96d5cb64ef8f5cea2f45a415c388301f852b3cf8ea2d52e085139b6096031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104300688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c967226c69d0fa470b803590a3db4f0d47ca48f4691259861dc5f16904036d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755db036d15ac84998f2eac830ac44d7e439c03ecb38bd242508a0481efc0fc`  
		Last Modified: Thu, 11 May 2023 19:43:32 GMT  
		Size: 15.3 MB (15325101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f85b23db6b3d2bdbfb74d5012a03f03cb9ef9ff1e86bc625be7fd7367750a`  
		Last Modified: Thu, 11 May 2023 19:43:31 GMT  
		Size: 14.4 MB (14441512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c2aaa7ad28f7b2dbb51676ad9d28a8dd94a62c33b7b67360abbdd877825a6`  
		Last Modified: Wed, 17 May 2023 00:05:19 GMT  
		Size: 14.9 MB (14861209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f732bb283cf7f3f4629f8f8fe627fe87c1a816e6b18fb43a474e9a0488ecfb`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef0fa04d98283db2caaecb633a590ebb724d80881afd74ab3a7a0cd65c868c9`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f747c1b4bde6324e1f2a1a5bd574a10060714e43ddb674da4c8c63e6bd817`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18139dccdfd465a21cc50f7973a2aab999e1ea3ce051cac86e9bd41527b53d`  
		Last Modified: Wed, 17 May 2023 00:05:32 GMT  
		Size: 7.2 MB (7245090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c86802d31a079a23a88f2dde8479a6832603e3e1fb4f09cf4b5d99d98fb481`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f890bcd554f3ab2798ec63eea6dae3a81e80b49ebad80afab0ff62f5dafd617`  
		Last Modified: Wed, 17 May 2023 00:05:36 GMT  
		Size: 47.1 MB (47053390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3de5c6d78526ef5a60d99f63b7459b261ef8ce726a8a4e5d04e2a7b6d3c3205`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8e069943ade3caee551dd7560eeb5ea0bfe3688bd6755994395c23b78c4b1a`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 2.8 KB (2795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6-dind-rootless`

```console
$ docker pull docker@sha256:26f0725b027bea7e699c27b411548d2e11560543d03b4301de24cac12f9372db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.6-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:3d5b0a0a81a2b8770652468b38847721050af219e94c5711a9a7bc8e8cdc1333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134450185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272062036ead322e794888251164e54b81a1f64cba944eda4f84db8d820accae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 15 May 2023 22:39:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/var/lib/docker]
# Mon, 15 May 2023 22:39:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 15 May 2023 22:39:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 15 May 2023 22:39:50 GMT
CMD []
# Mon, 15 May 2023 22:39:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 15 May 2023 22:39:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058b1c95dcd434f93391bf0ec0c404ae630b363de88563fa9a4a4d3c6889b90`  
		Last Modified: Thu, 11 May 2023 19:25:14 GMT  
		Size: 7.0 MB (7025224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1c4c35af9e9b29cde02d3d5b488ed71b7821d39319354f4aba1a8ae8ace24`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d938c8b2399339aaf8caeefbdc85c8b8dddf7d27d57d8c3d09bf070e0a4374b`  
		Last Modified: Thu, 11 May 2023 19:25:20 GMT  
		Size: 51.7 MB (51657452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2885b54919758712d2ab1b9d1e43574e5fa8d8fe06612e193c876de7d221ea`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3ce26085aa03b6fc712003b8cd4e3675c6975181aca50368e8af84866d7b9e`  
		Last Modified: Tue, 16 May 2023 00:21:06 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98ac734fba950213b5eef3e34a74cfb050771d2dcfb9e09bf8849e430a97171`  
		Last Modified: Tue, 16 May 2023 00:21:32 GMT  
		Size: 1.4 MB (1362380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a2dc52b58512c04b6f21d9013089f46e944d25ee401bf249410fbfee0a386a`  
		Last Modified: Tue, 16 May 2023 00:21:32 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d714531a153f83a639d0577eb97fbabde8a658d045e1a5934d0fdd66e1647e`  
		Last Modified: Tue, 16 May 2023 00:21:32 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d363f0101be8e2f3cf083449298d611caf75351c46d338317982af0bac53317e`  
		Last Modified: Tue, 16 May 2023 00:21:35 GMT  
		Size: 20.3 MB (20347094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9fecae1fab5b25b43bb2d749c2266c981b255b6ab3505f483a58c208da98e4e`  
		Last Modified: Tue, 16 May 2023 00:21:32 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.6-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b1c63d3c2d46ccf56935ea78e081c6961e8aff55b19f67b649b290a8f74b7cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127956751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:529cab109e8578d5364ffa8c1460b6f14313ad7cfcd5fd20af761767ca17c53b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 16 May 2023 17:59:38 GMT
USER rootless
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755db036d15ac84998f2eac830ac44d7e439c03ecb38bd242508a0481efc0fc`  
		Last Modified: Thu, 11 May 2023 19:43:32 GMT  
		Size: 15.3 MB (15325101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f85b23db6b3d2bdbfb74d5012a03f03cb9ef9ff1e86bc625be7fd7367750a`  
		Last Modified: Thu, 11 May 2023 19:43:31 GMT  
		Size: 14.4 MB (14441512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c2aaa7ad28f7b2dbb51676ad9d28a8dd94a62c33b7b67360abbdd877825a6`  
		Last Modified: Wed, 17 May 2023 00:05:19 GMT  
		Size: 14.9 MB (14861209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f732bb283cf7f3f4629f8f8fe627fe87c1a816e6b18fb43a474e9a0488ecfb`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef0fa04d98283db2caaecb633a590ebb724d80881afd74ab3a7a0cd65c868c9`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f747c1b4bde6324e1f2a1a5bd574a10060714e43ddb674da4c8c63e6bd817`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18139dccdfd465a21cc50f7973a2aab999e1ea3ce051cac86e9bd41527b53d`  
		Last Modified: Wed, 17 May 2023 00:05:32 GMT  
		Size: 7.2 MB (7245090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c86802d31a079a23a88f2dde8479a6832603e3e1fb4f09cf4b5d99d98fb481`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f890bcd554f3ab2798ec63eea6dae3a81e80b49ebad80afab0ff62f5dafd617`  
		Last Modified: Wed, 17 May 2023 00:05:36 GMT  
		Size: 47.1 MB (47053390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3de5c6d78526ef5a60d99f63b7459b261ef8ce726a8a4e5d04e2a7b6d3c3205`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8e069943ade3caee551dd7560eeb5ea0bfe3688bd6755994395c23b78c4b1a`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 2.8 KB (2795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f403fc6a76be877efebea34e9697fa8940f81bd7930562034d51cbbb16ee7836`  
		Last Modified: Wed, 17 May 2023 00:05:59 GMT  
		Size: 1.4 MB (1413346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d638bdef2674041ed5d4d4540aaf98cc1778c9b56db593a6d62d2f68d16c6dba`  
		Last Modified: Wed, 17 May 2023 00:05:58 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e827686ffa7ac4e0f2de8bf334fc2657f11eb7205ba4c8646b9b1c58e812da`  
		Last Modified: Wed, 17 May 2023 00:05:58 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77316858144b4c941955823a315a78cb335fc7fc0bab38f0bfe28fac673029ad`  
		Last Modified: Wed, 17 May 2023 00:06:03 GMT  
		Size: 22.2 MB (22240980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff39cfa386a5ac16b38135820005cf8ac5d291d71b2078ae17079ecf2eb3fc30`  
		Last Modified: Wed, 17 May 2023 00:05:58 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6-git`

```console
$ docker pull docker@sha256:336d51df0ca7e0094a5bc3b72ddaf5ff68f9430e1b511eec7cc82193b6ecfd3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.6-git` - linux; amd64

```console
$ docker pull docker@sha256:e0a9ff309d9d4d49f145163565cf50106de9bb15023321d9f6027da8243fba86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117658830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd2153f16eee41cf91fc1f892e613b7acfd0411a50ed24492a54719464d87a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 15 May 2023 22:39:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/var/lib/docker]
# Mon, 15 May 2023 22:39:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 15 May 2023 22:39:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 15 May 2023 22:39:50 GMT
CMD []
# Mon, 15 May 2023 22:39:50 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058b1c95dcd434f93391bf0ec0c404ae630b363de88563fa9a4a4d3c6889b90`  
		Last Modified: Thu, 11 May 2023 19:25:14 GMT  
		Size: 7.0 MB (7025224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1c4c35af9e9b29cde02d3d5b488ed71b7821d39319354f4aba1a8ae8ace24`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d938c8b2399339aaf8caeefbdc85c8b8dddf7d27d57d8c3d09bf070e0a4374b`  
		Last Modified: Thu, 11 May 2023 19:25:20 GMT  
		Size: 51.7 MB (51657452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2885b54919758712d2ab1b9d1e43574e5fa8d8fe06612e193c876de7d221ea`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3ce26085aa03b6fc712003b8cd4e3675c6975181aca50368e8af84866d7b9e`  
		Last Modified: Tue, 16 May 2023 00:21:06 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0eaf8da2ec7a0ad445e808e182a80a080ca992008cce921c5013474d44087e`  
		Last Modified: Tue, 16 May 2023 00:21:51 GMT  
		Size: 4.9 MB (4919867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.6-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7960c408821f0ae78825fa1d16ae3c624e622043f6bd22886009b376fc9875af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109312273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d556ee0123586a92b57931a25dfa7f48300f769681dfcd14f6bf84633a9e4092`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755db036d15ac84998f2eac830ac44d7e439c03ecb38bd242508a0481efc0fc`  
		Last Modified: Thu, 11 May 2023 19:43:32 GMT  
		Size: 15.3 MB (15325101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f85b23db6b3d2bdbfb74d5012a03f03cb9ef9ff1e86bc625be7fd7367750a`  
		Last Modified: Thu, 11 May 2023 19:43:31 GMT  
		Size: 14.4 MB (14441512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c2aaa7ad28f7b2dbb51676ad9d28a8dd94a62c33b7b67360abbdd877825a6`  
		Last Modified: Wed, 17 May 2023 00:05:19 GMT  
		Size: 14.9 MB (14861209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f732bb283cf7f3f4629f8f8fe627fe87c1a816e6b18fb43a474e9a0488ecfb`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef0fa04d98283db2caaecb633a590ebb724d80881afd74ab3a7a0cd65c868c9`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f747c1b4bde6324e1f2a1a5bd574a10060714e43ddb674da4c8c63e6bd817`  
		Last Modified: Wed, 17 May 2023 00:05:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18139dccdfd465a21cc50f7973a2aab999e1ea3ce051cac86e9bd41527b53d`  
		Last Modified: Wed, 17 May 2023 00:05:32 GMT  
		Size: 7.2 MB (7245090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c86802d31a079a23a88f2dde8479a6832603e3e1fb4f09cf4b5d99d98fb481`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f890bcd554f3ab2798ec63eea6dae3a81e80b49ebad80afab0ff62f5dafd617`  
		Last Modified: Wed, 17 May 2023 00:05:36 GMT  
		Size: 47.1 MB (47053390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3de5c6d78526ef5a60d99f63b7459b261ef8ce726a8a4e5d04e2a7b6d3c3205`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8e069943ade3caee551dd7560eeb5ea0bfe3688bd6755994395c23b78c4b1a`  
		Last Modified: Wed, 17 May 2023 00:05:31 GMT  
		Size: 2.8 KB (2795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ea70a033aec128fc750a0d6d759753695ba4227b1e7f769d29c65e44121ed2`  
		Last Modified: Wed, 17 May 2023 00:06:15 GMT  
		Size: 5.0 MB (5011585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6-windowsservercore`

```console
$ docker pull docker@sha256:5ece48bf73b8c468e9da42e73104a47deb073ce38dff0342c64b8d5fd1c1aac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1726; amd64
	-	windows version 10.0.17763.4377; amd64

### `docker:23.0.6-windowsservercore` - windows version 10.0.20348.1726; amd64

```console
$ docker pull docker@sha256:49feec5ed8108d054e24262a0263775b0dea7ea6161420279ead5035f8f7ca2a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1826042174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb39d95d7392898fc2a92fe045c7948e23bac13e88a2771b9628a6fcd00df72`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:13:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 May 2023 03:24:47 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 03:24:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Wed, 10 May 2023 03:25:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:25:32 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 03:25:32 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 10 May 2023 03:25:33 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 10 May 2023 03:25:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:25:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 03:25:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-windows-x86_64.exe
# Wed, 10 May 2023 03:25:59 GMT
ENV DOCKER_COMPOSE_SHA256=556cc1d373503a897ecc2def998a40b2ad1fe27ff049769eb912c7e208772e74
# Wed, 10 May 2023 03:26:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d178a10e123ab9f41a66d7e6d8ffca4aab5fba57cf381f48bc0090f603be2d5`  
		Last Modified: Wed, 10 May 2023 01:45:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94bc80e6c1e6606bc432e9fa1ebc3ed83fe3ceb5a176e0a7b2c8334bf863c53`  
		Last Modified: Wed, 10 May 2023 07:11:29 GMT  
		Size: 446.9 KB (446946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e927fbd88402bacc902c2a4593f281068b2a6657c7f8b4e53ac01f8e636901`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165e88795de1230f78ac3b0186a534bd16fad90474fddb00254443f5440c8c65`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438806a743132696d59ff6500d80c1c45b0742da1613dbde135436ef14f725af`  
		Last Modified: Wed, 10 May 2023 07:12:05 GMT  
		Size: 17.3 MB (17316446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c96495f4df59195a31aba0ef651c79d5519baf34e22333d63d5a8bfe03900b`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f5f979d4f16ed05773444607ec525a26e8c703f03f102d8759e864981d5c82`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d23d10667208a1b8d0f8e33582643dd1c513834082f55a73336deecf2b3e829`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f367dbae07d50a7ea9664467f0f6935dd7ba395cf98c8f7d2e39925ff3f64e`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 16.5 MB (16457754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2158efcafa6303ace2a8d3f0d2442bddd73799341b2a6258c21abd8bd7fcac`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4a3d8cbc64bd1d463e94f091e7177ec22f9f28eb318370cdb0506d93494666`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca474991c2a553554d33df3995317383bfa4ec8b4f4249b931de5a485a27adc`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b95097e5ada96414856478813a948262a40d9c84537402939e98cd82036573`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 16.8 MB (16826864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.6-windowsservercore` - windows version 10.0.17763.4377; amd64

```console
$ docker pull docker@sha256:ce1be907c58a74261c54ae870470d5c36ef2f63674c4e4cf8372e83777330ac4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2123136881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136da637bc1dc002acdb31b90bd13bb45820f2e95343006a0e97d66e2e39037b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:16:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 May 2023 03:26:29 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 03:26:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Wed, 10 May 2023 03:27:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:27:42 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 03:27:43 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 10 May 2023 03:27:43 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 10 May 2023 03:28:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:28:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 03:28:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-windows-x86_64.exe
# Wed, 10 May 2023 03:28:55 GMT
ENV DOCKER_COMPOSE_SHA256=556cc1d373503a897ecc2def998a40b2ad1fe27ff049769eb912c7e208772e74
# Wed, 10 May 2023 03:30:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5869a0b27170ed378e5d22763ab388eaf4a9dbd91cb7eaee4cef7d8639a2ff74`  
		Last Modified: Wed, 10 May 2023 07:11:47 GMT  
		Size: 451.5 KB (451506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470efce6095b6077dfd4d6bac6f6e2010f4d5bcdf636e954d0c3e9051baa7a30`  
		Last Modified: Wed, 10 May 2023 07:12:22 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf94d195dbf8bcb75f6433208dda2b0af64c556bf5eed006468d61cccf49971`  
		Last Modified: Wed, 10 May 2023 07:12:22 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f57c72aed2637dc5fc359ff575642812168a390b96d73791c2e00a8aa6c341`  
		Last Modified: Wed, 10 May 2023 07:12:25 GMT  
		Size: 17.3 MB (17330027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3802307c89ea480234035e4a743bf5fcb7af504addfaeeccdae1e83d0286ea03`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf5c7bff562bb1a033d8a2f465437525a829a56113ca6204efed01ecd6ba653`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6608073b14838ddabd4f13d2848b33488d2a7e42d3646245fc6f163e333e551`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412458425ced3171f449f28b8c40912d57931270d9d427efe39dfc669c81baa1`  
		Last Modified: Wed, 10 May 2023 07:12:23 GMT  
		Size: 16.5 MB (16467670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef29bfe39940055963010676df5645f3c05482f819eb0a729b16d43c7bc3af8`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ee6d41023794ee61421888956d914f83fedaedc16321d0aa3d0ac7e1315c25`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adecc2295964edd8cc0fd6feb81e6c3d28e20be1318d1b70c52acac1651a769b`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8302c4a8fb9f7dfb47a9992223517957000b185668adcb36a0e3f24b913406`  
		Last Modified: Wed, 10 May 2023 07:12:23 GMT  
		Size: 16.8 MB (16839833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6-windowsservercore-1809`

```console
$ docker pull docker@sha256:3ae378fb4bac1f8f4fd2f950e2e961da4eeec2fa1c4e07394c2d81e3401b4d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `docker:23.0.6-windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull docker@sha256:ce1be907c58a74261c54ae870470d5c36ef2f63674c4e4cf8372e83777330ac4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2123136881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136da637bc1dc002acdb31b90bd13bb45820f2e95343006a0e97d66e2e39037b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:16:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 May 2023 03:26:29 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 03:26:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Wed, 10 May 2023 03:27:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:27:42 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 03:27:43 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 10 May 2023 03:27:43 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 10 May 2023 03:28:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:28:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 03:28:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-windows-x86_64.exe
# Wed, 10 May 2023 03:28:55 GMT
ENV DOCKER_COMPOSE_SHA256=556cc1d373503a897ecc2def998a40b2ad1fe27ff049769eb912c7e208772e74
# Wed, 10 May 2023 03:30:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5869a0b27170ed378e5d22763ab388eaf4a9dbd91cb7eaee4cef7d8639a2ff74`  
		Last Modified: Wed, 10 May 2023 07:11:47 GMT  
		Size: 451.5 KB (451506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470efce6095b6077dfd4d6bac6f6e2010f4d5bcdf636e954d0c3e9051baa7a30`  
		Last Modified: Wed, 10 May 2023 07:12:22 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf94d195dbf8bcb75f6433208dda2b0af64c556bf5eed006468d61cccf49971`  
		Last Modified: Wed, 10 May 2023 07:12:22 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f57c72aed2637dc5fc359ff575642812168a390b96d73791c2e00a8aa6c341`  
		Last Modified: Wed, 10 May 2023 07:12:25 GMT  
		Size: 17.3 MB (17330027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3802307c89ea480234035e4a743bf5fcb7af504addfaeeccdae1e83d0286ea03`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf5c7bff562bb1a033d8a2f465437525a829a56113ca6204efed01ecd6ba653`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6608073b14838ddabd4f13d2848b33488d2a7e42d3646245fc6f163e333e551`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412458425ced3171f449f28b8c40912d57931270d9d427efe39dfc669c81baa1`  
		Last Modified: Wed, 10 May 2023 07:12:23 GMT  
		Size: 16.5 MB (16467670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef29bfe39940055963010676df5645f3c05482f819eb0a729b16d43c7bc3af8`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ee6d41023794ee61421888956d914f83fedaedc16321d0aa3d0ac7e1315c25`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adecc2295964edd8cc0fd6feb81e6c3d28e20be1318d1b70c52acac1651a769b`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8302c4a8fb9f7dfb47a9992223517957000b185668adcb36a0e3f24b913406`  
		Last Modified: Wed, 10 May 2023 07:12:23 GMT  
		Size: 16.8 MB (16839833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.6-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:146958020dbeb7898c0db7c57aa5753ac981d68e700983b0d2ce745f9438aa6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1726; amd64

### `docker:23.0.6-windowsservercore-ltsc2022` - windows version 10.0.20348.1726; amd64

```console
$ docker pull docker@sha256:49feec5ed8108d054e24262a0263775b0dea7ea6161420279ead5035f8f7ca2a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1826042174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb39d95d7392898fc2a92fe045c7948e23bac13e88a2771b9628a6fcd00df72`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:13:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 May 2023 03:24:47 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 03:24:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Wed, 10 May 2023 03:25:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:25:32 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 03:25:32 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 10 May 2023 03:25:33 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 10 May 2023 03:25:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:25:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 03:25:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-windows-x86_64.exe
# Wed, 10 May 2023 03:25:59 GMT
ENV DOCKER_COMPOSE_SHA256=556cc1d373503a897ecc2def998a40b2ad1fe27ff049769eb912c7e208772e74
# Wed, 10 May 2023 03:26:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d178a10e123ab9f41a66d7e6d8ffca4aab5fba57cf381f48bc0090f603be2d5`  
		Last Modified: Wed, 10 May 2023 01:45:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94bc80e6c1e6606bc432e9fa1ebc3ed83fe3ceb5a176e0a7b2c8334bf863c53`  
		Last Modified: Wed, 10 May 2023 07:11:29 GMT  
		Size: 446.9 KB (446946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e927fbd88402bacc902c2a4593f281068b2a6657c7f8b4e53ac01f8e636901`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165e88795de1230f78ac3b0186a534bd16fad90474fddb00254443f5440c8c65`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438806a743132696d59ff6500d80c1c45b0742da1613dbde135436ef14f725af`  
		Last Modified: Wed, 10 May 2023 07:12:05 GMT  
		Size: 17.3 MB (17316446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c96495f4df59195a31aba0ef651c79d5519baf34e22333d63d5a8bfe03900b`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f5f979d4f16ed05773444607ec525a26e8c703f03f102d8759e864981d5c82`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d23d10667208a1b8d0f8e33582643dd1c513834082f55a73336deecf2b3e829`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f367dbae07d50a7ea9664467f0f6935dd7ba395cf98c8f7d2e39925ff3f64e`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 16.5 MB (16457754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2158efcafa6303ace2a8d3f0d2442bddd73799341b2a6258c21abd8bd7fcac`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4a3d8cbc64bd1d463e94f091e7177ec22f9f28eb318370cdb0506d93494666`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca474991c2a553554d33df3995317383bfa4ec8b4f4249b931de5a485a27adc`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b95097e5ada96414856478813a948262a40d9c84537402939e98cd82036573`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 16.8 MB (16826864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24`

```console
$ docker pull docker@sha256:61580af84f2ed8b43e9ffc58213a0e068bd15bfb5ef3f28d0cffcb96bcb59fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:24` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e2889e32eb63f26495075e3e72c26c90d9dfddbe6b742eb099853240841a26f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106800114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1eada20d7ce614ccc2e919b00572bb0598c2db217e7310b2ef0b9ac4502474`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22442686bd72e2c0ecd000948826aebc8dcb3136fe1142b6ef334fa4a389f388`  
		Last Modified: Wed, 17 May 2023 00:04:11 GMT  
		Size: 7.2 MB (7245057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538120297d91ba480effca7fc88d637aab474129879b223a9120eb3d7648e0c3`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff4018a72e47b5a3546eb439499e864408cef1745148eb85b5af6026a7282`  
		Last Modified: Wed, 17 May 2023 00:04:15 GMT  
		Size: 49.5 MB (49455389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398e5219c811f7cb87f34450cf1a01a217122fcc492cbc68437dcee7fe05e156`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a054eb5e9d233a1fae4b8399984152cfd30e385282d002072fb7d5db6b0fdd84`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24-cli`

```console
$ docker pull docker@sha256:8c9cee9d3e0fe8e690e17780221beb433978be0d935862c3953350c82557aa32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:24-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9c88bee6d1758fe02442a9f63d44488250d3fe2f1eeed02422e28cffde7a031a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50094511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386dea7015873d311819193f58ef3f374b4449a5a7deaeb50650bf9e54142db3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24-dind`

```console
$ docker pull docker@sha256:61580af84f2ed8b43e9ffc58213a0e068bd15bfb5ef3f28d0cffcb96bcb59fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:24-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e2889e32eb63f26495075e3e72c26c90d9dfddbe6b742eb099853240841a26f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106800114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1eada20d7ce614ccc2e919b00572bb0598c2db217e7310b2ef0b9ac4502474`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22442686bd72e2c0ecd000948826aebc8dcb3136fe1142b6ef334fa4a389f388`  
		Last Modified: Wed, 17 May 2023 00:04:11 GMT  
		Size: 7.2 MB (7245057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538120297d91ba480effca7fc88d637aab474129879b223a9120eb3d7648e0c3`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff4018a72e47b5a3546eb439499e864408cef1745148eb85b5af6026a7282`  
		Last Modified: Wed, 17 May 2023 00:04:15 GMT  
		Size: 49.5 MB (49455389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398e5219c811f7cb87f34450cf1a01a217122fcc492cbc68437dcee7fe05e156`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a054eb5e9d233a1fae4b8399984152cfd30e385282d002072fb7d5db6b0fdd84`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24-dind-rootless`

```console
$ docker pull docker@sha256:756d1568bc6c7ee6e753af1ccf4d7c5c38bc3f6632bb0005b9f12bfd9cc99aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:24-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d5fea20e13ddd78513d02a2331f6d31f1c48314431094bc8225a58a3e199628e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130662457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025c163c83c0cec89c2e216140bc53ad1a14a3841a37e30e5c248eadf340561e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 16 May 2023 17:59:38 GMT
USER rootless
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22442686bd72e2c0ecd000948826aebc8dcb3136fe1142b6ef334fa4a389f388`  
		Last Modified: Wed, 17 May 2023 00:04:11 GMT  
		Size: 7.2 MB (7245057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538120297d91ba480effca7fc88d637aab474129879b223a9120eb3d7648e0c3`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff4018a72e47b5a3546eb439499e864408cef1745148eb85b5af6026a7282`  
		Last Modified: Wed, 17 May 2023 00:04:15 GMT  
		Size: 49.5 MB (49455389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398e5219c811f7cb87f34450cf1a01a217122fcc492cbc68437dcee7fe05e156`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a054eb5e9d233a1fae4b8399984152cfd30e385282d002072fb7d5db6b0fdd84`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ee53f4852847948f043ca06a0787f96b227b7a89bd3a96c001e0a015ed0fa1`  
		Last Modified: Wed, 17 May 2023 00:04:45 GMT  
		Size: 1.4 MB (1413339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1da8cd837f1a67565e17645d233f693dd101d1f489eee2a9b9e539419953232`  
		Last Modified: Wed, 17 May 2023 00:04:45 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da12c61e018b49d59351af2c58c6aa2d838fd2c66bd096040afd3f98b37e39d`  
		Last Modified: Wed, 17 May 2023 00:04:45 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826a4dc1d8c55308e6d04bed73f3d53650e3a05a030d0b8e398968bae5148d96`  
		Last Modified: Wed, 17 May 2023 00:04:48 GMT  
		Size: 22.4 MB (22447264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39be7db13eba707e002fc9857aa46ae80d8c6c28c3a28f380b1a580aecb6e388`  
		Last Modified: Wed, 17 May 2023 00:04:45 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24-git`

```console
$ docker pull docker@sha256:b60f5335ffd4c3e5bd33c4e10566b71942f3febd1190a18a8096ccd9173c8379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:24-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e080720de9821d7798727a4b42345477112b560895be9d75f7968b37ac9022d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111811702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30f0722482b8c94d89e4906b5e4f1e48a5e369c035ae13e74e088eee327baa1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22442686bd72e2c0ecd000948826aebc8dcb3136fe1142b6ef334fa4a389f388`  
		Last Modified: Wed, 17 May 2023 00:04:11 GMT  
		Size: 7.2 MB (7245057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538120297d91ba480effca7fc88d637aab474129879b223a9120eb3d7648e0c3`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff4018a72e47b5a3546eb439499e864408cef1745148eb85b5af6026a7282`  
		Last Modified: Wed, 17 May 2023 00:04:15 GMT  
		Size: 49.5 MB (49455389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398e5219c811f7cb87f34450cf1a01a217122fcc492cbc68437dcee7fe05e156`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a054eb5e9d233a1fae4b8399984152cfd30e385282d002072fb7d5db6b0fdd84`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee49b1c7c0b9892261471f527ffd51ada102f9143c374f52a4df759fa592242d`  
		Last Modified: Wed, 17 May 2023 00:05:04 GMT  
		Size: 5.0 MB (5011588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24-windowsservercore`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:24-windowsservercore-1809`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:24-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:24.0`

```console
$ docker pull docker@sha256:61580af84f2ed8b43e9ffc58213a0e068bd15bfb5ef3f28d0cffcb96bcb59fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:24.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e2889e32eb63f26495075e3e72c26c90d9dfddbe6b742eb099853240841a26f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106800114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1eada20d7ce614ccc2e919b00572bb0598c2db217e7310b2ef0b9ac4502474`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22442686bd72e2c0ecd000948826aebc8dcb3136fe1142b6ef334fa4a389f388`  
		Last Modified: Wed, 17 May 2023 00:04:11 GMT  
		Size: 7.2 MB (7245057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538120297d91ba480effca7fc88d637aab474129879b223a9120eb3d7648e0c3`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff4018a72e47b5a3546eb439499e864408cef1745148eb85b5af6026a7282`  
		Last Modified: Wed, 17 May 2023 00:04:15 GMT  
		Size: 49.5 MB (49455389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398e5219c811f7cb87f34450cf1a01a217122fcc492cbc68437dcee7fe05e156`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a054eb5e9d233a1fae4b8399984152cfd30e385282d002072fb7d5db6b0fdd84`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0-cli`

```console
$ docker pull docker@sha256:8c9cee9d3e0fe8e690e17780221beb433978be0d935862c3953350c82557aa32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:24.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9c88bee6d1758fe02442a9f63d44488250d3fe2f1eeed02422e28cffde7a031a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50094511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386dea7015873d311819193f58ef3f374b4449a5a7deaeb50650bf9e54142db3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0-dind`

```console
$ docker pull docker@sha256:61580af84f2ed8b43e9ffc58213a0e068bd15bfb5ef3f28d0cffcb96bcb59fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:24.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e2889e32eb63f26495075e3e72c26c90d9dfddbe6b742eb099853240841a26f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106800114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1eada20d7ce614ccc2e919b00572bb0598c2db217e7310b2ef0b9ac4502474`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22442686bd72e2c0ecd000948826aebc8dcb3136fe1142b6ef334fa4a389f388`  
		Last Modified: Wed, 17 May 2023 00:04:11 GMT  
		Size: 7.2 MB (7245057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538120297d91ba480effca7fc88d637aab474129879b223a9120eb3d7648e0c3`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff4018a72e47b5a3546eb439499e864408cef1745148eb85b5af6026a7282`  
		Last Modified: Wed, 17 May 2023 00:04:15 GMT  
		Size: 49.5 MB (49455389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398e5219c811f7cb87f34450cf1a01a217122fcc492cbc68437dcee7fe05e156`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a054eb5e9d233a1fae4b8399984152cfd30e385282d002072fb7d5db6b0fdd84`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0-dind-rootless`

```console
$ docker pull docker@sha256:756d1568bc6c7ee6e753af1ccf4d7c5c38bc3f6632bb0005b9f12bfd9cc99aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:24.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d5fea20e13ddd78513d02a2331f6d31f1c48314431094bc8225a58a3e199628e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130662457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025c163c83c0cec89c2e216140bc53ad1a14a3841a37e30e5c248eadf340561e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 16 May 2023 17:59:38 GMT
USER rootless
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22442686bd72e2c0ecd000948826aebc8dcb3136fe1142b6ef334fa4a389f388`  
		Last Modified: Wed, 17 May 2023 00:04:11 GMT  
		Size: 7.2 MB (7245057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538120297d91ba480effca7fc88d637aab474129879b223a9120eb3d7648e0c3`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff4018a72e47b5a3546eb439499e864408cef1745148eb85b5af6026a7282`  
		Last Modified: Wed, 17 May 2023 00:04:15 GMT  
		Size: 49.5 MB (49455389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398e5219c811f7cb87f34450cf1a01a217122fcc492cbc68437dcee7fe05e156`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a054eb5e9d233a1fae4b8399984152cfd30e385282d002072fb7d5db6b0fdd84`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ee53f4852847948f043ca06a0787f96b227b7a89bd3a96c001e0a015ed0fa1`  
		Last Modified: Wed, 17 May 2023 00:04:45 GMT  
		Size: 1.4 MB (1413339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1da8cd837f1a67565e17645d233f693dd101d1f489eee2a9b9e539419953232`  
		Last Modified: Wed, 17 May 2023 00:04:45 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da12c61e018b49d59351af2c58c6aa2d838fd2c66bd096040afd3f98b37e39d`  
		Last Modified: Wed, 17 May 2023 00:04:45 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826a4dc1d8c55308e6d04bed73f3d53650e3a05a030d0b8e398968bae5148d96`  
		Last Modified: Wed, 17 May 2023 00:04:48 GMT  
		Size: 22.4 MB (22447264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39be7db13eba707e002fc9857aa46ae80d8c6c28c3a28f380b1a580aecb6e388`  
		Last Modified: Wed, 17 May 2023 00:04:45 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0-git`

```console
$ docker pull docker@sha256:b60f5335ffd4c3e5bd33c4e10566b71942f3febd1190a18a8096ccd9173c8379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:24.0-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e080720de9821d7798727a4b42345477112b560895be9d75f7968b37ac9022d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111811702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30f0722482b8c94d89e4906b5e4f1e48a5e369c035ae13e74e088eee327baa1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22442686bd72e2c0ecd000948826aebc8dcb3136fe1142b6ef334fa4a389f388`  
		Last Modified: Wed, 17 May 2023 00:04:11 GMT  
		Size: 7.2 MB (7245057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538120297d91ba480effca7fc88d637aab474129879b223a9120eb3d7648e0c3`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff4018a72e47b5a3546eb439499e864408cef1745148eb85b5af6026a7282`  
		Last Modified: Wed, 17 May 2023 00:04:15 GMT  
		Size: 49.5 MB (49455389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398e5219c811f7cb87f34450cf1a01a217122fcc492cbc68437dcee7fe05e156`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a054eb5e9d233a1fae4b8399984152cfd30e385282d002072fb7d5db6b0fdd84`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee49b1c7c0b9892261471f527ffd51ada102f9143c374f52a4df759fa592242d`  
		Last Modified: Wed, 17 May 2023 00:05:04 GMT  
		Size: 5.0 MB (5011588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0-windowsservercore`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:24.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:24.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:24.0.0`

```console
$ docker pull docker@sha256:61580af84f2ed8b43e9ffc58213a0e068bd15bfb5ef3f28d0cffcb96bcb59fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:24.0.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e2889e32eb63f26495075e3e72c26c90d9dfddbe6b742eb099853240841a26f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106800114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1eada20d7ce614ccc2e919b00572bb0598c2db217e7310b2ef0b9ac4502474`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22442686bd72e2c0ecd000948826aebc8dcb3136fe1142b6ef334fa4a389f388`  
		Last Modified: Wed, 17 May 2023 00:04:11 GMT  
		Size: 7.2 MB (7245057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538120297d91ba480effca7fc88d637aab474129879b223a9120eb3d7648e0c3`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff4018a72e47b5a3546eb439499e864408cef1745148eb85b5af6026a7282`  
		Last Modified: Wed, 17 May 2023 00:04:15 GMT  
		Size: 49.5 MB (49455389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398e5219c811f7cb87f34450cf1a01a217122fcc492cbc68437dcee7fe05e156`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a054eb5e9d233a1fae4b8399984152cfd30e385282d002072fb7d5db6b0fdd84`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0.0-alpine3.18`

```console
$ docker pull docker@sha256:61580af84f2ed8b43e9ffc58213a0e068bd15bfb5ef3f28d0cffcb96bcb59fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:24.0.0-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e2889e32eb63f26495075e3e72c26c90d9dfddbe6b742eb099853240841a26f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106800114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1eada20d7ce614ccc2e919b00572bb0598c2db217e7310b2ef0b9ac4502474`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22442686bd72e2c0ecd000948826aebc8dcb3136fe1142b6ef334fa4a389f388`  
		Last Modified: Wed, 17 May 2023 00:04:11 GMT  
		Size: 7.2 MB (7245057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538120297d91ba480effca7fc88d637aab474129879b223a9120eb3d7648e0c3`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff4018a72e47b5a3546eb439499e864408cef1745148eb85b5af6026a7282`  
		Last Modified: Wed, 17 May 2023 00:04:15 GMT  
		Size: 49.5 MB (49455389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398e5219c811f7cb87f34450cf1a01a217122fcc492cbc68437dcee7fe05e156`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a054eb5e9d233a1fae4b8399984152cfd30e385282d002072fb7d5db6b0fdd84`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0.0-cli`

```console
$ docker pull docker@sha256:8c9cee9d3e0fe8e690e17780221beb433978be0d935862c3953350c82557aa32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:24.0.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9c88bee6d1758fe02442a9f63d44488250d3fe2f1eeed02422e28cffde7a031a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50094511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386dea7015873d311819193f58ef3f374b4449a5a7deaeb50650bf9e54142db3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0.0-cli-alpine3.18`

```console
$ docker pull docker@sha256:8c9cee9d3e0fe8e690e17780221beb433978be0d935862c3953350c82557aa32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:24.0.0-cli-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9c88bee6d1758fe02442a9f63d44488250d3fe2f1eeed02422e28cffde7a031a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50094511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386dea7015873d311819193f58ef3f374b4449a5a7deaeb50650bf9e54142db3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0.0-dind`

```console
$ docker pull docker@sha256:61580af84f2ed8b43e9ffc58213a0e068bd15bfb5ef3f28d0cffcb96bcb59fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:24.0.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e2889e32eb63f26495075e3e72c26c90d9dfddbe6b742eb099853240841a26f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106800114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1eada20d7ce614ccc2e919b00572bb0598c2db217e7310b2ef0b9ac4502474`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22442686bd72e2c0ecd000948826aebc8dcb3136fe1142b6ef334fa4a389f388`  
		Last Modified: Wed, 17 May 2023 00:04:11 GMT  
		Size: 7.2 MB (7245057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538120297d91ba480effca7fc88d637aab474129879b223a9120eb3d7648e0c3`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff4018a72e47b5a3546eb439499e864408cef1745148eb85b5af6026a7282`  
		Last Modified: Wed, 17 May 2023 00:04:15 GMT  
		Size: 49.5 MB (49455389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398e5219c811f7cb87f34450cf1a01a217122fcc492cbc68437dcee7fe05e156`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a054eb5e9d233a1fae4b8399984152cfd30e385282d002072fb7d5db6b0fdd84`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0.0-dind-alpine3.18`

```console
$ docker pull docker@sha256:61580af84f2ed8b43e9ffc58213a0e068bd15bfb5ef3f28d0cffcb96bcb59fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:24.0.0-dind-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e2889e32eb63f26495075e3e72c26c90d9dfddbe6b742eb099853240841a26f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106800114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1eada20d7ce614ccc2e919b00572bb0598c2db217e7310b2ef0b9ac4502474`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22442686bd72e2c0ecd000948826aebc8dcb3136fe1142b6ef334fa4a389f388`  
		Last Modified: Wed, 17 May 2023 00:04:11 GMT  
		Size: 7.2 MB (7245057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538120297d91ba480effca7fc88d637aab474129879b223a9120eb3d7648e0c3`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff4018a72e47b5a3546eb439499e864408cef1745148eb85b5af6026a7282`  
		Last Modified: Wed, 17 May 2023 00:04:15 GMT  
		Size: 49.5 MB (49455389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398e5219c811f7cb87f34450cf1a01a217122fcc492cbc68437dcee7fe05e156`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a054eb5e9d233a1fae4b8399984152cfd30e385282d002072fb7d5db6b0fdd84`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0.0-dind-rootless`

```console
$ docker pull docker@sha256:756d1568bc6c7ee6e753af1ccf4d7c5c38bc3f6632bb0005b9f12bfd9cc99aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:24.0.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d5fea20e13ddd78513d02a2331f6d31f1c48314431094bc8225a58a3e199628e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130662457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025c163c83c0cec89c2e216140bc53ad1a14a3841a37e30e5c248eadf340561e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 16 May 2023 17:59:38 GMT
USER rootless
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22442686bd72e2c0ecd000948826aebc8dcb3136fe1142b6ef334fa4a389f388`  
		Last Modified: Wed, 17 May 2023 00:04:11 GMT  
		Size: 7.2 MB (7245057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538120297d91ba480effca7fc88d637aab474129879b223a9120eb3d7648e0c3`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff4018a72e47b5a3546eb439499e864408cef1745148eb85b5af6026a7282`  
		Last Modified: Wed, 17 May 2023 00:04:15 GMT  
		Size: 49.5 MB (49455389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398e5219c811f7cb87f34450cf1a01a217122fcc492cbc68437dcee7fe05e156`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a054eb5e9d233a1fae4b8399984152cfd30e385282d002072fb7d5db6b0fdd84`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ee53f4852847948f043ca06a0787f96b227b7a89bd3a96c001e0a015ed0fa1`  
		Last Modified: Wed, 17 May 2023 00:04:45 GMT  
		Size: 1.4 MB (1413339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1da8cd837f1a67565e17645d233f693dd101d1f489eee2a9b9e539419953232`  
		Last Modified: Wed, 17 May 2023 00:04:45 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da12c61e018b49d59351af2c58c6aa2d838fd2c66bd096040afd3f98b37e39d`  
		Last Modified: Wed, 17 May 2023 00:04:45 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826a4dc1d8c55308e6d04bed73f3d53650e3a05a030d0b8e398968bae5148d96`  
		Last Modified: Wed, 17 May 2023 00:04:48 GMT  
		Size: 22.4 MB (22447264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39be7db13eba707e002fc9857aa46ae80d8c6c28c3a28f380b1a580aecb6e388`  
		Last Modified: Wed, 17 May 2023 00:04:45 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0.0-git`

```console
$ docker pull docker@sha256:b60f5335ffd4c3e5bd33c4e10566b71942f3febd1190a18a8096ccd9173c8379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `docker:24.0.0-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e080720de9821d7798727a4b42345477112b560895be9d75f7968b37ac9022d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111811702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30f0722482b8c94d89e4906b5e4f1e48a5e369c035ae13e74e088eee327baa1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22442686bd72e2c0ecd000948826aebc8dcb3136fe1142b6ef334fa4a389f388`  
		Last Modified: Wed, 17 May 2023 00:04:11 GMT  
		Size: 7.2 MB (7245057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538120297d91ba480effca7fc88d637aab474129879b223a9120eb3d7648e0c3`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff4018a72e47b5a3546eb439499e864408cef1745148eb85b5af6026a7282`  
		Last Modified: Wed, 17 May 2023 00:04:15 GMT  
		Size: 49.5 MB (49455389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398e5219c811f7cb87f34450cf1a01a217122fcc492cbc68437dcee7fe05e156`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a054eb5e9d233a1fae4b8399984152cfd30e385282d002072fb7d5db6b0fdd84`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee49b1c7c0b9892261471f527ffd51ada102f9143c374f52a4df759fa592242d`  
		Last Modified: Wed, 17 May 2023 00:05:04 GMT  
		Size: 5.0 MB (5011588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:24.0.0-windowsservercore`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:24.0.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:24.0.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:98d1cbfe8a5e890535d7921ab535cf55dc3759f4159a7509347e00b214330694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1726; amd64

### `docker:24.0.0-windowsservercore-ltsc2022` - windows version 10.0.20348.1726; amd64

```console
$ docker pull docker@sha256:c39f2cafaf7a2113f53ceabc666d4f3da44e4fed368541fd1e0fefb022779cdb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1826210257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996e23b75ca81e66d7030448de71db6aa0a76923181e45c812c20d718775ed7f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:13:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 17 May 2023 00:15:07 GMT
ENV DOCKER_VERSION=24.0.0
# Wed, 17 May 2023 00:15:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.0.zip
# Wed, 17 May 2023 00:15:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 17 May 2023 00:15:41 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 17 May 2023 00:15:42 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 17 May 2023 00:15:43 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 17 May 2023 00:16:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 17 May 2023 00:16:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Wed, 17 May 2023 00:16:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-windows-x86_64.exe
# Wed, 17 May 2023 00:16:13 GMT
ENV DOCKER_COMPOSE_SHA256=a98df8912c7a5cc7be00c1819a920e0ecdd5e2a7402bb390606c7f3f3b28b24e
# Wed, 17 May 2023 00:16:42 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d178a10e123ab9f41a66d7e6d8ffca4aab5fba57cf381f48bc0090f603be2d5`  
		Last Modified: Wed, 10 May 2023 01:45:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94bc80e6c1e6606bc432e9fa1ebc3ed83fe3ceb5a176e0a7b2c8334bf863c53`  
		Last Modified: Wed, 10 May 2023 07:11:29 GMT  
		Size: 446.9 KB (446946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754b058ebe9d76bf5f207307ce41413d0f5c8eaabaebaf489958f1363668d6b5`  
		Last Modified: Wed, 17 May 2023 00:24:02 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592e351bad5ff395b3b60e6392723040c6005e72ad9aae924bd1198ab972c214`  
		Last Modified: Wed, 17 May 2023 00:24:01 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e77e36d569e84596cf651b73f62ab576a440370c438558dfcfd78554cac113`  
		Last Modified: Wed, 17 May 2023 00:24:04 GMT  
		Size: 17.4 MB (17442983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9246257a5e5d53dfd7f0b5e864b6a266305e9c35842e58158de0b26304dbb4a3`  
		Last Modified: Wed, 17 May 2023 00:23:59 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39741ec300d3c142a9eae6a3710fe9bcefce767490369b7df1ace62a72eff3ff`  
		Last Modified: Wed, 17 May 2023 00:23:58 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4f248c6427e16274eb11e9b8deb80a40290e14da00b3fa9bd6d9e729e73490`  
		Last Modified: Wed, 17 May 2023 00:23:58 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30edc5d5771d539f50f8143e1308a12857cf8996cf2dcc0c7a4d780e12aaa13`  
		Last Modified: Wed, 17 May 2023 00:24:01 GMT  
		Size: 16.5 MB (16469255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3052c4cc6b687a78c47fc0cfd2c574efadb84263410c22ec610643c4c38e25`  
		Last Modified: Wed, 17 May 2023 00:23:55 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a922fb9abdb3020cdf8e738f697ac55457026c6ab8d778265e6037aa7c3c0bf`  
		Last Modified: Wed, 17 May 2023 00:23:55 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327393e9c7a5e9b1a3551c3b4f75bb0baf9d3729f9c9a0f160cae60519864a24`  
		Last Modified: Wed, 17 May 2023 00:23:55 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ad20660a7939522f8a6f7952e39828470c266a0a3224c9b645dfdfd816c062`  
		Last Modified: Wed, 17 May 2023 00:24:01 GMT  
		Size: 16.9 MB (16856921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:5c1665d39eb29adca7e8c1a73bb4bb419e6f94b5a6a8f06eb28240e5edaaf9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:cli` - linux; amd64

```console
$ docker pull docker@sha256:3b2d99643c86bfd09e5c2ae0c610a7820b755d71d270949f0b1e7e7ff9836ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54051122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ea5edbac8ee1fa4488a13fcf136fa3eeaff8c92b78ce78993f60a07967de99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9c88bee6d1758fe02442a9f63d44488250d3fe2f1eeed02422e28cffde7a031a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50094511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386dea7015873d311819193f58ef3f374b4449a5a7deaeb50650bf9e54142db3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind`

```console
$ docker pull docker@sha256:305f795d52bdb6680ac10b647e42a6abe634c045438289063a07f381d90119dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:af8a4eb8e61f87ea50c72057624c1710dd0c6356d74e64465bc01123c7d37795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112738963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4966f34e6de695acc18297ea9b1c513a58c4048554aaaac4f10bf6080be3b32`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 15 May 2023 22:39:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/var/lib/docker]
# Mon, 15 May 2023 22:39:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 15 May 2023 22:39:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 15 May 2023 22:39:50 GMT
CMD []
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058b1c95dcd434f93391bf0ec0c404ae630b363de88563fa9a4a4d3c6889b90`  
		Last Modified: Thu, 11 May 2023 19:25:14 GMT  
		Size: 7.0 MB (7025224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1c4c35af9e9b29cde02d3d5b488ed71b7821d39319354f4aba1a8ae8ace24`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d938c8b2399339aaf8caeefbdc85c8b8dddf7d27d57d8c3d09bf070e0a4374b`  
		Last Modified: Thu, 11 May 2023 19:25:20 GMT  
		Size: 51.7 MB (51657452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2885b54919758712d2ab1b9d1e43574e5fa8d8fe06612e193c876de7d221ea`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3ce26085aa03b6fc712003b8cd4e3675c6975181aca50368e8af84866d7b9e`  
		Last Modified: Tue, 16 May 2023 00:21:06 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e2889e32eb63f26495075e3e72c26c90d9dfddbe6b742eb099853240841a26f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106800114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1eada20d7ce614ccc2e919b00572bb0598c2db217e7310b2ef0b9ac4502474`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22442686bd72e2c0ecd000948826aebc8dcb3136fe1142b6ef334fa4a389f388`  
		Last Modified: Wed, 17 May 2023 00:04:11 GMT  
		Size: 7.2 MB (7245057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538120297d91ba480effca7fc88d637aab474129879b223a9120eb3d7648e0c3`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff4018a72e47b5a3546eb439499e864408cef1745148eb85b5af6026a7282`  
		Last Modified: Wed, 17 May 2023 00:04:15 GMT  
		Size: 49.5 MB (49455389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398e5219c811f7cb87f34450cf1a01a217122fcc492cbc68437dcee7fe05e156`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a054eb5e9d233a1fae4b8399984152cfd30e385282d002072fb7d5db6b0fdd84`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:736a5b9015e149b42af36fdbcf81a0a41f0fbf4173bbe4e265278d03cbb9aa68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:3d5b0a0a81a2b8770652468b38847721050af219e94c5711a9a7bc8e8cdc1333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134450185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272062036ead322e794888251164e54b81a1f64cba944eda4f84db8d820accae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 15 May 2023 22:39:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/var/lib/docker]
# Mon, 15 May 2023 22:39:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 15 May 2023 22:39:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 15 May 2023 22:39:50 GMT
CMD []
# Mon, 15 May 2023 22:39:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 15 May 2023 22:39:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058b1c95dcd434f93391bf0ec0c404ae630b363de88563fa9a4a4d3c6889b90`  
		Last Modified: Thu, 11 May 2023 19:25:14 GMT  
		Size: 7.0 MB (7025224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1c4c35af9e9b29cde02d3d5b488ed71b7821d39319354f4aba1a8ae8ace24`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d938c8b2399339aaf8caeefbdc85c8b8dddf7d27d57d8c3d09bf070e0a4374b`  
		Last Modified: Thu, 11 May 2023 19:25:20 GMT  
		Size: 51.7 MB (51657452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2885b54919758712d2ab1b9d1e43574e5fa8d8fe06612e193c876de7d221ea`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3ce26085aa03b6fc712003b8cd4e3675c6975181aca50368e8af84866d7b9e`  
		Last Modified: Tue, 16 May 2023 00:21:06 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98ac734fba950213b5eef3e34a74cfb050771d2dcfb9e09bf8849e430a97171`  
		Last Modified: Tue, 16 May 2023 00:21:32 GMT  
		Size: 1.4 MB (1362380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a2dc52b58512c04b6f21d9013089f46e944d25ee401bf249410fbfee0a386a`  
		Last Modified: Tue, 16 May 2023 00:21:32 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d714531a153f83a639d0577eb97fbabde8a658d045e1a5934d0fdd66e1647e`  
		Last Modified: Tue, 16 May 2023 00:21:32 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d363f0101be8e2f3cf083449298d611caf75351c46d338317982af0bac53317e`  
		Last Modified: Tue, 16 May 2023 00:21:35 GMT  
		Size: 20.3 MB (20347094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9fecae1fab5b25b43bb2d749c2266c981b255b6ab3505f483a58c208da98e4e`  
		Last Modified: Tue, 16 May 2023 00:21:32 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d5fea20e13ddd78513d02a2331f6d31f1c48314431094bc8225a58a3e199628e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130662457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025c163c83c0cec89c2e216140bc53ad1a14a3841a37e30e5c248eadf340561e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 16 May 2023 17:59:38 GMT
USER rootless
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22442686bd72e2c0ecd000948826aebc8dcb3136fe1142b6ef334fa4a389f388`  
		Last Modified: Wed, 17 May 2023 00:04:11 GMT  
		Size: 7.2 MB (7245057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538120297d91ba480effca7fc88d637aab474129879b223a9120eb3d7648e0c3`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff4018a72e47b5a3546eb439499e864408cef1745148eb85b5af6026a7282`  
		Last Modified: Wed, 17 May 2023 00:04:15 GMT  
		Size: 49.5 MB (49455389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398e5219c811f7cb87f34450cf1a01a217122fcc492cbc68437dcee7fe05e156`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a054eb5e9d233a1fae4b8399984152cfd30e385282d002072fb7d5db6b0fdd84`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ee53f4852847948f043ca06a0787f96b227b7a89bd3a96c001e0a015ed0fa1`  
		Last Modified: Wed, 17 May 2023 00:04:45 GMT  
		Size: 1.4 MB (1413339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1da8cd837f1a67565e17645d233f693dd101d1f489eee2a9b9e539419953232`  
		Last Modified: Wed, 17 May 2023 00:04:45 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da12c61e018b49d59351af2c58c6aa2d838fd2c66bd096040afd3f98b37e39d`  
		Last Modified: Wed, 17 May 2023 00:04:45 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826a4dc1d8c55308e6d04bed73f3d53650e3a05a030d0b8e398968bae5148d96`  
		Last Modified: Wed, 17 May 2023 00:04:48 GMT  
		Size: 22.4 MB (22447264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39be7db13eba707e002fc9857aa46ae80d8c6c28c3a28f380b1a580aecb6e388`  
		Last Modified: Wed, 17 May 2023 00:04:45 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:git`

```console
$ docker pull docker@sha256:e16a01960e6020b96635fd02087b2ceef1815fc73305867b5a141f73110d7882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:e0a9ff309d9d4d49f145163565cf50106de9bb15023321d9f6027da8243fba86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117658830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd2153f16eee41cf91fc1f892e613b7acfd0411a50ed24492a54719464d87a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 15 May 2023 22:39:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/var/lib/docker]
# Mon, 15 May 2023 22:39:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 15 May 2023 22:39:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 15 May 2023 22:39:50 GMT
CMD []
# Mon, 15 May 2023 22:39:50 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058b1c95dcd434f93391bf0ec0c404ae630b363de88563fa9a4a4d3c6889b90`  
		Last Modified: Thu, 11 May 2023 19:25:14 GMT  
		Size: 7.0 MB (7025224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1c4c35af9e9b29cde02d3d5b488ed71b7821d39319354f4aba1a8ae8ace24`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d938c8b2399339aaf8caeefbdc85c8b8dddf7d27d57d8c3d09bf070e0a4374b`  
		Last Modified: Thu, 11 May 2023 19:25:20 GMT  
		Size: 51.7 MB (51657452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2885b54919758712d2ab1b9d1e43574e5fa8d8fe06612e193c876de7d221ea`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3ce26085aa03b6fc712003b8cd4e3675c6975181aca50368e8af84866d7b9e`  
		Last Modified: Tue, 16 May 2023 00:21:06 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0eaf8da2ec7a0ad445e808e182a80a080ca992008cce921c5013474d44087e`  
		Last Modified: Tue, 16 May 2023 00:21:51 GMT  
		Size: 4.9 MB (4919867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e080720de9821d7798727a4b42345477112b560895be9d75f7968b37ac9022d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111811702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30f0722482b8c94d89e4906b5e4f1e48a5e369c035ae13e74e088eee327baa1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22442686bd72e2c0ecd000948826aebc8dcb3136fe1142b6ef334fa4a389f388`  
		Last Modified: Wed, 17 May 2023 00:04:11 GMT  
		Size: 7.2 MB (7245057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538120297d91ba480effca7fc88d637aab474129879b223a9120eb3d7648e0c3`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff4018a72e47b5a3546eb439499e864408cef1745148eb85b5af6026a7282`  
		Last Modified: Wed, 17 May 2023 00:04:15 GMT  
		Size: 49.5 MB (49455389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398e5219c811f7cb87f34450cf1a01a217122fcc492cbc68437dcee7fe05e156`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a054eb5e9d233a1fae4b8399984152cfd30e385282d002072fb7d5db6b0fdd84`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee49b1c7c0b9892261471f527ffd51ada102f9143c374f52a4df759fa592242d`  
		Last Modified: Wed, 17 May 2023 00:05:04 GMT  
		Size: 5.0 MB (5011588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:latest`

```console
$ docker pull docker@sha256:305f795d52bdb6680ac10b647e42a6abe634c045438289063a07f381d90119dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:af8a4eb8e61f87ea50c72057624c1710dd0c6356d74e64465bc01123c7d37795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112738963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4966f34e6de695acc18297ea9b1c513a58c4048554aaaac4f10bf6080be3b32`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 15 May 2023 22:39:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/var/lib/docker]
# Mon, 15 May 2023 22:39:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 15 May 2023 22:39:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 15 May 2023 22:39:50 GMT
CMD []
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058b1c95dcd434f93391bf0ec0c404ae630b363de88563fa9a4a4d3c6889b90`  
		Last Modified: Thu, 11 May 2023 19:25:14 GMT  
		Size: 7.0 MB (7025224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1c4c35af9e9b29cde02d3d5b488ed71b7821d39319354f4aba1a8ae8ace24`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d938c8b2399339aaf8caeefbdc85c8b8dddf7d27d57d8c3d09bf070e0a4374b`  
		Last Modified: Thu, 11 May 2023 19:25:20 GMT  
		Size: 51.7 MB (51657452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2885b54919758712d2ab1b9d1e43574e5fa8d8fe06612e193c876de7d221ea`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3ce26085aa03b6fc712003b8cd4e3675c6975181aca50368e8af84866d7b9e`  
		Last Modified: Tue, 16 May 2023 00:21:06 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e2889e32eb63f26495075e3e72c26c90d9dfddbe6b742eb099853240841a26f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106800114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1eada20d7ce614ccc2e919b00572bb0598c2db217e7310b2ef0b9ac4502474`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22442686bd72e2c0ecd000948826aebc8dcb3136fe1142b6ef334fa4a389f388`  
		Last Modified: Wed, 17 May 2023 00:04:11 GMT  
		Size: 7.2 MB (7245057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538120297d91ba480effca7fc88d637aab474129879b223a9120eb3d7648e0c3`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff4018a72e47b5a3546eb439499e864408cef1745148eb85b5af6026a7282`  
		Last Modified: Wed, 17 May 2023 00:04:15 GMT  
		Size: 49.5 MB (49455389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398e5219c811f7cb87f34450cf1a01a217122fcc492cbc68437dcee7fe05e156`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a054eb5e9d233a1fae4b8399984152cfd30e385282d002072fb7d5db6b0fdd84`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:5ece48bf73b8c468e9da42e73104a47deb073ce38dff0342c64b8d5fd1c1aac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1726; amd64
	-	windows version 10.0.17763.4377; amd64

### `docker:windowsservercore` - windows version 10.0.20348.1726; amd64

```console
$ docker pull docker@sha256:49feec5ed8108d054e24262a0263775b0dea7ea6161420279ead5035f8f7ca2a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1826042174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb39d95d7392898fc2a92fe045c7948e23bac13e88a2771b9628a6fcd00df72`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:13:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 May 2023 03:24:47 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 03:24:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Wed, 10 May 2023 03:25:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:25:32 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 03:25:32 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 10 May 2023 03:25:33 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 10 May 2023 03:25:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:25:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 03:25:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-windows-x86_64.exe
# Wed, 10 May 2023 03:25:59 GMT
ENV DOCKER_COMPOSE_SHA256=556cc1d373503a897ecc2def998a40b2ad1fe27ff049769eb912c7e208772e74
# Wed, 10 May 2023 03:26:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d178a10e123ab9f41a66d7e6d8ffca4aab5fba57cf381f48bc0090f603be2d5`  
		Last Modified: Wed, 10 May 2023 01:45:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94bc80e6c1e6606bc432e9fa1ebc3ed83fe3ceb5a176e0a7b2c8334bf863c53`  
		Last Modified: Wed, 10 May 2023 07:11:29 GMT  
		Size: 446.9 KB (446946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e927fbd88402bacc902c2a4593f281068b2a6657c7f8b4e53ac01f8e636901`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165e88795de1230f78ac3b0186a534bd16fad90474fddb00254443f5440c8c65`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438806a743132696d59ff6500d80c1c45b0742da1613dbde135436ef14f725af`  
		Last Modified: Wed, 10 May 2023 07:12:05 GMT  
		Size: 17.3 MB (17316446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c96495f4df59195a31aba0ef651c79d5519baf34e22333d63d5a8bfe03900b`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f5f979d4f16ed05773444607ec525a26e8c703f03f102d8759e864981d5c82`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d23d10667208a1b8d0f8e33582643dd1c513834082f55a73336deecf2b3e829`  
		Last Modified: Wed, 10 May 2023 07:12:00 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f367dbae07d50a7ea9664467f0f6935dd7ba395cf98c8f7d2e39925ff3f64e`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 16.5 MB (16457754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2158efcafa6303ace2a8d3f0d2442bddd73799341b2a6258c21abd8bd7fcac`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4a3d8cbc64bd1d463e94f091e7177ec22f9f28eb318370cdb0506d93494666`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca474991c2a553554d33df3995317383bfa4ec8b4f4249b931de5a485a27adc`  
		Last Modified: Wed, 10 May 2023 07:11:58 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b95097e5ada96414856478813a948262a40d9c84537402939e98cd82036573`  
		Last Modified: Wed, 10 May 2023 07:12:02 GMT  
		Size: 16.8 MB (16826864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.4377; amd64

```console
$ docker pull docker@sha256:ce1be907c58a74261c54ae870470d5c36ef2f63674c4e4cf8372e83777330ac4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2123136881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136da637bc1dc002acdb31b90bd13bb45820f2e95343006a0e97d66e2e39037b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:16:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 May 2023 03:26:29 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 03:26:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.6.zip
# Wed, 10 May 2023 03:27:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:27:42 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 03:27:43 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 10 May 2023 03:27:43 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 10 May 2023 03:28:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 03:28:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 03:28:54 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-windows-x86_64.exe
# Wed, 10 May 2023 03:28:55 GMT
ENV DOCKER_COMPOSE_SHA256=556cc1d373503a897ecc2def998a40b2ad1fe27ff049769eb912c7e208772e74
# Wed, 10 May 2023 03:30:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5869a0b27170ed378e5d22763ab388eaf4a9dbd91cb7eaee4cef7d8639a2ff74`  
		Last Modified: Wed, 10 May 2023 07:11:47 GMT  
		Size: 451.5 KB (451506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470efce6095b6077dfd4d6bac6f6e2010f4d5bcdf636e954d0c3e9051baa7a30`  
		Last Modified: Wed, 10 May 2023 07:12:22 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf94d195dbf8bcb75f6433208dda2b0af64c556bf5eed006468d61cccf49971`  
		Last Modified: Wed, 10 May 2023 07:12:22 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f57c72aed2637dc5fc359ff575642812168a390b96d73791c2e00a8aa6c341`  
		Last Modified: Wed, 10 May 2023 07:12:25 GMT  
		Size: 17.3 MB (17330027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3802307c89ea480234035e4a743bf5fcb7af504addfaeeccdae1e83d0286ea03`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf5c7bff562bb1a033d8a2f465437525a829a56113ca6204efed01ecd6ba653`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6608073b14838ddabd4f13d2848b33488d2a7e42d3646245fc6f163e333e551`  
		Last Modified: Wed, 10 May 2023 07:12:20 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412458425ced3171f449f28b8c40912d57931270d9d427efe39dfc669c81baa1`  
		Last Modified: Wed, 10 May 2023 07:12:23 GMT  
		Size: 16.5 MB (16467670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef29bfe39940055963010676df5645f3c05482f819eb0a729b16d43c7bc3af8`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ee6d41023794ee61421888956d914f83fedaedc16321d0aa3d0ac7e1315c25`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adecc2295964edd8cc0fd6feb81e6c3d28e20be1318d1b70c52acac1651a769b`  
		Last Modified: Wed, 10 May 2023 07:12:18 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8302c4a8fb9f7dfb47a9992223517957000b185668adcb36a0e3f24b913406`  
		Last Modified: Wed, 10 May 2023 07:12:23 GMT  
		Size: 16.8 MB (16839833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:665b4c02c553f700f3903f0f5ac07ad8b6bd51bff964865f0fb9d1bfa704dd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull docker@sha256:fcb85505ec865447d0aed1b5bab48a698051ff070db02daaa5bd870a058758ef
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2123337444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9edeceb20c70d9069b5a0fc3b8d4dd79ef4e8f8f20215655f7b3ed669f6d5655`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:16:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 17 May 2023 00:16:49 GMT
ENV DOCKER_VERSION=24.0.0
# Wed, 17 May 2023 00:16:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.0.zip
# Wed, 17 May 2023 00:18:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 17 May 2023 00:18:09 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 17 May 2023 00:18:10 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 17 May 2023 00:18:11 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 17 May 2023 00:19:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 17 May 2023 00:19:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Wed, 17 May 2023 00:19:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-windows-x86_64.exe
# Wed, 17 May 2023 00:19:30 GMT
ENV DOCKER_COMPOSE_SHA256=a98df8912c7a5cc7be00c1819a920e0ecdd5e2a7402bb390606c7f3f3b28b24e
# Wed, 17 May 2023 00:20:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5869a0b27170ed378e5d22763ab388eaf4a9dbd91cb7eaee4cef7d8639a2ff74`  
		Last Modified: Wed, 10 May 2023 07:11:47 GMT  
		Size: 451.5 KB (451506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb10affc8126734dd238241f8b3d9b71ceb5438dbbf84ee566a608cabf606cf`  
		Last Modified: Wed, 17 May 2023 00:24:26 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2fa9db965b5b82349ba01960f80952db3950276056ab9d6bb71b6d03285657`  
		Last Modified: Wed, 17 May 2023 00:24:25 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488def41cc4d70f5f7d926c623387e4f9de65a96a76a26c93c69f8793794ff52`  
		Last Modified: Wed, 17 May 2023 00:24:28 GMT  
		Size: 17.5 MB (17474717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19e5946eb44fb1d2408597a8aa7c915a48a67152dd3580b096f2a2ef09ebe56`  
		Last Modified: Wed, 17 May 2023 00:24:23 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba14be958dafdb9c8bddb473c4d9f6a413ea8000553bc33052a094f072e7c81`  
		Last Modified: Wed, 17 May 2023 00:24:23 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf7ee67a691dc1e667d0b7f5a05c35d769e974da4d0610c7b33baeafff6e747`  
		Last Modified: Wed, 17 May 2023 00:24:23 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af36c6acb9577a67a110ace2b0eceb25a9bc040e3f0b139c60365116199d177d`  
		Last Modified: Wed, 17 May 2023 00:24:26 GMT  
		Size: 16.5 MB (16489581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4666710f418290fa73b37425fd70664b5225d7f3db0911d6fa516b156ed9e76`  
		Last Modified: Wed, 17 May 2023 00:24:21 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc16c515a2893706cf28df91b18301845e669020c787da40e3829b4b5e7061`  
		Last Modified: Wed, 17 May 2023 00:24:21 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7db07e583aca75ac9f8e3c7a696c79216b441ca799ea4aea1e19d81f8efb9e0`  
		Last Modified: Wed, 17 May 2023 00:24:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ac593855ec5ef54040bdd7847c5dd2e71fda55d1f38b7e67441fa4ed0fe0a6`  
		Last Modified: Wed, 17 May 2023 00:24:26 GMT  
		Size: 16.9 MB (16873694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:98d1cbfe8a5e890535d7921ab535cf55dc3759f4159a7509347e00b214330694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1726; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.1726; amd64

```console
$ docker pull docker@sha256:c39f2cafaf7a2113f53ceabc666d4f3da44e4fed368541fd1e0fefb022779cdb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1826210257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996e23b75ca81e66d7030448de71db6aa0a76923181e45c812c20d718775ed7f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:13:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 17 May 2023 00:15:07 GMT
ENV DOCKER_VERSION=24.0.0
# Wed, 17 May 2023 00:15:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.0.zip
# Wed, 17 May 2023 00:15:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 17 May 2023 00:15:41 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 17 May 2023 00:15:42 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 17 May 2023 00:15:43 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 17 May 2023 00:16:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 17 May 2023 00:16:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Wed, 17 May 2023 00:16:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-windows-x86_64.exe
# Wed, 17 May 2023 00:16:13 GMT
ENV DOCKER_COMPOSE_SHA256=a98df8912c7a5cc7be00c1819a920e0ecdd5e2a7402bb390606c7f3f3b28b24e
# Wed, 17 May 2023 00:16:42 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d178a10e123ab9f41a66d7e6d8ffca4aab5fba57cf381f48bc0090f603be2d5`  
		Last Modified: Wed, 10 May 2023 01:45:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94bc80e6c1e6606bc432e9fa1ebc3ed83fe3ceb5a176e0a7b2c8334bf863c53`  
		Last Modified: Wed, 10 May 2023 07:11:29 GMT  
		Size: 446.9 KB (446946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754b058ebe9d76bf5f207307ce41413d0f5c8eaabaebaf489958f1363668d6b5`  
		Last Modified: Wed, 17 May 2023 00:24:02 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592e351bad5ff395b3b60e6392723040c6005e72ad9aae924bd1198ab972c214`  
		Last Modified: Wed, 17 May 2023 00:24:01 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e77e36d569e84596cf651b73f62ab576a440370c438558dfcfd78554cac113`  
		Last Modified: Wed, 17 May 2023 00:24:04 GMT  
		Size: 17.4 MB (17442983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9246257a5e5d53dfd7f0b5e864b6a266305e9c35842e58158de0b26304dbb4a3`  
		Last Modified: Wed, 17 May 2023 00:23:59 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39741ec300d3c142a9eae6a3710fe9bcefce767490369b7df1ace62a72eff3ff`  
		Last Modified: Wed, 17 May 2023 00:23:58 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4f248c6427e16274eb11e9b8deb80a40290e14da00b3fa9bd6d9e729e73490`  
		Last Modified: Wed, 17 May 2023 00:23:58 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30edc5d5771d539f50f8143e1308a12857cf8996cf2dcc0c7a4d780e12aaa13`  
		Last Modified: Wed, 17 May 2023 00:24:01 GMT  
		Size: 16.5 MB (16469255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3052c4cc6b687a78c47fc0cfd2c574efadb84263410c22ec610643c4c38e25`  
		Last Modified: Wed, 17 May 2023 00:23:55 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a922fb9abdb3020cdf8e738f697ac55457026c6ab8d778265e6037aa7c3c0bf`  
		Last Modified: Wed, 17 May 2023 00:23:55 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327393e9c7a5e9b1a3551c3b4f75bb0baf9d3729f9c9a0f160cae60519864a24`  
		Last Modified: Wed, 17 May 2023 00:23:55 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ad20660a7939522f8a6f7952e39828470c266a0a3224c9b645dfdfd816c062`  
		Last Modified: Wed, 17 May 2023 00:24:01 GMT  
		Size: 16.9 MB (16856921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
