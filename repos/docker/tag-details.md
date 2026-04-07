<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:29`](#docker29)
-	[`docker:29-cli`](#docker29-cli)
-	[`docker:29-dind`](#docker29-dind)
-	[`docker:29-dind-rootless`](#docker29-dind-rootless)
-	[`docker:29-windowsservercore`](#docker29-windowsservercore)
-	[`docker:29-windowsservercore-ltsc2022`](#docker29-windowsservercore-ltsc2022)
-	[`docker:29-windowsservercore-ltsc2025`](#docker29-windowsservercore-ltsc2025)
-	[`docker:29.4`](#docker294)
-	[`docker:29.4-cli`](#docker294-cli)
-	[`docker:29.4-dind`](#docker294-dind)
-	[`docker:29.4-dind-rootless`](#docker294-dind-rootless)
-	[`docker:29.4-windowsservercore`](#docker294-windowsservercore)
-	[`docker:29.4-windowsservercore-ltsc2022`](#docker294-windowsservercore-ltsc2022)
-	[`docker:29.4-windowsservercore-ltsc2025`](#docker294-windowsservercore-ltsc2025)
-	[`docker:29.4.0`](#docker2940)
-	[`docker:29.4.0-alpine3.23`](#docker2940-alpine323)
-	[`docker:29.4.0-cli`](#docker2940-cli)
-	[`docker:29.4.0-cli-alpine3.23`](#docker2940-cli-alpine323)
-	[`docker:29.4.0-dind`](#docker2940-dind)
-	[`docker:29.4.0-dind-alpine3.23`](#docker2940-dind-alpine323)
-	[`docker:29.4.0-dind-rootless`](#docker2940-dind-rootless)
-	[`docker:29.4.0-windowsservercore`](#docker2940-windowsservercore)
-	[`docker:29.4.0-windowsservercore-ltsc2022`](#docker2940-windowsservercore-ltsc2022)
-	[`docker:29.4.0-windowsservercore-ltsc2025`](#docker2940-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:29`

```console
$ docker pull docker@sha256:686d2c5464787b0ca42420e0aa03a94fc9781ff9bf8b5ff947614b9fa4c3c3e0
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

### `docker:29` - linux; amd64

```console
$ docker pull docker@sha256:a8d074fe486e65abe4ce251c264b78727be7b63a789ccb1eff2dcc786b443cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138543816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f54e33ee2ddd176e83bf6161114efa18dc63c00326ed58fa0697a8796417994`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:45:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:45:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:45:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:45:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:45:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:45:38 GMT
CMD ["sh"]
# Fri, 03 Apr 2026 17:05:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 03 Apr 2026 17:05:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 03 Apr 2026 17:05:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 17:05:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 03 Apr 2026 17:05:18 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 03 Apr 2026 17:05:18 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 03 Apr 2026 17:05:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 17:05:18 GMT
VOLUME [/var/lib/docker]
# Fri, 03 Apr 2026 17:05:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 03 Apr 2026 17:05:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 03 Apr 2026 17:05:18 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5679c6e6d45e2117c7e3c64d19dab37d2a751f6a8695b274011446785f5d974c`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 8.4 MB (8399808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13651ff9f98a7a01804bc4cf9e0eb2c832d0e3943fafd7033fbc5323ee9433b`  
		Last Modified: Fri, 03 Apr 2026 16:45:44 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544adb853f84f48115a46cfc76c5571249eea3bba4d011cdd2597ca0de7ffef8`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 18.9 MB (18925071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba1b50fe56ad29f6925651dd92625d4036f4c2aacf7849211e6d670b1ff4d06`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6d188f4a78bc49c0959c568bafb7bc8fcd0ac75759eeafd11d4992d107ba85`  
		Last Modified: Fri, 03 Apr 2026 16:45:46 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc67e139528a062178a1c30de103fb26dda0f6ebf4830c41d1f9aaee8152ede`  
		Last Modified: Fri, 03 Apr 2026 16:45:46 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b27d2c00ac1735fa633c45701bedfe7dd9da3e3d8b88a55988b308f2723376`  
		Last Modified: Fri, 03 Apr 2026 16:45:47 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222c8ebb2714f03d9f0f7843bae67f66f6338ccc90a8112f7c5a9521fc5801fe`  
		Last Modified: Fri, 03 Apr 2026 16:45:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86d96e88e4e907e31d182840119fabe703605b2e06c4a09d8a6d834754f12d4`  
		Last Modified: Fri, 03 Apr 2026 17:05:28 GMT  
		Size: 6.9 MB (6941639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cd9ca13141b31f2e62665957ee09ef0c28043fd9387d9c0c8ab048c3ca733b`  
		Last Modified: Fri, 03 Apr 2026 17:05:28 GMT  
		Size: 92.5 KB (92467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e127f411f6f1e1e5c228b9abf2ffe140a51edd2fc7e01e10f288525cdc36ebb`  
		Last Modified: Fri, 03 Apr 2026 17:05:28 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dcdc10364839056046aa19eb6a60c4d58e4d10c5b1abfd55f7d59b892ea910`  
		Last Modified: Fri, 03 Apr 2026 17:05:29 GMT  
		Size: 66.8 MB (66820522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4e9dea14a990a6b4f886171b26e24c66a6dbf851770b89afecd957b1d474d3`  
		Last Modified: Fri, 03 Apr 2026 17:05:29 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7602952982b750a0406fdf55807029c5e9eec431c1b585249b645782c0bb9640`  
		Last Modified: Fri, 03 Apr 2026 17:05:29 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:6a9cb94ed582de72b8c20772159e4beccdef0872fcd8373329db8894ab929e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1082d29eecf0a87567132592c6cafae8a6d6224d31b0844e86b08efcaa01f2f`

```dockerfile
```

-	Layers:
	-	`sha256:6a125f5c2f04596e1020bab77445cd2a497a2232e932e788ff5c43b8b7044737`  
		Last Modified: Fri, 03 Apr 2026 17:05:27 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v6

```console
$ docker pull docker@sha256:7472af905743da87fcc68ddf6d8e36229f3ed09052d60180527bb92d6ecacf7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130713665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd63b01ea25750846b6b8c1a8f2d216ff8bf3fd2d5e44ec3d9377ee811893d31`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:42:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:42:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:42:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:42:53 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:42:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:42:53 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:42:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:42:54 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:42:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:42:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:42:55 GMT
CMD ["sh"]
# Fri, 03 Apr 2026 16:46:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 03 Apr 2026 16:46:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 03 Apr 2026 16:46:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 16:46:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 03 Apr 2026 16:46:18 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 03 Apr 2026 16:46:18 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 03 Apr 2026 16:46:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:46:18 GMT
VOLUME [/var/lib/docker]
# Fri, 03 Apr 2026 16:46:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 03 Apr 2026 16:46:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 03 Apr 2026 16:46:18 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740b77d615bd7056fdfa10ac45a84e645f200a1dd058906d2f7c5a35bcc02e0e`  
		Last Modified: Fri, 03 Apr 2026 16:42:40 GMT  
		Size: 8.3 MB (8300856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db9e15d099697e3e0f63334517990f0d02a61abec8f671ec78dada6c111aeb8`  
		Last Modified: Fri, 03 Apr 2026 16:42:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badfb5fc5bffef95600bd56a253abb2c9e0aa7be994d332c5bdc962dbf98badb`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 17.7 MB (17704829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b890c9d4f91eb3442685e449c8b2f364c130782eab7dde7ebf5bd1211e1cd5`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 21.2 MB (21151883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea243840babbe8bdb5e0b7671978e226849103468c141766d1e18ed194d5bd3`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 10.4 MB (10388833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d072a6693dba53c8443bed1cc8779971ded28b6d831cbe0ca5d27a86f601ca0`  
		Last Modified: Fri, 03 Apr 2026 16:43:01 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34d0b523dd86a1840dbb3798720e0049c99c117ab5e91e11075b17fd08d2585`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b8f16743d3303cdfbdc56baf88120b4f52d0611ab208ee368a51267c360ac3`  
		Last Modified: Fri, 03 Apr 2026 16:43:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab55bf4153bdd56cb5f39f6650cfd9ba51c20e91bf2cff28e2cfcd749065c33`  
		Last Modified: Fri, 03 Apr 2026 16:46:29 GMT  
		Size: 7.3 MB (7278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02343a21b91c469b5cea7d6b52bd1422865f8d2fad041c5227903c82f5f39af`  
		Last Modified: Fri, 03 Apr 2026 16:46:29 GMT  
		Size: 91.8 KB (91785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fa33dfd5171fc56035c6f6fcc1a091d64971f1358915351923d6ca04a57328`  
		Last Modified: Fri, 03 Apr 2026 16:46:29 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d009d61277728e00d4620b798dcf41f5fc05bab7202c4b473db5f31426c2526e`  
		Last Modified: Fri, 03 Apr 2026 16:46:36 GMT  
		Size: 62.2 MB (62219223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604ede2b569e27b5f9062e1be9e2c95edd8a6f095e32a5a30d97ba08a0b9c4df`  
		Last Modified: Fri, 03 Apr 2026 16:46:30 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310af0449d43a19911330553d114ddf7f4acfdcade100c8b95295a23955f3bf6`  
		Last Modified: Fri, 03 Apr 2026 16:46:30 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:671d618f4f9d1fa039add9a97d36ddf277f9504c1def3a3d120398991873ac5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e404d9d065a5ea816b651f07800e4324288d09559d495c93eb8474784512c29a`

```dockerfile
```

-	Layers:
	-	`sha256:f961aeca8ebff8d2f0901fffaa890d60bb5143ab2780e15a0cce286525bbdea6`  
		Last Modified: Fri, 03 Apr 2026 16:46:28 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v7

```console
$ docker pull docker@sha256:76eff0f95837c7139e58b0c525b423dc55e518b976071fae0d564a2caaddfeb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128787145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2840bf830b179b108077625e8aac3296cd18b0b9abe8e0a0955df919559debba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:45:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:45:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:45:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:45:44 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:45:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:45:44 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:45:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:45:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:45:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:45:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:45:46 GMT
CMD ["sh"]
# Fri, 03 Apr 2026 16:58:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 03 Apr 2026 16:58:00 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 03 Apr 2026 16:58:00 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 16:58:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 03 Apr 2026 16:58:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 03 Apr 2026 16:58:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 03 Apr 2026 16:58:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:58:04 GMT
VOLUME [/var/lib/docker]
# Fri, 03 Apr 2026 16:58:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 03 Apr 2026 16:58:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 03 Apr 2026 16:58:04 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016deb0202a065a4c852f3f2050e118fc65d7c3cce2eafbe19ccf98d8ed89edf`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 7.6 MB (7597815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef50c437805c0b30e4f0d9a2b1d424511b36073620692593b22fec111a773a71`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576962e4d5abd715552603309b7b55bb37f0a2b337d7c0b8a5ebeb2fe76b8263`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 17.7 MB (17694914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f613c15806dfc400bd7f32c8ebf8b36aa8f94dbc6df38a83ec9b2e8545aa4717`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 21.1 MB (21129788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d06fdd3ade3c55eccdb7f475a525319fd35fdc888d2979c3e6c50b2048a502`  
		Last Modified: Fri, 03 Apr 2026 16:45:53 GMT  
		Size: 10.4 MB (10371886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf810380a1fd5b8ab1b6e406255fdb1fed4dda97ccb12e9d2ae40d9af7db41`  
		Last Modified: Fri, 03 Apr 2026 16:45:53 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ec359a5914fb65f503ead971c0c75e173d64dae3c1aad16c7f61c5069e969b`  
		Last Modified: Fri, 03 Apr 2026 16:45:54 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daefd04887b003c1b0328270d847084792ec4a75fed804f2ecd74a52ce074a31`  
		Last Modified: Fri, 03 Apr 2026 16:45:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b87d725529cf9b2c6f3e97907240a840520238ccce0347a64b1748962550d0f`  
		Last Modified: Fri, 03 Apr 2026 16:58:13 GMT  
		Size: 6.6 MB (6576423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b442283958037b11199976c605936942e358ab2758f524892a7086d676731e3`  
		Last Modified: Fri, 03 Apr 2026 16:58:13 GMT  
		Size: 88.1 KB (88144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ddc76cf55621abb7f91ecb29cae63e62c062164faf0c5a3c3361ed24fd2cd8`  
		Last Modified: Fri, 03 Apr 2026 16:58:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872cc131a341fa5dadabaaee49da5ba50dede23673dc81b20f75734504c4d23`  
		Last Modified: Fri, 03 Apr 2026 16:58:15 GMT  
		Size: 62.0 MB (62038306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b637186d0c474f679193ffe3a56fa55c6f81b6f7dbc46d85f24b68cefc03a4ae`  
		Last Modified: Fri, 03 Apr 2026 16:58:15 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36899143ff8194ff19a37d1bf9a5fa09858b0681841d180bd4e941278083cca9`  
		Last Modified: Fri, 03 Apr 2026 16:58:14 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:5435bf083ece270255a97e1bb24b88fce07499c1f6157a9d2cf8c414ace837bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83848fa250ffaaec1fe904ba1e1ae70d36dc8271f888b9e7574093eca93ed810`

```dockerfile
```

-	Layers:
	-	`sha256:59371fc5db1308a770e76bb8a671353b4b304c4fa257b097f02ad3acc7ecab70`  
		Last Modified: Fri, 03 Apr 2026 16:58:13 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ef75021c3c564a7977f21b23cd6d6cf0057441a0f6bb0e018410c5711de72f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128500378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a51c77dd3447c7efe6d0d9a8d2b8293a6e2c3f699667a6d85bbe6682d82647b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:46:07 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:46:07 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:46:07 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:46:10 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:46:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:46:10 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:46:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:46:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:46:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:46:11 GMT
CMD ["sh"]
# Fri, 03 Apr 2026 17:13:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 03 Apr 2026 17:13:13 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 03 Apr 2026 17:13:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 03 Apr 2026 17:13:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
VOLUME [/var/lib/docker]
# Fri, 03 Apr 2026 17:13:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 03 Apr 2026 17:13:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 03 Apr 2026 17:13:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777cc0dfb6b156ba8ae2d58bdc626d37d561285c3d8cb9f5dfab9e421b95c97a`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 8.5 MB (8453640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61cf8459e2976d9c1523c4817274c5542c2f14ca192664d8d5ad6eb7e492a00`  
		Last Modified: Fri, 03 Apr 2026 16:46:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8767096605cd5df8361d730cb51cdf77ce65a6d78016bfdcb25429f12a3b3c82`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 17.5 MB (17476968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14802cd569774821b1ac9c941f04e235ed46274c4a8ac0eae1b4b1ea971b6b2`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 20.5 MB (20453120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63242b8f6c4c149d7a76bebad8e17208b476be636d6f2c9ed5dca0a6e87eebd6`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 10.0 MB (9982610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f92f7532507e0be265cd5a585468bfba3ed63c8f64943bfffbdb4c8e2bc29d3`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1144373d60167579bb44d4f4ec630998cc0bf64b287b2e5ba3c03aa31aa1f3d`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1b6b3e13fd596fa602ee41b47089c2aa97d6adb582e423ec45a54312bda585`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7bcce9135e50e8113ce567e771818f45458b22e72a5b64b70da654eebd0e99`  
		Last Modified: Fri, 03 Apr 2026 17:13:25 GMT  
		Size: 7.2 MB (7219478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830d8e038e6c3e9055a2326f9fee1c908c9b60277c26df9b8ac5decd85cd3c08`  
		Last Modified: Fri, 03 Apr 2026 17:13:24 GMT  
		Size: 101.3 KB (101299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce438bd7121c26756c9344834a818efa8088cbd191053f8237e7ab52a55bee8b`  
		Last Modified: Fri, 03 Apr 2026 17:13:25 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8572ba2382e471780ecdf47f897386999474a08611c84b60f7f9664f27c0c7`  
		Last Modified: Fri, 03 Apr 2026 17:13:26 GMT  
		Size: 60.6 MB (60608023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0059d0fd9057439969d2dbf52619e8c263ad6c554c1f948b3cba6c9c94912e80`  
		Last Modified: Fri, 03 Apr 2026 17:13:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3764136014318e546423f2772475f4d7562d75fcd1407fd1c1bd941b0d1542`  
		Last Modified: Fri, 03 Apr 2026 17:13:26 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:cfa3bba5e17688594fc44b1a3d2f036d316ec72d1087c5cfcda980e17099085e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1edcd89a3d057104931b35657c5c97cd175a0a2255935ec50e46250e09864642`

```dockerfile
```

-	Layers:
	-	`sha256:a6f088a054073c23988be89705d5498a22b7cedd81fad3d5bb5196ffeebafc6d`  
		Last Modified: Fri, 03 Apr 2026 17:13:24 GMT  
		Size: 34.8 KB (34775 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:18f5ab0fab739ea822819b342357947dfba235cdef438cce345ebc0c143c5b34
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

### `docker:29-cli` - linux; amd64

```console
$ docker pull docker@sha256:b5fd064ef9d1ecb6980bebaf40d58cffca1a189e72805faca59af065bd7f7cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64683189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc513c142fdd740f7b4713af29da1dec9fa9ff53f9733566ae0635682df5c6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:45:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:45:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:45:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:45:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:45:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:45:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5679c6e6d45e2117c7e3c64d19dab37d2a751f6a8695b274011446785f5d974c`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 8.4 MB (8399808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13651ff9f98a7a01804bc4cf9e0eb2c832d0e3943fafd7033fbc5323ee9433b`  
		Last Modified: Fri, 03 Apr 2026 16:45:44 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544adb853f84f48115a46cfc76c5571249eea3bba4d011cdd2597ca0de7ffef8`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 18.9 MB (18925071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba1b50fe56ad29f6925651dd92625d4036f4c2aacf7849211e6d670b1ff4d06`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6d188f4a78bc49c0959c568bafb7bc8fcd0ac75759eeafd11d4992d107ba85`  
		Last Modified: Fri, 03 Apr 2026 16:45:46 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc67e139528a062178a1c30de103fb26dda0f6ebf4830c41d1f9aaee8152ede`  
		Last Modified: Fri, 03 Apr 2026 16:45:46 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b27d2c00ac1735fa633c45701bedfe7dd9da3e3d8b88a55988b308f2723376`  
		Last Modified: Fri, 03 Apr 2026 16:45:47 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222c8ebb2714f03d9f0f7843bae67f66f6338ccc90a8112f7c5a9521fc5801fe`  
		Last Modified: Fri, 03 Apr 2026 16:45:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:61f6aa987355fd2c723f0770e3ec586287cfeb2a5a6dbdd9b815a4e2698e65bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db60dc956064ff657e5f67c712353b02b3b6cd1485d9767db1a8d03f2086d283`

```dockerfile
```

-	Layers:
	-	`sha256:a204fa9bc3a5008e92de29f8d9daa46eed02f6ade4cd0ee9ec3ff376dd092c9c`  
		Last Modified: Fri, 03 Apr 2026 16:45:44 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:534c81ceedd13f40a95d76431719eb5313b5aa7bc18c41a43cc220d52027ee78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61118378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdf1a50937f4c1b699422c7b1abb8bf0e7611be6c37d6b9f421c6d176d3c342`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:42:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:42:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:42:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:42:53 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:42:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:42:53 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:42:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:42:54 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:42:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:42:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:42:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740b77d615bd7056fdfa10ac45a84e645f200a1dd058906d2f7c5a35bcc02e0e`  
		Last Modified: Fri, 03 Apr 2026 16:42:40 GMT  
		Size: 8.3 MB (8300856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db9e15d099697e3e0f63334517990f0d02a61abec8f671ec78dada6c111aeb8`  
		Last Modified: Fri, 03 Apr 2026 16:42:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badfb5fc5bffef95600bd56a253abb2c9e0aa7be994d332c5bdc962dbf98badb`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 17.7 MB (17704829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b890c9d4f91eb3442685e449c8b2f364c130782eab7dde7ebf5bd1211e1cd5`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 21.2 MB (21151883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea243840babbe8bdb5e0b7671978e226849103468c141766d1e18ed194d5bd3`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 10.4 MB (10388833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d072a6693dba53c8443bed1cc8779971ded28b6d831cbe0ca5d27a86f601ca0`  
		Last Modified: Fri, 03 Apr 2026 16:43:01 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34d0b523dd86a1840dbb3798720e0049c99c117ab5e91e11075b17fd08d2585`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b8f16743d3303cdfbdc56baf88120b4f52d0611ab208ee368a51267c360ac3`  
		Last Modified: Fri, 03 Apr 2026 16:43:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:b9f0cd3c948f74de09a3047847ff1e29faad7b1a37b2a3e69a71eb8b18b6575f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764dd95beb61967fbecd25eaf5f1ddc926733263c1639855c122542000811423`

```dockerfile
```

-	Layers:
	-	`sha256:fb68f5b71deb7dc273f37425417366ffbcdd93dde04bee331c80ab0c99479d03`  
		Last Modified: Fri, 03 Apr 2026 16:43:01 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:51ff322f0054df2754fef335caeddc581e016d5fd1d0e3a52e023bf0bdf63b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60078278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5398a87e24104d708e0ccfb588dc51aba6911a6975c22cdde0975c105b46b192`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:45:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:45:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:45:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:45:44 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:45:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:45:44 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:45:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:45:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:45:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:45:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:45:46 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016deb0202a065a4c852f3f2050e118fc65d7c3cce2eafbe19ccf98d8ed89edf`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 7.6 MB (7597815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef50c437805c0b30e4f0d9a2b1d424511b36073620692593b22fec111a773a71`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576962e4d5abd715552603309b7b55bb37f0a2b337d7c0b8a5ebeb2fe76b8263`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 17.7 MB (17694914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f613c15806dfc400bd7f32c8ebf8b36aa8f94dbc6df38a83ec9b2e8545aa4717`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 21.1 MB (21129788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d06fdd3ade3c55eccdb7f475a525319fd35fdc888d2979c3e6c50b2048a502`  
		Last Modified: Fri, 03 Apr 2026 16:45:53 GMT  
		Size: 10.4 MB (10371886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf810380a1fd5b8ab1b6e406255fdb1fed4dda97ccb12e9d2ae40d9af7db41`  
		Last Modified: Fri, 03 Apr 2026 16:45:53 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ec359a5914fb65f503ead971c0c75e173d64dae3c1aad16c7f61c5069e969b`  
		Last Modified: Fri, 03 Apr 2026 16:45:54 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daefd04887b003c1b0328270d847084792ec4a75fed804f2ecd74a52ce074a31`  
		Last Modified: Fri, 03 Apr 2026 16:45:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:56b264f893b723521f9fe0c351f1ca921498328532e56c70ecbf19fbf217c5a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924ed150b180f7d94211c148a7d63f6e87ed1af907a149b95668d778ed15dc7e`

```dockerfile
```

-	Layers:
	-	`sha256:acbb087569d7a7926fa874efebe27fa3cc848d12859399bfe0d348106e197809`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3194496094bc2ff85b6e27d6e084a1a2cb962c9252dfc3daf5813991023e880a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60565584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0485c76ca15edf3e39284ff7f13d0ac4d9548b79983311b6ded1b6e439d17579`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:46:07 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:46:07 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:46:07 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:46:10 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:46:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:46:10 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:46:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:46:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:46:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:46:11 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777cc0dfb6b156ba8ae2d58bdc626d37d561285c3d8cb9f5dfab9e421b95c97a`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 8.5 MB (8453640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61cf8459e2976d9c1523c4817274c5542c2f14ca192664d8d5ad6eb7e492a00`  
		Last Modified: Fri, 03 Apr 2026 16:46:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8767096605cd5df8361d730cb51cdf77ce65a6d78016bfdcb25429f12a3b3c82`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 17.5 MB (17476968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14802cd569774821b1ac9c941f04e235ed46274c4a8ac0eae1b4b1ea971b6b2`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 20.5 MB (20453120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63242b8f6c4c149d7a76bebad8e17208b476be636d6f2c9ed5dca0a6e87eebd6`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 10.0 MB (9982610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f92f7532507e0be265cd5a585468bfba3ed63c8f64943bfffbdb4c8e2bc29d3`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1144373d60167579bb44d4f4ec630998cc0bf64b287b2e5ba3c03aa31aa1f3d`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1b6b3e13fd596fa602ee41b47089c2aa97d6adb582e423ec45a54312bda585`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0680a367e5ffbce2c37efea411c79239cce4ba10e11fa3f8bf240f9b4696c40f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3bd6f7d935b2ea4dcebd0a62a2f6534301269753ddf098dcb5ccbfe08ed63c9`

```dockerfile
```

-	Layers:
	-	`sha256:74e8e8209c9cead51c4d4165ab182f2b610af1f09c61fe4adf46ac23dc87428b`  
		Last Modified: Fri, 03 Apr 2026 16:46:17 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind`

```console
$ docker pull docker@sha256:686d2c5464787b0ca42420e0aa03a94fc9781ff9bf8b5ff947614b9fa4c3c3e0
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

### `docker:29-dind` - linux; amd64

```console
$ docker pull docker@sha256:a8d074fe486e65abe4ce251c264b78727be7b63a789ccb1eff2dcc786b443cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138543816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f54e33ee2ddd176e83bf6161114efa18dc63c00326ed58fa0697a8796417994`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:45:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:45:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:45:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:45:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:45:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:45:38 GMT
CMD ["sh"]
# Fri, 03 Apr 2026 17:05:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 03 Apr 2026 17:05:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 03 Apr 2026 17:05:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 17:05:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 03 Apr 2026 17:05:18 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 03 Apr 2026 17:05:18 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 03 Apr 2026 17:05:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 17:05:18 GMT
VOLUME [/var/lib/docker]
# Fri, 03 Apr 2026 17:05:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 03 Apr 2026 17:05:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 03 Apr 2026 17:05:18 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5679c6e6d45e2117c7e3c64d19dab37d2a751f6a8695b274011446785f5d974c`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 8.4 MB (8399808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13651ff9f98a7a01804bc4cf9e0eb2c832d0e3943fafd7033fbc5323ee9433b`  
		Last Modified: Fri, 03 Apr 2026 16:45:44 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544adb853f84f48115a46cfc76c5571249eea3bba4d011cdd2597ca0de7ffef8`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 18.9 MB (18925071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba1b50fe56ad29f6925651dd92625d4036f4c2aacf7849211e6d670b1ff4d06`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6d188f4a78bc49c0959c568bafb7bc8fcd0ac75759eeafd11d4992d107ba85`  
		Last Modified: Fri, 03 Apr 2026 16:45:46 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc67e139528a062178a1c30de103fb26dda0f6ebf4830c41d1f9aaee8152ede`  
		Last Modified: Fri, 03 Apr 2026 16:45:46 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b27d2c00ac1735fa633c45701bedfe7dd9da3e3d8b88a55988b308f2723376`  
		Last Modified: Fri, 03 Apr 2026 16:45:47 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222c8ebb2714f03d9f0f7843bae67f66f6338ccc90a8112f7c5a9521fc5801fe`  
		Last Modified: Fri, 03 Apr 2026 16:45:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86d96e88e4e907e31d182840119fabe703605b2e06c4a09d8a6d834754f12d4`  
		Last Modified: Fri, 03 Apr 2026 17:05:28 GMT  
		Size: 6.9 MB (6941639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cd9ca13141b31f2e62665957ee09ef0c28043fd9387d9c0c8ab048c3ca733b`  
		Last Modified: Fri, 03 Apr 2026 17:05:28 GMT  
		Size: 92.5 KB (92467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e127f411f6f1e1e5c228b9abf2ffe140a51edd2fc7e01e10f288525cdc36ebb`  
		Last Modified: Fri, 03 Apr 2026 17:05:28 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dcdc10364839056046aa19eb6a60c4d58e4d10c5b1abfd55f7d59b892ea910`  
		Last Modified: Fri, 03 Apr 2026 17:05:29 GMT  
		Size: 66.8 MB (66820522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4e9dea14a990a6b4f886171b26e24c66a6dbf851770b89afecd957b1d474d3`  
		Last Modified: Fri, 03 Apr 2026 17:05:29 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7602952982b750a0406fdf55807029c5e9eec431c1b585249b645782c0bb9640`  
		Last Modified: Fri, 03 Apr 2026 17:05:29 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6a9cb94ed582de72b8c20772159e4beccdef0872fcd8373329db8894ab929e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1082d29eecf0a87567132592c6cafae8a6d6224d31b0844e86b08efcaa01f2f`

```dockerfile
```

-	Layers:
	-	`sha256:6a125f5c2f04596e1020bab77445cd2a497a2232e932e788ff5c43b8b7044737`  
		Last Modified: Fri, 03 Apr 2026 17:05:27 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:7472af905743da87fcc68ddf6d8e36229f3ed09052d60180527bb92d6ecacf7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130713665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd63b01ea25750846b6b8c1a8f2d216ff8bf3fd2d5e44ec3d9377ee811893d31`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:42:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:42:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:42:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:42:53 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:42:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:42:53 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:42:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:42:54 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:42:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:42:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:42:55 GMT
CMD ["sh"]
# Fri, 03 Apr 2026 16:46:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 03 Apr 2026 16:46:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 03 Apr 2026 16:46:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 16:46:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 03 Apr 2026 16:46:18 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 03 Apr 2026 16:46:18 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 03 Apr 2026 16:46:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:46:18 GMT
VOLUME [/var/lib/docker]
# Fri, 03 Apr 2026 16:46:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 03 Apr 2026 16:46:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 03 Apr 2026 16:46:18 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740b77d615bd7056fdfa10ac45a84e645f200a1dd058906d2f7c5a35bcc02e0e`  
		Last Modified: Fri, 03 Apr 2026 16:42:40 GMT  
		Size: 8.3 MB (8300856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db9e15d099697e3e0f63334517990f0d02a61abec8f671ec78dada6c111aeb8`  
		Last Modified: Fri, 03 Apr 2026 16:42:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badfb5fc5bffef95600bd56a253abb2c9e0aa7be994d332c5bdc962dbf98badb`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 17.7 MB (17704829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b890c9d4f91eb3442685e449c8b2f364c130782eab7dde7ebf5bd1211e1cd5`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 21.2 MB (21151883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea243840babbe8bdb5e0b7671978e226849103468c141766d1e18ed194d5bd3`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 10.4 MB (10388833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d072a6693dba53c8443bed1cc8779971ded28b6d831cbe0ca5d27a86f601ca0`  
		Last Modified: Fri, 03 Apr 2026 16:43:01 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34d0b523dd86a1840dbb3798720e0049c99c117ab5e91e11075b17fd08d2585`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b8f16743d3303cdfbdc56baf88120b4f52d0611ab208ee368a51267c360ac3`  
		Last Modified: Fri, 03 Apr 2026 16:43:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab55bf4153bdd56cb5f39f6650cfd9ba51c20e91bf2cff28e2cfcd749065c33`  
		Last Modified: Fri, 03 Apr 2026 16:46:29 GMT  
		Size: 7.3 MB (7278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02343a21b91c469b5cea7d6b52bd1422865f8d2fad041c5227903c82f5f39af`  
		Last Modified: Fri, 03 Apr 2026 16:46:29 GMT  
		Size: 91.8 KB (91785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fa33dfd5171fc56035c6f6fcc1a091d64971f1358915351923d6ca04a57328`  
		Last Modified: Fri, 03 Apr 2026 16:46:29 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d009d61277728e00d4620b798dcf41f5fc05bab7202c4b473db5f31426c2526e`  
		Last Modified: Fri, 03 Apr 2026 16:46:36 GMT  
		Size: 62.2 MB (62219223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604ede2b569e27b5f9062e1be9e2c95edd8a6f095e32a5a30d97ba08a0b9c4df`  
		Last Modified: Fri, 03 Apr 2026 16:46:30 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310af0449d43a19911330553d114ddf7f4acfdcade100c8b95295a23955f3bf6`  
		Last Modified: Fri, 03 Apr 2026 16:46:30 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:671d618f4f9d1fa039add9a97d36ddf277f9504c1def3a3d120398991873ac5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e404d9d065a5ea816b651f07800e4324288d09559d495c93eb8474784512c29a`

```dockerfile
```

-	Layers:
	-	`sha256:f961aeca8ebff8d2f0901fffaa890d60bb5143ab2780e15a0cce286525bbdea6`  
		Last Modified: Fri, 03 Apr 2026 16:46:28 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:76eff0f95837c7139e58b0c525b423dc55e518b976071fae0d564a2caaddfeb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128787145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2840bf830b179b108077625e8aac3296cd18b0b9abe8e0a0955df919559debba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:45:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:45:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:45:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:45:44 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:45:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:45:44 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:45:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:45:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:45:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:45:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:45:46 GMT
CMD ["sh"]
# Fri, 03 Apr 2026 16:58:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 03 Apr 2026 16:58:00 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 03 Apr 2026 16:58:00 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 16:58:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 03 Apr 2026 16:58:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 03 Apr 2026 16:58:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 03 Apr 2026 16:58:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:58:04 GMT
VOLUME [/var/lib/docker]
# Fri, 03 Apr 2026 16:58:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 03 Apr 2026 16:58:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 03 Apr 2026 16:58:04 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016deb0202a065a4c852f3f2050e118fc65d7c3cce2eafbe19ccf98d8ed89edf`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 7.6 MB (7597815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef50c437805c0b30e4f0d9a2b1d424511b36073620692593b22fec111a773a71`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576962e4d5abd715552603309b7b55bb37f0a2b337d7c0b8a5ebeb2fe76b8263`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 17.7 MB (17694914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f613c15806dfc400bd7f32c8ebf8b36aa8f94dbc6df38a83ec9b2e8545aa4717`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 21.1 MB (21129788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d06fdd3ade3c55eccdb7f475a525319fd35fdc888d2979c3e6c50b2048a502`  
		Last Modified: Fri, 03 Apr 2026 16:45:53 GMT  
		Size: 10.4 MB (10371886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf810380a1fd5b8ab1b6e406255fdb1fed4dda97ccb12e9d2ae40d9af7db41`  
		Last Modified: Fri, 03 Apr 2026 16:45:53 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ec359a5914fb65f503ead971c0c75e173d64dae3c1aad16c7f61c5069e969b`  
		Last Modified: Fri, 03 Apr 2026 16:45:54 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daefd04887b003c1b0328270d847084792ec4a75fed804f2ecd74a52ce074a31`  
		Last Modified: Fri, 03 Apr 2026 16:45:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b87d725529cf9b2c6f3e97907240a840520238ccce0347a64b1748962550d0f`  
		Last Modified: Fri, 03 Apr 2026 16:58:13 GMT  
		Size: 6.6 MB (6576423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b442283958037b11199976c605936942e358ab2758f524892a7086d676731e3`  
		Last Modified: Fri, 03 Apr 2026 16:58:13 GMT  
		Size: 88.1 KB (88144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ddc76cf55621abb7f91ecb29cae63e62c062164faf0c5a3c3361ed24fd2cd8`  
		Last Modified: Fri, 03 Apr 2026 16:58:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872cc131a341fa5dadabaaee49da5ba50dede23673dc81b20f75734504c4d23`  
		Last Modified: Fri, 03 Apr 2026 16:58:15 GMT  
		Size: 62.0 MB (62038306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b637186d0c474f679193ffe3a56fa55c6f81b6f7dbc46d85f24b68cefc03a4ae`  
		Last Modified: Fri, 03 Apr 2026 16:58:15 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36899143ff8194ff19a37d1bf9a5fa09858b0681841d180bd4e941278083cca9`  
		Last Modified: Fri, 03 Apr 2026 16:58:14 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5435bf083ece270255a97e1bb24b88fce07499c1f6157a9d2cf8c414ace837bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83848fa250ffaaec1fe904ba1e1ae70d36dc8271f888b9e7574093eca93ed810`

```dockerfile
```

-	Layers:
	-	`sha256:59371fc5db1308a770e76bb8a671353b4b304c4fa257b097f02ad3acc7ecab70`  
		Last Modified: Fri, 03 Apr 2026 16:58:13 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ef75021c3c564a7977f21b23cd6d6cf0057441a0f6bb0e018410c5711de72f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128500378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a51c77dd3447c7efe6d0d9a8d2b8293a6e2c3f699667a6d85bbe6682d82647b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:46:07 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:46:07 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:46:07 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:46:10 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:46:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:46:10 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:46:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:46:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:46:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:46:11 GMT
CMD ["sh"]
# Fri, 03 Apr 2026 17:13:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 03 Apr 2026 17:13:13 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 03 Apr 2026 17:13:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 03 Apr 2026 17:13:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
VOLUME [/var/lib/docker]
# Fri, 03 Apr 2026 17:13:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 03 Apr 2026 17:13:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 03 Apr 2026 17:13:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777cc0dfb6b156ba8ae2d58bdc626d37d561285c3d8cb9f5dfab9e421b95c97a`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 8.5 MB (8453640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61cf8459e2976d9c1523c4817274c5542c2f14ca192664d8d5ad6eb7e492a00`  
		Last Modified: Fri, 03 Apr 2026 16:46:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8767096605cd5df8361d730cb51cdf77ce65a6d78016bfdcb25429f12a3b3c82`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 17.5 MB (17476968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14802cd569774821b1ac9c941f04e235ed46274c4a8ac0eae1b4b1ea971b6b2`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 20.5 MB (20453120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63242b8f6c4c149d7a76bebad8e17208b476be636d6f2c9ed5dca0a6e87eebd6`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 10.0 MB (9982610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f92f7532507e0be265cd5a585468bfba3ed63c8f64943bfffbdb4c8e2bc29d3`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1144373d60167579bb44d4f4ec630998cc0bf64b287b2e5ba3c03aa31aa1f3d`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1b6b3e13fd596fa602ee41b47089c2aa97d6adb582e423ec45a54312bda585`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7bcce9135e50e8113ce567e771818f45458b22e72a5b64b70da654eebd0e99`  
		Last Modified: Fri, 03 Apr 2026 17:13:25 GMT  
		Size: 7.2 MB (7219478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830d8e038e6c3e9055a2326f9fee1c908c9b60277c26df9b8ac5decd85cd3c08`  
		Last Modified: Fri, 03 Apr 2026 17:13:24 GMT  
		Size: 101.3 KB (101299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce438bd7121c26756c9344834a818efa8088cbd191053f8237e7ab52a55bee8b`  
		Last Modified: Fri, 03 Apr 2026 17:13:25 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8572ba2382e471780ecdf47f897386999474a08611c84b60f7f9664f27c0c7`  
		Last Modified: Fri, 03 Apr 2026 17:13:26 GMT  
		Size: 60.6 MB (60608023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0059d0fd9057439969d2dbf52619e8c263ad6c554c1f948b3cba6c9c94912e80`  
		Last Modified: Fri, 03 Apr 2026 17:13:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3764136014318e546423f2772475f4d7562d75fcd1407fd1c1bd941b0d1542`  
		Last Modified: Fri, 03 Apr 2026 17:13:26 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:cfa3bba5e17688594fc44b1a3d2f036d316ec72d1087c5cfcda980e17099085e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1edcd89a3d057104931b35657c5c97cd175a0a2255935ec50e46250e09864642`

```dockerfile
```

-	Layers:
	-	`sha256:a6f088a054073c23988be89705d5498a22b7cedd81fad3d5bb5196ffeebafc6d`  
		Last Modified: Fri, 03 Apr 2026 17:13:24 GMT  
		Size: 34.8 KB (34775 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:5fd70e50e710078a3c8c3eaa96c0e788740ee71934f48efce17573a47db7cf4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9ad408a87b7bc68a51b5b9b7480e6d5b603dcdcf8bcf760a0bf1bd80127dca3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.4 MB (159350536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c26f0075065a8672e7fc616d39b9a0b70b5965bc967269e06fcefe2ff62f31e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:45:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:45:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:45:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:45:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:45:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:45:38 GMT
CMD ["sh"]
# Fri, 03 Apr 2026 17:05:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 03 Apr 2026 17:05:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 03 Apr 2026 17:05:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 17:05:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 03 Apr 2026 17:05:18 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 03 Apr 2026 17:05:18 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 03 Apr 2026 17:05:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 17:05:18 GMT
VOLUME [/var/lib/docker]
# Fri, 03 Apr 2026 17:05:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 03 Apr 2026 17:05:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 03 Apr 2026 17:05:18 GMT
CMD []
# Fri, 03 Apr 2026 17:13:33 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 03 Apr 2026 17:13:33 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 03 Apr 2026 17:13:34 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 17:13:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 03 Apr 2026 17:13:34 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 03 Apr 2026 17:13:34 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 03 Apr 2026 17:13:34 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5679c6e6d45e2117c7e3c64d19dab37d2a751f6a8695b274011446785f5d974c`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 8.4 MB (8399808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13651ff9f98a7a01804bc4cf9e0eb2c832d0e3943fafd7033fbc5323ee9433b`  
		Last Modified: Fri, 03 Apr 2026 16:45:44 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544adb853f84f48115a46cfc76c5571249eea3bba4d011cdd2597ca0de7ffef8`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 18.9 MB (18925071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba1b50fe56ad29f6925651dd92625d4036f4c2aacf7849211e6d670b1ff4d06`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6d188f4a78bc49c0959c568bafb7bc8fcd0ac75759eeafd11d4992d107ba85`  
		Last Modified: Fri, 03 Apr 2026 16:45:46 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc67e139528a062178a1c30de103fb26dda0f6ebf4830c41d1f9aaee8152ede`  
		Last Modified: Fri, 03 Apr 2026 16:45:46 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b27d2c00ac1735fa633c45701bedfe7dd9da3e3d8b88a55988b308f2723376`  
		Last Modified: Fri, 03 Apr 2026 16:45:47 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222c8ebb2714f03d9f0f7843bae67f66f6338ccc90a8112f7c5a9521fc5801fe`  
		Last Modified: Fri, 03 Apr 2026 16:45:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86d96e88e4e907e31d182840119fabe703605b2e06c4a09d8a6d834754f12d4`  
		Last Modified: Fri, 03 Apr 2026 17:05:28 GMT  
		Size: 6.9 MB (6941639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cd9ca13141b31f2e62665957ee09ef0c28043fd9387d9c0c8ab048c3ca733b`  
		Last Modified: Fri, 03 Apr 2026 17:05:28 GMT  
		Size: 92.5 KB (92467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e127f411f6f1e1e5c228b9abf2ffe140a51edd2fc7e01e10f288525cdc36ebb`  
		Last Modified: Fri, 03 Apr 2026 17:05:28 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dcdc10364839056046aa19eb6a60c4d58e4d10c5b1abfd55f7d59b892ea910`  
		Last Modified: Fri, 03 Apr 2026 17:05:29 GMT  
		Size: 66.8 MB (66820522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4e9dea14a990a6b4f886171b26e24c66a6dbf851770b89afecd957b1d474d3`  
		Last Modified: Fri, 03 Apr 2026 17:05:29 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7602952982b750a0406fdf55807029c5e9eec431c1b585249b645782c0bb9640`  
		Last Modified: Fri, 03 Apr 2026 17:05:29 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77d1d2a4fe8087c79d70a0f3b208fde9e5083b9cdace6e9fbba1410b76615c9`  
		Last Modified: Fri, 03 Apr 2026 17:13:41 GMT  
		Size: 3.4 MB (3419946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ed1b22f98a868fa49be3cf3b6f43c9c7e240d3a0491fd7d4399ef5dbda8f5d`  
		Last Modified: Fri, 03 Apr 2026 17:13:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392e87366b916c8d9cf5dea477b6770a49d0e13bdae6b512026b87a6366dd02b`  
		Last Modified: Fri, 03 Apr 2026 17:13:41 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1e7a9eed6561ca743cfd7ed4c6759d717e1d577c39ecbd7d59fe6b566300d5`  
		Last Modified: Fri, 03 Apr 2026 17:13:41 GMT  
		Size: 17.4 MB (17385434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce6f31a4b269f5fd157606d7d1ed46c45b48062ea29c18422af40d9beb35417`  
		Last Modified: Fri, 03 Apr 2026 17:13:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:03c8886a0bd50b365eaf01a8cc97410db4dc94bd215ebb71297064b4affea7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ac462145506cc6d2425ae86571456b9c24115bc341b6d68dcf5fd2df3677fb`

```dockerfile
```

-	Layers:
	-	`sha256:9f182fcb771b62e6a69a3a73b529aca8b87bd308a7af152db961de64d5e36783`  
		Last Modified: Fri, 03 Apr 2026 17:13:40 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6679cb2aefe477b0d944091963ef8d1f8b8db4cd4404cc8add23e4313fce04ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.6 MB (149610516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da1dfa1a7531898d0ffb21ba6c3a9cf596386b2c008f0b644ba8c67be847cbb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:46:07 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:46:07 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:46:07 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:46:10 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:46:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:46:10 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:46:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:46:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:46:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:46:11 GMT
CMD ["sh"]
# Fri, 03 Apr 2026 17:13:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 03 Apr 2026 17:13:13 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 03 Apr 2026 17:13:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 03 Apr 2026 17:13:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
VOLUME [/var/lib/docker]
# Fri, 03 Apr 2026 17:13:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 03 Apr 2026 17:13:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 03 Apr 2026 17:13:15 GMT
CMD []
# Fri, 03 Apr 2026 17:25:14 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 03 Apr 2026 17:25:14 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 03 Apr 2026 17:25:14 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 17:25:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 03 Apr 2026 17:25:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 03 Apr 2026 17:25:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 03 Apr 2026 17:25:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777cc0dfb6b156ba8ae2d58bdc626d37d561285c3d8cb9f5dfab9e421b95c97a`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 8.5 MB (8453640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61cf8459e2976d9c1523c4817274c5542c2f14ca192664d8d5ad6eb7e492a00`  
		Last Modified: Fri, 03 Apr 2026 16:46:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8767096605cd5df8361d730cb51cdf77ce65a6d78016bfdcb25429f12a3b3c82`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 17.5 MB (17476968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14802cd569774821b1ac9c941f04e235ed46274c4a8ac0eae1b4b1ea971b6b2`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 20.5 MB (20453120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63242b8f6c4c149d7a76bebad8e17208b476be636d6f2c9ed5dca0a6e87eebd6`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 10.0 MB (9982610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f92f7532507e0be265cd5a585468bfba3ed63c8f64943bfffbdb4c8e2bc29d3`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1144373d60167579bb44d4f4ec630998cc0bf64b287b2e5ba3c03aa31aa1f3d`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1b6b3e13fd596fa602ee41b47089c2aa97d6adb582e423ec45a54312bda585`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7bcce9135e50e8113ce567e771818f45458b22e72a5b64b70da654eebd0e99`  
		Last Modified: Fri, 03 Apr 2026 17:13:25 GMT  
		Size: 7.2 MB (7219478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830d8e038e6c3e9055a2326f9fee1c908c9b60277c26df9b8ac5decd85cd3c08`  
		Last Modified: Fri, 03 Apr 2026 17:13:24 GMT  
		Size: 101.3 KB (101299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce438bd7121c26756c9344834a818efa8088cbd191053f8237e7ab52a55bee8b`  
		Last Modified: Fri, 03 Apr 2026 17:13:25 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8572ba2382e471780ecdf47f897386999474a08611c84b60f7f9664f27c0c7`  
		Last Modified: Fri, 03 Apr 2026 17:13:26 GMT  
		Size: 60.6 MB (60608023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0059d0fd9057439969d2dbf52619e8c263ad6c554c1f948b3cba6c9c94912e80`  
		Last Modified: Fri, 03 Apr 2026 17:13:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3764136014318e546423f2772475f4d7562d75fcd1407fd1c1bd941b0d1542`  
		Last Modified: Fri, 03 Apr 2026 17:13:26 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503dd12c2fdaa4e9d1ca00275d42321966bc1ea7f174b1af8b4a4383afcd22e4`  
		Last Modified: Fri, 03 Apr 2026 17:25:21 GMT  
		Size: 3.4 MB (3394365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9267ed34f5f7b5284c28c8d607dcbd616fd8d15cb5e9f3a6e7a98d79ee3d02f`  
		Last Modified: Fri, 03 Apr 2026 17:25:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97dcc6860b1c94957073ca4b75a0bc2b662ad2c642f27f1fc2e903edb407f9f`  
		Last Modified: Fri, 03 Apr 2026 17:25:21 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90d00483cc8dcbb6d0186a4ef64291f65acb96973d6a288d7895cd2fe03688b`  
		Last Modified: Fri, 03 Apr 2026 17:25:22 GMT  
		Size: 17.7 MB (17714430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225856b6401e13d11d803a1b9b8c24cec5de0a863f43e8b3a0c128526ced06f4`  
		Last Modified: Fri, 03 Apr 2026 17:25:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bdc6ca529abd59bb8aea5ee4c333dc839cddfb3859157f4a157f484458a4a426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f669db25bcbdc78b0e1bed87de14f4f4c286679900eba52e9f3c547d90db8a96`

```dockerfile
```

-	Layers:
	-	`sha256:a082c4facd362ebcdd9ae60cfe71df1d11ae9c3eb0daea05952c744240c2cf8c`  
		Last Modified: Fri, 03 Apr 2026 17:25:21 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:155a3d0470bc1209d0e007c462b889f181e8c5f50d2cbeafc3c09fe35dd7958f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:a105d81267b506d283738c2eab0c3e5f2339533f55a3f4e578543f31a10c0559
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2136248524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5d491b6f638ed8098ef9803e3c78743401083c443ad9969e0c8c97b4a5061c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Fri, 03 Apr 2026 16:48:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Apr 2026 16:49:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Apr 2026 16:49:27 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:49:28 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.1.zip
# Fri, 03 Apr 2026 16:49:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:49:46 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:49:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Fri, 03 Apr 2026 16:49:48 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Fri, 03 Apr 2026 16:50:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:50:05 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:50:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Fri, 03 Apr 2026 16:50:07 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Fri, 03 Apr 2026 16:50:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be287d655249644e43f567922c8ace0ebd34d2029a63b5f7aff779c7f0ea81f`  
		Last Modified: Fri, 03 Apr 2026 16:50:28 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bacc8dcf99a4b510435fd53e918e3bd0d6f4fdf27dcb309c4534ce03060f4e4`  
		Last Modified: Fri, 03 Apr 2026 16:50:27 GMT  
		Size: 370.7 KB (370685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75b1a0e09957eca68ed1d9ce466b166f611394669ffd7e2ef3cb280d2e86086`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cd9630a95f491844d8e8a681bc533e92b0e16ccf40b4842c76d47b05c88b82`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea0afb7d1d92072a6f67dc1f20ac520593a6d5b6e34fd654db0236504072e6b`  
		Last Modified: Fri, 03 Apr 2026 16:50:29 GMT  
		Size: 19.6 MB (19592556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2851c661eadabfff21636e396053a6ef65d7806e441da086e892a0570aa37b52`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55eeafb0e1065fbf8e495e596ab0979a2351aff4f33b4e1dc7d6c99f871eae97`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a24fd78eaaa140c5da70cb45d1a53de3c80317b8541f80a1d05bd6e4560022c`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe15c09ff0502ba71e3b975f0220d421f288c20d8c5d5f64c098496b4d84efdc`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 23.4 MB (23432034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39061e0c2bb20d115f630e4eb90cda590eae044db260d399ae125e5b4328ff96`  
		Last Modified: Fri, 03 Apr 2026 16:50:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb55d0d2e05e9f25e431de1cb3fea9bd5a99ce82e687614b9e3d5ac2bfbfaafd`  
		Last Modified: Fri, 03 Apr 2026 16:50:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4c676b321d5f609545214e994c74729fcfa063fb1814060367301f2b68aca4`  
		Last Modified: Fri, 03 Apr 2026 16:50:23 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194caab5fefbe0467dced96b2a1e8533cd36bc07325c3061cff834433fab53d5`  
		Last Modified: Fri, 03 Apr 2026 16:50:25 GMT  
		Size: 11.6 MB (11645348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull docker@sha256:ab04187c13089ceac6c8818c2cee7ecaa4e2bcd39577cfe00552451287b6b504
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037474662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e24418c7a3a82d1da61a8aa6cd06b4a3d16a6fd1812578771b1d9af9cd36f32`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Fri, 03 Apr 2026 16:47:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Apr 2026 16:49:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Apr 2026 16:49:08 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:49:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.1.zip
# Fri, 03 Apr 2026 16:49:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:49:34 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:49:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Fri, 03 Apr 2026 16:49:36 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Fri, 03 Apr 2026 16:50:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:50:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:50:05 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Fri, 03 Apr 2026 16:50:06 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Fri, 03 Apr 2026 16:50:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ebc372135025e6455cdea33dd82b8909666f97ad0f0b8089e919cf8b924f91`  
		Last Modified: Fri, 03 Apr 2026 16:50:29 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a0847e4437ba3ef85e9d7047c62200d08f8b3a8a0324073b8c84df7f3f7ebd`  
		Last Modified: Fri, 03 Apr 2026 16:50:28 GMT  
		Size: 506.6 KB (506574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb834b3ffd73d9ed8159b55a49c6253d1c85f02ffac59225e3b9079a78dfd48c`  
		Last Modified: Fri, 03 Apr 2026 16:50:27 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78b00d43926aab381c0a1e819e40df628b0aaea20b0bed307acf7ada3e0d982`  
		Last Modified: Fri, 03 Apr 2026 16:50:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cad0814bf145decf1ec3cb79bec86b593fb57d01ebee80ac54f51a6af6fc720`  
		Last Modified: Fri, 03 Apr 2026 16:50:29 GMT  
		Size: 19.6 MB (19590099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270311dfd8f5531d6c32b37406f2b41b3e7ff9507a8bb14652d73535bfdd3441`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae99ac7ec1d7ab5a58d53f31b9a42850062421eaec71a4d870507a0c5807dcc`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8314d29cc08fe7941d705655bf4b8147b9260ef4948d41c42e276fb722d25291`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f0a73598ec6395d9181e8c1b347790635350d4747fb0470ce9362ba194a633`  
		Last Modified: Fri, 03 Apr 2026 16:50:39 GMT  
		Size: 23.4 MB (23437302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2085add922e64596325b1d712784edd2e4140f08996288115cef8e3a9124e354`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d126d916f3b83dd6f3e9b0c72322b5aea0fd8dca636eb24a8fcb310d246056`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842d24a00195d53f2b7a645e88c31a5b96671f836f2bfd39d06c6c3227a83d92`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c989b6a66281fbd8d67f03b69e1f471e216f3155c0a8bd5119b79c41ee8fab5`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 11.6 MB (11647528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:7544ccc6e4ea00729bf7d28604a8b6fb4315bdf05d8f441f01793865f20046a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull docker@sha256:ab04187c13089ceac6c8818c2cee7ecaa4e2bcd39577cfe00552451287b6b504
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037474662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e24418c7a3a82d1da61a8aa6cd06b4a3d16a6fd1812578771b1d9af9cd36f32`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Fri, 03 Apr 2026 16:47:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Apr 2026 16:49:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Apr 2026 16:49:08 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:49:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.1.zip
# Fri, 03 Apr 2026 16:49:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:49:34 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:49:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Fri, 03 Apr 2026 16:49:36 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Fri, 03 Apr 2026 16:50:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:50:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:50:05 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Fri, 03 Apr 2026 16:50:06 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Fri, 03 Apr 2026 16:50:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ebc372135025e6455cdea33dd82b8909666f97ad0f0b8089e919cf8b924f91`  
		Last Modified: Fri, 03 Apr 2026 16:50:29 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a0847e4437ba3ef85e9d7047c62200d08f8b3a8a0324073b8c84df7f3f7ebd`  
		Last Modified: Fri, 03 Apr 2026 16:50:28 GMT  
		Size: 506.6 KB (506574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb834b3ffd73d9ed8159b55a49c6253d1c85f02ffac59225e3b9079a78dfd48c`  
		Last Modified: Fri, 03 Apr 2026 16:50:27 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78b00d43926aab381c0a1e819e40df628b0aaea20b0bed307acf7ada3e0d982`  
		Last Modified: Fri, 03 Apr 2026 16:50:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cad0814bf145decf1ec3cb79bec86b593fb57d01ebee80ac54f51a6af6fc720`  
		Last Modified: Fri, 03 Apr 2026 16:50:29 GMT  
		Size: 19.6 MB (19590099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270311dfd8f5531d6c32b37406f2b41b3e7ff9507a8bb14652d73535bfdd3441`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae99ac7ec1d7ab5a58d53f31b9a42850062421eaec71a4d870507a0c5807dcc`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8314d29cc08fe7941d705655bf4b8147b9260ef4948d41c42e276fb722d25291`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f0a73598ec6395d9181e8c1b347790635350d4747fb0470ce9362ba194a633`  
		Last Modified: Fri, 03 Apr 2026 16:50:39 GMT  
		Size: 23.4 MB (23437302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2085add922e64596325b1d712784edd2e4140f08996288115cef8e3a9124e354`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d126d916f3b83dd6f3e9b0c72322b5aea0fd8dca636eb24a8fcb310d246056`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842d24a00195d53f2b7a645e88c31a5b96671f836f2bfd39d06c6c3227a83d92`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c989b6a66281fbd8d67f03b69e1f471e216f3155c0a8bd5119b79c41ee8fab5`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 11.6 MB (11647528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:570b2a0cb54cc1e4fb3c9c360c9fbf31c58a67160ffac2f851d5320b2220ee3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:a105d81267b506d283738c2eab0c3e5f2339533f55a3f4e578543f31a10c0559
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2136248524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5d491b6f638ed8098ef9803e3c78743401083c443ad9969e0c8c97b4a5061c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Fri, 03 Apr 2026 16:48:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Apr 2026 16:49:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Apr 2026 16:49:27 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:49:28 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.1.zip
# Fri, 03 Apr 2026 16:49:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:49:46 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:49:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Fri, 03 Apr 2026 16:49:48 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Fri, 03 Apr 2026 16:50:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:50:05 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:50:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Fri, 03 Apr 2026 16:50:07 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Fri, 03 Apr 2026 16:50:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be287d655249644e43f567922c8ace0ebd34d2029a63b5f7aff779c7f0ea81f`  
		Last Modified: Fri, 03 Apr 2026 16:50:28 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bacc8dcf99a4b510435fd53e918e3bd0d6f4fdf27dcb309c4534ce03060f4e4`  
		Last Modified: Fri, 03 Apr 2026 16:50:27 GMT  
		Size: 370.7 KB (370685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75b1a0e09957eca68ed1d9ce466b166f611394669ffd7e2ef3cb280d2e86086`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cd9630a95f491844d8e8a681bc533e92b0e16ccf40b4842c76d47b05c88b82`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea0afb7d1d92072a6f67dc1f20ac520593a6d5b6e34fd654db0236504072e6b`  
		Last Modified: Fri, 03 Apr 2026 16:50:29 GMT  
		Size: 19.6 MB (19592556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2851c661eadabfff21636e396053a6ef65d7806e441da086e892a0570aa37b52`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55eeafb0e1065fbf8e495e596ab0979a2351aff4f33b4e1dc7d6c99f871eae97`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a24fd78eaaa140c5da70cb45d1a53de3c80317b8541f80a1d05bd6e4560022c`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe15c09ff0502ba71e3b975f0220d421f288c20d8c5d5f64c098496b4d84efdc`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 23.4 MB (23432034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39061e0c2bb20d115f630e4eb90cda590eae044db260d399ae125e5b4328ff96`  
		Last Modified: Fri, 03 Apr 2026 16:50:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb55d0d2e05e9f25e431de1cb3fea9bd5a99ce82e687614b9e3d5ac2bfbfaafd`  
		Last Modified: Fri, 03 Apr 2026 16:50:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4c676b321d5f609545214e994c74729fcfa063fb1814060367301f2b68aca4`  
		Last Modified: Fri, 03 Apr 2026 16:50:23 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194caab5fefbe0467dced96b2a1e8533cd36bc07325c3061cff834433fab53d5`  
		Last Modified: Fri, 03 Apr 2026 16:50:25 GMT  
		Size: 11.6 MB (11645348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.4`

**does not exist** (yet?)

## `docker:29.4-cli`

**does not exist** (yet?)

## `docker:29.4-dind`

**does not exist** (yet?)

## `docker:29.4-dind-rootless`

**does not exist** (yet?)

## `docker:29.4-windowsservercore`

**does not exist** (yet?)

## `docker:29.4-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `docker:29.4-windowsservercore-ltsc2025`

**does not exist** (yet?)

## `docker:29.4.0`

**does not exist** (yet?)

## `docker:29.4.0-alpine3.23`

**does not exist** (yet?)

## `docker:29.4.0-cli`

**does not exist** (yet?)

## `docker:29.4.0-cli-alpine3.23`

**does not exist** (yet?)

## `docker:29.4.0-dind`

**does not exist** (yet?)

## `docker:29.4.0-dind-alpine3.23`

**does not exist** (yet?)

## `docker:29.4.0-dind-rootless`

**does not exist** (yet?)

## `docker:29.4.0-windowsservercore`

**does not exist** (yet?)

## `docker:29.4.0-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `docker:29.4.0-windowsservercore-ltsc2025`

**does not exist** (yet?)

## `docker:cli`

```console
$ docker pull docker@sha256:18f5ab0fab739ea822819b342357947dfba235cdef438cce345ebc0c143c5b34
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
$ docker pull docker@sha256:b5fd064ef9d1ecb6980bebaf40d58cffca1a189e72805faca59af065bd7f7cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64683189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc513c142fdd740f7b4713af29da1dec9fa9ff53f9733566ae0635682df5c6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:45:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:45:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:45:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:45:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:45:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:45:38 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5679c6e6d45e2117c7e3c64d19dab37d2a751f6a8695b274011446785f5d974c`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 8.4 MB (8399808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13651ff9f98a7a01804bc4cf9e0eb2c832d0e3943fafd7033fbc5323ee9433b`  
		Last Modified: Fri, 03 Apr 2026 16:45:44 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544adb853f84f48115a46cfc76c5571249eea3bba4d011cdd2597ca0de7ffef8`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 18.9 MB (18925071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba1b50fe56ad29f6925651dd92625d4036f4c2aacf7849211e6d670b1ff4d06`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6d188f4a78bc49c0959c568bafb7bc8fcd0ac75759eeafd11d4992d107ba85`  
		Last Modified: Fri, 03 Apr 2026 16:45:46 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc67e139528a062178a1c30de103fb26dda0f6ebf4830c41d1f9aaee8152ede`  
		Last Modified: Fri, 03 Apr 2026 16:45:46 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b27d2c00ac1735fa633c45701bedfe7dd9da3e3d8b88a55988b308f2723376`  
		Last Modified: Fri, 03 Apr 2026 16:45:47 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222c8ebb2714f03d9f0f7843bae67f66f6338ccc90a8112f7c5a9521fc5801fe`  
		Last Modified: Fri, 03 Apr 2026 16:45:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:61f6aa987355fd2c723f0770e3ec586287cfeb2a5a6dbdd9b815a4e2698e65bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db60dc956064ff657e5f67c712353b02b3b6cd1485d9767db1a8d03f2086d283`

```dockerfile
```

-	Layers:
	-	`sha256:a204fa9bc3a5008e92de29f8d9daa46eed02f6ade4cd0ee9ec3ff376dd092c9c`  
		Last Modified: Fri, 03 Apr 2026 16:45:44 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:534c81ceedd13f40a95d76431719eb5313b5aa7bc18c41a43cc220d52027ee78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61118378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdf1a50937f4c1b699422c7b1abb8bf0e7611be6c37d6b9f421c6d176d3c342`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:42:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:42:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:42:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:42:53 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:42:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:42:53 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:42:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:42:54 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:42:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:42:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:42:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740b77d615bd7056fdfa10ac45a84e645f200a1dd058906d2f7c5a35bcc02e0e`  
		Last Modified: Fri, 03 Apr 2026 16:42:40 GMT  
		Size: 8.3 MB (8300856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db9e15d099697e3e0f63334517990f0d02a61abec8f671ec78dada6c111aeb8`  
		Last Modified: Fri, 03 Apr 2026 16:42:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badfb5fc5bffef95600bd56a253abb2c9e0aa7be994d332c5bdc962dbf98badb`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 17.7 MB (17704829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b890c9d4f91eb3442685e449c8b2f364c130782eab7dde7ebf5bd1211e1cd5`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 21.2 MB (21151883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea243840babbe8bdb5e0b7671978e226849103468c141766d1e18ed194d5bd3`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 10.4 MB (10388833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d072a6693dba53c8443bed1cc8779971ded28b6d831cbe0ca5d27a86f601ca0`  
		Last Modified: Fri, 03 Apr 2026 16:43:01 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34d0b523dd86a1840dbb3798720e0049c99c117ab5e91e11075b17fd08d2585`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b8f16743d3303cdfbdc56baf88120b4f52d0611ab208ee368a51267c360ac3`  
		Last Modified: Fri, 03 Apr 2026 16:43:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:b9f0cd3c948f74de09a3047847ff1e29faad7b1a37b2a3e69a71eb8b18b6575f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764dd95beb61967fbecd25eaf5f1ddc926733263c1639855c122542000811423`

```dockerfile
```

-	Layers:
	-	`sha256:fb68f5b71deb7dc273f37425417366ffbcdd93dde04bee331c80ab0c99479d03`  
		Last Modified: Fri, 03 Apr 2026 16:43:01 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:51ff322f0054df2754fef335caeddc581e016d5fd1d0e3a52e023bf0bdf63b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60078278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5398a87e24104d708e0ccfb588dc51aba6911a6975c22cdde0975c105b46b192`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:45:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:45:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:45:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:45:44 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:45:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:45:44 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:45:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:45:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:45:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:45:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:45:46 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016deb0202a065a4c852f3f2050e118fc65d7c3cce2eafbe19ccf98d8ed89edf`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 7.6 MB (7597815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef50c437805c0b30e4f0d9a2b1d424511b36073620692593b22fec111a773a71`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576962e4d5abd715552603309b7b55bb37f0a2b337d7c0b8a5ebeb2fe76b8263`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 17.7 MB (17694914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f613c15806dfc400bd7f32c8ebf8b36aa8f94dbc6df38a83ec9b2e8545aa4717`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 21.1 MB (21129788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d06fdd3ade3c55eccdb7f475a525319fd35fdc888d2979c3e6c50b2048a502`  
		Last Modified: Fri, 03 Apr 2026 16:45:53 GMT  
		Size: 10.4 MB (10371886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf810380a1fd5b8ab1b6e406255fdb1fed4dda97ccb12e9d2ae40d9af7db41`  
		Last Modified: Fri, 03 Apr 2026 16:45:53 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ec359a5914fb65f503ead971c0c75e173d64dae3c1aad16c7f61c5069e969b`  
		Last Modified: Fri, 03 Apr 2026 16:45:54 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daefd04887b003c1b0328270d847084792ec4a75fed804f2ecd74a52ce074a31`  
		Last Modified: Fri, 03 Apr 2026 16:45:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:56b264f893b723521f9fe0c351f1ca921498328532e56c70ecbf19fbf217c5a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924ed150b180f7d94211c148a7d63f6e87ed1af907a149b95668d778ed15dc7e`

```dockerfile
```

-	Layers:
	-	`sha256:acbb087569d7a7926fa874efebe27fa3cc848d12859399bfe0d348106e197809`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3194496094bc2ff85b6e27d6e084a1a2cb962c9252dfc3daf5813991023e880a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60565584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0485c76ca15edf3e39284ff7f13d0ac4d9548b79983311b6ded1b6e439d17579`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:46:07 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:46:07 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:46:07 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:46:10 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:46:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:46:10 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:46:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:46:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:46:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:46:11 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777cc0dfb6b156ba8ae2d58bdc626d37d561285c3d8cb9f5dfab9e421b95c97a`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 8.5 MB (8453640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61cf8459e2976d9c1523c4817274c5542c2f14ca192664d8d5ad6eb7e492a00`  
		Last Modified: Fri, 03 Apr 2026 16:46:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8767096605cd5df8361d730cb51cdf77ce65a6d78016bfdcb25429f12a3b3c82`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 17.5 MB (17476968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14802cd569774821b1ac9c941f04e235ed46274c4a8ac0eae1b4b1ea971b6b2`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 20.5 MB (20453120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63242b8f6c4c149d7a76bebad8e17208b476be636d6f2c9ed5dca0a6e87eebd6`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 10.0 MB (9982610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f92f7532507e0be265cd5a585468bfba3ed63c8f64943bfffbdb4c8e2bc29d3`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1144373d60167579bb44d4f4ec630998cc0bf64b287b2e5ba3c03aa31aa1f3d`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1b6b3e13fd596fa602ee41b47089c2aa97d6adb582e423ec45a54312bda585`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:0680a367e5ffbce2c37efea411c79239cce4ba10e11fa3f8bf240f9b4696c40f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3bd6f7d935b2ea4dcebd0a62a2f6534301269753ddf098dcb5ccbfe08ed63c9`

```dockerfile
```

-	Layers:
	-	`sha256:74e8e8209c9cead51c4d4165ab182f2b610af1f09c61fe4adf46ac23dc87428b`  
		Last Modified: Fri, 03 Apr 2026 16:46:17 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:686d2c5464787b0ca42420e0aa03a94fc9781ff9bf8b5ff947614b9fa4c3c3e0
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
$ docker pull docker@sha256:a8d074fe486e65abe4ce251c264b78727be7b63a789ccb1eff2dcc786b443cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138543816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f54e33ee2ddd176e83bf6161114efa18dc63c00326ed58fa0697a8796417994`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:45:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:45:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:45:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:45:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:45:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:45:38 GMT
CMD ["sh"]
# Fri, 03 Apr 2026 17:05:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 03 Apr 2026 17:05:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 03 Apr 2026 17:05:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 17:05:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 03 Apr 2026 17:05:18 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 03 Apr 2026 17:05:18 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 03 Apr 2026 17:05:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 17:05:18 GMT
VOLUME [/var/lib/docker]
# Fri, 03 Apr 2026 17:05:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 03 Apr 2026 17:05:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 03 Apr 2026 17:05:18 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5679c6e6d45e2117c7e3c64d19dab37d2a751f6a8695b274011446785f5d974c`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 8.4 MB (8399808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13651ff9f98a7a01804bc4cf9e0eb2c832d0e3943fafd7033fbc5323ee9433b`  
		Last Modified: Fri, 03 Apr 2026 16:45:44 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544adb853f84f48115a46cfc76c5571249eea3bba4d011cdd2597ca0de7ffef8`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 18.9 MB (18925071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba1b50fe56ad29f6925651dd92625d4036f4c2aacf7849211e6d670b1ff4d06`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6d188f4a78bc49c0959c568bafb7bc8fcd0ac75759eeafd11d4992d107ba85`  
		Last Modified: Fri, 03 Apr 2026 16:45:46 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc67e139528a062178a1c30de103fb26dda0f6ebf4830c41d1f9aaee8152ede`  
		Last Modified: Fri, 03 Apr 2026 16:45:46 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b27d2c00ac1735fa633c45701bedfe7dd9da3e3d8b88a55988b308f2723376`  
		Last Modified: Fri, 03 Apr 2026 16:45:47 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222c8ebb2714f03d9f0f7843bae67f66f6338ccc90a8112f7c5a9521fc5801fe`  
		Last Modified: Fri, 03 Apr 2026 16:45:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86d96e88e4e907e31d182840119fabe703605b2e06c4a09d8a6d834754f12d4`  
		Last Modified: Fri, 03 Apr 2026 17:05:28 GMT  
		Size: 6.9 MB (6941639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cd9ca13141b31f2e62665957ee09ef0c28043fd9387d9c0c8ab048c3ca733b`  
		Last Modified: Fri, 03 Apr 2026 17:05:28 GMT  
		Size: 92.5 KB (92467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e127f411f6f1e1e5c228b9abf2ffe140a51edd2fc7e01e10f288525cdc36ebb`  
		Last Modified: Fri, 03 Apr 2026 17:05:28 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dcdc10364839056046aa19eb6a60c4d58e4d10c5b1abfd55f7d59b892ea910`  
		Last Modified: Fri, 03 Apr 2026 17:05:29 GMT  
		Size: 66.8 MB (66820522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4e9dea14a990a6b4f886171b26e24c66a6dbf851770b89afecd957b1d474d3`  
		Last Modified: Fri, 03 Apr 2026 17:05:29 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7602952982b750a0406fdf55807029c5e9eec431c1b585249b645782c0bb9640`  
		Last Modified: Fri, 03 Apr 2026 17:05:29 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:6a9cb94ed582de72b8c20772159e4beccdef0872fcd8373329db8894ab929e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1082d29eecf0a87567132592c6cafae8a6d6224d31b0844e86b08efcaa01f2f`

```dockerfile
```

-	Layers:
	-	`sha256:6a125f5c2f04596e1020bab77445cd2a497a2232e932e788ff5c43b8b7044737`  
		Last Modified: Fri, 03 Apr 2026 17:05:27 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:7472af905743da87fcc68ddf6d8e36229f3ed09052d60180527bb92d6ecacf7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130713665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd63b01ea25750846b6b8c1a8f2d216ff8bf3fd2d5e44ec3d9377ee811893d31`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:42:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:42:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:42:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:42:53 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:42:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:42:53 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:42:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:42:54 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:42:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:42:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:42:55 GMT
CMD ["sh"]
# Fri, 03 Apr 2026 16:46:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 03 Apr 2026 16:46:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 03 Apr 2026 16:46:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 16:46:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 03 Apr 2026 16:46:18 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 03 Apr 2026 16:46:18 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 03 Apr 2026 16:46:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:46:18 GMT
VOLUME [/var/lib/docker]
# Fri, 03 Apr 2026 16:46:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 03 Apr 2026 16:46:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 03 Apr 2026 16:46:18 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740b77d615bd7056fdfa10ac45a84e645f200a1dd058906d2f7c5a35bcc02e0e`  
		Last Modified: Fri, 03 Apr 2026 16:42:40 GMT  
		Size: 8.3 MB (8300856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db9e15d099697e3e0f63334517990f0d02a61abec8f671ec78dada6c111aeb8`  
		Last Modified: Fri, 03 Apr 2026 16:42:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badfb5fc5bffef95600bd56a253abb2c9e0aa7be994d332c5bdc962dbf98badb`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 17.7 MB (17704829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b890c9d4f91eb3442685e449c8b2f364c130782eab7dde7ebf5bd1211e1cd5`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 21.2 MB (21151883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea243840babbe8bdb5e0b7671978e226849103468c141766d1e18ed194d5bd3`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 10.4 MB (10388833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d072a6693dba53c8443bed1cc8779971ded28b6d831cbe0ca5d27a86f601ca0`  
		Last Modified: Fri, 03 Apr 2026 16:43:01 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34d0b523dd86a1840dbb3798720e0049c99c117ab5e91e11075b17fd08d2585`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b8f16743d3303cdfbdc56baf88120b4f52d0611ab208ee368a51267c360ac3`  
		Last Modified: Fri, 03 Apr 2026 16:43:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab55bf4153bdd56cb5f39f6650cfd9ba51c20e91bf2cff28e2cfcd749065c33`  
		Last Modified: Fri, 03 Apr 2026 16:46:29 GMT  
		Size: 7.3 MB (7278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02343a21b91c469b5cea7d6b52bd1422865f8d2fad041c5227903c82f5f39af`  
		Last Modified: Fri, 03 Apr 2026 16:46:29 GMT  
		Size: 91.8 KB (91785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fa33dfd5171fc56035c6f6fcc1a091d64971f1358915351923d6ca04a57328`  
		Last Modified: Fri, 03 Apr 2026 16:46:29 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d009d61277728e00d4620b798dcf41f5fc05bab7202c4b473db5f31426c2526e`  
		Last Modified: Fri, 03 Apr 2026 16:46:36 GMT  
		Size: 62.2 MB (62219223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604ede2b569e27b5f9062e1be9e2c95edd8a6f095e32a5a30d97ba08a0b9c4df`  
		Last Modified: Fri, 03 Apr 2026 16:46:30 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310af0449d43a19911330553d114ddf7f4acfdcade100c8b95295a23955f3bf6`  
		Last Modified: Fri, 03 Apr 2026 16:46:30 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:671d618f4f9d1fa039add9a97d36ddf277f9504c1def3a3d120398991873ac5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e404d9d065a5ea816b651f07800e4324288d09559d495c93eb8474784512c29a`

```dockerfile
```

-	Layers:
	-	`sha256:f961aeca8ebff8d2f0901fffaa890d60bb5143ab2780e15a0cce286525bbdea6`  
		Last Modified: Fri, 03 Apr 2026 16:46:28 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:76eff0f95837c7139e58b0c525b423dc55e518b976071fae0d564a2caaddfeb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128787145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2840bf830b179b108077625e8aac3296cd18b0b9abe8e0a0955df919559debba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:45:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:45:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:45:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:45:44 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:45:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:45:44 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:45:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:45:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:45:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:45:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:45:46 GMT
CMD ["sh"]
# Fri, 03 Apr 2026 16:58:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 03 Apr 2026 16:58:00 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 03 Apr 2026 16:58:00 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 16:58:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 03 Apr 2026 16:58:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 03 Apr 2026 16:58:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 03 Apr 2026 16:58:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:58:04 GMT
VOLUME [/var/lib/docker]
# Fri, 03 Apr 2026 16:58:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 03 Apr 2026 16:58:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 03 Apr 2026 16:58:04 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016deb0202a065a4c852f3f2050e118fc65d7c3cce2eafbe19ccf98d8ed89edf`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 7.6 MB (7597815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef50c437805c0b30e4f0d9a2b1d424511b36073620692593b22fec111a773a71`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576962e4d5abd715552603309b7b55bb37f0a2b337d7c0b8a5ebeb2fe76b8263`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 17.7 MB (17694914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f613c15806dfc400bd7f32c8ebf8b36aa8f94dbc6df38a83ec9b2e8545aa4717`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 21.1 MB (21129788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d06fdd3ade3c55eccdb7f475a525319fd35fdc888d2979c3e6c50b2048a502`  
		Last Modified: Fri, 03 Apr 2026 16:45:53 GMT  
		Size: 10.4 MB (10371886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf810380a1fd5b8ab1b6e406255fdb1fed4dda97ccb12e9d2ae40d9af7db41`  
		Last Modified: Fri, 03 Apr 2026 16:45:53 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ec359a5914fb65f503ead971c0c75e173d64dae3c1aad16c7f61c5069e969b`  
		Last Modified: Fri, 03 Apr 2026 16:45:54 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daefd04887b003c1b0328270d847084792ec4a75fed804f2ecd74a52ce074a31`  
		Last Modified: Fri, 03 Apr 2026 16:45:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b87d725529cf9b2c6f3e97907240a840520238ccce0347a64b1748962550d0f`  
		Last Modified: Fri, 03 Apr 2026 16:58:13 GMT  
		Size: 6.6 MB (6576423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b442283958037b11199976c605936942e358ab2758f524892a7086d676731e3`  
		Last Modified: Fri, 03 Apr 2026 16:58:13 GMT  
		Size: 88.1 KB (88144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ddc76cf55621abb7f91ecb29cae63e62c062164faf0c5a3c3361ed24fd2cd8`  
		Last Modified: Fri, 03 Apr 2026 16:58:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872cc131a341fa5dadabaaee49da5ba50dede23673dc81b20f75734504c4d23`  
		Last Modified: Fri, 03 Apr 2026 16:58:15 GMT  
		Size: 62.0 MB (62038306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b637186d0c474f679193ffe3a56fa55c6f81b6f7dbc46d85f24b68cefc03a4ae`  
		Last Modified: Fri, 03 Apr 2026 16:58:15 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36899143ff8194ff19a37d1bf9a5fa09858b0681841d180bd4e941278083cca9`  
		Last Modified: Fri, 03 Apr 2026 16:58:14 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:5435bf083ece270255a97e1bb24b88fce07499c1f6157a9d2cf8c414ace837bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83848fa250ffaaec1fe904ba1e1ae70d36dc8271f888b9e7574093eca93ed810`

```dockerfile
```

-	Layers:
	-	`sha256:59371fc5db1308a770e76bb8a671353b4b304c4fa257b097f02ad3acc7ecab70`  
		Last Modified: Fri, 03 Apr 2026 16:58:13 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ef75021c3c564a7977f21b23cd6d6cf0057441a0f6bb0e018410c5711de72f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128500378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a51c77dd3447c7efe6d0d9a8d2b8293a6e2c3f699667a6d85bbe6682d82647b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:46:07 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:46:07 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:46:07 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:46:10 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:46:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:46:10 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:46:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:46:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:46:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:46:11 GMT
CMD ["sh"]
# Fri, 03 Apr 2026 17:13:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 03 Apr 2026 17:13:13 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 03 Apr 2026 17:13:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 03 Apr 2026 17:13:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
VOLUME [/var/lib/docker]
# Fri, 03 Apr 2026 17:13:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 03 Apr 2026 17:13:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 03 Apr 2026 17:13:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777cc0dfb6b156ba8ae2d58bdc626d37d561285c3d8cb9f5dfab9e421b95c97a`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 8.5 MB (8453640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61cf8459e2976d9c1523c4817274c5542c2f14ca192664d8d5ad6eb7e492a00`  
		Last Modified: Fri, 03 Apr 2026 16:46:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8767096605cd5df8361d730cb51cdf77ce65a6d78016bfdcb25429f12a3b3c82`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 17.5 MB (17476968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14802cd569774821b1ac9c941f04e235ed46274c4a8ac0eae1b4b1ea971b6b2`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 20.5 MB (20453120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63242b8f6c4c149d7a76bebad8e17208b476be636d6f2c9ed5dca0a6e87eebd6`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 10.0 MB (9982610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f92f7532507e0be265cd5a585468bfba3ed63c8f64943bfffbdb4c8e2bc29d3`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1144373d60167579bb44d4f4ec630998cc0bf64b287b2e5ba3c03aa31aa1f3d`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1b6b3e13fd596fa602ee41b47089c2aa97d6adb582e423ec45a54312bda585`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7bcce9135e50e8113ce567e771818f45458b22e72a5b64b70da654eebd0e99`  
		Last Modified: Fri, 03 Apr 2026 17:13:25 GMT  
		Size: 7.2 MB (7219478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830d8e038e6c3e9055a2326f9fee1c908c9b60277c26df9b8ac5decd85cd3c08`  
		Last Modified: Fri, 03 Apr 2026 17:13:24 GMT  
		Size: 101.3 KB (101299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce438bd7121c26756c9344834a818efa8088cbd191053f8237e7ab52a55bee8b`  
		Last Modified: Fri, 03 Apr 2026 17:13:25 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8572ba2382e471780ecdf47f897386999474a08611c84b60f7f9664f27c0c7`  
		Last Modified: Fri, 03 Apr 2026 17:13:26 GMT  
		Size: 60.6 MB (60608023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0059d0fd9057439969d2dbf52619e8c263ad6c554c1f948b3cba6c9c94912e80`  
		Last Modified: Fri, 03 Apr 2026 17:13:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3764136014318e546423f2772475f4d7562d75fcd1407fd1c1bd941b0d1542`  
		Last Modified: Fri, 03 Apr 2026 17:13:26 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:cfa3bba5e17688594fc44b1a3d2f036d316ec72d1087c5cfcda980e17099085e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1edcd89a3d057104931b35657c5c97cd175a0a2255935ec50e46250e09864642`

```dockerfile
```

-	Layers:
	-	`sha256:a6f088a054073c23988be89705d5498a22b7cedd81fad3d5bb5196ffeebafc6d`  
		Last Modified: Fri, 03 Apr 2026 17:13:24 GMT  
		Size: 34.8 KB (34775 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:5fd70e50e710078a3c8c3eaa96c0e788740ee71934f48efce17573a47db7cf4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9ad408a87b7bc68a51b5b9b7480e6d5b603dcdcf8bcf760a0bf1bd80127dca3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.4 MB (159350536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c26f0075065a8672e7fc616d39b9a0b70b5965bc967269e06fcefe2ff62f31e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:45:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:45:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:45:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:45:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:45:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:45:38 GMT
CMD ["sh"]
# Fri, 03 Apr 2026 17:05:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 03 Apr 2026 17:05:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 03 Apr 2026 17:05:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 17:05:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 03 Apr 2026 17:05:18 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 03 Apr 2026 17:05:18 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 03 Apr 2026 17:05:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 17:05:18 GMT
VOLUME [/var/lib/docker]
# Fri, 03 Apr 2026 17:05:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 03 Apr 2026 17:05:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 03 Apr 2026 17:05:18 GMT
CMD []
# Fri, 03 Apr 2026 17:13:33 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 03 Apr 2026 17:13:33 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 03 Apr 2026 17:13:34 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 17:13:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 03 Apr 2026 17:13:34 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 03 Apr 2026 17:13:34 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 03 Apr 2026 17:13:34 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5679c6e6d45e2117c7e3c64d19dab37d2a751f6a8695b274011446785f5d974c`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 8.4 MB (8399808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13651ff9f98a7a01804bc4cf9e0eb2c832d0e3943fafd7033fbc5323ee9433b`  
		Last Modified: Fri, 03 Apr 2026 16:45:44 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544adb853f84f48115a46cfc76c5571249eea3bba4d011cdd2597ca0de7ffef8`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 18.9 MB (18925071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba1b50fe56ad29f6925651dd92625d4036f4c2aacf7849211e6d670b1ff4d06`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6d188f4a78bc49c0959c568bafb7bc8fcd0ac75759eeafd11d4992d107ba85`  
		Last Modified: Fri, 03 Apr 2026 16:45:46 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc67e139528a062178a1c30de103fb26dda0f6ebf4830c41d1f9aaee8152ede`  
		Last Modified: Fri, 03 Apr 2026 16:45:46 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b27d2c00ac1735fa633c45701bedfe7dd9da3e3d8b88a55988b308f2723376`  
		Last Modified: Fri, 03 Apr 2026 16:45:47 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222c8ebb2714f03d9f0f7843bae67f66f6338ccc90a8112f7c5a9521fc5801fe`  
		Last Modified: Fri, 03 Apr 2026 16:45:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86d96e88e4e907e31d182840119fabe703605b2e06c4a09d8a6d834754f12d4`  
		Last Modified: Fri, 03 Apr 2026 17:05:28 GMT  
		Size: 6.9 MB (6941639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cd9ca13141b31f2e62665957ee09ef0c28043fd9387d9c0c8ab048c3ca733b`  
		Last Modified: Fri, 03 Apr 2026 17:05:28 GMT  
		Size: 92.5 KB (92467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e127f411f6f1e1e5c228b9abf2ffe140a51edd2fc7e01e10f288525cdc36ebb`  
		Last Modified: Fri, 03 Apr 2026 17:05:28 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dcdc10364839056046aa19eb6a60c4d58e4d10c5b1abfd55f7d59b892ea910`  
		Last Modified: Fri, 03 Apr 2026 17:05:29 GMT  
		Size: 66.8 MB (66820522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4e9dea14a990a6b4f886171b26e24c66a6dbf851770b89afecd957b1d474d3`  
		Last Modified: Fri, 03 Apr 2026 17:05:29 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7602952982b750a0406fdf55807029c5e9eec431c1b585249b645782c0bb9640`  
		Last Modified: Fri, 03 Apr 2026 17:05:29 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77d1d2a4fe8087c79d70a0f3b208fde9e5083b9cdace6e9fbba1410b76615c9`  
		Last Modified: Fri, 03 Apr 2026 17:13:41 GMT  
		Size: 3.4 MB (3419946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ed1b22f98a868fa49be3cf3b6f43c9c7e240d3a0491fd7d4399ef5dbda8f5d`  
		Last Modified: Fri, 03 Apr 2026 17:13:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392e87366b916c8d9cf5dea477b6770a49d0e13bdae6b512026b87a6366dd02b`  
		Last Modified: Fri, 03 Apr 2026 17:13:41 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1e7a9eed6561ca743cfd7ed4c6759d717e1d577c39ecbd7d59fe6b566300d5`  
		Last Modified: Fri, 03 Apr 2026 17:13:41 GMT  
		Size: 17.4 MB (17385434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce6f31a4b269f5fd157606d7d1ed46c45b48062ea29c18422af40d9beb35417`  
		Last Modified: Fri, 03 Apr 2026 17:13:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:03c8886a0bd50b365eaf01a8cc97410db4dc94bd215ebb71297064b4affea7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ac462145506cc6d2425ae86571456b9c24115bc341b6d68dcf5fd2df3677fb`

```dockerfile
```

-	Layers:
	-	`sha256:9f182fcb771b62e6a69a3a73b529aca8b87bd308a7af152db961de64d5e36783`  
		Last Modified: Fri, 03 Apr 2026 17:13:40 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6679cb2aefe477b0d944091963ef8d1f8b8db4cd4404cc8add23e4313fce04ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.6 MB (149610516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da1dfa1a7531898d0ffb21ba6c3a9cf596386b2c008f0b644ba8c67be847cbb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:46:07 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:46:07 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:46:07 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:46:10 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:46:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:46:10 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:46:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:46:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:46:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:46:11 GMT
CMD ["sh"]
# Fri, 03 Apr 2026 17:13:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 03 Apr 2026 17:13:13 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 03 Apr 2026 17:13:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 03 Apr 2026 17:13:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
VOLUME [/var/lib/docker]
# Fri, 03 Apr 2026 17:13:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 03 Apr 2026 17:13:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 03 Apr 2026 17:13:15 GMT
CMD []
# Fri, 03 Apr 2026 17:25:14 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 03 Apr 2026 17:25:14 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 03 Apr 2026 17:25:14 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 17:25:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 03 Apr 2026 17:25:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 03 Apr 2026 17:25:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 03 Apr 2026 17:25:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777cc0dfb6b156ba8ae2d58bdc626d37d561285c3d8cb9f5dfab9e421b95c97a`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 8.5 MB (8453640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61cf8459e2976d9c1523c4817274c5542c2f14ca192664d8d5ad6eb7e492a00`  
		Last Modified: Fri, 03 Apr 2026 16:46:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8767096605cd5df8361d730cb51cdf77ce65a6d78016bfdcb25429f12a3b3c82`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 17.5 MB (17476968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14802cd569774821b1ac9c941f04e235ed46274c4a8ac0eae1b4b1ea971b6b2`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 20.5 MB (20453120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63242b8f6c4c149d7a76bebad8e17208b476be636d6f2c9ed5dca0a6e87eebd6`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 10.0 MB (9982610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f92f7532507e0be265cd5a585468bfba3ed63c8f64943bfffbdb4c8e2bc29d3`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1144373d60167579bb44d4f4ec630998cc0bf64b287b2e5ba3c03aa31aa1f3d`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1b6b3e13fd596fa602ee41b47089c2aa97d6adb582e423ec45a54312bda585`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7bcce9135e50e8113ce567e771818f45458b22e72a5b64b70da654eebd0e99`  
		Last Modified: Fri, 03 Apr 2026 17:13:25 GMT  
		Size: 7.2 MB (7219478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830d8e038e6c3e9055a2326f9fee1c908c9b60277c26df9b8ac5decd85cd3c08`  
		Last Modified: Fri, 03 Apr 2026 17:13:24 GMT  
		Size: 101.3 KB (101299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce438bd7121c26756c9344834a818efa8088cbd191053f8237e7ab52a55bee8b`  
		Last Modified: Fri, 03 Apr 2026 17:13:25 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8572ba2382e471780ecdf47f897386999474a08611c84b60f7f9664f27c0c7`  
		Last Modified: Fri, 03 Apr 2026 17:13:26 GMT  
		Size: 60.6 MB (60608023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0059d0fd9057439969d2dbf52619e8c263ad6c554c1f948b3cba6c9c94912e80`  
		Last Modified: Fri, 03 Apr 2026 17:13:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3764136014318e546423f2772475f4d7562d75fcd1407fd1c1bd941b0d1542`  
		Last Modified: Fri, 03 Apr 2026 17:13:26 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503dd12c2fdaa4e9d1ca00275d42321966bc1ea7f174b1af8b4a4383afcd22e4`  
		Last Modified: Fri, 03 Apr 2026 17:25:21 GMT  
		Size: 3.4 MB (3394365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9267ed34f5f7b5284c28c8d607dcbd616fd8d15cb5e9f3a6e7a98d79ee3d02f`  
		Last Modified: Fri, 03 Apr 2026 17:25:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97dcc6860b1c94957073ca4b75a0bc2b662ad2c642f27f1fc2e903edb407f9f`  
		Last Modified: Fri, 03 Apr 2026 17:25:21 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90d00483cc8dcbb6d0186a4ef64291f65acb96973d6a288d7895cd2fe03688b`  
		Last Modified: Fri, 03 Apr 2026 17:25:22 GMT  
		Size: 17.7 MB (17714430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225856b6401e13d11d803a1b9b8c24cec5de0a863f43e8b3a0c128526ced06f4`  
		Last Modified: Fri, 03 Apr 2026 17:25:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bdc6ca529abd59bb8aea5ee4c333dc839cddfb3859157f4a157f484458a4a426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f669db25bcbdc78b0e1bed87de14f4f4c286679900eba52e9f3c547d90db8a96`

```dockerfile
```

-	Layers:
	-	`sha256:a082c4facd362ebcdd9ae60cfe71df1d11ae9c3eb0daea05952c744240c2cf8c`  
		Last Modified: Fri, 03 Apr 2026 17:25:21 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:686d2c5464787b0ca42420e0aa03a94fc9781ff9bf8b5ff947614b9fa4c3c3e0
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
$ docker pull docker@sha256:a8d074fe486e65abe4ce251c264b78727be7b63a789ccb1eff2dcc786b443cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138543816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f54e33ee2ddd176e83bf6161114efa18dc63c00326ed58fa0697a8796417994`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:45:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:45:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:45:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:45:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:45:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:45:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:45:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:45:38 GMT
CMD ["sh"]
# Fri, 03 Apr 2026 17:05:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 03 Apr 2026 17:05:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 03 Apr 2026 17:05:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 17:05:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 03 Apr 2026 17:05:18 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 03 Apr 2026 17:05:18 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 03 Apr 2026 17:05:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 17:05:18 GMT
VOLUME [/var/lib/docker]
# Fri, 03 Apr 2026 17:05:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 03 Apr 2026 17:05:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 03 Apr 2026 17:05:18 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5679c6e6d45e2117c7e3c64d19dab37d2a751f6a8695b274011446785f5d974c`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 8.4 MB (8399808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13651ff9f98a7a01804bc4cf9e0eb2c832d0e3943fafd7033fbc5323ee9433b`  
		Last Modified: Fri, 03 Apr 2026 16:45:44 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544adb853f84f48115a46cfc76c5571249eea3bba4d011cdd2597ca0de7ffef8`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 18.9 MB (18925071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba1b50fe56ad29f6925651dd92625d4036f4c2aacf7849211e6d670b1ff4d06`  
		Last Modified: Fri, 03 Apr 2026 16:45:45 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6d188f4a78bc49c0959c568bafb7bc8fcd0ac75759eeafd11d4992d107ba85`  
		Last Modified: Fri, 03 Apr 2026 16:45:46 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc67e139528a062178a1c30de103fb26dda0f6ebf4830c41d1f9aaee8152ede`  
		Last Modified: Fri, 03 Apr 2026 16:45:46 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b27d2c00ac1735fa633c45701bedfe7dd9da3e3d8b88a55988b308f2723376`  
		Last Modified: Fri, 03 Apr 2026 16:45:47 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222c8ebb2714f03d9f0f7843bae67f66f6338ccc90a8112f7c5a9521fc5801fe`  
		Last Modified: Fri, 03 Apr 2026 16:45:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86d96e88e4e907e31d182840119fabe703605b2e06c4a09d8a6d834754f12d4`  
		Last Modified: Fri, 03 Apr 2026 17:05:28 GMT  
		Size: 6.9 MB (6941639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cd9ca13141b31f2e62665957ee09ef0c28043fd9387d9c0c8ab048c3ca733b`  
		Last Modified: Fri, 03 Apr 2026 17:05:28 GMT  
		Size: 92.5 KB (92467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e127f411f6f1e1e5c228b9abf2ffe140a51edd2fc7e01e10f288525cdc36ebb`  
		Last Modified: Fri, 03 Apr 2026 17:05:28 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dcdc10364839056046aa19eb6a60c4d58e4d10c5b1abfd55f7d59b892ea910`  
		Last Modified: Fri, 03 Apr 2026 17:05:29 GMT  
		Size: 66.8 MB (66820522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4e9dea14a990a6b4f886171b26e24c66a6dbf851770b89afecd957b1d474d3`  
		Last Modified: Fri, 03 Apr 2026 17:05:29 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7602952982b750a0406fdf55807029c5e9eec431c1b585249b645782c0bb9640`  
		Last Modified: Fri, 03 Apr 2026 17:05:29 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:6a9cb94ed582de72b8c20772159e4beccdef0872fcd8373329db8894ab929e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1082d29eecf0a87567132592c6cafae8a6d6224d31b0844e86b08efcaa01f2f`

```dockerfile
```

-	Layers:
	-	`sha256:6a125f5c2f04596e1020bab77445cd2a497a2232e932e788ff5c43b8b7044737`  
		Last Modified: Fri, 03 Apr 2026 17:05:27 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:7472af905743da87fcc68ddf6d8e36229f3ed09052d60180527bb92d6ecacf7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130713665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd63b01ea25750846b6b8c1a8f2d216ff8bf3fd2d5e44ec3d9377ee811893d31`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:42:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:42:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:42:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:42:53 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:42:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:42:53 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:42:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:42:54 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:42:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:42:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:42:55 GMT
CMD ["sh"]
# Fri, 03 Apr 2026 16:46:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 03 Apr 2026 16:46:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 03 Apr 2026 16:46:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 16:46:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 03 Apr 2026 16:46:18 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 03 Apr 2026 16:46:18 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 03 Apr 2026 16:46:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:46:18 GMT
VOLUME [/var/lib/docker]
# Fri, 03 Apr 2026 16:46:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 03 Apr 2026 16:46:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 03 Apr 2026 16:46:18 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740b77d615bd7056fdfa10ac45a84e645f200a1dd058906d2f7c5a35bcc02e0e`  
		Last Modified: Fri, 03 Apr 2026 16:42:40 GMT  
		Size: 8.3 MB (8300856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db9e15d099697e3e0f63334517990f0d02a61abec8f671ec78dada6c111aeb8`  
		Last Modified: Fri, 03 Apr 2026 16:42:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badfb5fc5bffef95600bd56a253abb2c9e0aa7be994d332c5bdc962dbf98badb`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 17.7 MB (17704829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b890c9d4f91eb3442685e449c8b2f364c130782eab7dde7ebf5bd1211e1cd5`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 21.2 MB (21151883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea243840babbe8bdb5e0b7671978e226849103468c141766d1e18ed194d5bd3`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 10.4 MB (10388833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d072a6693dba53c8443bed1cc8779971ded28b6d831cbe0ca5d27a86f601ca0`  
		Last Modified: Fri, 03 Apr 2026 16:43:01 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34d0b523dd86a1840dbb3798720e0049c99c117ab5e91e11075b17fd08d2585`  
		Last Modified: Fri, 03 Apr 2026 16:43:02 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b8f16743d3303cdfbdc56baf88120b4f52d0611ab208ee368a51267c360ac3`  
		Last Modified: Fri, 03 Apr 2026 16:43:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab55bf4153bdd56cb5f39f6650cfd9ba51c20e91bf2cff28e2cfcd749065c33`  
		Last Modified: Fri, 03 Apr 2026 16:46:29 GMT  
		Size: 7.3 MB (7278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02343a21b91c469b5cea7d6b52bd1422865f8d2fad041c5227903c82f5f39af`  
		Last Modified: Fri, 03 Apr 2026 16:46:29 GMT  
		Size: 91.8 KB (91785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fa33dfd5171fc56035c6f6fcc1a091d64971f1358915351923d6ca04a57328`  
		Last Modified: Fri, 03 Apr 2026 16:46:29 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d009d61277728e00d4620b798dcf41f5fc05bab7202c4b473db5f31426c2526e`  
		Last Modified: Fri, 03 Apr 2026 16:46:36 GMT  
		Size: 62.2 MB (62219223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604ede2b569e27b5f9062e1be9e2c95edd8a6f095e32a5a30d97ba08a0b9c4df`  
		Last Modified: Fri, 03 Apr 2026 16:46:30 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310af0449d43a19911330553d114ddf7f4acfdcade100c8b95295a23955f3bf6`  
		Last Modified: Fri, 03 Apr 2026 16:46:30 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:671d618f4f9d1fa039add9a97d36ddf277f9504c1def3a3d120398991873ac5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e404d9d065a5ea816b651f07800e4324288d09559d495c93eb8474784512c29a`

```dockerfile
```

-	Layers:
	-	`sha256:f961aeca8ebff8d2f0901fffaa890d60bb5143ab2780e15a0cce286525bbdea6`  
		Last Modified: Fri, 03 Apr 2026 16:46:28 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:76eff0f95837c7139e58b0c525b423dc55e518b976071fae0d564a2caaddfeb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128787145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2840bf830b179b108077625e8aac3296cd18b0b9abe8e0a0955df919559debba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:45:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:45:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:45:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:45:44 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:45:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:45:44 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:45:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:45:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:45:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:45:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:45:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:45:46 GMT
CMD ["sh"]
# Fri, 03 Apr 2026 16:58:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 03 Apr 2026 16:58:00 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 03 Apr 2026 16:58:00 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 16:58:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 03 Apr 2026 16:58:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 03 Apr 2026 16:58:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 03 Apr 2026 16:58:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:58:04 GMT
VOLUME [/var/lib/docker]
# Fri, 03 Apr 2026 16:58:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 03 Apr 2026 16:58:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 03 Apr 2026 16:58:04 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016deb0202a065a4c852f3f2050e118fc65d7c3cce2eafbe19ccf98d8ed89edf`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 7.6 MB (7597815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef50c437805c0b30e4f0d9a2b1d424511b36073620692593b22fec111a773a71`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576962e4d5abd715552603309b7b55bb37f0a2b337d7c0b8a5ebeb2fe76b8263`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 17.7 MB (17694914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f613c15806dfc400bd7f32c8ebf8b36aa8f94dbc6df38a83ec9b2e8545aa4717`  
		Last Modified: Fri, 03 Apr 2026 16:45:52 GMT  
		Size: 21.1 MB (21129788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d06fdd3ade3c55eccdb7f475a525319fd35fdc888d2979c3e6c50b2048a502`  
		Last Modified: Fri, 03 Apr 2026 16:45:53 GMT  
		Size: 10.4 MB (10371886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf810380a1fd5b8ab1b6e406255fdb1fed4dda97ccb12e9d2ae40d9af7db41`  
		Last Modified: Fri, 03 Apr 2026 16:45:53 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ec359a5914fb65f503ead971c0c75e173d64dae3c1aad16c7f61c5069e969b`  
		Last Modified: Fri, 03 Apr 2026 16:45:54 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daefd04887b003c1b0328270d847084792ec4a75fed804f2ecd74a52ce074a31`  
		Last Modified: Fri, 03 Apr 2026 16:45:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b87d725529cf9b2c6f3e97907240a840520238ccce0347a64b1748962550d0f`  
		Last Modified: Fri, 03 Apr 2026 16:58:13 GMT  
		Size: 6.6 MB (6576423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b442283958037b11199976c605936942e358ab2758f524892a7086d676731e3`  
		Last Modified: Fri, 03 Apr 2026 16:58:13 GMT  
		Size: 88.1 KB (88144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ddc76cf55621abb7f91ecb29cae63e62c062164faf0c5a3c3361ed24fd2cd8`  
		Last Modified: Fri, 03 Apr 2026 16:58:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872cc131a341fa5dadabaaee49da5ba50dede23673dc81b20f75734504c4d23`  
		Last Modified: Fri, 03 Apr 2026 16:58:15 GMT  
		Size: 62.0 MB (62038306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b637186d0c474f679193ffe3a56fa55c6f81b6f7dbc46d85f24b68cefc03a4ae`  
		Last Modified: Fri, 03 Apr 2026 16:58:15 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36899143ff8194ff19a37d1bf9a5fa09858b0681841d180bd4e941278083cca9`  
		Last Modified: Fri, 03 Apr 2026 16:58:14 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:5435bf083ece270255a97e1bb24b88fce07499c1f6157a9d2cf8c414ace837bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83848fa250ffaaec1fe904ba1e1ae70d36dc8271f888b9e7574093eca93ed810`

```dockerfile
```

-	Layers:
	-	`sha256:59371fc5db1308a770e76bb8a671353b4b304c4fa257b097f02ad3acc7ecab70`  
		Last Modified: Fri, 03 Apr 2026 16:58:13 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ef75021c3c564a7977f21b23cd6d6cf0057441a0f6bb0e018410c5711de72f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128500378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a51c77dd3447c7efe6d0d9a8d2b8293a6e2c3f699667a6d85bbe6682d82647b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:46:07 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:46:07 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:46:07 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:46:10 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:46:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:46:10 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:46:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:46:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:46:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:46:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:46:11 GMT
CMD ["sh"]
# Fri, 03 Apr 2026 17:13:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 03 Apr 2026 17:13:13 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 03 Apr 2026 17:13:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 03 Apr 2026 17:13:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 17:13:15 GMT
VOLUME [/var/lib/docker]
# Fri, 03 Apr 2026 17:13:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 03 Apr 2026 17:13:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 03 Apr 2026 17:13:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777cc0dfb6b156ba8ae2d58bdc626d37d561285c3d8cb9f5dfab9e421b95c97a`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 8.5 MB (8453640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61cf8459e2976d9c1523c4817274c5542c2f14ca192664d8d5ad6eb7e492a00`  
		Last Modified: Fri, 03 Apr 2026 16:46:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8767096605cd5df8361d730cb51cdf77ce65a6d78016bfdcb25429f12a3b3c82`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 17.5 MB (17476968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14802cd569774821b1ac9c941f04e235ed46274c4a8ac0eae1b4b1ea971b6b2`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 20.5 MB (20453120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63242b8f6c4c149d7a76bebad8e17208b476be636d6f2c9ed5dca0a6e87eebd6`  
		Last Modified: Fri, 03 Apr 2026 16:46:18 GMT  
		Size: 10.0 MB (9982610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f92f7532507e0be265cd5a585468bfba3ed63c8f64943bfffbdb4c8e2bc29d3`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1144373d60167579bb44d4f4ec630998cc0bf64b287b2e5ba3c03aa31aa1f3d`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1b6b3e13fd596fa602ee41b47089c2aa97d6adb582e423ec45a54312bda585`  
		Last Modified: Fri, 03 Apr 2026 16:46:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7bcce9135e50e8113ce567e771818f45458b22e72a5b64b70da654eebd0e99`  
		Last Modified: Fri, 03 Apr 2026 17:13:25 GMT  
		Size: 7.2 MB (7219478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830d8e038e6c3e9055a2326f9fee1c908c9b60277c26df9b8ac5decd85cd3c08`  
		Last Modified: Fri, 03 Apr 2026 17:13:24 GMT  
		Size: 101.3 KB (101299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce438bd7121c26756c9344834a818efa8088cbd191053f8237e7ab52a55bee8b`  
		Last Modified: Fri, 03 Apr 2026 17:13:25 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8572ba2382e471780ecdf47f897386999474a08611c84b60f7f9664f27c0c7`  
		Last Modified: Fri, 03 Apr 2026 17:13:26 GMT  
		Size: 60.6 MB (60608023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0059d0fd9057439969d2dbf52619e8c263ad6c554c1f948b3cba6c9c94912e80`  
		Last Modified: Fri, 03 Apr 2026 17:13:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3764136014318e546423f2772475f4d7562d75fcd1407fd1c1bd941b0d1542`  
		Last Modified: Fri, 03 Apr 2026 17:13:26 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:cfa3bba5e17688594fc44b1a3d2f036d316ec72d1087c5cfcda980e17099085e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1edcd89a3d057104931b35657c5c97cd175a0a2255935ec50e46250e09864642`

```dockerfile
```

-	Layers:
	-	`sha256:a6f088a054073c23988be89705d5498a22b7cedd81fad3d5bb5196ffeebafc6d`  
		Last Modified: Fri, 03 Apr 2026 17:13:24 GMT  
		Size: 34.8 KB (34775 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:155a3d0470bc1209d0e007c462b889f181e8c5f50d2cbeafc3c09fe35dd7958f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `docker:windowsservercore` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:a105d81267b506d283738c2eab0c3e5f2339533f55a3f4e578543f31a10c0559
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2136248524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5d491b6f638ed8098ef9803e3c78743401083c443ad9969e0c8c97b4a5061c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Fri, 03 Apr 2026 16:48:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Apr 2026 16:49:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Apr 2026 16:49:27 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:49:28 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.1.zip
# Fri, 03 Apr 2026 16:49:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:49:46 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:49:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Fri, 03 Apr 2026 16:49:48 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Fri, 03 Apr 2026 16:50:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:50:05 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:50:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Fri, 03 Apr 2026 16:50:07 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Fri, 03 Apr 2026 16:50:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be287d655249644e43f567922c8ace0ebd34d2029a63b5f7aff779c7f0ea81f`  
		Last Modified: Fri, 03 Apr 2026 16:50:28 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bacc8dcf99a4b510435fd53e918e3bd0d6f4fdf27dcb309c4534ce03060f4e4`  
		Last Modified: Fri, 03 Apr 2026 16:50:27 GMT  
		Size: 370.7 KB (370685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75b1a0e09957eca68ed1d9ce466b166f611394669ffd7e2ef3cb280d2e86086`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cd9630a95f491844d8e8a681bc533e92b0e16ccf40b4842c76d47b05c88b82`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea0afb7d1d92072a6f67dc1f20ac520593a6d5b6e34fd654db0236504072e6b`  
		Last Modified: Fri, 03 Apr 2026 16:50:29 GMT  
		Size: 19.6 MB (19592556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2851c661eadabfff21636e396053a6ef65d7806e441da086e892a0570aa37b52`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55eeafb0e1065fbf8e495e596ab0979a2351aff4f33b4e1dc7d6c99f871eae97`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a24fd78eaaa140c5da70cb45d1a53de3c80317b8541f80a1d05bd6e4560022c`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe15c09ff0502ba71e3b975f0220d421f288c20d8c5d5f64c098496b4d84efdc`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 23.4 MB (23432034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39061e0c2bb20d115f630e4eb90cda590eae044db260d399ae125e5b4328ff96`  
		Last Modified: Fri, 03 Apr 2026 16:50:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb55d0d2e05e9f25e431de1cb3fea9bd5a99ce82e687614b9e3d5ac2bfbfaafd`  
		Last Modified: Fri, 03 Apr 2026 16:50:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4c676b321d5f609545214e994c74729fcfa063fb1814060367301f2b68aca4`  
		Last Modified: Fri, 03 Apr 2026 16:50:23 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194caab5fefbe0467dced96b2a1e8533cd36bc07325c3061cff834433fab53d5`  
		Last Modified: Fri, 03 Apr 2026 16:50:25 GMT  
		Size: 11.6 MB (11645348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull docker@sha256:ab04187c13089ceac6c8818c2cee7ecaa4e2bcd39577cfe00552451287b6b504
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037474662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e24418c7a3a82d1da61a8aa6cd06b4a3d16a6fd1812578771b1d9af9cd36f32`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Fri, 03 Apr 2026 16:47:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Apr 2026 16:49:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Apr 2026 16:49:08 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:49:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.1.zip
# Fri, 03 Apr 2026 16:49:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:49:34 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:49:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Fri, 03 Apr 2026 16:49:36 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Fri, 03 Apr 2026 16:50:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:50:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:50:05 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Fri, 03 Apr 2026 16:50:06 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Fri, 03 Apr 2026 16:50:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ebc372135025e6455cdea33dd82b8909666f97ad0f0b8089e919cf8b924f91`  
		Last Modified: Fri, 03 Apr 2026 16:50:29 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a0847e4437ba3ef85e9d7047c62200d08f8b3a8a0324073b8c84df7f3f7ebd`  
		Last Modified: Fri, 03 Apr 2026 16:50:28 GMT  
		Size: 506.6 KB (506574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb834b3ffd73d9ed8159b55a49c6253d1c85f02ffac59225e3b9079a78dfd48c`  
		Last Modified: Fri, 03 Apr 2026 16:50:27 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78b00d43926aab381c0a1e819e40df628b0aaea20b0bed307acf7ada3e0d982`  
		Last Modified: Fri, 03 Apr 2026 16:50:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cad0814bf145decf1ec3cb79bec86b593fb57d01ebee80ac54f51a6af6fc720`  
		Last Modified: Fri, 03 Apr 2026 16:50:29 GMT  
		Size: 19.6 MB (19590099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270311dfd8f5531d6c32b37406f2b41b3e7ff9507a8bb14652d73535bfdd3441`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae99ac7ec1d7ab5a58d53f31b9a42850062421eaec71a4d870507a0c5807dcc`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8314d29cc08fe7941d705655bf4b8147b9260ef4948d41c42e276fb722d25291`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f0a73598ec6395d9181e8c1b347790635350d4747fb0470ce9362ba194a633`  
		Last Modified: Fri, 03 Apr 2026 16:50:39 GMT  
		Size: 23.4 MB (23437302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2085add922e64596325b1d712784edd2e4140f08996288115cef8e3a9124e354`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d126d916f3b83dd6f3e9b0c72322b5aea0fd8dca636eb24a8fcb310d246056`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842d24a00195d53f2b7a645e88c31a5b96671f836f2bfd39d06c6c3227a83d92`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c989b6a66281fbd8d67f03b69e1f471e216f3155c0a8bd5119b79c41ee8fab5`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 11.6 MB (11647528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:7544ccc6e4ea00729bf7d28604a8b6fb4315bdf05d8f441f01793865f20046a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull docker@sha256:ab04187c13089ceac6c8818c2cee7ecaa4e2bcd39577cfe00552451287b6b504
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037474662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e24418c7a3a82d1da61a8aa6cd06b4a3d16a6fd1812578771b1d9af9cd36f32`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Fri, 03 Apr 2026 16:47:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Apr 2026 16:49:07 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Apr 2026 16:49:08 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:49:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.1.zip
# Fri, 03 Apr 2026 16:49:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:49:34 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:49:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Fri, 03 Apr 2026 16:49:36 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Fri, 03 Apr 2026 16:50:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:50:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:50:05 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Fri, 03 Apr 2026 16:50:06 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Fri, 03 Apr 2026 16:50:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ebc372135025e6455cdea33dd82b8909666f97ad0f0b8089e919cf8b924f91`  
		Last Modified: Fri, 03 Apr 2026 16:50:29 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a0847e4437ba3ef85e9d7047c62200d08f8b3a8a0324073b8c84df7f3f7ebd`  
		Last Modified: Fri, 03 Apr 2026 16:50:28 GMT  
		Size: 506.6 KB (506574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb834b3ffd73d9ed8159b55a49c6253d1c85f02ffac59225e3b9079a78dfd48c`  
		Last Modified: Fri, 03 Apr 2026 16:50:27 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78b00d43926aab381c0a1e819e40df628b0aaea20b0bed307acf7ada3e0d982`  
		Last Modified: Fri, 03 Apr 2026 16:50:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cad0814bf145decf1ec3cb79bec86b593fb57d01ebee80ac54f51a6af6fc720`  
		Last Modified: Fri, 03 Apr 2026 16:50:29 GMT  
		Size: 19.6 MB (19590099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270311dfd8f5531d6c32b37406f2b41b3e7ff9507a8bb14652d73535bfdd3441`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae99ac7ec1d7ab5a58d53f31b9a42850062421eaec71a4d870507a0c5807dcc`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8314d29cc08fe7941d705655bf4b8147b9260ef4948d41c42e276fb722d25291`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f0a73598ec6395d9181e8c1b347790635350d4747fb0470ce9362ba194a633`  
		Last Modified: Fri, 03 Apr 2026 16:50:39 GMT  
		Size: 23.4 MB (23437302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2085add922e64596325b1d712784edd2e4140f08996288115cef8e3a9124e354`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d126d916f3b83dd6f3e9b0c72322b5aea0fd8dca636eb24a8fcb310d246056`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842d24a00195d53f2b7a645e88c31a5b96671f836f2bfd39d06c6c3227a83d92`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c989b6a66281fbd8d67f03b69e1f471e216f3155c0a8bd5119b79c41ee8fab5`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 11.6 MB (11647528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:570b2a0cb54cc1e4fb3c9c360c9fbf31c58a67160ffac2f851d5320b2220ee3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:a105d81267b506d283738c2eab0c3e5f2339533f55a3f4e578543f31a10c0559
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2136248524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5d491b6f638ed8098ef9803e3c78743401083c443ad9969e0c8c97b4a5061c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Fri, 03 Apr 2026 16:48:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Apr 2026 16:49:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Apr 2026 16:49:27 GMT
ENV DOCKER_VERSION=29.3.1
# Fri, 03 Apr 2026 16:49:28 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.1.zip
# Fri, 03 Apr 2026 16:49:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:49:46 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:49:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Fri, 03 Apr 2026 16:49:48 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Fri, 03 Apr 2026 16:50:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:50:05 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:50:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Fri, 03 Apr 2026 16:50:07 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Fri, 03 Apr 2026 16:50:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be287d655249644e43f567922c8ace0ebd34d2029a63b5f7aff779c7f0ea81f`  
		Last Modified: Fri, 03 Apr 2026 16:50:28 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bacc8dcf99a4b510435fd53e918e3bd0d6f4fdf27dcb309c4534ce03060f4e4`  
		Last Modified: Fri, 03 Apr 2026 16:50:27 GMT  
		Size: 370.7 KB (370685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75b1a0e09957eca68ed1d9ce466b166f611394669ffd7e2ef3cb280d2e86086`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cd9630a95f491844d8e8a681bc533e92b0e16ccf40b4842c76d47b05c88b82`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea0afb7d1d92072a6f67dc1f20ac520593a6d5b6e34fd654db0236504072e6b`  
		Last Modified: Fri, 03 Apr 2026 16:50:29 GMT  
		Size: 19.6 MB (19592556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2851c661eadabfff21636e396053a6ef65d7806e441da086e892a0570aa37b52`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55eeafb0e1065fbf8e495e596ab0979a2351aff4f33b4e1dc7d6c99f871eae97`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a24fd78eaaa140c5da70cb45d1a53de3c80317b8541f80a1d05bd6e4560022c`  
		Last Modified: Fri, 03 Apr 2026 16:50:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe15c09ff0502ba71e3b975f0220d421f288c20d8c5d5f64c098496b4d84efdc`  
		Last Modified: Fri, 03 Apr 2026 16:50:26 GMT  
		Size: 23.4 MB (23432034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39061e0c2bb20d115f630e4eb90cda590eae044db260d399ae125e5b4328ff96`  
		Last Modified: Fri, 03 Apr 2026 16:50:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb55d0d2e05e9f25e431de1cb3fea9bd5a99ce82e687614b9e3d5ac2bfbfaafd`  
		Last Modified: Fri, 03 Apr 2026 16:50:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4c676b321d5f609545214e994c74729fcfa063fb1814060367301f2b68aca4`  
		Last Modified: Fri, 03 Apr 2026 16:50:23 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194caab5fefbe0467dced96b2a1e8533cd36bc07325c3061cff834433fab53d5`  
		Last Modified: Fri, 03 Apr 2026 16:50:25 GMT  
		Size: 11.6 MB (11645348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
