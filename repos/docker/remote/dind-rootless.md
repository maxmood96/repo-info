## `docker:dind-rootless`

```console
$ docker pull docker@sha256:1c3d8dd8b7d51320ceed85cb59c13c8e525758121fd54e9a2eaccf297a7db3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:4ff6e32c46b4798b965ac477fe8fef7066ee7bb10d9214d21e13ee2e10713a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140473529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1f8ff044c7f7eff3b3fa28cb89e4c985fb3983b61d049be0c7a69edbbf92d1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 21 Jun 2023 17:05:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 21 Jun 2023 17:05:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 21 Jun 2023 17:05:45 GMT
ENV DOCKER_VERSION=24.0.2
# Wed, 21 Jun 2023 17:05:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 21 Jun 2023 17:05:45 GMT
ENV DOCKER_BUILDX_VERSION=0.11.0
# Wed, 21 Jun 2023 17:05:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-amd64'; 			sha256='ec2c9da22c3b733ad96d6a6897750153d884f1b2b86f2864ee5f743ce931055d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-arm-v6'; 			sha256='a925462288a55b709a42431fe39bb0e67f033961f02a4754897c4a388355feea'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-arm-v7'; 			sha256='e3f18a0d10346d8e53aff743fccfc0b95e45dc0235c3b0b72b49d3452c72b9e0'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-arm64'; 			sha256='e50f34f8feb7004407f826a375090bec6191891c473347b41b05cf5864bc5240'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-ppc64le'; 			sha256='de8670ab6b2c34feb32289d04af07014bb4517de879d1fdb6e31a00da28f1df4'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-riscv64'; 			sha256='a07ad5791d6e60094e38147ef5f5eac406b2692aa380eae5ac866bde91bcdc89'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-s390x'; 			sha256='fc1a57b9fb69f7736908bbea94013eb17b5ae03cd5ed99b0bd61e223f9b6e4a7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 21 Jun 2023 17:05:45 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.0
# Wed, 21 Jun 2023 17:05:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.0/docker-compose-linux-x86_64'; 			sha256='34e3b754d13eab683222f67827e20f640dfe0630b3b786c49a9de3f7fc7400a6'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.0/docker-compose-linux-armv6'; 			sha256='49ba58cabcdc0778507f152baa2a84ef5d1417ac3dc4d7f4fbd492a77ec0638b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.0/docker-compose-linux-armv7'; 			sha256='0c0e3af9ae2b833e09b303899ef3330d40c09ec13a4def861c22b3d0a7ec8540'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.0/docker-compose-linux-aarch64'; 			sha256='c963c6d913a57e0571104ecb8f8ba0502516eafd7b784b5abc4a0d96ebb54d04'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.0/docker-compose-linux-ppc64le'; 			sha256='317696f8a7cefc244d2e97779b926da93ce3bfb95be5ca56dde868c495560d50'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.0/docker-compose-linux-riscv64'; 			sha256='e1b150cb49b34598c7b06985df5f19268394869902e787aa6a0542e700c20a50'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.0/docker-compose-linux-s390x'; 			sha256='83cb57f3b8025afd7002f0ab48056e857ce2d8aece9ff47193c772d05966a137'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 21 Jun 2023 17:05:45 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 21 Jun 2023 17:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jun 2023 17:05:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 21 Jun 2023 17:05:45 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 21 Jun 2023 17:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jun 2023 17:05:45 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:05:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:05:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:05:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:05:39 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:05:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:05:39 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:05:39 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:05:39 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:05:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:05:39 GMT
CMD []
# Fri, 26 May 2023 11:04:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 26 May 2023 11:04:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 26 May 2023 11:04:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 26 May 2023 11:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 26 May 2023 11:04:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 26 May 2023 11:04:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 26 May 2023 11:04:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366db03861711486fedda5cd6f1359c0261a1734594df3a61eafc2e920d92488`  
		Last Modified: Thu, 15 Jun 2023 05:27:07 GMT  
		Size: 16.4 MB (16376159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e922f84bca8da20b7db33748ee6660acc3629598bc8e5f5e7bc158c08339a426`  
		Last Modified: Thu, 15 Jun 2023 05:27:06 GMT  
		Size: 17.5 MB (17450708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061e30d30e9db09099cc0d089baa2f67758bd2488120c38d7dcb692e8b4f2ee2`  
		Last Modified: Thu, 22 Jun 2023 00:20:55 GMT  
		Size: 18.0 MB (17978984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b85ee8a5cc7b2ce91ddcab20590d44f7474c131658349b82319438233a1cab`  
		Last Modified: Thu, 22 Jun 2023 00:20:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a9d0187a043c57714b0e18e32cf0cf6e978ea072dc1b01d610ae6da421db3f`  
		Last Modified: Thu, 22 Jun 2023 00:20:52 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c95c19c4b4b01a8bf6f238239fa63ae67e71ae636c0c3dc6b4f2a8cce37678`  
		Last Modified: Thu, 22 Jun 2023 00:20:51 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b23bc32942f4f44ea8784d25ebffe30179c20c9ea3e9cd63715c46f8adc4f16`  
		Last Modified: Thu, 22 Jun 2023 00:21:11 GMT  
		Size: 7.1 MB (7080765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bba840244334cb68cbf88f959009af2c0c6cb7cb0e4734c9ac58eae06b2f22d`  
		Last Modified: Thu, 22 Jun 2023 00:21:09 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee990d83c62e41383305cceaa092e7dad6e2f34a716cb9563f846f876d99a174`  
		Last Modified: Thu, 22 Jun 2023 00:21:17 GMT  
		Size: 54.2 MB (54155473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22f484fbc3f760f991a1c3c9344c2a893ce8727629babc5d3f1eb97ebc312cc`  
		Last Modified: Thu, 22 Jun 2023 00:21:09 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b5d94921fb65559e031545640f58e47c9ebaa0f1935cd40d48dec8b98f27df`  
		Last Modified: Thu, 22 Jun 2023 00:21:09 GMT  
		Size: 2.8 KB (2792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e609f3ff46f779e74f1ec8a604ac6e8fe03c065be7586001c6828792756142`  
		Last Modified: Thu, 22 Jun 2023 00:21:47 GMT  
		Size: 1.4 MB (1362356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ad3281ae4efdad8fdbb55297cd0e8265bb4ad3c1fd7e7e5aa53a0368e43d06`  
		Last Modified: Thu, 22 Jun 2023 00:21:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1a43511db2a5d109910c8f1ae2b429e56c4a2d574ccf96330f8b25b25e82d1`  
		Last Modified: Thu, 22 Jun 2023 00:21:47 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d36cb9bb3920f55d94586989f8e7b33da643cd9a2825507ca7811fad3aaa42`  
		Last Modified: Thu, 22 Jun 2023 00:21:50 GMT  
		Size: 20.6 MB (20648107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0920472c0a1deea34691ccc0246d085d4ac7c54e2936d9ed5146fe45c45d7eb1`  
		Last Modified: Thu, 22 Jun 2023 00:21:47 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:371d5cab8af7045313eb35e128caf9f6b37e2eefcb6592ccf388c8e63a36b721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133468784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60b9329aad0fb988800150f788731cbcba7523b0ca0b966400de69edc359711`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 29 Jun 2023 23:05:40 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 29 Jun 2023 23:05:40 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 29 Jun 2023 23:05:40 GMT
ENV DOCKER_VERSION=24.0.2
# Thu, 29 Jun 2023 23:05:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 29 Jun 2023 23:05:40 GMT
ENV DOCKER_BUILDX_VERSION=0.11.0
# Thu, 29 Jun 2023 23:05:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-amd64'; 			sha256='ec2c9da22c3b733ad96d6a6897750153d884f1b2b86f2864ee5f743ce931055d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-arm-v6'; 			sha256='a925462288a55b709a42431fe39bb0e67f033961f02a4754897c4a388355feea'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-arm-v7'; 			sha256='e3f18a0d10346d8e53aff743fccfc0b95e45dc0235c3b0b72b49d3452c72b9e0'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-arm64'; 			sha256='e50f34f8feb7004407f826a375090bec6191891c473347b41b05cf5864bc5240'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-ppc64le'; 			sha256='de8670ab6b2c34feb32289d04af07014bb4517de879d1fdb6e31a00da28f1df4'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-riscv64'; 			sha256='a07ad5791d6e60094e38147ef5f5eac406b2692aa380eae5ac866bde91bcdc89'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-s390x'; 			sha256='fc1a57b9fb69f7736908bbea94013eb17b5ae03cd5ed99b0bd61e223f9b6e4a7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 29 Jun 2023 23:05:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 29 Jun 2023 23:05:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-x86_64'; 			sha256='8d3ecd3e48c598ba2e2d8eb3b59380f74c8c0c46259008fcd16d0dc058aaebd1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv6'; 			sha256='78639fa8323f0f60cd8b45a882bbb63cc630b44a7187e922195855cb64607d8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-armv7'; 			sha256='bc9646ecf835e5e2665b7de6455c07cb21d4e892a4c212f9ca9f3024a26ff880'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-aarch64'; 			sha256='35db0e5207c66e002bfde3cab84e907aa7e552812803bebebf990487729eb2bf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-ppc64le'; 			sha256='9c79eada1314e63734eb33e9d1815b5f494c357b45ac1c3ec035188ee616f215'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-riscv64'; 			sha256='bcca185b3f1f2e6dbb392149f52676075b1e42ba64a3ed6508c2f9fc1b60c634'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-linux-s390x'; 			sha256='152e40b9f600b84223b8c2f217c45ed4813af8cdd98017cdcbdb35b81423f8d9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 29 Jun 2023 23:05:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 29 Jun 2023 23:05:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Jun 2023 23:05:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 29 Jun 2023 23:05:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 29 Jun 2023 23:05:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jun 2023 23:05:40 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:05:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:05:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:05:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:05:39 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:05:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:05:39 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:05:39 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:05:39 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:05:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:05:39 GMT
CMD []
# Fri, 26 May 2023 11:04:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 26 May 2023 11:04:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 26 May 2023 11:04:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 26 May 2023 11:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 26 May 2023 11:04:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 26 May 2023 11:04:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 26 May 2023 11:04:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9586bf63fa36870e788c8a018102294740f7423584b67cd9109415feef2bfd5e`  
		Last Modified: Wed, 14 Jun 2023 22:40:53 GMT  
		Size: 15.4 MB (15422673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1478b55d813a1aa989a4c3214a2e2dc0570eec3865fceae167d1ee66a440f4`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 15.8 MB (15758023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fdc50f005e049694ace3914d5f1f6136e60a11bc5fb52e3674636187dfce13`  
		Last Modified: Tue, 04 Jul 2023 00:40:34 GMT  
		Size: 16.3 MB (16312961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18eaf9e0867e77c4aae4ae3ee7f8498ee6910b33df6cc7d7aabb052254ccf0e`  
		Last Modified: Tue, 04 Jul 2023 00:40:32 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288c6f8cca98a591de3bef3f72fa6e72fa05dc48bb7c151357d269f105e282c0`  
		Last Modified: Tue, 04 Jul 2023 00:40:32 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d003c443699d93502858aade5b1103c74cb7f7b79f755eafde9b1707109ceebc`  
		Last Modified: Tue, 04 Jul 2023 00:40:32 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1122c74b8be96849feb2df27205900943e9489cbbbc1514aee6341f89ebabe58`  
		Last Modified: Tue, 04 Jul 2023 00:40:49 GMT  
		Size: 7.3 MB (7291367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0511e4472f995553892e3e9eae1730dc479f27d73911845e35b8a648960a6c`  
		Last Modified: Tue, 04 Jul 2023 00:40:48 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3a8d1362fe35fbba16eb34c7b62a9f554d6d09db79e1560094c8a1b0e9586c`  
		Last Modified: Tue, 04 Jul 2023 00:40:53 GMT  
		Size: 49.5 MB (49460720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26e466edb290083b7bad6147362cf043f9ea4c75d3880f27f6efe5c1d593202`  
		Last Modified: Tue, 04 Jul 2023 00:40:48 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f5cadd9777ec0b50d9325a74a31b97784cf9fd06e98da3436edda7c2bc4003`  
		Last Modified: Tue, 04 Jul 2023 00:40:48 GMT  
		Size: 2.8 KB (2795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f714784001e9d8c14948baac4835ded976982aac8a222a9b2a2791f59cd58d5`  
		Last Modified: Tue, 04 Jul 2023 00:41:21 GMT  
		Size: 1.4 MB (1413240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66eabe53b410390d19d597c4ab31ee16cd0f77b5efa4e85e6d93fc1c3aeebfa`  
		Last Modified: Tue, 04 Jul 2023 00:41:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65ef0e8cf7c2b897cd9fd8758cd812be95d2ae0f90bd4767c30b891e552e0ef`  
		Last Modified: Tue, 04 Jul 2023 00:41:21 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c421e62f4bf588f68492e056bcd6c83f0a2752dc121219df0291109930a0d1e0`  
		Last Modified: Tue, 04 Jul 2023 00:41:24 GMT  
		Size: 22.4 MB (22447282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dced6027db50499673892f95086ef051e029d2a09bcb4054ec070467aa7c326f`  
		Last Modified: Tue, 04 Jul 2023 00:41:21 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
