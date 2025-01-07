## `docker:rc-dind`

```console
$ docker pull docker@sha256:cba84cc0407783510051acb23c21a8227c061bdb06245c41d10324600afc8ff7
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

### `docker:rc-dind` - linux; amd64

```console
$ docker pull docker@sha256:863fc3002db8b064b04ec20a6bb6ec4dad25a4b2d20481f1a25bf90402969337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133774479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb56d31f4cd4e78dea0eb2785f5f4009d958e5baf90166710a1130bc8e1ff7c0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 23 Dec 2024 12:04:24 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 12:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENV DOCKER_VERSION=27.5.0-rc.1
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.5.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.5.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.5.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.5.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Dec 2024 12:04:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 12:04:24 GMT
CMD ["sh"]
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.5.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.5.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.5.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.5.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Dec 2024 12:04:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 23 Dec 2024 12:04:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Dec 2024 12:04:24 GMT
CMD []
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1283cdc684342da4e0e297d2eb7ee888abbbd433bf317de4bb6d100a108bbdb`  
		Last Modified: Tue, 07 Jan 2025 03:14:25 GMT  
		Size: 8.0 MB (8040056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9128eca6c9be8b8056b36ce7815f03df13743962faac48cd0c01ff75e88a1af3`  
		Last Modified: Tue, 07 Jan 2025 03:14:24 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5912efe820160d288a842852379a70553e942e893009613643101c0a61b4e70f`  
		Last Modified: Tue, 07 Jan 2025 03:14:26 GMT  
		Size: 18.8 MB (18849782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8c90236a4e00c27bf29b4ab068021a74cbfb2561459d587a7a048a91dcb16a`  
		Last Modified: Tue, 07 Jan 2025 03:14:26 GMT  
		Size: 18.8 MB (18798847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924e1f4b47bf013aec5defdac39389472f8c8748ccd9be2eecc99996fba972a6`  
		Last Modified: Tue, 07 Jan 2025 03:14:26 GMT  
		Size: 19.3 MB (19295663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ff5bbdf57918c3fe56d84739e329d0c297d806d3ad4cc355b926fdc73f766c`  
		Last Modified: Tue, 07 Jan 2025 03:14:26 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c985ca7edf81de8ed3847d7983944e6f4a4e2648b02a21563d0d50f6f54cc695`  
		Last Modified: Tue, 07 Jan 2025 03:14:27 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d952cd56f9e50947e5430a563a6b94fa4bf5d57c63b4fb35c1efdc8d004c2f89`  
		Last Modified: Tue, 07 Jan 2025 03:14:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76390d236ae9d32a87ec1c62c70d89a6b9c7865564075e9d1408417bde205ccd`  
		Last Modified: Tue, 07 Jan 2025 04:18:16 GMT  
		Size: 6.7 MB (6733405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ddbfc27aaef80fcef2cfa1abbc5bbe8192af0c0ec2375428ee3d28405ad31c`  
		Last Modified: Tue, 07 Jan 2025 04:18:15 GMT  
		Size: 89.2 KB (89154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052970de14f6f198767a8cbfed48f0ef1dfcc32d3515ee720af1f6654723bb27`  
		Last Modified: Tue, 07 Jan 2025 04:18:15 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da2d019ad3872c6a73c47056942660bdd284135589be8efcbdeee19f9b05667`  
		Last Modified: Tue, 07 Jan 2025 04:18:17 GMT  
		Size: 58.3 MB (58323403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe9befdc7ceb46ac23ec7a0b317cb7c31c75f97aa1bc8df7ba29e9f1ec15442`  
		Last Modified: Tue, 07 Jan 2025 04:18:16 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51737514e274463676355614f703b6bf80fff7878c8e73efebee9579384e13e3`  
		Last Modified: Tue, 07 Jan 2025 04:18:16 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:c8d182c94a9536af4ea1fde21a95301d6b286251f79ea46a516602ccf70a9c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 KB (34114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ea1fcf85d205d31b2f283d35290e294429dee5d5aabe5dc03cd71fb7cce2e3`

```dockerfile
```

-	Layers:
	-	`sha256:12f0cfa98d13613c2fcca9e713c649eb93116ff77b108ecf7bc8244d5046a492`  
		Last Modified: Tue, 07 Jan 2025 04:18:15 GMT  
		Size: 34.1 KB (34114 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b0d7ef371f3fcff4b22ccfebdb0fc58a329c8f0196b1c78d70f8955b0563e94d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124891729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516e7c90a99a3d8a9d0ee319b485917241a2efa49e1305b52801115a86e39161`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 12:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENV DOCKER_VERSION=27.5.0-rc.1
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.5.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.5.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.5.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.5.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Dec 2024 12:04:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 12:04:24 GMT
CMD ["sh"]
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.5.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.5.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.5.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.5.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Dec 2024 12:04:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 23 Dec 2024 12:04:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Dec 2024 12:04:24 GMT
CMD []
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940b936da18aa92a4b6e16da51c5826b9782e017e91de8002f94ce58348c8b3`  
		Last Modified: Tue, 10 Dec 2024 01:47:48 GMT  
		Size: 8.0 MB (7974528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7eaba796f2c5345fa5efffc39c084ec36a28d0aa4a646e7b7a8f4a5479bd94`  
		Last Modified: Tue, 10 Dec 2024 01:47:47 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686f61b1e85f75d49e6956f96daf3875027d322cd62a406afb737b6df807a39`  
		Last Modified: Tue, 24 Dec 2024 21:33:26 GMT  
		Size: 16.9 MB (16866130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585b3de0fb9397a2bedd9cb1fee9b8b9a54639198b6d3117d000a1b2d9a5cc3d`  
		Last Modified: Tue, 24 Dec 2024 21:33:26 GMT  
		Size: 17.4 MB (17448789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd79cd8ae47c15878a943856d90091f0fb1f8d8d1871fde4b67a66588d33fd5e`  
		Last Modified: Tue, 24 Dec 2024 21:33:26 GMT  
		Size: 18.1 MB (18106581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5331b7572110f5b7f4ee3e82be7e176b1b57f9f3c433338248b5863ca63a3651`  
		Last Modified: Tue, 24 Dec 2024 21:33:25 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c17e6698b77632e457585b99b7ee17f1435e4176e10f1cf54080bced92c6e4c`  
		Last Modified: Tue, 24 Dec 2024 21:33:26 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd43c5c9df1024560a12188cf094ed7d40a7dc5c802695baf8291bf8d923af7`  
		Last Modified: Tue, 24 Dec 2024 21:33:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb23af53db0c29f7af180b83db9819a8fbc830cdab4ef8d631ff962e46d1c3e`  
		Last Modified: Tue, 24 Dec 2024 22:18:30 GMT  
		Size: 7.0 MB (7041195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1571b8592a4db23f2810a9a54df0aedd610fceccee4bb2b476f0b019d43e8e`  
		Last Modified: Tue, 24 Dec 2024 22:18:29 GMT  
		Size: 89.1 KB (89111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d6074a9a5a7642b9c9e8e75ea54b4a9777da6225d19d7ddc36603c11c67039`  
		Last Modified: Tue, 24 Dec 2024 22:18:29 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8360d15c35524b4a35d69bcf5b4b6002dfb67c221a6e1156ea679f84031fd1`  
		Last Modified: Tue, 24 Dec 2024 22:18:31 GMT  
		Size: 54.0 MB (53990251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed75973e38845f39a203043ab1958d3469e496b49b9ab66e78b5eef2dc81fbe`  
		Last Modified: Tue, 24 Dec 2024 22:18:30 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f322de1d262b96d21a81539f3418de0f4cb4c224e9f1bbe385c366c757ff46`  
		Last Modified: Tue, 24 Dec 2024 22:18:30 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:79afef07b0c5b287145e7a623302981e08fec6c0d5616cc34883026559972eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8097e6fa280883325adaffb31f512bb82122e607060014cc1e6fe4ed096903e`

```dockerfile
```

-	Layers:
	-	`sha256:bc4f51b98231de4e4d8a4e3567673ef93fef4212f3be51b7e8ad5fa9815262fc`  
		Last Modified: Tue, 24 Dec 2024 22:18:28 GMT  
		Size: 34.3 KB (34274 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:5877085ce0e39f6780670d43c047b2e952f238e13ec53d0239119aa9670cfb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123235511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2488bc0e3b2bc493246380d86ec06d9b4360576ec013537faddf757f835138b6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 12:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENV DOCKER_VERSION=27.5.0-rc.1
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.5.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.5.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.5.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.5.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Dec 2024 12:04:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 12:04:24 GMT
CMD ["sh"]
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.5.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.5.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.5.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.5.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Dec 2024 12:04:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 23 Dec 2024 12:04:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Dec 2024 12:04:24 GMT
CMD []
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd06c9d79e0561a10b25968a89bb9ec7884f3a271df5cce1a2202a6f1aaf4cb`  
		Last Modified: Tue, 24 Dec 2024 21:38:41 GMT  
		Size: 7.3 MB (7308398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278a3412eb1b55c458e544ddd911ca6d6d67ceceb0a070ea23bf463f2a888ed0`  
		Last Modified: Tue, 24 Dec 2024 21:38:41 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a82651c3475d1a7b721b097aa7c17578d5243398fe8d447c16438eae890e8`  
		Last Modified: Tue, 24 Dec 2024 21:38:42 GMT  
		Size: 16.9 MB (16856029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6972a835de36907ce2b72f23c3b39f1faeea432d24a99f5a0474e68da1031506`  
		Last Modified: Tue, 24 Dec 2024 21:38:42 GMT  
		Size: 17.4 MB (17427572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8e6650a2034760c9ab663a65a74e88794a4c5e79313a0cb0a900eb0c1201f6`  
		Last Modified: Tue, 24 Dec 2024 21:38:43 GMT  
		Size: 18.1 MB (18092636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b78414a91784ceb3fe68c6886ad3be4270c8bb54d3be6b6f5bf8719d2b6a04e`  
		Last Modified: Tue, 24 Dec 2024 21:38:43 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9abe64edefa9ae66c894d3d6bf229282f7282e1587855e2bdbb266a9ea3ce9`  
		Last Modified: Tue, 24 Dec 2024 21:38:43 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a38ac591aaf2d68cf6547c031297fa69ede3a818dfa208b862ce70c38991e73`  
		Last Modified: Tue, 24 Dec 2024 21:38:43 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fb5f560bea58fa36d1e72707b632111b5cf7e65f25e10e81beaab1049696f1`  
		Last Modified: Tue, 24 Dec 2024 22:19:19 GMT  
		Size: 6.4 MB (6367379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b48304f6c549b773e8bc00691e8bb90b4039d6c029b28a5095571b86f32ea0c`  
		Last Modified: Tue, 24 Dec 2024 22:19:18 GMT  
		Size: 85.3 KB (85263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dee58ceaad3d7b729b801b87cab409d5ff363fd62948e78f32859f72ac1a61a`  
		Last Modified: Tue, 24 Dec 2024 22:19:18 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76451b9b366e844c955846a25be2dbab29d42cdc421d04cea2168d38f17cc3c8`  
		Last Modified: Tue, 24 Dec 2024 22:19:20 GMT  
		Size: 54.0 MB (53990252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bb70330ed4cbba7e60315b48515daf8602161581427a4e4d662fcccdcb5b1a`  
		Last Modified: Tue, 24 Dec 2024 22:19:19 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df778b47c919b77de85103b1f4fe46afad73fb28dd583e127bd1fc24b5c1cfc`  
		Last Modified: Tue, 24 Dec 2024 22:19:19 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:ee209cf7f31936e400a12da455a84d5d1ec1fffb5ea3e0abc2bde0b0829a1939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3dc66869579ae5572a1fd9ae230dcb9008c34a73c76aa11c2523fae37f9f80`

```dockerfile
```

-	Layers:
	-	`sha256:c35af97abfd974486bc2359400210db84926dccbe6007dfa97ebd2a62a28c649`  
		Last Modified: Tue, 24 Dec 2024 22:19:17 GMT  
		Size: 34.3 KB (34275 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d9cf3005d44f50cc4be0f415f0c43a1b7228b854bde3a4e33684947827425878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125569045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fa33943d2aefa559aef803bf5cd865ed54e06551bd2b97d80061bbf98267d6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 23 Dec 2024 12:04:24 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 12:04:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENV DOCKER_VERSION=27.5.0-rc.1
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.5.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.5.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.5.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.5.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Dec 2024 12:04:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 12:04:24 GMT
CMD ["sh"]
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.5.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.5.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.5.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.5.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Dec 2024 12:04:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 23 Dec 2024 12:04:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Dec 2024 12:04:24 GMT
CMD []
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1026b13fd592f6fa6a885d53bf65cac408ee796ee206649d79e2795598db4303`  
		Last Modified: Tue, 07 Jan 2025 03:58:19 GMT  
		Size: 8.1 MB (8061737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cefd242c27cedfdf6449858e7a043307dc02aab49d7e6e4dbc4b422c96d721`  
		Last Modified: Tue, 07 Jan 2025 03:58:18 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4086a2b57c164d45ac16ef99f4435c13bf55663b45f2c0df147d6af6328b31a1`  
		Last Modified: Tue, 07 Jan 2025 03:58:20 GMT  
		Size: 17.8 MB (17795782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed4b357a90f503f4a98ba16cbd149d588c15be3a5a47729850cb92dea6935ee`  
		Last Modified: Tue, 07 Jan 2025 03:58:19 GMT  
		Size: 17.1 MB (17106450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fe1b6abf6b11917a5f681cf5dfaaa3ffabaacc6c8c757d940848de94ab3307`  
		Last Modified: Tue, 07 Jan 2025 03:58:20 GMT  
		Size: 17.6 MB (17642752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c24edd094d4f8e1ea9e99f7157be1b026a24d612a9d4c3ca37126a21c85cbc`  
		Last Modified: Tue, 07 Jan 2025 03:58:20 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128f5f436d77dc8f7c7ebff45ea11d00ba3a5d7efcb4fd55b0aedb0e6d6e8944`  
		Last Modified: Tue, 07 Jan 2025 03:58:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1b8819e5ecf002feadf8251df1576047ae14795dd796e6097af004e10b0233`  
		Last Modified: Tue, 07 Jan 2025 03:58:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad572cdf2574dc4706d23f572cbb10462b3667e4e0cbb3890ded4b1045c51243`  
		Last Modified: Tue, 07 Jan 2025 15:51:20 GMT  
		Size: 7.0 MB (6982190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbddc2907206238e813651483b3fe407f95ad10240dcb99407fe986837b30f5`  
		Last Modified: Tue, 07 Jan 2025 15:51:19 GMT  
		Size: 97.6 KB (97556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e795b4e3ec93e6b32d452c7164671683e900ed95fc986397fdf22fc34c2bc81d`  
		Last Modified: Tue, 07 Jan 2025 15:51:19 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31057ccdd638840631ac652fca0092668837a9155c035f9336ef90c64614c8c1`  
		Last Modified: Tue, 07 Jan 2025 15:51:21 GMT  
		Size: 53.9 MB (53891624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175867424b94b65ed5f1c6c0c57d2f5b1c68db897a981e1e0ee4c7bdff3ec05c`  
		Last Modified: Tue, 07 Jan 2025 15:51:20 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c5509a8633fd679586dd9e89860f1e646371e8dc562d0bf7ab5f2b27260a90`  
		Last Modified: Tue, 07 Jan 2025 15:51:20 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:430795642a77e6d8cfa5346984f0fc331783aa20268c808e30d7a03f59c08a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066073474fb36ad4670edb6ac9c1396aafa105172f3a5209458f19585d3606b1`

```dockerfile
```

-	Layers:
	-	`sha256:f5f864e7d82b9227abe0a0247534f16d1f0fe8fbb0559e90b7d3456ac478bf07`  
		Last Modified: Tue, 07 Jan 2025 15:51:19 GMT  
		Size: 34.3 KB (34327 bytes)  
		MIME: application/vnd.in-toto+json
