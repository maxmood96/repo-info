<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:27`](#docker27)
-	[`docker:27-cli`](#docker27-cli)
-	[`docker:27-dind`](#docker27-dind)
-	[`docker:27-dind-rootless`](#docker27-dind-rootless)
-	[`docker:27-windowsservercore`](#docker27-windowsservercore)
-	[`docker:27-windowsservercore-1809`](#docker27-windowsservercore-1809)
-	[`docker:27-windowsservercore-ltsc2022`](#docker27-windowsservercore-ltsc2022)
-	[`docker:27.4`](#docker274)
-	[`docker:27.4-cli`](#docker274-cli)
-	[`docker:27.4-dind`](#docker274-dind)
-	[`docker:27.4-dind-rootless`](#docker274-dind-rootless)
-	[`docker:27.4-windowsservercore`](#docker274-windowsservercore)
-	[`docker:27.4-windowsservercore-1809`](#docker274-windowsservercore-1809)
-	[`docker:27.4-windowsservercore-ltsc2022`](#docker274-windowsservercore-ltsc2022)
-	[`docker:27.4.1`](#docker2741)
-	[`docker:27.4.1-alpine3.21`](#docker2741-alpine321)
-	[`docker:27.4.1-cli`](#docker2741-cli)
-	[`docker:27.4.1-cli-alpine3.21`](#docker2741-cli-alpine321)
-	[`docker:27.4.1-dind`](#docker2741-dind)
-	[`docker:27.4.1-dind-alpine3.21`](#docker2741-dind-alpine321)
-	[`docker:27.4.1-dind-rootless`](#docker2741-dind-rootless)
-	[`docker:27.4.1-windowsservercore`](#docker2741-windowsservercore)
-	[`docker:27.4.1-windowsservercore-1809`](#docker2741-windowsservercore-1809)
-	[`docker:27.4.1-windowsservercore-ltsc2022`](#docker2741-windowsservercore-ltsc2022)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)

## `docker:27`

```console
$ docker pull docker@sha256:d33ffba5909705d375ef1a99bb69fe6e21d80482134283226b119acf18bb08b4
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
$ docker pull docker@sha256:197a4c5f8ffb8e4940e2518b1863588839743d062576c9d144a91fc64400c25b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133448845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c9711c027ed5c0c1bc82bf858e1a428676cd76681a56c53068db5510594f55`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b98de49fe1ed993db53e09ac1d349e04edc68f3a669a0166fe861e63f21139`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 8.1 MB (8060708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af95ea946dd1ea6ddb09d4d16636c6dbdaf31f2a92f21fccf332f412f91978b`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313c9b4ec4148bbc92f321352088134bd5c79313a32b0346277392e67f81276a`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 18.7 MB (18669944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7c930da0eae6c203479c2208bc111980211a355e5ebe1d8b9d771bd3b3f5a2`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 18.8 MB (18798867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0028ab84266b23892e8257b849272b905514e4111ccc878a47fc9e050d94e`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf34514361d460f057db2b94643dcc0fa3771b2df3b514bcc118a203a10c95ba`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003372bc0a71b5fee80b7721b00c600392a2d1297a7bdc1382c4fe9b7a3c478`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654c3b9f6f86104ad7ac2a1861a8a6a3c9624bdb262e0024f0daee392ebdc1d`  
		Last Modified: Thu, 19 Dec 2024 06:27:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccacb1ec449ea2d8be4c5f1323c8f8f438ca6cbadb852569e5a1d30b2fccfb0`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 6.7 MB (6733442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db08b2b56d721154b01a601fafbf1388da92317b2a6fd84636403d145397cab`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 89.5 KB (89464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf58bc5c124acd8cd7867de0e5bfe811139bb7efbdfb4d3f384f5047368feadb`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed661c2bc3605af63c34b0e0e6b44c343cfaaeaeff5a9c5a1e90636c29b3c3`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 58.1 MB (58148385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd93031177fed6768ebac95908f7214e148aec625cde4db347278f785e7061f`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4580133da14d68ef765c552929a21bcefda14fd6f6d46ecd79ba394349848a`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:4d1ebca4fc352915e574abaa96ff6ed6588607144b48d49638664664171da1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785a52cc7646ffa85e15d5ffe60aac7f0f1a2d5253c2b101b6f346064092b53f`

```dockerfile
```

-	Layers:
	-	`sha256:57153e86db239ac28d0ccf1ea7c7b4f48b51df48813df21eab3ef9fec0624f79`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v6

```console
$ docker pull docker@sha256:8e53f8a2914c30d65228120667a050c54a74382d87f8e8205383be62560c9f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124579368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cc11a65e103a89e82e0f00f3eaea3ee929960b8b89fbf699a59f2bd46a109d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:148e72cbc3a4643c87b410580b6ae972ceafb99447e0d85bef2dd888ed7916d9`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 16.7 MB (16706481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfe37eaf11de403418a16f112ea736966145c615c0468af955274ca2d468276`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 17.4 MB (17448788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f071b9292f7441268ea76098e71b9dff0a1ec9f8311e4de77c6cd5af2c52a65`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 18.1 MB (18106565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a4fe84fb2fdef0c93d4c522edb4470e1d3558b04db73d6dc740cca4f2d3da6`  
		Last Modified: Thu, 19 Dec 2024 06:27:55 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa58f5b177c2d4b9d8d25bce148cba72f6b2db6ae71652dce2a49d1b4ecd88e`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755888e89afeff341e55361b436c6b35c8e67e7e05993e006c02d845c09320c3`  
		Last Modified: Thu, 19 Dec 2024 06:27:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ef02b0ebd56b76a25032f347f442a87fd532e2f07932b029c5a5ed2863ebdf`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 7.0 MB (7041137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa00a89210cf6cc619d32ecde33bcc417a048e4089420d3376e126502a34e868`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 89.1 KB (89114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314e6fc0bd408cd71d4f12dc2b30c175f02d576782580764a4d18dbe9397962a`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d2a39a9ca8dfcdf48360a081c2bacbd295c376b777d17ab83e02ace23e3d98`  
		Last Modified: Thu, 19 Dec 2024 07:08:09 GMT  
		Size: 53.8 MB (53837606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000fe248e69901663cba49cff877d5d4494f61261374eebd3e76654fdb4a9bb`  
		Last Modified: Thu, 19 Dec 2024 07:07:40 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e0a412273d2de4a63cf252e2955333edbb0387dab642897062720249f4180`  
		Last Modified: Thu, 19 Dec 2024 07:07:40 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:fbb76334b758da06115ce3db141b3a8d0384cf0fdfe0f1ae084cf566558cde04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05008ccd944add8210466657f1c49a19e043efce63da526e66de9aebb4b80ef`

```dockerfile
```

-	Layers:
	-	`sha256:d0c1d9bc2a056393fa0f5f33e177e88c39f2ff3b3ecab57b5172ba3064dfd763`  
		Last Modified: Thu, 19 Dec 2024 07:07:38 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v7

```console
$ docker pull docker@sha256:42fe1f55c44d24a6c3dabf704278f5beef25d390ca4c15966d714fb6e7908b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122921457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9248a004d8a619e67677191683cde42174b0b6a6f031c1bff04422a56ab7fafa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7384c11421040c34c2db4c9cbdff405dc1cb373620affa19cef0e6cd7889776b`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 16.7 MB (16694610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07bb9d6b4efc8e73c712cd756cad4ebdc7e4cd974f3b61319673b399cff7696`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 17.4 MB (17427589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e028074a72228d620c07c0306033af62a3bc33ecdbfdd182451a3940dbb3c47d`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 18.1 MB (18092645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b53f0105da3d54066118dde45e2db91fb53e54796d793199cb4d2ab602e9e2`  
		Last Modified: Thu, 19 Dec 2024 06:27:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6833631438bdcae5d6656508822939365cfd74de741e43abe8301361021b317`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b86ced47599bbfc27aa7dc389fb9cb257d493873490cc411bd8d27bdbf33bf`  
		Last Modified: Thu, 19 Dec 2024 06:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3cfec5adb0a4b5698f388de77eec77ddfae962de5b040d830dd95fded5c623`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 6.4 MB (6367338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f665ffa7443f60c8c9314082dba5723e72ede3f3451817173783b2ff36ffcb3`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 85.3 KB (85264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f8f3552eba49a36113015c2b82fecdb0cc6496614371b415212e14847dc60`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f31fefce9d3a0d0f1c7eb75b6cbde54e15ec723205ceea52b7da59ab4fb0dc`  
		Last Modified: Thu, 19 Dec 2024 07:07:45 GMT  
		Size: 53.8 MB (53837588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2522c47823d994b730d265c55af844c265eae9c9556e8e2200a9a35b9ac91a7`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06aa58a0bf71133cf40669589cd7fee930c7c0be06f93c2ff27147fd89bb1169`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:17996dd91287a758efee2344a070f6699509883f0d901af5ab238e9b387229bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b073ab412e1ae045cda1a9e0d874b37c17d7a32b94ca5af476daa61f0ae58438`

```dockerfile
```

-	Layers:
	-	`sha256:a559ea4afc9f0276e8285aa1e894d114568f8fc93aded28f64880c5b07631b25`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c4618ee87c867fff3b390aab9eeb59d889e39a14fb3bfbf40560f7faf78f841b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125264161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a74c04d0ac72b0d4df5a0d63124bff4cce8b81fe2f6d669d6272b5c426ef00e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc8b2386f26a19ff7e378d0b71a659c1c6185ff0418ab0ba70f91c9d7564766`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 8.1 MB (8077202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb804615f812dd41590a2167ce26fcd2bc94e936ef063d6ad5d47716653c51e`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500337a2754d23cb29983332f91f13bafcc80a7c299b977b077090a0fdf6e5a9`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.6 MB (17619412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821da57d87be4b4be2263810265c5fdfbee2a0815f9ba40aab6a34d602dbf10f`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.1 MB (17106449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a3e8ce8d46be94b3c36743d7add34488c85986d7d67dc65e6b0024b4f9629`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 17.6 MB (17642746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9727d9b709f029f03a062308481e155e1e44a388f1c90336ea9e6e9c98f4bf02`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5132ed17107a2140233d234c98fe9ff02ed459ac10f5b4ed2256ac52caff0ba2`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c450deeac7bd4e43a7a23a0608a88019260374cee39dc6371807295ef79a48`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95254613e12389bf1f1f60f9b295f28cef95138ce1dbc50738110a66f798909e`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 7.0 MB (6982148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3b84891c5b5b5525368fd009a3faa7c2ce7964cb220ec38caec428b7a4e023`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 97.8 KB (97810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f85e673a5bfddb9b35bc2893ca0b6dce01582d542e954e1f8522a5dc5bb96fc`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e62d3dc2daa4a6f98b762917d7f0adea4d641834acf4f0f8a44e1d79d577ab7`  
		Last Modified: Thu, 19 Dec 2024 07:07:59 GMT  
		Size: 53.7 MB (53737262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a6c5cd3176c0cc42a77bceba546446aac5d823c9f2fe97ef71fa20cc12bea4`  
		Last Modified: Thu, 19 Dec 2024 07:07:58 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01edfa8f426bf8debb954258fd0e37e36488fa9ba98d3d941a5b763aec91984f`  
		Last Modified: Thu, 19 Dec 2024 07:07:58 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:b944da17175c77080cb8774711d10f0b88e7b131c7036b9ad130642f29955bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754b5f14591dc682613445f666f9460bab283af4d13ee4f7a9e3e47c27451707`

```dockerfile
```

-	Layers:
	-	`sha256:cc7c1950a5e5557483555eef92ae1c730a5df8239e11efd4015d579f2c48b149`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-cli`

```console
$ docker pull docker@sha256:2a9c1ba4816ddafdcf49a561201a9af2c451017e263a16a4fb1f878c454e1c44
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
$ docker pull docker@sha256:0d052bc5fcedc9b04935ffc5c1ca039c2c3f442c22dac9fab600f1e8348bc810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68471761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b387bcd9f4eb8854253fbd37d44ddd3a01ae6ed50d46fcf2371fbd0a72bf874e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b98de49fe1ed993db53e09ac1d349e04edc68f3a669a0166fe861e63f21139`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 8.1 MB (8060708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af95ea946dd1ea6ddb09d4d16636c6dbdaf31f2a92f21fccf332f412f91978b`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313c9b4ec4148bbc92f321352088134bd5c79313a32b0346277392e67f81276a`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 18.7 MB (18669944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7c930da0eae6c203479c2208bc111980211a355e5ebe1d8b9d771bd3b3f5a2`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 18.8 MB (18798867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0028ab84266b23892e8257b849272b905514e4111ccc878a47fc9e050d94e`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf34514361d460f057db2b94643dcc0fa3771b2df3b514bcc118a203a10c95ba`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003372bc0a71b5fee80b7721b00c600392a2d1297a7bdc1382c4fe9b7a3c478`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654c3b9f6f86104ad7ac2a1861a8a6a3c9624bdb262e0024f0daee392ebdc1d`  
		Last Modified: Thu, 19 Dec 2024 06:27:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:25b71b84216a6b6fa15b2e5d77e03b34e15d770a4e7bd0d5a12dc5a94e712a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32b3f66abca23fa334f7a356d599e2b285535319198c82ba778c5ae1d68c0d1`

```dockerfile
```

-	Layers:
	-	`sha256:e4b152243122d2a2b2ba6915e1be8a0003ac4d08efd17fcdf8208957caf3a8cb`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:2e6d722b4ad5fe9d873cddaf4f60fc20dcb740a401df852ba406b3068398b7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63605712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3487d4e2b40727fa327f1bc3ac2976f9c228483c0f71198a14759f48b37a693`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:148e72cbc3a4643c87b410580b6ae972ceafb99447e0d85bef2dd888ed7916d9`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 16.7 MB (16706481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfe37eaf11de403418a16f112ea736966145c615c0468af955274ca2d468276`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 17.4 MB (17448788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f071b9292f7441268ea76098e71b9dff0a1ec9f8311e4de77c6cd5af2c52a65`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 18.1 MB (18106565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a4fe84fb2fdef0c93d4c522edb4470e1d3558b04db73d6dc740cca4f2d3da6`  
		Last Modified: Thu, 19 Dec 2024 06:27:55 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa58f5b177c2d4b9d8d25bce148cba72f6b2db6ae71652dce2a49d1b4ecd88e`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755888e89afeff341e55361b436c6b35c8e67e7e05993e006c02d845c09320c3`  
		Last Modified: Thu, 19 Dec 2024 06:27:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:ff1cbb618b403ea74aa5eaef6d1ce343a27b799a14e73accc6d45186a8183c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ef782c195058519b295e8b5f7623848187120a6c037d0c852bc65400041fb6`

```dockerfile
```

-	Layers:
	-	`sha256:d4a3b6f2edb30ef6c175dc855c3cac8939a2acc6acf24bdba215d5e4bf9af607`  
		Last Modified: Thu, 19 Dec 2024 06:27:55 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:f89c36bd6f08a78078044ca2606b40abfd6e2bee5c34d5d0a227e545e70b31f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62625475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0973c3f1d70b0f02dd2301a26effa977c42a8930649cb0bb1dba2cad5abba685`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7384c11421040c34c2db4c9cbdff405dc1cb373620affa19cef0e6cd7889776b`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 16.7 MB (16694610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07bb9d6b4efc8e73c712cd756cad4ebdc7e4cd974f3b61319673b399cff7696`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 17.4 MB (17427589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e028074a72228d620c07c0306033af62a3bc33ecdbfdd182451a3940dbb3c47d`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 18.1 MB (18092645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b53f0105da3d54066118dde45e2db91fb53e54796d793199cb4d2ab602e9e2`  
		Last Modified: Thu, 19 Dec 2024 06:27:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6833631438bdcae5d6656508822939365cfd74de741e43abe8301361021b317`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b86ced47599bbfc27aa7dc389fb9cb257d493873490cc411bd8d27bdbf33bf`  
		Last Modified: Thu, 19 Dec 2024 06:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:82ae1c7b8fe94fdc49f39f3eec184d02572b400c4a225d2c5bc3a811850bbcb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394c76df731da9a4b7d8ffb5fc4820c5cabe9516f2202a945000d67de063966a`

```dockerfile
```

-	Layers:
	-	`sha256:4eac62d6a3079b4b3118e6b704cd97ad9ecd8ff718b1097e1cb02a713120697f`  
		Last Modified: Thu, 19 Dec 2024 06:27:30 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8e85a9901bc8d85c147f51091bc0a91ad62559db69480b088d838f5b52cdf542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64441149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b503fae5efdeebe409c4458ec85ccbe53f3abf5c2833f311ee7720d7a0b1bd60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc8b2386f26a19ff7e378d0b71a659c1c6185ff0418ab0ba70f91c9d7564766`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 8.1 MB (8077202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb804615f812dd41590a2167ce26fcd2bc94e936ef063d6ad5d47716653c51e`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500337a2754d23cb29983332f91f13bafcc80a7c299b977b077090a0fdf6e5a9`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.6 MB (17619412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821da57d87be4b4be2263810265c5fdfbee2a0815f9ba40aab6a34d602dbf10f`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.1 MB (17106449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a3e8ce8d46be94b3c36743d7add34488c85986d7d67dc65e6b0024b4f9629`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 17.6 MB (17642746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9727d9b709f029f03a062308481e155e1e44a388f1c90336ea9e6e9c98f4bf02`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5132ed17107a2140233d234c98fe9ff02ed459ac10f5b4ed2256ac52caff0ba2`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c450deeac7bd4e43a7a23a0608a88019260374cee39dc6371807295ef79a48`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:5a1c761171de4faf5bbd2753ce69aedb70bf0172682167323093305a9172bf8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d8489705c0a7ad5281a14fa0580dfe1e84ac35e8ed32f1e4746b551b3ec27d`

```dockerfile
```

-	Layers:
	-	`sha256:34348583b40c1f2b4ae040bdaa91a20e47adaa05541d9cafe8e43557dc582b3a`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind`

```console
$ docker pull docker@sha256:d33ffba5909705d375ef1a99bb69fe6e21d80482134283226b119acf18bb08b4
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
$ docker pull docker@sha256:197a4c5f8ffb8e4940e2518b1863588839743d062576c9d144a91fc64400c25b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133448845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c9711c027ed5c0c1bc82bf858e1a428676cd76681a56c53068db5510594f55`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b98de49fe1ed993db53e09ac1d349e04edc68f3a669a0166fe861e63f21139`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 8.1 MB (8060708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af95ea946dd1ea6ddb09d4d16636c6dbdaf31f2a92f21fccf332f412f91978b`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313c9b4ec4148bbc92f321352088134bd5c79313a32b0346277392e67f81276a`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 18.7 MB (18669944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7c930da0eae6c203479c2208bc111980211a355e5ebe1d8b9d771bd3b3f5a2`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 18.8 MB (18798867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0028ab84266b23892e8257b849272b905514e4111ccc878a47fc9e050d94e`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf34514361d460f057db2b94643dcc0fa3771b2df3b514bcc118a203a10c95ba`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003372bc0a71b5fee80b7721b00c600392a2d1297a7bdc1382c4fe9b7a3c478`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654c3b9f6f86104ad7ac2a1861a8a6a3c9624bdb262e0024f0daee392ebdc1d`  
		Last Modified: Thu, 19 Dec 2024 06:27:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccacb1ec449ea2d8be4c5f1323c8f8f438ca6cbadb852569e5a1d30b2fccfb0`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 6.7 MB (6733442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db08b2b56d721154b01a601fafbf1388da92317b2a6fd84636403d145397cab`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 89.5 KB (89464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf58bc5c124acd8cd7867de0e5bfe811139bb7efbdfb4d3f384f5047368feadb`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed661c2bc3605af63c34b0e0e6b44c343cfaaeaeff5a9c5a1e90636c29b3c3`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 58.1 MB (58148385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd93031177fed6768ebac95908f7214e148aec625cde4db347278f785e7061f`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4580133da14d68ef765c552929a21bcefda14fd6f6d46ecd79ba394349848a`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4d1ebca4fc352915e574abaa96ff6ed6588607144b48d49638664664171da1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785a52cc7646ffa85e15d5ffe60aac7f0f1a2d5253c2b101b6f346064092b53f`

```dockerfile
```

-	Layers:
	-	`sha256:57153e86db239ac28d0ccf1ea7c7b4f48b51df48813df21eab3ef9fec0624f79`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:8e53f8a2914c30d65228120667a050c54a74382d87f8e8205383be62560c9f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124579368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cc11a65e103a89e82e0f00f3eaea3ee929960b8b89fbf699a59f2bd46a109d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:148e72cbc3a4643c87b410580b6ae972ceafb99447e0d85bef2dd888ed7916d9`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 16.7 MB (16706481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfe37eaf11de403418a16f112ea736966145c615c0468af955274ca2d468276`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 17.4 MB (17448788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f071b9292f7441268ea76098e71b9dff0a1ec9f8311e4de77c6cd5af2c52a65`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 18.1 MB (18106565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a4fe84fb2fdef0c93d4c522edb4470e1d3558b04db73d6dc740cca4f2d3da6`  
		Last Modified: Thu, 19 Dec 2024 06:27:55 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa58f5b177c2d4b9d8d25bce148cba72f6b2db6ae71652dce2a49d1b4ecd88e`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755888e89afeff341e55361b436c6b35c8e67e7e05993e006c02d845c09320c3`  
		Last Modified: Thu, 19 Dec 2024 06:27:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ef02b0ebd56b76a25032f347f442a87fd532e2f07932b029c5a5ed2863ebdf`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 7.0 MB (7041137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa00a89210cf6cc619d32ecde33bcc417a048e4089420d3376e126502a34e868`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 89.1 KB (89114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314e6fc0bd408cd71d4f12dc2b30c175f02d576782580764a4d18dbe9397962a`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d2a39a9ca8dfcdf48360a081c2bacbd295c376b777d17ab83e02ace23e3d98`  
		Last Modified: Thu, 19 Dec 2024 07:08:09 GMT  
		Size: 53.8 MB (53837606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000fe248e69901663cba49cff877d5d4494f61261374eebd3e76654fdb4a9bb`  
		Last Modified: Thu, 19 Dec 2024 07:07:40 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e0a412273d2de4a63cf252e2955333edbb0387dab642897062720249f4180`  
		Last Modified: Thu, 19 Dec 2024 07:07:40 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:fbb76334b758da06115ce3db141b3a8d0384cf0fdfe0f1ae084cf566558cde04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05008ccd944add8210466657f1c49a19e043efce63da526e66de9aebb4b80ef`

```dockerfile
```

-	Layers:
	-	`sha256:d0c1d9bc2a056393fa0f5f33e177e88c39f2ff3b3ecab57b5172ba3064dfd763`  
		Last Modified: Thu, 19 Dec 2024 07:07:38 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:42fe1f55c44d24a6c3dabf704278f5beef25d390ca4c15966d714fb6e7908b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122921457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9248a004d8a619e67677191683cde42174b0b6a6f031c1bff04422a56ab7fafa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7384c11421040c34c2db4c9cbdff405dc1cb373620affa19cef0e6cd7889776b`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 16.7 MB (16694610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07bb9d6b4efc8e73c712cd756cad4ebdc7e4cd974f3b61319673b399cff7696`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 17.4 MB (17427589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e028074a72228d620c07c0306033af62a3bc33ecdbfdd182451a3940dbb3c47d`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 18.1 MB (18092645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b53f0105da3d54066118dde45e2db91fb53e54796d793199cb4d2ab602e9e2`  
		Last Modified: Thu, 19 Dec 2024 06:27:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6833631438bdcae5d6656508822939365cfd74de741e43abe8301361021b317`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b86ced47599bbfc27aa7dc389fb9cb257d493873490cc411bd8d27bdbf33bf`  
		Last Modified: Thu, 19 Dec 2024 06:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3cfec5adb0a4b5698f388de77eec77ddfae962de5b040d830dd95fded5c623`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 6.4 MB (6367338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f665ffa7443f60c8c9314082dba5723e72ede3f3451817173783b2ff36ffcb3`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 85.3 KB (85264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f8f3552eba49a36113015c2b82fecdb0cc6496614371b415212e14847dc60`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f31fefce9d3a0d0f1c7eb75b6cbde54e15ec723205ceea52b7da59ab4fb0dc`  
		Last Modified: Thu, 19 Dec 2024 07:07:45 GMT  
		Size: 53.8 MB (53837588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2522c47823d994b730d265c55af844c265eae9c9556e8e2200a9a35b9ac91a7`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06aa58a0bf71133cf40669589cd7fee930c7c0be06f93c2ff27147fd89bb1169`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:17996dd91287a758efee2344a070f6699509883f0d901af5ab238e9b387229bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b073ab412e1ae045cda1a9e0d874b37c17d7a32b94ca5af476daa61f0ae58438`

```dockerfile
```

-	Layers:
	-	`sha256:a559ea4afc9f0276e8285aa1e894d114568f8fc93aded28f64880c5b07631b25`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c4618ee87c867fff3b390aab9eeb59d889e39a14fb3bfbf40560f7faf78f841b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125264161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a74c04d0ac72b0d4df5a0d63124bff4cce8b81fe2f6d669d6272b5c426ef00e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc8b2386f26a19ff7e378d0b71a659c1c6185ff0418ab0ba70f91c9d7564766`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 8.1 MB (8077202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb804615f812dd41590a2167ce26fcd2bc94e936ef063d6ad5d47716653c51e`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500337a2754d23cb29983332f91f13bafcc80a7c299b977b077090a0fdf6e5a9`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.6 MB (17619412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821da57d87be4b4be2263810265c5fdfbee2a0815f9ba40aab6a34d602dbf10f`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.1 MB (17106449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a3e8ce8d46be94b3c36743d7add34488c85986d7d67dc65e6b0024b4f9629`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 17.6 MB (17642746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9727d9b709f029f03a062308481e155e1e44a388f1c90336ea9e6e9c98f4bf02`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5132ed17107a2140233d234c98fe9ff02ed459ac10f5b4ed2256ac52caff0ba2`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c450deeac7bd4e43a7a23a0608a88019260374cee39dc6371807295ef79a48`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95254613e12389bf1f1f60f9b295f28cef95138ce1dbc50738110a66f798909e`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 7.0 MB (6982148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3b84891c5b5b5525368fd009a3faa7c2ce7964cb220ec38caec428b7a4e023`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 97.8 KB (97810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f85e673a5bfddb9b35bc2893ca0b6dce01582d542e954e1f8522a5dc5bb96fc`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e62d3dc2daa4a6f98b762917d7f0adea4d641834acf4f0f8a44e1d79d577ab7`  
		Last Modified: Thu, 19 Dec 2024 07:07:59 GMT  
		Size: 53.7 MB (53737262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a6c5cd3176c0cc42a77bceba546446aac5d823c9f2fe97ef71fa20cc12bea4`  
		Last Modified: Thu, 19 Dec 2024 07:07:58 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01edfa8f426bf8debb954258fd0e37e36488fa9ba98d3d941a5b763aec91984f`  
		Last Modified: Thu, 19 Dec 2024 07:07:58 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b944da17175c77080cb8774711d10f0b88e7b131c7036b9ad130642f29955bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754b5f14591dc682613445f666f9460bab283af4d13ee4f7a9e3e47c27451707`

```dockerfile
```

-	Layers:
	-	`sha256:cc7c1950a5e5557483555eef92ae1c730a5df8239e11efd4015d579f2c48b149`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:5b6982daa87eac334c19156bfbcaa7931ac5758857d951b05be6136184534394
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:fc55380e4b93f80c1ed6d12d49cc548099c2cf4fc463a40d2e45a7441a15d625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155737519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8322a7c3c8154f09895c7509500e24519267dec8b762f4d2243bd47bfefd97`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
USER rootless
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b7051d06b1d34b73deaa52f5754a4c978be3600910f7b3c2b0fd99f3804cf`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 8.1 MB (8060784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be87b6ab9de77ee2bb24607f32584efd4c8d288fb0ebd92f21da27c6fb0fe05`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32318e2f30f796ed4b7af8e3685d3687fc883573db4a149b52ea74788725ff21`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 18.7 MB (18670168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eade46c9571ec550a556f19f01811aa5ed2c8d6d66dbe5c6b879696d6652b1b`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 18.8 MB (18799497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d7b24eacf786b52d80c07bc9d227f80f4b4ff879b36937506ba00283a87474`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 19.3 MB (19295662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a2d527e845f1b9d701a4f3acad785c3a2e23f0b660308cd25b755e606b275`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e2987b6254b27b8f98fd687e63ba6e98b22435e5b511b084f07928f607dd0`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f92ad0aa8787ef6e63b311833061f3d5251fb1a1f17dac1f8fe5a2a3c16dc`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c5d3db468870faaa078287545ebd4ce0c97ee7272f3bdb295dc466bfa5f372`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 6.7 MB (6729883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df9d86b50821da8baad5d1beab4920cef028caa1db97dff5f7b8ff6dc5cf47d`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 89.4 KB (89379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5068e4b2be3e0e95ca33a3f2ec02acc8405790e4b354aaeadb98bb913222bbf9`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9ce30e2857d84e08bbf13baf09599072c31f64a45cca98a5d2db5f034a63b`  
		Last Modified: Sat, 14 Dec 2024 02:09:04 GMT  
		Size: 58.1 MB (58147954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1484582dafdf336ddc9c0e4b9c157decc41f125fd5f9213a67fa254ed83765e8`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620491d45b64abb50f190afd835976134a08e3951aa9736fb39eee4acba99053`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e959b26a34438101745b4a6b12e2158e837753abb318a703d6a997acee940b32`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 986.6 KB (986587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c29d0936b41295dfa648ee92b27ebca2e18c10700ce27472e57dfdbcec4c6a`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485d19b2a60bc8d264042588663e4e123d26cbedf4aa96bbcf6ca5483bc82ca2`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50381dd0e19aea2b08429ae4b5824848b0e9e42926ee71822ae02df5e2693d16`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 21.3 MB (21303866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653b8fb52f49b277b1595dfbe1e5b2c3689df958d2df014003ce5cba5b7aa0c7`  
		Last Modified: Sat, 14 Dec 2024 03:07:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f6e358577a60d964b0f1b11ecf89a63cb21351522e15f87d7dfc6ebcda5969ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28cc68cd831df9a34e164fc2ea5b3f364ee6b02cc1f49f036ca59a72bc72571`

```dockerfile
```

-	Layers:
	-	`sha256:644bc1fff97fcf26268d33246cca53014486994146f0e5d4b02de3f5a26c9bcc`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:47cd9b46cc39d1ea39ce702f2b197f78006e12d471ac0d9143046b0805d3880c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149423499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486e46f1028dafc6440042fcd3a8a6bb5cefda114320b24a99730bc21b9f2484`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
USER rootless
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f29899ccbbf1e741f60597ba30d60ac9c1b90e66805313b199804e42bb26b8`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 8.1 MB (8077216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf82dff70ae622662fa9a73a5223978930a18a6ae224cf22cb4cb544d20e54cb`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4006eb8ef403cfad925fa266ee6c97b8e7437d82fada3b11ee40c73d1346fd29`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 17.6 MB (17619303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca033ddc28f236317e2717e08b0599bce7dc57f062d50e105789d951301709c1`  
		Last Modified: Sat, 14 Dec 2024 01:30:53 GMT  
		Size: 17.1 MB (17105676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac67c8631984a4a76018ae6dfcd431e33f8a842a5a41427c93622147b484e75`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 17.6 MB (17642698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca12aa3e41222dda17ff5dd783455ae9139e3b877645182502adeab17258e8`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2a18af15ca954957a7847214082e4df2bce64335dedd3ff4fba98f76284eb5`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df37b79dff77ef37f0d3e37560e1338f542f623ef54cfe86bb41fa8d10608a7`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa3443190ca0ce3c9348be68ac733b8e7eabb68fdf3494490329f5e4d077cf7`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 7.0 MB (6980417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df7beef76ff5ec34871261980d7ce36275d1e7863bacf11eb94ba868cdcb57d`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 97.8 KB (97751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2626027f39080c44a7fa749d2373483f2542a2948eb8ac4d5882687213fe6a0e`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb24cb7fa88f82359854c9298528e58874dd980f2287c10cff566c0b9443a467`  
		Last Modified: Sat, 14 Dec 2024 02:11:28 GMT  
		Size: 53.7 MB (53728638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a2a3c134987087aa5476cad229889681f776f2e8be759adb1c64cbb7d11855`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabb2966a6d122e4ad14e5c38fec5c030edb1573f093739072db71a5fa52ec29`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1095688739528f200fadd7670e4c7b354566e5b6a5663acc8690e24430f6e3`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 1.0 MB (1014153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecbf2c620964818ee2dcbc20a175aad27a6fb8b052fb19dd701cbbdb6f23e78`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac17c515dbd19f47019153943183a2995ace4060877f16ef7a715db68ae4181`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8818bf23aa3c08119351a436f05fc62b25a1fa448a59f02e05804a5ab92f00`  
		Last Modified: Sat, 14 Dec 2024 03:07:29 GMT  
		Size: 23.2 MB (23155158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056092e1c446a0219de668b0289797f8369a23417dd278d159af0606bf9b74c5`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3f695216a693f4d4041900f72c45a3e39ab19ae5c1727df82414c0e158a605ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c5773897944ec73002da42dd7bafb32c8788aadf785e3ffbd20df78b3d7de2`

```dockerfile
```

-	Layers:
	-	`sha256:732f97201f7324ad6916ceab73e27ea9cf755fc3a41522c77793bdef203efd55`  
		Last Modified: Sat, 14 Dec 2024 03:07:27 GMT  
		Size: 30.8 KB (30787 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:ce26a4b6892bb5fff408af70028fd1f7aadf1ba1817049f7c36d386b938f2a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:b59b50eddc96fa024759736642b20d31e812c747839aa0e04e6b3cd306d9c08f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312956798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dac0ff62690131e5cbadefa8b3173ce78f2fedeb1bedfb9599c99488be059a9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Thu, 19 Dec 2024 06:27:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Dec 2024 06:28:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Dec 2024 06:28:35 GMT
ENV DOCKER_VERSION=27.4.1
# Thu, 19 Dec 2024 06:28:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.1.zip
# Thu, 19 Dec 2024 06:28:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:28:58 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 19 Dec 2024 06:28:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 19 Dec 2024 06:28:59 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 19 Dec 2024 06:29:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Thu, 19 Dec 2024 06:29:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-windows-x86_64.exe
# Thu, 19 Dec 2024 06:29:12 GMT
ENV DOCKER_COMPOSE_SHA256=5dc7ac86e8d3972c2c68066c6ac370daf0a42b7c8d3338336c9dbde34af06213
# Thu, 19 Dec 2024 06:29:24 GMT
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
	-	`sha256:c2d7502a1bbe13300d252a2f9df8e505261a1640bc1bd25b0948e9c00fcc5b01`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c5b28592218521960824b8276896946f244fbb3651810d08c43452a2582cb`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 357.3 KB (357322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6330b409518a6d4ccfc671760fb4c29c3aa61745511abc8406e7598afdeb72f4`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff2da6ec5d910a6c45c3b7bc2ada4de7ee595addaae450cfea2ba3fba3571f0`  
		Last Modified: Thu, 19 Dec 2024 06:29:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981fcf2dca12be8aa09825096e39af48ab18642d75e6e2791014b5511999719c`  
		Last Modified: Thu, 19 Dec 2024 06:29:30 GMT  
		Size: 19.0 MB (18965788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559ffe22c82820dbe4c523868249c3f6a55385142d2e0ead71e852d8a7251d56`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458e70a57b4ce24dfc2a913ab05c3222397fe2e8a5d93868622a5da7a9340e81`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dd3b199caac21501453ed73a1b07e07e8909c492da3b0c12264e12be24f8f7`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffced5034da239bcce196f61166f31fa32a1046a0b90925f73df0a56a4540555`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 19.6 MB (19615775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d1d24e414a381ae30c27fae03be0f84206adbad1d9b6b30407bfecceb5e1e5`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deeb14568d7a7f723c99e08a5b860258c0e121c9b475c7f14d316ac30cb06d68`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a34da183fbb7bde6f718a61627a8077978264175188a7e437d8f791c46033e`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdb77e5d84cc05ce04533280006424bb2742fe825cfe58eb5f5934b7a430dcf`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 20.1 MB (20132656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:c442ec204cc8c3af89a231557d7113d731304aa9004ecc2fd2b7fdea9a2a5ed5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073460288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd24b1732cd2a56ef18bd248405211562b17b3b25cc385edc36040b8cea00146`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Thu, 19 Dec 2024 06:27:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Dec 2024 06:28:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Dec 2024 06:28:36 GMT
ENV DOCKER_VERSION=27.4.1
# Thu, 19 Dec 2024 06:28:37 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.1.zip
# Thu, 19 Dec 2024 06:29:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:00 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 19 Dec 2024 06:29:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 19 Dec 2024 06:29:01 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 19 Dec 2024 06:29:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Thu, 19 Dec 2024 06:29:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-windows-x86_64.exe
# Thu, 19 Dec 2024 06:29:16 GMT
ENV DOCKER_COMPOSE_SHA256=5dc7ac86e8d3972c2c68066c6ac370daf0a42b7c8d3338336c9dbde34af06213
# Thu, 19 Dec 2024 06:29:30 GMT
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
	-	`sha256:e1cfd0430e259e32b94429bf581ea5f74b25080ea9e68899e17062c55bfdba4f`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089d2b012e4350683f7592078e0330072d47face607cfdcfa1b177015a1d055d`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 475.3 KB (475261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e54e6e8f743b8e62247f614caa153507aeea30e39ec7d133b120770472d150d`  
		Last Modified: Thu, 19 Dec 2024 06:29:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c46ebe5f7bc661958c2410ed2a60431be6d40269618a1223f8bc2c1f5392c26`  
		Last Modified: Thu, 19 Dec 2024 06:29:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac2d753848f2b9292c76be0e8c43f38d7c04ed25979be15179b781a3c2b47b9`  
		Last Modified: Thu, 19 Dec 2024 06:29:36 GMT  
		Size: 19.0 MB (18997863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4c651853f033dafb87a17fdd7690c1c3c3a0f4dfb6e083cf06ba8d91234d98`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1a3389962e8b333bfcead93ec3aad31713a4bafd7b7be628b737077da7d60b`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e030ce22f45d6c461af01d11e768dcd4638cd9b989e6dc8aa7e384b7ccb80129`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d987b1383b6b76eb88c20a38bac7e305fe1f8c311242b83bc819be0eee3eb3`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 19.6 MB (19648080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e0d2a17e8fa800de7106ca7d9cce51ab9562558d2d155ddfaaa0d979138750`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d9b36807cefb176cc3c814de379c2bf6a17663ed8e0372f69d2cb06a02cd4e`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f2c79cb8ac15f188f4afd8366afee1f46ec780fa70082a4c9e991ac09c8537`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f72ede2a361313c0a7e7b059df25505b175cc277540b12cb48ee012d5a4ba93`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 20.2 MB (20157227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:5a5cd9f42944d54ac3da3dfda65c1d0342f266339ac3fde581f7021a2aa3c54c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:c442ec204cc8c3af89a231557d7113d731304aa9004ecc2fd2b7fdea9a2a5ed5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073460288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd24b1732cd2a56ef18bd248405211562b17b3b25cc385edc36040b8cea00146`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Thu, 19 Dec 2024 06:27:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Dec 2024 06:28:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Dec 2024 06:28:36 GMT
ENV DOCKER_VERSION=27.4.1
# Thu, 19 Dec 2024 06:28:37 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.1.zip
# Thu, 19 Dec 2024 06:29:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:00 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 19 Dec 2024 06:29:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 19 Dec 2024 06:29:01 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 19 Dec 2024 06:29:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Thu, 19 Dec 2024 06:29:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-windows-x86_64.exe
# Thu, 19 Dec 2024 06:29:16 GMT
ENV DOCKER_COMPOSE_SHA256=5dc7ac86e8d3972c2c68066c6ac370daf0a42b7c8d3338336c9dbde34af06213
# Thu, 19 Dec 2024 06:29:30 GMT
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
	-	`sha256:e1cfd0430e259e32b94429bf581ea5f74b25080ea9e68899e17062c55bfdba4f`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089d2b012e4350683f7592078e0330072d47face607cfdcfa1b177015a1d055d`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 475.3 KB (475261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e54e6e8f743b8e62247f614caa153507aeea30e39ec7d133b120770472d150d`  
		Last Modified: Thu, 19 Dec 2024 06:29:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c46ebe5f7bc661958c2410ed2a60431be6d40269618a1223f8bc2c1f5392c26`  
		Last Modified: Thu, 19 Dec 2024 06:29:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac2d753848f2b9292c76be0e8c43f38d7c04ed25979be15179b781a3c2b47b9`  
		Last Modified: Thu, 19 Dec 2024 06:29:36 GMT  
		Size: 19.0 MB (18997863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4c651853f033dafb87a17fdd7690c1c3c3a0f4dfb6e083cf06ba8d91234d98`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1a3389962e8b333bfcead93ec3aad31713a4bafd7b7be628b737077da7d60b`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e030ce22f45d6c461af01d11e768dcd4638cd9b989e6dc8aa7e384b7ccb80129`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d987b1383b6b76eb88c20a38bac7e305fe1f8c311242b83bc819be0eee3eb3`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 19.6 MB (19648080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e0d2a17e8fa800de7106ca7d9cce51ab9562558d2d155ddfaaa0d979138750`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d9b36807cefb176cc3c814de379c2bf6a17663ed8e0372f69d2cb06a02cd4e`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f2c79cb8ac15f188f4afd8366afee1f46ec780fa70082a4c9e991ac09c8537`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f72ede2a361313c0a7e7b059df25505b175cc277540b12cb48ee012d5a4ba93`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 20.2 MB (20157227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:bbaca47510bc3b68824fca9b3d27ac84ec15755c88e1ac61a53c6f93ace9c225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:b59b50eddc96fa024759736642b20d31e812c747839aa0e04e6b3cd306d9c08f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312956798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dac0ff62690131e5cbadefa8b3173ce78f2fedeb1bedfb9599c99488be059a9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Thu, 19 Dec 2024 06:27:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Dec 2024 06:28:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Dec 2024 06:28:35 GMT
ENV DOCKER_VERSION=27.4.1
# Thu, 19 Dec 2024 06:28:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.1.zip
# Thu, 19 Dec 2024 06:28:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:28:58 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 19 Dec 2024 06:28:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 19 Dec 2024 06:28:59 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 19 Dec 2024 06:29:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Thu, 19 Dec 2024 06:29:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-windows-x86_64.exe
# Thu, 19 Dec 2024 06:29:12 GMT
ENV DOCKER_COMPOSE_SHA256=5dc7ac86e8d3972c2c68066c6ac370daf0a42b7c8d3338336c9dbde34af06213
# Thu, 19 Dec 2024 06:29:24 GMT
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
	-	`sha256:c2d7502a1bbe13300d252a2f9df8e505261a1640bc1bd25b0948e9c00fcc5b01`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c5b28592218521960824b8276896946f244fbb3651810d08c43452a2582cb`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 357.3 KB (357322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6330b409518a6d4ccfc671760fb4c29c3aa61745511abc8406e7598afdeb72f4`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff2da6ec5d910a6c45c3b7bc2ada4de7ee595addaae450cfea2ba3fba3571f0`  
		Last Modified: Thu, 19 Dec 2024 06:29:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981fcf2dca12be8aa09825096e39af48ab18642d75e6e2791014b5511999719c`  
		Last Modified: Thu, 19 Dec 2024 06:29:30 GMT  
		Size: 19.0 MB (18965788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559ffe22c82820dbe4c523868249c3f6a55385142d2e0ead71e852d8a7251d56`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458e70a57b4ce24dfc2a913ab05c3222397fe2e8a5d93868622a5da7a9340e81`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dd3b199caac21501453ed73a1b07e07e8909c492da3b0c12264e12be24f8f7`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffced5034da239bcce196f61166f31fa32a1046a0b90925f73df0a56a4540555`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 19.6 MB (19615775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d1d24e414a381ae30c27fae03be0f84206adbad1d9b6b30407bfecceb5e1e5`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deeb14568d7a7f723c99e08a5b860258c0e121c9b475c7f14d316ac30cb06d68`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a34da183fbb7bde6f718a61627a8077978264175188a7e437d8f791c46033e`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdb77e5d84cc05ce04533280006424bb2742fe825cfe58eb5f5934b7a430dcf`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 20.1 MB (20132656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.4`

```console
$ docker pull docker@sha256:d33ffba5909705d375ef1a99bb69fe6e21d80482134283226b119acf18bb08b4
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

### `docker:27.4` - linux; amd64

```console
$ docker pull docker@sha256:197a4c5f8ffb8e4940e2518b1863588839743d062576c9d144a91fc64400c25b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133448845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c9711c027ed5c0c1bc82bf858e1a428676cd76681a56c53068db5510594f55`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b98de49fe1ed993db53e09ac1d349e04edc68f3a669a0166fe861e63f21139`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 8.1 MB (8060708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af95ea946dd1ea6ddb09d4d16636c6dbdaf31f2a92f21fccf332f412f91978b`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313c9b4ec4148bbc92f321352088134bd5c79313a32b0346277392e67f81276a`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 18.7 MB (18669944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7c930da0eae6c203479c2208bc111980211a355e5ebe1d8b9d771bd3b3f5a2`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 18.8 MB (18798867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0028ab84266b23892e8257b849272b905514e4111ccc878a47fc9e050d94e`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf34514361d460f057db2b94643dcc0fa3771b2df3b514bcc118a203a10c95ba`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003372bc0a71b5fee80b7721b00c600392a2d1297a7bdc1382c4fe9b7a3c478`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654c3b9f6f86104ad7ac2a1861a8a6a3c9624bdb262e0024f0daee392ebdc1d`  
		Last Modified: Thu, 19 Dec 2024 06:27:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccacb1ec449ea2d8be4c5f1323c8f8f438ca6cbadb852569e5a1d30b2fccfb0`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 6.7 MB (6733442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db08b2b56d721154b01a601fafbf1388da92317b2a6fd84636403d145397cab`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 89.5 KB (89464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf58bc5c124acd8cd7867de0e5bfe811139bb7efbdfb4d3f384f5047368feadb`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed661c2bc3605af63c34b0e0e6b44c343cfaaeaeff5a9c5a1e90636c29b3c3`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 58.1 MB (58148385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd93031177fed6768ebac95908f7214e148aec625cde4db347278f785e7061f`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4580133da14d68ef765c552929a21bcefda14fd6f6d46ecd79ba394349848a`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4` - unknown; unknown

```console
$ docker pull docker@sha256:4d1ebca4fc352915e574abaa96ff6ed6588607144b48d49638664664171da1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785a52cc7646ffa85e15d5ffe60aac7f0f1a2d5253c2b101b6f346064092b53f`

```dockerfile
```

-	Layers:
	-	`sha256:57153e86db239ac28d0ccf1ea7c7b4f48b51df48813df21eab3ef9fec0624f79`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4` - linux; arm variant v6

```console
$ docker pull docker@sha256:8e53f8a2914c30d65228120667a050c54a74382d87f8e8205383be62560c9f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124579368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cc11a65e103a89e82e0f00f3eaea3ee929960b8b89fbf699a59f2bd46a109d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:148e72cbc3a4643c87b410580b6ae972ceafb99447e0d85bef2dd888ed7916d9`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 16.7 MB (16706481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfe37eaf11de403418a16f112ea736966145c615c0468af955274ca2d468276`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 17.4 MB (17448788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f071b9292f7441268ea76098e71b9dff0a1ec9f8311e4de77c6cd5af2c52a65`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 18.1 MB (18106565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a4fe84fb2fdef0c93d4c522edb4470e1d3558b04db73d6dc740cca4f2d3da6`  
		Last Modified: Thu, 19 Dec 2024 06:27:55 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa58f5b177c2d4b9d8d25bce148cba72f6b2db6ae71652dce2a49d1b4ecd88e`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755888e89afeff341e55361b436c6b35c8e67e7e05993e006c02d845c09320c3`  
		Last Modified: Thu, 19 Dec 2024 06:27:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ef02b0ebd56b76a25032f347f442a87fd532e2f07932b029c5a5ed2863ebdf`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 7.0 MB (7041137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa00a89210cf6cc619d32ecde33bcc417a048e4089420d3376e126502a34e868`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 89.1 KB (89114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314e6fc0bd408cd71d4f12dc2b30c175f02d576782580764a4d18dbe9397962a`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d2a39a9ca8dfcdf48360a081c2bacbd295c376b777d17ab83e02ace23e3d98`  
		Last Modified: Thu, 19 Dec 2024 07:08:09 GMT  
		Size: 53.8 MB (53837606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000fe248e69901663cba49cff877d5d4494f61261374eebd3e76654fdb4a9bb`  
		Last Modified: Thu, 19 Dec 2024 07:07:40 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e0a412273d2de4a63cf252e2955333edbb0387dab642897062720249f4180`  
		Last Modified: Thu, 19 Dec 2024 07:07:40 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4` - unknown; unknown

```console
$ docker pull docker@sha256:fbb76334b758da06115ce3db141b3a8d0384cf0fdfe0f1ae084cf566558cde04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05008ccd944add8210466657f1c49a19e043efce63da526e66de9aebb4b80ef`

```dockerfile
```

-	Layers:
	-	`sha256:d0c1d9bc2a056393fa0f5f33e177e88c39f2ff3b3ecab57b5172ba3064dfd763`  
		Last Modified: Thu, 19 Dec 2024 07:07:38 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4` - linux; arm variant v7

```console
$ docker pull docker@sha256:42fe1f55c44d24a6c3dabf704278f5beef25d390ca4c15966d714fb6e7908b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122921457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9248a004d8a619e67677191683cde42174b0b6a6f031c1bff04422a56ab7fafa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7384c11421040c34c2db4c9cbdff405dc1cb373620affa19cef0e6cd7889776b`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 16.7 MB (16694610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07bb9d6b4efc8e73c712cd756cad4ebdc7e4cd974f3b61319673b399cff7696`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 17.4 MB (17427589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e028074a72228d620c07c0306033af62a3bc33ecdbfdd182451a3940dbb3c47d`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 18.1 MB (18092645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b53f0105da3d54066118dde45e2db91fb53e54796d793199cb4d2ab602e9e2`  
		Last Modified: Thu, 19 Dec 2024 06:27:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6833631438bdcae5d6656508822939365cfd74de741e43abe8301361021b317`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b86ced47599bbfc27aa7dc389fb9cb257d493873490cc411bd8d27bdbf33bf`  
		Last Modified: Thu, 19 Dec 2024 06:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3cfec5adb0a4b5698f388de77eec77ddfae962de5b040d830dd95fded5c623`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 6.4 MB (6367338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f665ffa7443f60c8c9314082dba5723e72ede3f3451817173783b2ff36ffcb3`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 85.3 KB (85264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f8f3552eba49a36113015c2b82fecdb0cc6496614371b415212e14847dc60`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f31fefce9d3a0d0f1c7eb75b6cbde54e15ec723205ceea52b7da59ab4fb0dc`  
		Last Modified: Thu, 19 Dec 2024 07:07:45 GMT  
		Size: 53.8 MB (53837588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2522c47823d994b730d265c55af844c265eae9c9556e8e2200a9a35b9ac91a7`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06aa58a0bf71133cf40669589cd7fee930c7c0be06f93c2ff27147fd89bb1169`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4` - unknown; unknown

```console
$ docker pull docker@sha256:17996dd91287a758efee2344a070f6699509883f0d901af5ab238e9b387229bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b073ab412e1ae045cda1a9e0d874b37c17d7a32b94ca5af476daa61f0ae58438`

```dockerfile
```

-	Layers:
	-	`sha256:a559ea4afc9f0276e8285aa1e894d114568f8fc93aded28f64880c5b07631b25`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c4618ee87c867fff3b390aab9eeb59d889e39a14fb3bfbf40560f7faf78f841b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125264161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a74c04d0ac72b0d4df5a0d63124bff4cce8b81fe2f6d669d6272b5c426ef00e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc8b2386f26a19ff7e378d0b71a659c1c6185ff0418ab0ba70f91c9d7564766`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 8.1 MB (8077202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb804615f812dd41590a2167ce26fcd2bc94e936ef063d6ad5d47716653c51e`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500337a2754d23cb29983332f91f13bafcc80a7c299b977b077090a0fdf6e5a9`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.6 MB (17619412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821da57d87be4b4be2263810265c5fdfbee2a0815f9ba40aab6a34d602dbf10f`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.1 MB (17106449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a3e8ce8d46be94b3c36743d7add34488c85986d7d67dc65e6b0024b4f9629`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 17.6 MB (17642746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9727d9b709f029f03a062308481e155e1e44a388f1c90336ea9e6e9c98f4bf02`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5132ed17107a2140233d234c98fe9ff02ed459ac10f5b4ed2256ac52caff0ba2`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c450deeac7bd4e43a7a23a0608a88019260374cee39dc6371807295ef79a48`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95254613e12389bf1f1f60f9b295f28cef95138ce1dbc50738110a66f798909e`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 7.0 MB (6982148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3b84891c5b5b5525368fd009a3faa7c2ce7964cb220ec38caec428b7a4e023`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 97.8 KB (97810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f85e673a5bfddb9b35bc2893ca0b6dce01582d542e954e1f8522a5dc5bb96fc`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e62d3dc2daa4a6f98b762917d7f0adea4d641834acf4f0f8a44e1d79d577ab7`  
		Last Modified: Thu, 19 Dec 2024 07:07:59 GMT  
		Size: 53.7 MB (53737262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a6c5cd3176c0cc42a77bceba546446aac5d823c9f2fe97ef71fa20cc12bea4`  
		Last Modified: Thu, 19 Dec 2024 07:07:58 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01edfa8f426bf8debb954258fd0e37e36488fa9ba98d3d941a5b763aec91984f`  
		Last Modified: Thu, 19 Dec 2024 07:07:58 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4` - unknown; unknown

```console
$ docker pull docker@sha256:b944da17175c77080cb8774711d10f0b88e7b131c7036b9ad130642f29955bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754b5f14591dc682613445f666f9460bab283af4d13ee4f7a9e3e47c27451707`

```dockerfile
```

-	Layers:
	-	`sha256:cc7c1950a5e5557483555eef92ae1c730a5df8239e11efd4015d579f2c48b149`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.4-cli`

```console
$ docker pull docker@sha256:2a9c1ba4816ddafdcf49a561201a9af2c451017e263a16a4fb1f878c454e1c44
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

### `docker:27.4-cli` - linux; amd64

```console
$ docker pull docker@sha256:0d052bc5fcedc9b04935ffc5c1ca039c2c3f442c22dac9fab600f1e8348bc810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68471761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b387bcd9f4eb8854253fbd37d44ddd3a01ae6ed50d46fcf2371fbd0a72bf874e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b98de49fe1ed993db53e09ac1d349e04edc68f3a669a0166fe861e63f21139`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 8.1 MB (8060708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af95ea946dd1ea6ddb09d4d16636c6dbdaf31f2a92f21fccf332f412f91978b`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313c9b4ec4148bbc92f321352088134bd5c79313a32b0346277392e67f81276a`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 18.7 MB (18669944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7c930da0eae6c203479c2208bc111980211a355e5ebe1d8b9d771bd3b3f5a2`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 18.8 MB (18798867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0028ab84266b23892e8257b849272b905514e4111ccc878a47fc9e050d94e`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf34514361d460f057db2b94643dcc0fa3771b2df3b514bcc118a203a10c95ba`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003372bc0a71b5fee80b7721b00c600392a2d1297a7bdc1382c4fe9b7a3c478`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654c3b9f6f86104ad7ac2a1861a8a6a3c9624bdb262e0024f0daee392ebdc1d`  
		Last Modified: Thu, 19 Dec 2024 06:27:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:25b71b84216a6b6fa15b2e5d77e03b34e15d770a4e7bd0d5a12dc5a94e712a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32b3f66abca23fa334f7a356d599e2b285535319198c82ba778c5ae1d68c0d1`

```dockerfile
```

-	Layers:
	-	`sha256:e4b152243122d2a2b2ba6915e1be8a0003ac4d08efd17fcdf8208957caf3a8cb`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:2e6d722b4ad5fe9d873cddaf4f60fc20dcb740a401df852ba406b3068398b7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63605712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3487d4e2b40727fa327f1bc3ac2976f9c228483c0f71198a14759f48b37a693`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:148e72cbc3a4643c87b410580b6ae972ceafb99447e0d85bef2dd888ed7916d9`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 16.7 MB (16706481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfe37eaf11de403418a16f112ea736966145c615c0468af955274ca2d468276`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 17.4 MB (17448788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f071b9292f7441268ea76098e71b9dff0a1ec9f8311e4de77c6cd5af2c52a65`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 18.1 MB (18106565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a4fe84fb2fdef0c93d4c522edb4470e1d3558b04db73d6dc740cca4f2d3da6`  
		Last Modified: Thu, 19 Dec 2024 06:27:55 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa58f5b177c2d4b9d8d25bce148cba72f6b2db6ae71652dce2a49d1b4ecd88e`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755888e89afeff341e55361b436c6b35c8e67e7e05993e006c02d845c09320c3`  
		Last Modified: Thu, 19 Dec 2024 06:27:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:ff1cbb618b403ea74aa5eaef6d1ce343a27b799a14e73accc6d45186a8183c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ef782c195058519b295e8b5f7623848187120a6c037d0c852bc65400041fb6`

```dockerfile
```

-	Layers:
	-	`sha256:d4a3b6f2edb30ef6c175dc855c3cac8939a2acc6acf24bdba215d5e4bf9af607`  
		Last Modified: Thu, 19 Dec 2024 06:27:55 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:f89c36bd6f08a78078044ca2606b40abfd6e2bee5c34d5d0a227e545e70b31f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62625475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0973c3f1d70b0f02dd2301a26effa977c42a8930649cb0bb1dba2cad5abba685`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7384c11421040c34c2db4c9cbdff405dc1cb373620affa19cef0e6cd7889776b`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 16.7 MB (16694610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07bb9d6b4efc8e73c712cd756cad4ebdc7e4cd974f3b61319673b399cff7696`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 17.4 MB (17427589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e028074a72228d620c07c0306033af62a3bc33ecdbfdd182451a3940dbb3c47d`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 18.1 MB (18092645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b53f0105da3d54066118dde45e2db91fb53e54796d793199cb4d2ab602e9e2`  
		Last Modified: Thu, 19 Dec 2024 06:27:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6833631438bdcae5d6656508822939365cfd74de741e43abe8301361021b317`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b86ced47599bbfc27aa7dc389fb9cb257d493873490cc411bd8d27bdbf33bf`  
		Last Modified: Thu, 19 Dec 2024 06:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:82ae1c7b8fe94fdc49f39f3eec184d02572b400c4a225d2c5bc3a811850bbcb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394c76df731da9a4b7d8ffb5fc4820c5cabe9516f2202a945000d67de063966a`

```dockerfile
```

-	Layers:
	-	`sha256:4eac62d6a3079b4b3118e6b704cd97ad9ecd8ff718b1097e1cb02a713120697f`  
		Last Modified: Thu, 19 Dec 2024 06:27:30 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8e85a9901bc8d85c147f51091bc0a91ad62559db69480b088d838f5b52cdf542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64441149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b503fae5efdeebe409c4458ec85ccbe53f3abf5c2833f311ee7720d7a0b1bd60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc8b2386f26a19ff7e378d0b71a659c1c6185ff0418ab0ba70f91c9d7564766`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 8.1 MB (8077202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb804615f812dd41590a2167ce26fcd2bc94e936ef063d6ad5d47716653c51e`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500337a2754d23cb29983332f91f13bafcc80a7c299b977b077090a0fdf6e5a9`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.6 MB (17619412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821da57d87be4b4be2263810265c5fdfbee2a0815f9ba40aab6a34d602dbf10f`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.1 MB (17106449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a3e8ce8d46be94b3c36743d7add34488c85986d7d67dc65e6b0024b4f9629`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 17.6 MB (17642746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9727d9b709f029f03a062308481e155e1e44a388f1c90336ea9e6e9c98f4bf02`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5132ed17107a2140233d234c98fe9ff02ed459ac10f5b4ed2256ac52caff0ba2`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c450deeac7bd4e43a7a23a0608a88019260374cee39dc6371807295ef79a48`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:5a1c761171de4faf5bbd2753ce69aedb70bf0172682167323093305a9172bf8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d8489705c0a7ad5281a14fa0580dfe1e84ac35e8ed32f1e4746b551b3ec27d`

```dockerfile
```

-	Layers:
	-	`sha256:34348583b40c1f2b4ae040bdaa91a20e47adaa05541d9cafe8e43557dc582b3a`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.4-dind`

```console
$ docker pull docker@sha256:d33ffba5909705d375ef1a99bb69fe6e21d80482134283226b119acf18bb08b4
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

### `docker:27.4-dind` - linux; amd64

```console
$ docker pull docker@sha256:197a4c5f8ffb8e4940e2518b1863588839743d062576c9d144a91fc64400c25b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133448845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c9711c027ed5c0c1bc82bf858e1a428676cd76681a56c53068db5510594f55`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b98de49fe1ed993db53e09ac1d349e04edc68f3a669a0166fe861e63f21139`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 8.1 MB (8060708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af95ea946dd1ea6ddb09d4d16636c6dbdaf31f2a92f21fccf332f412f91978b`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313c9b4ec4148bbc92f321352088134bd5c79313a32b0346277392e67f81276a`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 18.7 MB (18669944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7c930da0eae6c203479c2208bc111980211a355e5ebe1d8b9d771bd3b3f5a2`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 18.8 MB (18798867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0028ab84266b23892e8257b849272b905514e4111ccc878a47fc9e050d94e`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf34514361d460f057db2b94643dcc0fa3771b2df3b514bcc118a203a10c95ba`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003372bc0a71b5fee80b7721b00c600392a2d1297a7bdc1382c4fe9b7a3c478`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654c3b9f6f86104ad7ac2a1861a8a6a3c9624bdb262e0024f0daee392ebdc1d`  
		Last Modified: Thu, 19 Dec 2024 06:27:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccacb1ec449ea2d8be4c5f1323c8f8f438ca6cbadb852569e5a1d30b2fccfb0`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 6.7 MB (6733442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db08b2b56d721154b01a601fafbf1388da92317b2a6fd84636403d145397cab`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 89.5 KB (89464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf58bc5c124acd8cd7867de0e5bfe811139bb7efbdfb4d3f384f5047368feadb`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed661c2bc3605af63c34b0e0e6b44c343cfaaeaeff5a9c5a1e90636c29b3c3`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 58.1 MB (58148385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd93031177fed6768ebac95908f7214e148aec625cde4db347278f785e7061f`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4580133da14d68ef765c552929a21bcefda14fd6f6d46ecd79ba394349848a`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4d1ebca4fc352915e574abaa96ff6ed6588607144b48d49638664664171da1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785a52cc7646ffa85e15d5ffe60aac7f0f1a2d5253c2b101b6f346064092b53f`

```dockerfile
```

-	Layers:
	-	`sha256:57153e86db239ac28d0ccf1ea7c7b4f48b51df48813df21eab3ef9fec0624f79`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:8e53f8a2914c30d65228120667a050c54a74382d87f8e8205383be62560c9f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124579368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cc11a65e103a89e82e0f00f3eaea3ee929960b8b89fbf699a59f2bd46a109d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:148e72cbc3a4643c87b410580b6ae972ceafb99447e0d85bef2dd888ed7916d9`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 16.7 MB (16706481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfe37eaf11de403418a16f112ea736966145c615c0468af955274ca2d468276`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 17.4 MB (17448788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f071b9292f7441268ea76098e71b9dff0a1ec9f8311e4de77c6cd5af2c52a65`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 18.1 MB (18106565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a4fe84fb2fdef0c93d4c522edb4470e1d3558b04db73d6dc740cca4f2d3da6`  
		Last Modified: Thu, 19 Dec 2024 06:27:55 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa58f5b177c2d4b9d8d25bce148cba72f6b2db6ae71652dce2a49d1b4ecd88e`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755888e89afeff341e55361b436c6b35c8e67e7e05993e006c02d845c09320c3`  
		Last Modified: Thu, 19 Dec 2024 06:27:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ef02b0ebd56b76a25032f347f442a87fd532e2f07932b029c5a5ed2863ebdf`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 7.0 MB (7041137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa00a89210cf6cc619d32ecde33bcc417a048e4089420d3376e126502a34e868`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 89.1 KB (89114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314e6fc0bd408cd71d4f12dc2b30c175f02d576782580764a4d18dbe9397962a`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d2a39a9ca8dfcdf48360a081c2bacbd295c376b777d17ab83e02ace23e3d98`  
		Last Modified: Thu, 19 Dec 2024 07:08:09 GMT  
		Size: 53.8 MB (53837606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000fe248e69901663cba49cff877d5d4494f61261374eebd3e76654fdb4a9bb`  
		Last Modified: Thu, 19 Dec 2024 07:07:40 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e0a412273d2de4a63cf252e2955333edbb0387dab642897062720249f4180`  
		Last Modified: Thu, 19 Dec 2024 07:07:40 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:fbb76334b758da06115ce3db141b3a8d0384cf0fdfe0f1ae084cf566558cde04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05008ccd944add8210466657f1c49a19e043efce63da526e66de9aebb4b80ef`

```dockerfile
```

-	Layers:
	-	`sha256:d0c1d9bc2a056393fa0f5f33e177e88c39f2ff3b3ecab57b5172ba3064dfd763`  
		Last Modified: Thu, 19 Dec 2024 07:07:38 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:42fe1f55c44d24a6c3dabf704278f5beef25d390ca4c15966d714fb6e7908b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122921457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9248a004d8a619e67677191683cde42174b0b6a6f031c1bff04422a56ab7fafa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7384c11421040c34c2db4c9cbdff405dc1cb373620affa19cef0e6cd7889776b`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 16.7 MB (16694610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07bb9d6b4efc8e73c712cd756cad4ebdc7e4cd974f3b61319673b399cff7696`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 17.4 MB (17427589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e028074a72228d620c07c0306033af62a3bc33ecdbfdd182451a3940dbb3c47d`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 18.1 MB (18092645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b53f0105da3d54066118dde45e2db91fb53e54796d793199cb4d2ab602e9e2`  
		Last Modified: Thu, 19 Dec 2024 06:27:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6833631438bdcae5d6656508822939365cfd74de741e43abe8301361021b317`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b86ced47599bbfc27aa7dc389fb9cb257d493873490cc411bd8d27bdbf33bf`  
		Last Modified: Thu, 19 Dec 2024 06:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3cfec5adb0a4b5698f388de77eec77ddfae962de5b040d830dd95fded5c623`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 6.4 MB (6367338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f665ffa7443f60c8c9314082dba5723e72ede3f3451817173783b2ff36ffcb3`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 85.3 KB (85264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f8f3552eba49a36113015c2b82fecdb0cc6496614371b415212e14847dc60`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f31fefce9d3a0d0f1c7eb75b6cbde54e15ec723205ceea52b7da59ab4fb0dc`  
		Last Modified: Thu, 19 Dec 2024 07:07:45 GMT  
		Size: 53.8 MB (53837588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2522c47823d994b730d265c55af844c265eae9c9556e8e2200a9a35b9ac91a7`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06aa58a0bf71133cf40669589cd7fee930c7c0be06f93c2ff27147fd89bb1169`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:17996dd91287a758efee2344a070f6699509883f0d901af5ab238e9b387229bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b073ab412e1ae045cda1a9e0d874b37c17d7a32b94ca5af476daa61f0ae58438`

```dockerfile
```

-	Layers:
	-	`sha256:a559ea4afc9f0276e8285aa1e894d114568f8fc93aded28f64880c5b07631b25`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c4618ee87c867fff3b390aab9eeb59d889e39a14fb3bfbf40560f7faf78f841b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125264161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a74c04d0ac72b0d4df5a0d63124bff4cce8b81fe2f6d669d6272b5c426ef00e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc8b2386f26a19ff7e378d0b71a659c1c6185ff0418ab0ba70f91c9d7564766`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 8.1 MB (8077202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb804615f812dd41590a2167ce26fcd2bc94e936ef063d6ad5d47716653c51e`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500337a2754d23cb29983332f91f13bafcc80a7c299b977b077090a0fdf6e5a9`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.6 MB (17619412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821da57d87be4b4be2263810265c5fdfbee2a0815f9ba40aab6a34d602dbf10f`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.1 MB (17106449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a3e8ce8d46be94b3c36743d7add34488c85986d7d67dc65e6b0024b4f9629`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 17.6 MB (17642746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9727d9b709f029f03a062308481e155e1e44a388f1c90336ea9e6e9c98f4bf02`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5132ed17107a2140233d234c98fe9ff02ed459ac10f5b4ed2256ac52caff0ba2`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c450deeac7bd4e43a7a23a0608a88019260374cee39dc6371807295ef79a48`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95254613e12389bf1f1f60f9b295f28cef95138ce1dbc50738110a66f798909e`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 7.0 MB (6982148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3b84891c5b5b5525368fd009a3faa7c2ce7964cb220ec38caec428b7a4e023`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 97.8 KB (97810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f85e673a5bfddb9b35bc2893ca0b6dce01582d542e954e1f8522a5dc5bb96fc`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e62d3dc2daa4a6f98b762917d7f0adea4d641834acf4f0f8a44e1d79d577ab7`  
		Last Modified: Thu, 19 Dec 2024 07:07:59 GMT  
		Size: 53.7 MB (53737262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a6c5cd3176c0cc42a77bceba546446aac5d823c9f2fe97ef71fa20cc12bea4`  
		Last Modified: Thu, 19 Dec 2024 07:07:58 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01edfa8f426bf8debb954258fd0e37e36488fa9ba98d3d941a5b763aec91984f`  
		Last Modified: Thu, 19 Dec 2024 07:07:58 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b944da17175c77080cb8774711d10f0b88e7b131c7036b9ad130642f29955bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754b5f14591dc682613445f666f9460bab283af4d13ee4f7a9e3e47c27451707`

```dockerfile
```

-	Layers:
	-	`sha256:cc7c1950a5e5557483555eef92ae1c730a5df8239e11efd4015d579f2c48b149`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.4-dind-rootless`

```console
$ docker pull docker@sha256:5b6982daa87eac334c19156bfbcaa7931ac5758857d951b05be6136184534394
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.4-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:fc55380e4b93f80c1ed6d12d49cc548099c2cf4fc463a40d2e45a7441a15d625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155737519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8322a7c3c8154f09895c7509500e24519267dec8b762f4d2243bd47bfefd97`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
USER rootless
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b7051d06b1d34b73deaa52f5754a4c978be3600910f7b3c2b0fd99f3804cf`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 8.1 MB (8060784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be87b6ab9de77ee2bb24607f32584efd4c8d288fb0ebd92f21da27c6fb0fe05`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32318e2f30f796ed4b7af8e3685d3687fc883573db4a149b52ea74788725ff21`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 18.7 MB (18670168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eade46c9571ec550a556f19f01811aa5ed2c8d6d66dbe5c6b879696d6652b1b`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 18.8 MB (18799497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d7b24eacf786b52d80c07bc9d227f80f4b4ff879b36937506ba00283a87474`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 19.3 MB (19295662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a2d527e845f1b9d701a4f3acad785c3a2e23f0b660308cd25b755e606b275`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e2987b6254b27b8f98fd687e63ba6e98b22435e5b511b084f07928f607dd0`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f92ad0aa8787ef6e63b311833061f3d5251fb1a1f17dac1f8fe5a2a3c16dc`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c5d3db468870faaa078287545ebd4ce0c97ee7272f3bdb295dc466bfa5f372`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 6.7 MB (6729883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df9d86b50821da8baad5d1beab4920cef028caa1db97dff5f7b8ff6dc5cf47d`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 89.4 KB (89379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5068e4b2be3e0e95ca33a3f2ec02acc8405790e4b354aaeadb98bb913222bbf9`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9ce30e2857d84e08bbf13baf09599072c31f64a45cca98a5d2db5f034a63b`  
		Last Modified: Sat, 14 Dec 2024 02:09:04 GMT  
		Size: 58.1 MB (58147954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1484582dafdf336ddc9c0e4b9c157decc41f125fd5f9213a67fa254ed83765e8`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620491d45b64abb50f190afd835976134a08e3951aa9736fb39eee4acba99053`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e959b26a34438101745b4a6b12e2158e837753abb318a703d6a997acee940b32`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 986.6 KB (986587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c29d0936b41295dfa648ee92b27ebca2e18c10700ce27472e57dfdbcec4c6a`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485d19b2a60bc8d264042588663e4e123d26cbedf4aa96bbcf6ca5483bc82ca2`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50381dd0e19aea2b08429ae4b5824848b0e9e42926ee71822ae02df5e2693d16`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 21.3 MB (21303866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653b8fb52f49b277b1595dfbe1e5b2c3689df958d2df014003ce5cba5b7aa0c7`  
		Last Modified: Sat, 14 Dec 2024 03:07:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f6e358577a60d964b0f1b11ecf89a63cb21351522e15f87d7dfc6ebcda5969ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28cc68cd831df9a34e164fc2ea5b3f364ee6b02cc1f49f036ca59a72bc72571`

```dockerfile
```

-	Layers:
	-	`sha256:644bc1fff97fcf26268d33246cca53014486994146f0e5d4b02de3f5a26c9bcc`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:47cd9b46cc39d1ea39ce702f2b197f78006e12d471ac0d9143046b0805d3880c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149423499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486e46f1028dafc6440042fcd3a8a6bb5cefda114320b24a99730bc21b9f2484`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
USER rootless
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f29899ccbbf1e741f60597ba30d60ac9c1b90e66805313b199804e42bb26b8`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 8.1 MB (8077216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf82dff70ae622662fa9a73a5223978930a18a6ae224cf22cb4cb544d20e54cb`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4006eb8ef403cfad925fa266ee6c97b8e7437d82fada3b11ee40c73d1346fd29`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 17.6 MB (17619303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca033ddc28f236317e2717e08b0599bce7dc57f062d50e105789d951301709c1`  
		Last Modified: Sat, 14 Dec 2024 01:30:53 GMT  
		Size: 17.1 MB (17105676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac67c8631984a4a76018ae6dfcd431e33f8a842a5a41427c93622147b484e75`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 17.6 MB (17642698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca12aa3e41222dda17ff5dd783455ae9139e3b877645182502adeab17258e8`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2a18af15ca954957a7847214082e4df2bce64335dedd3ff4fba98f76284eb5`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df37b79dff77ef37f0d3e37560e1338f542f623ef54cfe86bb41fa8d10608a7`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa3443190ca0ce3c9348be68ac733b8e7eabb68fdf3494490329f5e4d077cf7`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 7.0 MB (6980417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df7beef76ff5ec34871261980d7ce36275d1e7863bacf11eb94ba868cdcb57d`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 97.8 KB (97751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2626027f39080c44a7fa749d2373483f2542a2948eb8ac4d5882687213fe6a0e`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb24cb7fa88f82359854c9298528e58874dd980f2287c10cff566c0b9443a467`  
		Last Modified: Sat, 14 Dec 2024 02:11:28 GMT  
		Size: 53.7 MB (53728638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a2a3c134987087aa5476cad229889681f776f2e8be759adb1c64cbb7d11855`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabb2966a6d122e4ad14e5c38fec5c030edb1573f093739072db71a5fa52ec29`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1095688739528f200fadd7670e4c7b354566e5b6a5663acc8690e24430f6e3`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 1.0 MB (1014153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecbf2c620964818ee2dcbc20a175aad27a6fb8b052fb19dd701cbbdb6f23e78`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac17c515dbd19f47019153943183a2995ace4060877f16ef7a715db68ae4181`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8818bf23aa3c08119351a436f05fc62b25a1fa448a59f02e05804a5ab92f00`  
		Last Modified: Sat, 14 Dec 2024 03:07:29 GMT  
		Size: 23.2 MB (23155158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056092e1c446a0219de668b0289797f8369a23417dd278d159af0606bf9b74c5`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3f695216a693f4d4041900f72c45a3e39ab19ae5c1727df82414c0e158a605ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c5773897944ec73002da42dd7bafb32c8788aadf785e3ffbd20df78b3d7de2`

```dockerfile
```

-	Layers:
	-	`sha256:732f97201f7324ad6916ceab73e27ea9cf755fc3a41522c77793bdef203efd55`  
		Last Modified: Sat, 14 Dec 2024 03:07:27 GMT  
		Size: 30.8 KB (30787 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.4-windowsservercore`

```console
$ docker pull docker@sha256:ce26a4b6892bb5fff408af70028fd1f7aadf1ba1817049f7c36d386b938f2a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `docker:27.4-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:b59b50eddc96fa024759736642b20d31e812c747839aa0e04e6b3cd306d9c08f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312956798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dac0ff62690131e5cbadefa8b3173ce78f2fedeb1bedfb9599c99488be059a9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Thu, 19 Dec 2024 06:27:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Dec 2024 06:28:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Dec 2024 06:28:35 GMT
ENV DOCKER_VERSION=27.4.1
# Thu, 19 Dec 2024 06:28:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.1.zip
# Thu, 19 Dec 2024 06:28:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:28:58 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 19 Dec 2024 06:28:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 19 Dec 2024 06:28:59 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 19 Dec 2024 06:29:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Thu, 19 Dec 2024 06:29:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-windows-x86_64.exe
# Thu, 19 Dec 2024 06:29:12 GMT
ENV DOCKER_COMPOSE_SHA256=5dc7ac86e8d3972c2c68066c6ac370daf0a42b7c8d3338336c9dbde34af06213
# Thu, 19 Dec 2024 06:29:24 GMT
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
	-	`sha256:c2d7502a1bbe13300d252a2f9df8e505261a1640bc1bd25b0948e9c00fcc5b01`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c5b28592218521960824b8276896946f244fbb3651810d08c43452a2582cb`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 357.3 KB (357322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6330b409518a6d4ccfc671760fb4c29c3aa61745511abc8406e7598afdeb72f4`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff2da6ec5d910a6c45c3b7bc2ada4de7ee595addaae450cfea2ba3fba3571f0`  
		Last Modified: Thu, 19 Dec 2024 06:29:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981fcf2dca12be8aa09825096e39af48ab18642d75e6e2791014b5511999719c`  
		Last Modified: Thu, 19 Dec 2024 06:29:30 GMT  
		Size: 19.0 MB (18965788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559ffe22c82820dbe4c523868249c3f6a55385142d2e0ead71e852d8a7251d56`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458e70a57b4ce24dfc2a913ab05c3222397fe2e8a5d93868622a5da7a9340e81`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dd3b199caac21501453ed73a1b07e07e8909c492da3b0c12264e12be24f8f7`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffced5034da239bcce196f61166f31fa32a1046a0b90925f73df0a56a4540555`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 19.6 MB (19615775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d1d24e414a381ae30c27fae03be0f84206adbad1d9b6b30407bfecceb5e1e5`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deeb14568d7a7f723c99e08a5b860258c0e121c9b475c7f14d316ac30cb06d68`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a34da183fbb7bde6f718a61627a8077978264175188a7e437d8f791c46033e`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdb77e5d84cc05ce04533280006424bb2742fe825cfe58eb5f5934b7a430dcf`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 20.1 MB (20132656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.4-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:c442ec204cc8c3af89a231557d7113d731304aa9004ecc2fd2b7fdea9a2a5ed5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073460288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd24b1732cd2a56ef18bd248405211562b17b3b25cc385edc36040b8cea00146`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Thu, 19 Dec 2024 06:27:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Dec 2024 06:28:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Dec 2024 06:28:36 GMT
ENV DOCKER_VERSION=27.4.1
# Thu, 19 Dec 2024 06:28:37 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.1.zip
# Thu, 19 Dec 2024 06:29:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:00 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 19 Dec 2024 06:29:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 19 Dec 2024 06:29:01 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 19 Dec 2024 06:29:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Thu, 19 Dec 2024 06:29:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-windows-x86_64.exe
# Thu, 19 Dec 2024 06:29:16 GMT
ENV DOCKER_COMPOSE_SHA256=5dc7ac86e8d3972c2c68066c6ac370daf0a42b7c8d3338336c9dbde34af06213
# Thu, 19 Dec 2024 06:29:30 GMT
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
	-	`sha256:e1cfd0430e259e32b94429bf581ea5f74b25080ea9e68899e17062c55bfdba4f`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089d2b012e4350683f7592078e0330072d47face607cfdcfa1b177015a1d055d`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 475.3 KB (475261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e54e6e8f743b8e62247f614caa153507aeea30e39ec7d133b120770472d150d`  
		Last Modified: Thu, 19 Dec 2024 06:29:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c46ebe5f7bc661958c2410ed2a60431be6d40269618a1223f8bc2c1f5392c26`  
		Last Modified: Thu, 19 Dec 2024 06:29:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac2d753848f2b9292c76be0e8c43f38d7c04ed25979be15179b781a3c2b47b9`  
		Last Modified: Thu, 19 Dec 2024 06:29:36 GMT  
		Size: 19.0 MB (18997863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4c651853f033dafb87a17fdd7690c1c3c3a0f4dfb6e083cf06ba8d91234d98`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1a3389962e8b333bfcead93ec3aad31713a4bafd7b7be628b737077da7d60b`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e030ce22f45d6c461af01d11e768dcd4638cd9b989e6dc8aa7e384b7ccb80129`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d987b1383b6b76eb88c20a38bac7e305fe1f8c311242b83bc819be0eee3eb3`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 19.6 MB (19648080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e0d2a17e8fa800de7106ca7d9cce51ab9562558d2d155ddfaaa0d979138750`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d9b36807cefb176cc3c814de379c2bf6a17663ed8e0372f69d2cb06a02cd4e`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f2c79cb8ac15f188f4afd8366afee1f46ec780fa70082a4c9e991ac09c8537`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f72ede2a361313c0a7e7b059df25505b175cc277540b12cb48ee012d5a4ba93`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 20.2 MB (20157227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.4-windowsservercore-1809`

```console
$ docker pull docker@sha256:5a5cd9f42944d54ac3da3dfda65c1d0342f266339ac3fde581f7021a2aa3c54c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `docker:27.4-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:c442ec204cc8c3af89a231557d7113d731304aa9004ecc2fd2b7fdea9a2a5ed5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073460288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd24b1732cd2a56ef18bd248405211562b17b3b25cc385edc36040b8cea00146`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Thu, 19 Dec 2024 06:27:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Dec 2024 06:28:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Dec 2024 06:28:36 GMT
ENV DOCKER_VERSION=27.4.1
# Thu, 19 Dec 2024 06:28:37 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.1.zip
# Thu, 19 Dec 2024 06:29:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:00 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 19 Dec 2024 06:29:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 19 Dec 2024 06:29:01 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 19 Dec 2024 06:29:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Thu, 19 Dec 2024 06:29:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-windows-x86_64.exe
# Thu, 19 Dec 2024 06:29:16 GMT
ENV DOCKER_COMPOSE_SHA256=5dc7ac86e8d3972c2c68066c6ac370daf0a42b7c8d3338336c9dbde34af06213
# Thu, 19 Dec 2024 06:29:30 GMT
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
	-	`sha256:e1cfd0430e259e32b94429bf581ea5f74b25080ea9e68899e17062c55bfdba4f`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089d2b012e4350683f7592078e0330072d47face607cfdcfa1b177015a1d055d`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 475.3 KB (475261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e54e6e8f743b8e62247f614caa153507aeea30e39ec7d133b120770472d150d`  
		Last Modified: Thu, 19 Dec 2024 06:29:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c46ebe5f7bc661958c2410ed2a60431be6d40269618a1223f8bc2c1f5392c26`  
		Last Modified: Thu, 19 Dec 2024 06:29:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac2d753848f2b9292c76be0e8c43f38d7c04ed25979be15179b781a3c2b47b9`  
		Last Modified: Thu, 19 Dec 2024 06:29:36 GMT  
		Size: 19.0 MB (18997863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4c651853f033dafb87a17fdd7690c1c3c3a0f4dfb6e083cf06ba8d91234d98`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1a3389962e8b333bfcead93ec3aad31713a4bafd7b7be628b737077da7d60b`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e030ce22f45d6c461af01d11e768dcd4638cd9b989e6dc8aa7e384b7ccb80129`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d987b1383b6b76eb88c20a38bac7e305fe1f8c311242b83bc819be0eee3eb3`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 19.6 MB (19648080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e0d2a17e8fa800de7106ca7d9cce51ab9562558d2d155ddfaaa0d979138750`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d9b36807cefb176cc3c814de379c2bf6a17663ed8e0372f69d2cb06a02cd4e`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f2c79cb8ac15f188f4afd8366afee1f46ec780fa70082a4c9e991ac09c8537`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f72ede2a361313c0a7e7b059df25505b175cc277540b12cb48ee012d5a4ba93`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 20.2 MB (20157227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.4-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:bbaca47510bc3b68824fca9b3d27ac84ec15755c88e1ac61a53c6f93ace9c225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `docker:27.4-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:b59b50eddc96fa024759736642b20d31e812c747839aa0e04e6b3cd306d9c08f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312956798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dac0ff62690131e5cbadefa8b3173ce78f2fedeb1bedfb9599c99488be059a9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Thu, 19 Dec 2024 06:27:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Dec 2024 06:28:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Dec 2024 06:28:35 GMT
ENV DOCKER_VERSION=27.4.1
# Thu, 19 Dec 2024 06:28:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.1.zip
# Thu, 19 Dec 2024 06:28:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:28:58 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 19 Dec 2024 06:28:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 19 Dec 2024 06:28:59 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 19 Dec 2024 06:29:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Thu, 19 Dec 2024 06:29:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-windows-x86_64.exe
# Thu, 19 Dec 2024 06:29:12 GMT
ENV DOCKER_COMPOSE_SHA256=5dc7ac86e8d3972c2c68066c6ac370daf0a42b7c8d3338336c9dbde34af06213
# Thu, 19 Dec 2024 06:29:24 GMT
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
	-	`sha256:c2d7502a1bbe13300d252a2f9df8e505261a1640bc1bd25b0948e9c00fcc5b01`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c5b28592218521960824b8276896946f244fbb3651810d08c43452a2582cb`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 357.3 KB (357322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6330b409518a6d4ccfc671760fb4c29c3aa61745511abc8406e7598afdeb72f4`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff2da6ec5d910a6c45c3b7bc2ada4de7ee595addaae450cfea2ba3fba3571f0`  
		Last Modified: Thu, 19 Dec 2024 06:29:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981fcf2dca12be8aa09825096e39af48ab18642d75e6e2791014b5511999719c`  
		Last Modified: Thu, 19 Dec 2024 06:29:30 GMT  
		Size: 19.0 MB (18965788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559ffe22c82820dbe4c523868249c3f6a55385142d2e0ead71e852d8a7251d56`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458e70a57b4ce24dfc2a913ab05c3222397fe2e8a5d93868622a5da7a9340e81`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dd3b199caac21501453ed73a1b07e07e8909c492da3b0c12264e12be24f8f7`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffced5034da239bcce196f61166f31fa32a1046a0b90925f73df0a56a4540555`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 19.6 MB (19615775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d1d24e414a381ae30c27fae03be0f84206adbad1d9b6b30407bfecceb5e1e5`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deeb14568d7a7f723c99e08a5b860258c0e121c9b475c7f14d316ac30cb06d68`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a34da183fbb7bde6f718a61627a8077978264175188a7e437d8f791c46033e`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdb77e5d84cc05ce04533280006424bb2742fe825cfe58eb5f5934b7a430dcf`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 20.1 MB (20132656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.4.1`

```console
$ docker pull docker@sha256:d33ffba5909705d375ef1a99bb69fe6e21d80482134283226b119acf18bb08b4
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

### `docker:27.4.1` - linux; amd64

```console
$ docker pull docker@sha256:197a4c5f8ffb8e4940e2518b1863588839743d062576c9d144a91fc64400c25b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133448845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c9711c027ed5c0c1bc82bf858e1a428676cd76681a56c53068db5510594f55`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b98de49fe1ed993db53e09ac1d349e04edc68f3a669a0166fe861e63f21139`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 8.1 MB (8060708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af95ea946dd1ea6ddb09d4d16636c6dbdaf31f2a92f21fccf332f412f91978b`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313c9b4ec4148bbc92f321352088134bd5c79313a32b0346277392e67f81276a`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 18.7 MB (18669944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7c930da0eae6c203479c2208bc111980211a355e5ebe1d8b9d771bd3b3f5a2`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 18.8 MB (18798867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0028ab84266b23892e8257b849272b905514e4111ccc878a47fc9e050d94e`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf34514361d460f057db2b94643dcc0fa3771b2df3b514bcc118a203a10c95ba`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003372bc0a71b5fee80b7721b00c600392a2d1297a7bdc1382c4fe9b7a3c478`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654c3b9f6f86104ad7ac2a1861a8a6a3c9624bdb262e0024f0daee392ebdc1d`  
		Last Modified: Thu, 19 Dec 2024 06:27:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccacb1ec449ea2d8be4c5f1323c8f8f438ca6cbadb852569e5a1d30b2fccfb0`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 6.7 MB (6733442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db08b2b56d721154b01a601fafbf1388da92317b2a6fd84636403d145397cab`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 89.5 KB (89464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf58bc5c124acd8cd7867de0e5bfe811139bb7efbdfb4d3f384f5047368feadb`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed661c2bc3605af63c34b0e0e6b44c343cfaaeaeff5a9c5a1e90636c29b3c3`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 58.1 MB (58148385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd93031177fed6768ebac95908f7214e148aec625cde4db347278f785e7061f`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4580133da14d68ef765c552929a21bcefda14fd6f6d46ecd79ba394349848a`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1` - unknown; unknown

```console
$ docker pull docker@sha256:4d1ebca4fc352915e574abaa96ff6ed6588607144b48d49638664664171da1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785a52cc7646ffa85e15d5ffe60aac7f0f1a2d5253c2b101b6f346064092b53f`

```dockerfile
```

-	Layers:
	-	`sha256:57153e86db239ac28d0ccf1ea7c7b4f48b51df48813df21eab3ef9fec0624f79`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4.1` - linux; arm variant v6

```console
$ docker pull docker@sha256:8e53f8a2914c30d65228120667a050c54a74382d87f8e8205383be62560c9f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124579368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cc11a65e103a89e82e0f00f3eaea3ee929960b8b89fbf699a59f2bd46a109d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:148e72cbc3a4643c87b410580b6ae972ceafb99447e0d85bef2dd888ed7916d9`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 16.7 MB (16706481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfe37eaf11de403418a16f112ea736966145c615c0468af955274ca2d468276`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 17.4 MB (17448788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f071b9292f7441268ea76098e71b9dff0a1ec9f8311e4de77c6cd5af2c52a65`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 18.1 MB (18106565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a4fe84fb2fdef0c93d4c522edb4470e1d3558b04db73d6dc740cca4f2d3da6`  
		Last Modified: Thu, 19 Dec 2024 06:27:55 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa58f5b177c2d4b9d8d25bce148cba72f6b2db6ae71652dce2a49d1b4ecd88e`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755888e89afeff341e55361b436c6b35c8e67e7e05993e006c02d845c09320c3`  
		Last Modified: Thu, 19 Dec 2024 06:27:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ef02b0ebd56b76a25032f347f442a87fd532e2f07932b029c5a5ed2863ebdf`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 7.0 MB (7041137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa00a89210cf6cc619d32ecde33bcc417a048e4089420d3376e126502a34e868`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 89.1 KB (89114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314e6fc0bd408cd71d4f12dc2b30c175f02d576782580764a4d18dbe9397962a`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d2a39a9ca8dfcdf48360a081c2bacbd295c376b777d17ab83e02ace23e3d98`  
		Last Modified: Thu, 19 Dec 2024 07:08:09 GMT  
		Size: 53.8 MB (53837606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000fe248e69901663cba49cff877d5d4494f61261374eebd3e76654fdb4a9bb`  
		Last Modified: Thu, 19 Dec 2024 07:07:40 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e0a412273d2de4a63cf252e2955333edbb0387dab642897062720249f4180`  
		Last Modified: Thu, 19 Dec 2024 07:07:40 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1` - unknown; unknown

```console
$ docker pull docker@sha256:fbb76334b758da06115ce3db141b3a8d0384cf0fdfe0f1ae084cf566558cde04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05008ccd944add8210466657f1c49a19e043efce63da526e66de9aebb4b80ef`

```dockerfile
```

-	Layers:
	-	`sha256:d0c1d9bc2a056393fa0f5f33e177e88c39f2ff3b3ecab57b5172ba3064dfd763`  
		Last Modified: Thu, 19 Dec 2024 07:07:38 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4.1` - linux; arm variant v7

```console
$ docker pull docker@sha256:42fe1f55c44d24a6c3dabf704278f5beef25d390ca4c15966d714fb6e7908b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122921457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9248a004d8a619e67677191683cde42174b0b6a6f031c1bff04422a56ab7fafa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7384c11421040c34c2db4c9cbdff405dc1cb373620affa19cef0e6cd7889776b`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 16.7 MB (16694610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07bb9d6b4efc8e73c712cd756cad4ebdc7e4cd974f3b61319673b399cff7696`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 17.4 MB (17427589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e028074a72228d620c07c0306033af62a3bc33ecdbfdd182451a3940dbb3c47d`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 18.1 MB (18092645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b53f0105da3d54066118dde45e2db91fb53e54796d793199cb4d2ab602e9e2`  
		Last Modified: Thu, 19 Dec 2024 06:27:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6833631438bdcae5d6656508822939365cfd74de741e43abe8301361021b317`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b86ced47599bbfc27aa7dc389fb9cb257d493873490cc411bd8d27bdbf33bf`  
		Last Modified: Thu, 19 Dec 2024 06:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3cfec5adb0a4b5698f388de77eec77ddfae962de5b040d830dd95fded5c623`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 6.4 MB (6367338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f665ffa7443f60c8c9314082dba5723e72ede3f3451817173783b2ff36ffcb3`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 85.3 KB (85264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f8f3552eba49a36113015c2b82fecdb0cc6496614371b415212e14847dc60`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f31fefce9d3a0d0f1c7eb75b6cbde54e15ec723205ceea52b7da59ab4fb0dc`  
		Last Modified: Thu, 19 Dec 2024 07:07:45 GMT  
		Size: 53.8 MB (53837588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2522c47823d994b730d265c55af844c265eae9c9556e8e2200a9a35b9ac91a7`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06aa58a0bf71133cf40669589cd7fee930c7c0be06f93c2ff27147fd89bb1169`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1` - unknown; unknown

```console
$ docker pull docker@sha256:17996dd91287a758efee2344a070f6699509883f0d901af5ab238e9b387229bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b073ab412e1ae045cda1a9e0d874b37c17d7a32b94ca5af476daa61f0ae58438`

```dockerfile
```

-	Layers:
	-	`sha256:a559ea4afc9f0276e8285aa1e894d114568f8fc93aded28f64880c5b07631b25`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c4618ee87c867fff3b390aab9eeb59d889e39a14fb3bfbf40560f7faf78f841b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125264161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a74c04d0ac72b0d4df5a0d63124bff4cce8b81fe2f6d669d6272b5c426ef00e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc8b2386f26a19ff7e378d0b71a659c1c6185ff0418ab0ba70f91c9d7564766`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 8.1 MB (8077202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb804615f812dd41590a2167ce26fcd2bc94e936ef063d6ad5d47716653c51e`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500337a2754d23cb29983332f91f13bafcc80a7c299b977b077090a0fdf6e5a9`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.6 MB (17619412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821da57d87be4b4be2263810265c5fdfbee2a0815f9ba40aab6a34d602dbf10f`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.1 MB (17106449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a3e8ce8d46be94b3c36743d7add34488c85986d7d67dc65e6b0024b4f9629`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 17.6 MB (17642746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9727d9b709f029f03a062308481e155e1e44a388f1c90336ea9e6e9c98f4bf02`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5132ed17107a2140233d234c98fe9ff02ed459ac10f5b4ed2256ac52caff0ba2`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c450deeac7bd4e43a7a23a0608a88019260374cee39dc6371807295ef79a48`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95254613e12389bf1f1f60f9b295f28cef95138ce1dbc50738110a66f798909e`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 7.0 MB (6982148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3b84891c5b5b5525368fd009a3faa7c2ce7964cb220ec38caec428b7a4e023`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 97.8 KB (97810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f85e673a5bfddb9b35bc2893ca0b6dce01582d542e954e1f8522a5dc5bb96fc`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e62d3dc2daa4a6f98b762917d7f0adea4d641834acf4f0f8a44e1d79d577ab7`  
		Last Modified: Thu, 19 Dec 2024 07:07:59 GMT  
		Size: 53.7 MB (53737262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a6c5cd3176c0cc42a77bceba546446aac5d823c9f2fe97ef71fa20cc12bea4`  
		Last Modified: Thu, 19 Dec 2024 07:07:58 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01edfa8f426bf8debb954258fd0e37e36488fa9ba98d3d941a5b763aec91984f`  
		Last Modified: Thu, 19 Dec 2024 07:07:58 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1` - unknown; unknown

```console
$ docker pull docker@sha256:b944da17175c77080cb8774711d10f0b88e7b131c7036b9ad130642f29955bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754b5f14591dc682613445f666f9460bab283af4d13ee4f7a9e3e47c27451707`

```dockerfile
```

-	Layers:
	-	`sha256:cc7c1950a5e5557483555eef92ae1c730a5df8239e11efd4015d579f2c48b149`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.4.1-alpine3.21`

```console
$ docker pull docker@sha256:d33ffba5909705d375ef1a99bb69fe6e21d80482134283226b119acf18bb08b4
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

### `docker:27.4.1-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:197a4c5f8ffb8e4940e2518b1863588839743d062576c9d144a91fc64400c25b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133448845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c9711c027ed5c0c1bc82bf858e1a428676cd76681a56c53068db5510594f55`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b98de49fe1ed993db53e09ac1d349e04edc68f3a669a0166fe861e63f21139`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 8.1 MB (8060708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af95ea946dd1ea6ddb09d4d16636c6dbdaf31f2a92f21fccf332f412f91978b`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313c9b4ec4148bbc92f321352088134bd5c79313a32b0346277392e67f81276a`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 18.7 MB (18669944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7c930da0eae6c203479c2208bc111980211a355e5ebe1d8b9d771bd3b3f5a2`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 18.8 MB (18798867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0028ab84266b23892e8257b849272b905514e4111ccc878a47fc9e050d94e`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf34514361d460f057db2b94643dcc0fa3771b2df3b514bcc118a203a10c95ba`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003372bc0a71b5fee80b7721b00c600392a2d1297a7bdc1382c4fe9b7a3c478`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654c3b9f6f86104ad7ac2a1861a8a6a3c9624bdb262e0024f0daee392ebdc1d`  
		Last Modified: Thu, 19 Dec 2024 06:27:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccacb1ec449ea2d8be4c5f1323c8f8f438ca6cbadb852569e5a1d30b2fccfb0`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 6.7 MB (6733442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db08b2b56d721154b01a601fafbf1388da92317b2a6fd84636403d145397cab`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 89.5 KB (89464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf58bc5c124acd8cd7867de0e5bfe811139bb7efbdfb4d3f384f5047368feadb`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed661c2bc3605af63c34b0e0e6b44c343cfaaeaeff5a9c5a1e90636c29b3c3`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 58.1 MB (58148385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd93031177fed6768ebac95908f7214e148aec625cde4db347278f785e7061f`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4580133da14d68ef765c552929a21bcefda14fd6f6d46ecd79ba394349848a`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:4d1ebca4fc352915e574abaa96ff6ed6588607144b48d49638664664171da1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785a52cc7646ffa85e15d5ffe60aac7f0f1a2d5253c2b101b6f346064092b53f`

```dockerfile
```

-	Layers:
	-	`sha256:57153e86db239ac28d0ccf1ea7c7b4f48b51df48813df21eab3ef9fec0624f79`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4.1-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:8e53f8a2914c30d65228120667a050c54a74382d87f8e8205383be62560c9f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124579368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cc11a65e103a89e82e0f00f3eaea3ee929960b8b89fbf699a59f2bd46a109d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:148e72cbc3a4643c87b410580b6ae972ceafb99447e0d85bef2dd888ed7916d9`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 16.7 MB (16706481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfe37eaf11de403418a16f112ea736966145c615c0468af955274ca2d468276`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 17.4 MB (17448788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f071b9292f7441268ea76098e71b9dff0a1ec9f8311e4de77c6cd5af2c52a65`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 18.1 MB (18106565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a4fe84fb2fdef0c93d4c522edb4470e1d3558b04db73d6dc740cca4f2d3da6`  
		Last Modified: Thu, 19 Dec 2024 06:27:55 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa58f5b177c2d4b9d8d25bce148cba72f6b2db6ae71652dce2a49d1b4ecd88e`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755888e89afeff341e55361b436c6b35c8e67e7e05993e006c02d845c09320c3`  
		Last Modified: Thu, 19 Dec 2024 06:27:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ef02b0ebd56b76a25032f347f442a87fd532e2f07932b029c5a5ed2863ebdf`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 7.0 MB (7041137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa00a89210cf6cc619d32ecde33bcc417a048e4089420d3376e126502a34e868`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 89.1 KB (89114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314e6fc0bd408cd71d4f12dc2b30c175f02d576782580764a4d18dbe9397962a`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d2a39a9ca8dfcdf48360a081c2bacbd295c376b777d17ab83e02ace23e3d98`  
		Last Modified: Thu, 19 Dec 2024 07:08:09 GMT  
		Size: 53.8 MB (53837606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000fe248e69901663cba49cff877d5d4494f61261374eebd3e76654fdb4a9bb`  
		Last Modified: Thu, 19 Dec 2024 07:07:40 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e0a412273d2de4a63cf252e2955333edbb0387dab642897062720249f4180`  
		Last Modified: Thu, 19 Dec 2024 07:07:40 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:fbb76334b758da06115ce3db141b3a8d0384cf0fdfe0f1ae084cf566558cde04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05008ccd944add8210466657f1c49a19e043efce63da526e66de9aebb4b80ef`

```dockerfile
```

-	Layers:
	-	`sha256:d0c1d9bc2a056393fa0f5f33e177e88c39f2ff3b3ecab57b5172ba3064dfd763`  
		Last Modified: Thu, 19 Dec 2024 07:07:38 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4.1-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:42fe1f55c44d24a6c3dabf704278f5beef25d390ca4c15966d714fb6e7908b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122921457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9248a004d8a619e67677191683cde42174b0b6a6f031c1bff04422a56ab7fafa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7384c11421040c34c2db4c9cbdff405dc1cb373620affa19cef0e6cd7889776b`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 16.7 MB (16694610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07bb9d6b4efc8e73c712cd756cad4ebdc7e4cd974f3b61319673b399cff7696`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 17.4 MB (17427589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e028074a72228d620c07c0306033af62a3bc33ecdbfdd182451a3940dbb3c47d`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 18.1 MB (18092645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b53f0105da3d54066118dde45e2db91fb53e54796d793199cb4d2ab602e9e2`  
		Last Modified: Thu, 19 Dec 2024 06:27:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6833631438bdcae5d6656508822939365cfd74de741e43abe8301361021b317`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b86ced47599bbfc27aa7dc389fb9cb257d493873490cc411bd8d27bdbf33bf`  
		Last Modified: Thu, 19 Dec 2024 06:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3cfec5adb0a4b5698f388de77eec77ddfae962de5b040d830dd95fded5c623`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 6.4 MB (6367338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f665ffa7443f60c8c9314082dba5723e72ede3f3451817173783b2ff36ffcb3`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 85.3 KB (85264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f8f3552eba49a36113015c2b82fecdb0cc6496614371b415212e14847dc60`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f31fefce9d3a0d0f1c7eb75b6cbde54e15ec723205ceea52b7da59ab4fb0dc`  
		Last Modified: Thu, 19 Dec 2024 07:07:45 GMT  
		Size: 53.8 MB (53837588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2522c47823d994b730d265c55af844c265eae9c9556e8e2200a9a35b9ac91a7`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06aa58a0bf71133cf40669589cd7fee930c7c0be06f93c2ff27147fd89bb1169`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:17996dd91287a758efee2344a070f6699509883f0d901af5ab238e9b387229bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b073ab412e1ae045cda1a9e0d874b37c17d7a32b94ca5af476daa61f0ae58438`

```dockerfile
```

-	Layers:
	-	`sha256:a559ea4afc9f0276e8285aa1e894d114568f8fc93aded28f64880c5b07631b25`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4.1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c4618ee87c867fff3b390aab9eeb59d889e39a14fb3bfbf40560f7faf78f841b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125264161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a74c04d0ac72b0d4df5a0d63124bff4cce8b81fe2f6d669d6272b5c426ef00e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc8b2386f26a19ff7e378d0b71a659c1c6185ff0418ab0ba70f91c9d7564766`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 8.1 MB (8077202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb804615f812dd41590a2167ce26fcd2bc94e936ef063d6ad5d47716653c51e`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500337a2754d23cb29983332f91f13bafcc80a7c299b977b077090a0fdf6e5a9`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.6 MB (17619412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821da57d87be4b4be2263810265c5fdfbee2a0815f9ba40aab6a34d602dbf10f`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.1 MB (17106449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a3e8ce8d46be94b3c36743d7add34488c85986d7d67dc65e6b0024b4f9629`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 17.6 MB (17642746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9727d9b709f029f03a062308481e155e1e44a388f1c90336ea9e6e9c98f4bf02`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5132ed17107a2140233d234c98fe9ff02ed459ac10f5b4ed2256ac52caff0ba2`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c450deeac7bd4e43a7a23a0608a88019260374cee39dc6371807295ef79a48`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95254613e12389bf1f1f60f9b295f28cef95138ce1dbc50738110a66f798909e`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 7.0 MB (6982148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3b84891c5b5b5525368fd009a3faa7c2ce7964cb220ec38caec428b7a4e023`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 97.8 KB (97810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f85e673a5bfddb9b35bc2893ca0b6dce01582d542e954e1f8522a5dc5bb96fc`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e62d3dc2daa4a6f98b762917d7f0adea4d641834acf4f0f8a44e1d79d577ab7`  
		Last Modified: Thu, 19 Dec 2024 07:07:59 GMT  
		Size: 53.7 MB (53737262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a6c5cd3176c0cc42a77bceba546446aac5d823c9f2fe97ef71fa20cc12bea4`  
		Last Modified: Thu, 19 Dec 2024 07:07:58 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01edfa8f426bf8debb954258fd0e37e36488fa9ba98d3d941a5b763aec91984f`  
		Last Modified: Thu, 19 Dec 2024 07:07:58 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:b944da17175c77080cb8774711d10f0b88e7b131c7036b9ad130642f29955bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754b5f14591dc682613445f666f9460bab283af4d13ee4f7a9e3e47c27451707`

```dockerfile
```

-	Layers:
	-	`sha256:cc7c1950a5e5557483555eef92ae1c730a5df8239e11efd4015d579f2c48b149`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.4.1-cli`

```console
$ docker pull docker@sha256:2a9c1ba4816ddafdcf49a561201a9af2c451017e263a16a4fb1f878c454e1c44
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

### `docker:27.4.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:0d052bc5fcedc9b04935ffc5c1ca039c2c3f442c22dac9fab600f1e8348bc810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68471761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b387bcd9f4eb8854253fbd37d44ddd3a01ae6ed50d46fcf2371fbd0a72bf874e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b98de49fe1ed993db53e09ac1d349e04edc68f3a669a0166fe861e63f21139`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 8.1 MB (8060708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af95ea946dd1ea6ddb09d4d16636c6dbdaf31f2a92f21fccf332f412f91978b`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313c9b4ec4148bbc92f321352088134bd5c79313a32b0346277392e67f81276a`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 18.7 MB (18669944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7c930da0eae6c203479c2208bc111980211a355e5ebe1d8b9d771bd3b3f5a2`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 18.8 MB (18798867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0028ab84266b23892e8257b849272b905514e4111ccc878a47fc9e050d94e`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf34514361d460f057db2b94643dcc0fa3771b2df3b514bcc118a203a10c95ba`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003372bc0a71b5fee80b7721b00c600392a2d1297a7bdc1382c4fe9b7a3c478`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654c3b9f6f86104ad7ac2a1861a8a6a3c9624bdb262e0024f0daee392ebdc1d`  
		Last Modified: Thu, 19 Dec 2024 06:27:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:25b71b84216a6b6fa15b2e5d77e03b34e15d770a4e7bd0d5a12dc5a94e712a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32b3f66abca23fa334f7a356d599e2b285535319198c82ba778c5ae1d68c0d1`

```dockerfile
```

-	Layers:
	-	`sha256:e4b152243122d2a2b2ba6915e1be8a0003ac4d08efd17fcdf8208957caf3a8cb`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:2e6d722b4ad5fe9d873cddaf4f60fc20dcb740a401df852ba406b3068398b7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63605712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3487d4e2b40727fa327f1bc3ac2976f9c228483c0f71198a14759f48b37a693`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:148e72cbc3a4643c87b410580b6ae972ceafb99447e0d85bef2dd888ed7916d9`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 16.7 MB (16706481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfe37eaf11de403418a16f112ea736966145c615c0468af955274ca2d468276`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 17.4 MB (17448788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f071b9292f7441268ea76098e71b9dff0a1ec9f8311e4de77c6cd5af2c52a65`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 18.1 MB (18106565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a4fe84fb2fdef0c93d4c522edb4470e1d3558b04db73d6dc740cca4f2d3da6`  
		Last Modified: Thu, 19 Dec 2024 06:27:55 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa58f5b177c2d4b9d8d25bce148cba72f6b2db6ae71652dce2a49d1b4ecd88e`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755888e89afeff341e55361b436c6b35c8e67e7e05993e006c02d845c09320c3`  
		Last Modified: Thu, 19 Dec 2024 06:27:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:ff1cbb618b403ea74aa5eaef6d1ce343a27b799a14e73accc6d45186a8183c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ef782c195058519b295e8b5f7623848187120a6c037d0c852bc65400041fb6`

```dockerfile
```

-	Layers:
	-	`sha256:d4a3b6f2edb30ef6c175dc855c3cac8939a2acc6acf24bdba215d5e4bf9af607`  
		Last Modified: Thu, 19 Dec 2024 06:27:55 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:f89c36bd6f08a78078044ca2606b40abfd6e2bee5c34d5d0a227e545e70b31f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62625475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0973c3f1d70b0f02dd2301a26effa977c42a8930649cb0bb1dba2cad5abba685`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7384c11421040c34c2db4c9cbdff405dc1cb373620affa19cef0e6cd7889776b`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 16.7 MB (16694610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07bb9d6b4efc8e73c712cd756cad4ebdc7e4cd974f3b61319673b399cff7696`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 17.4 MB (17427589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e028074a72228d620c07c0306033af62a3bc33ecdbfdd182451a3940dbb3c47d`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 18.1 MB (18092645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b53f0105da3d54066118dde45e2db91fb53e54796d793199cb4d2ab602e9e2`  
		Last Modified: Thu, 19 Dec 2024 06:27:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6833631438bdcae5d6656508822939365cfd74de741e43abe8301361021b317`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b86ced47599bbfc27aa7dc389fb9cb257d493873490cc411bd8d27bdbf33bf`  
		Last Modified: Thu, 19 Dec 2024 06:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:82ae1c7b8fe94fdc49f39f3eec184d02572b400c4a225d2c5bc3a811850bbcb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394c76df731da9a4b7d8ffb5fc4820c5cabe9516f2202a945000d67de063966a`

```dockerfile
```

-	Layers:
	-	`sha256:4eac62d6a3079b4b3118e6b704cd97ad9ecd8ff718b1097e1cb02a713120697f`  
		Last Modified: Thu, 19 Dec 2024 06:27:30 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8e85a9901bc8d85c147f51091bc0a91ad62559db69480b088d838f5b52cdf542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64441149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b503fae5efdeebe409c4458ec85ccbe53f3abf5c2833f311ee7720d7a0b1bd60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc8b2386f26a19ff7e378d0b71a659c1c6185ff0418ab0ba70f91c9d7564766`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 8.1 MB (8077202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb804615f812dd41590a2167ce26fcd2bc94e936ef063d6ad5d47716653c51e`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500337a2754d23cb29983332f91f13bafcc80a7c299b977b077090a0fdf6e5a9`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.6 MB (17619412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821da57d87be4b4be2263810265c5fdfbee2a0815f9ba40aab6a34d602dbf10f`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.1 MB (17106449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a3e8ce8d46be94b3c36743d7add34488c85986d7d67dc65e6b0024b4f9629`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 17.6 MB (17642746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9727d9b709f029f03a062308481e155e1e44a388f1c90336ea9e6e9c98f4bf02`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5132ed17107a2140233d234c98fe9ff02ed459ac10f5b4ed2256ac52caff0ba2`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c450deeac7bd4e43a7a23a0608a88019260374cee39dc6371807295ef79a48`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:5a1c761171de4faf5bbd2753ce69aedb70bf0172682167323093305a9172bf8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d8489705c0a7ad5281a14fa0580dfe1e84ac35e8ed32f1e4746b551b3ec27d`

```dockerfile
```

-	Layers:
	-	`sha256:34348583b40c1f2b4ae040bdaa91a20e47adaa05541d9cafe8e43557dc582b3a`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.4.1-cli-alpine3.21`

```console
$ docker pull docker@sha256:2a9c1ba4816ddafdcf49a561201a9af2c451017e263a16a4fb1f878c454e1c44
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

### `docker:27.4.1-cli-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:0d052bc5fcedc9b04935ffc5c1ca039c2c3f442c22dac9fab600f1e8348bc810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68471761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b387bcd9f4eb8854253fbd37d44ddd3a01ae6ed50d46fcf2371fbd0a72bf874e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b98de49fe1ed993db53e09ac1d349e04edc68f3a669a0166fe861e63f21139`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 8.1 MB (8060708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af95ea946dd1ea6ddb09d4d16636c6dbdaf31f2a92f21fccf332f412f91978b`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313c9b4ec4148bbc92f321352088134bd5c79313a32b0346277392e67f81276a`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 18.7 MB (18669944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7c930da0eae6c203479c2208bc111980211a355e5ebe1d8b9d771bd3b3f5a2`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 18.8 MB (18798867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0028ab84266b23892e8257b849272b905514e4111ccc878a47fc9e050d94e`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf34514361d460f057db2b94643dcc0fa3771b2df3b514bcc118a203a10c95ba`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003372bc0a71b5fee80b7721b00c600392a2d1297a7bdc1382c4fe9b7a3c478`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654c3b9f6f86104ad7ac2a1861a8a6a3c9624bdb262e0024f0daee392ebdc1d`  
		Last Modified: Thu, 19 Dec 2024 06:27:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:25b71b84216a6b6fa15b2e5d77e03b34e15d770a4e7bd0d5a12dc5a94e712a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32b3f66abca23fa334f7a356d599e2b285535319198c82ba778c5ae1d68c0d1`

```dockerfile
```

-	Layers:
	-	`sha256:e4b152243122d2a2b2ba6915e1be8a0003ac4d08efd17fcdf8208957caf3a8cb`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4.1-cli-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:2e6d722b4ad5fe9d873cddaf4f60fc20dcb740a401df852ba406b3068398b7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63605712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3487d4e2b40727fa327f1bc3ac2976f9c228483c0f71198a14759f48b37a693`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:148e72cbc3a4643c87b410580b6ae972ceafb99447e0d85bef2dd888ed7916d9`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 16.7 MB (16706481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfe37eaf11de403418a16f112ea736966145c615c0468af955274ca2d468276`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 17.4 MB (17448788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f071b9292f7441268ea76098e71b9dff0a1ec9f8311e4de77c6cd5af2c52a65`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 18.1 MB (18106565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a4fe84fb2fdef0c93d4c522edb4470e1d3558b04db73d6dc740cca4f2d3da6`  
		Last Modified: Thu, 19 Dec 2024 06:27:55 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa58f5b177c2d4b9d8d25bce148cba72f6b2db6ae71652dce2a49d1b4ecd88e`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755888e89afeff341e55361b436c6b35c8e67e7e05993e006c02d845c09320c3`  
		Last Modified: Thu, 19 Dec 2024 06:27:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:ff1cbb618b403ea74aa5eaef6d1ce343a27b799a14e73accc6d45186a8183c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ef782c195058519b295e8b5f7623848187120a6c037d0c852bc65400041fb6`

```dockerfile
```

-	Layers:
	-	`sha256:d4a3b6f2edb30ef6c175dc855c3cac8939a2acc6acf24bdba215d5e4bf9af607`  
		Last Modified: Thu, 19 Dec 2024 06:27:55 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4.1-cli-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:f89c36bd6f08a78078044ca2606b40abfd6e2bee5c34d5d0a227e545e70b31f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62625475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0973c3f1d70b0f02dd2301a26effa977c42a8930649cb0bb1dba2cad5abba685`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7384c11421040c34c2db4c9cbdff405dc1cb373620affa19cef0e6cd7889776b`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 16.7 MB (16694610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07bb9d6b4efc8e73c712cd756cad4ebdc7e4cd974f3b61319673b399cff7696`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 17.4 MB (17427589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e028074a72228d620c07c0306033af62a3bc33ecdbfdd182451a3940dbb3c47d`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 18.1 MB (18092645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b53f0105da3d54066118dde45e2db91fb53e54796d793199cb4d2ab602e9e2`  
		Last Modified: Thu, 19 Dec 2024 06:27:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6833631438bdcae5d6656508822939365cfd74de741e43abe8301361021b317`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b86ced47599bbfc27aa7dc389fb9cb257d493873490cc411bd8d27bdbf33bf`  
		Last Modified: Thu, 19 Dec 2024 06:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:82ae1c7b8fe94fdc49f39f3eec184d02572b400c4a225d2c5bc3a811850bbcb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394c76df731da9a4b7d8ffb5fc4820c5cabe9516f2202a945000d67de063966a`

```dockerfile
```

-	Layers:
	-	`sha256:4eac62d6a3079b4b3118e6b704cd97ad9ecd8ff718b1097e1cb02a713120697f`  
		Last Modified: Thu, 19 Dec 2024 06:27:30 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4.1-cli-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8e85a9901bc8d85c147f51091bc0a91ad62559db69480b088d838f5b52cdf542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64441149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b503fae5efdeebe409c4458ec85ccbe53f3abf5c2833f311ee7720d7a0b1bd60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc8b2386f26a19ff7e378d0b71a659c1c6185ff0418ab0ba70f91c9d7564766`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 8.1 MB (8077202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb804615f812dd41590a2167ce26fcd2bc94e936ef063d6ad5d47716653c51e`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500337a2754d23cb29983332f91f13bafcc80a7c299b977b077090a0fdf6e5a9`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.6 MB (17619412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821da57d87be4b4be2263810265c5fdfbee2a0815f9ba40aab6a34d602dbf10f`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.1 MB (17106449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a3e8ce8d46be94b3c36743d7add34488c85986d7d67dc65e6b0024b4f9629`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 17.6 MB (17642746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9727d9b709f029f03a062308481e155e1e44a388f1c90336ea9e6e9c98f4bf02`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5132ed17107a2140233d234c98fe9ff02ed459ac10f5b4ed2256ac52caff0ba2`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c450deeac7bd4e43a7a23a0608a88019260374cee39dc6371807295ef79a48`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:5a1c761171de4faf5bbd2753ce69aedb70bf0172682167323093305a9172bf8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d8489705c0a7ad5281a14fa0580dfe1e84ac35e8ed32f1e4746b551b3ec27d`

```dockerfile
```

-	Layers:
	-	`sha256:34348583b40c1f2b4ae040bdaa91a20e47adaa05541d9cafe8e43557dc582b3a`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.4.1-dind`

```console
$ docker pull docker@sha256:d33ffba5909705d375ef1a99bb69fe6e21d80482134283226b119acf18bb08b4
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

### `docker:27.4.1-dind` - linux; amd64

```console
$ docker pull docker@sha256:197a4c5f8ffb8e4940e2518b1863588839743d062576c9d144a91fc64400c25b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133448845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c9711c027ed5c0c1bc82bf858e1a428676cd76681a56c53068db5510594f55`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b98de49fe1ed993db53e09ac1d349e04edc68f3a669a0166fe861e63f21139`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 8.1 MB (8060708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af95ea946dd1ea6ddb09d4d16636c6dbdaf31f2a92f21fccf332f412f91978b`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313c9b4ec4148bbc92f321352088134bd5c79313a32b0346277392e67f81276a`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 18.7 MB (18669944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7c930da0eae6c203479c2208bc111980211a355e5ebe1d8b9d771bd3b3f5a2`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 18.8 MB (18798867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0028ab84266b23892e8257b849272b905514e4111ccc878a47fc9e050d94e`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf34514361d460f057db2b94643dcc0fa3771b2df3b514bcc118a203a10c95ba`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003372bc0a71b5fee80b7721b00c600392a2d1297a7bdc1382c4fe9b7a3c478`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654c3b9f6f86104ad7ac2a1861a8a6a3c9624bdb262e0024f0daee392ebdc1d`  
		Last Modified: Thu, 19 Dec 2024 06:27:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccacb1ec449ea2d8be4c5f1323c8f8f438ca6cbadb852569e5a1d30b2fccfb0`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 6.7 MB (6733442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db08b2b56d721154b01a601fafbf1388da92317b2a6fd84636403d145397cab`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 89.5 KB (89464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf58bc5c124acd8cd7867de0e5bfe811139bb7efbdfb4d3f384f5047368feadb`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed661c2bc3605af63c34b0e0e6b44c343cfaaeaeff5a9c5a1e90636c29b3c3`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 58.1 MB (58148385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd93031177fed6768ebac95908f7214e148aec625cde4db347278f785e7061f`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4580133da14d68ef765c552929a21bcefda14fd6f6d46ecd79ba394349848a`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4d1ebca4fc352915e574abaa96ff6ed6588607144b48d49638664664171da1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785a52cc7646ffa85e15d5ffe60aac7f0f1a2d5253c2b101b6f346064092b53f`

```dockerfile
```

-	Layers:
	-	`sha256:57153e86db239ac28d0ccf1ea7c7b4f48b51df48813df21eab3ef9fec0624f79`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4.1-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:8e53f8a2914c30d65228120667a050c54a74382d87f8e8205383be62560c9f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124579368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cc11a65e103a89e82e0f00f3eaea3ee929960b8b89fbf699a59f2bd46a109d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:148e72cbc3a4643c87b410580b6ae972ceafb99447e0d85bef2dd888ed7916d9`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 16.7 MB (16706481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfe37eaf11de403418a16f112ea736966145c615c0468af955274ca2d468276`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 17.4 MB (17448788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f071b9292f7441268ea76098e71b9dff0a1ec9f8311e4de77c6cd5af2c52a65`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 18.1 MB (18106565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a4fe84fb2fdef0c93d4c522edb4470e1d3558b04db73d6dc740cca4f2d3da6`  
		Last Modified: Thu, 19 Dec 2024 06:27:55 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa58f5b177c2d4b9d8d25bce148cba72f6b2db6ae71652dce2a49d1b4ecd88e`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755888e89afeff341e55361b436c6b35c8e67e7e05993e006c02d845c09320c3`  
		Last Modified: Thu, 19 Dec 2024 06:27:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ef02b0ebd56b76a25032f347f442a87fd532e2f07932b029c5a5ed2863ebdf`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 7.0 MB (7041137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa00a89210cf6cc619d32ecde33bcc417a048e4089420d3376e126502a34e868`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 89.1 KB (89114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314e6fc0bd408cd71d4f12dc2b30c175f02d576782580764a4d18dbe9397962a`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d2a39a9ca8dfcdf48360a081c2bacbd295c376b777d17ab83e02ace23e3d98`  
		Last Modified: Thu, 19 Dec 2024 07:08:09 GMT  
		Size: 53.8 MB (53837606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000fe248e69901663cba49cff877d5d4494f61261374eebd3e76654fdb4a9bb`  
		Last Modified: Thu, 19 Dec 2024 07:07:40 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e0a412273d2de4a63cf252e2955333edbb0387dab642897062720249f4180`  
		Last Modified: Thu, 19 Dec 2024 07:07:40 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:fbb76334b758da06115ce3db141b3a8d0384cf0fdfe0f1ae084cf566558cde04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05008ccd944add8210466657f1c49a19e043efce63da526e66de9aebb4b80ef`

```dockerfile
```

-	Layers:
	-	`sha256:d0c1d9bc2a056393fa0f5f33e177e88c39f2ff3b3ecab57b5172ba3064dfd763`  
		Last Modified: Thu, 19 Dec 2024 07:07:38 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4.1-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:42fe1f55c44d24a6c3dabf704278f5beef25d390ca4c15966d714fb6e7908b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122921457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9248a004d8a619e67677191683cde42174b0b6a6f031c1bff04422a56ab7fafa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7384c11421040c34c2db4c9cbdff405dc1cb373620affa19cef0e6cd7889776b`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 16.7 MB (16694610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07bb9d6b4efc8e73c712cd756cad4ebdc7e4cd974f3b61319673b399cff7696`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 17.4 MB (17427589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e028074a72228d620c07c0306033af62a3bc33ecdbfdd182451a3940dbb3c47d`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 18.1 MB (18092645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b53f0105da3d54066118dde45e2db91fb53e54796d793199cb4d2ab602e9e2`  
		Last Modified: Thu, 19 Dec 2024 06:27:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6833631438bdcae5d6656508822939365cfd74de741e43abe8301361021b317`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b86ced47599bbfc27aa7dc389fb9cb257d493873490cc411bd8d27bdbf33bf`  
		Last Modified: Thu, 19 Dec 2024 06:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3cfec5adb0a4b5698f388de77eec77ddfae962de5b040d830dd95fded5c623`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 6.4 MB (6367338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f665ffa7443f60c8c9314082dba5723e72ede3f3451817173783b2ff36ffcb3`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 85.3 KB (85264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f8f3552eba49a36113015c2b82fecdb0cc6496614371b415212e14847dc60`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f31fefce9d3a0d0f1c7eb75b6cbde54e15ec723205ceea52b7da59ab4fb0dc`  
		Last Modified: Thu, 19 Dec 2024 07:07:45 GMT  
		Size: 53.8 MB (53837588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2522c47823d994b730d265c55af844c265eae9c9556e8e2200a9a35b9ac91a7`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06aa58a0bf71133cf40669589cd7fee930c7c0be06f93c2ff27147fd89bb1169`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:17996dd91287a758efee2344a070f6699509883f0d901af5ab238e9b387229bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b073ab412e1ae045cda1a9e0d874b37c17d7a32b94ca5af476daa61f0ae58438`

```dockerfile
```

-	Layers:
	-	`sha256:a559ea4afc9f0276e8285aa1e894d114568f8fc93aded28f64880c5b07631b25`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c4618ee87c867fff3b390aab9eeb59d889e39a14fb3bfbf40560f7faf78f841b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125264161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a74c04d0ac72b0d4df5a0d63124bff4cce8b81fe2f6d669d6272b5c426ef00e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc8b2386f26a19ff7e378d0b71a659c1c6185ff0418ab0ba70f91c9d7564766`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 8.1 MB (8077202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb804615f812dd41590a2167ce26fcd2bc94e936ef063d6ad5d47716653c51e`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500337a2754d23cb29983332f91f13bafcc80a7c299b977b077090a0fdf6e5a9`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.6 MB (17619412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821da57d87be4b4be2263810265c5fdfbee2a0815f9ba40aab6a34d602dbf10f`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.1 MB (17106449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a3e8ce8d46be94b3c36743d7add34488c85986d7d67dc65e6b0024b4f9629`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 17.6 MB (17642746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9727d9b709f029f03a062308481e155e1e44a388f1c90336ea9e6e9c98f4bf02`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5132ed17107a2140233d234c98fe9ff02ed459ac10f5b4ed2256ac52caff0ba2`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c450deeac7bd4e43a7a23a0608a88019260374cee39dc6371807295ef79a48`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95254613e12389bf1f1f60f9b295f28cef95138ce1dbc50738110a66f798909e`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 7.0 MB (6982148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3b84891c5b5b5525368fd009a3faa7c2ce7964cb220ec38caec428b7a4e023`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 97.8 KB (97810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f85e673a5bfddb9b35bc2893ca0b6dce01582d542e954e1f8522a5dc5bb96fc`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e62d3dc2daa4a6f98b762917d7f0adea4d641834acf4f0f8a44e1d79d577ab7`  
		Last Modified: Thu, 19 Dec 2024 07:07:59 GMT  
		Size: 53.7 MB (53737262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a6c5cd3176c0cc42a77bceba546446aac5d823c9f2fe97ef71fa20cc12bea4`  
		Last Modified: Thu, 19 Dec 2024 07:07:58 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01edfa8f426bf8debb954258fd0e37e36488fa9ba98d3d941a5b763aec91984f`  
		Last Modified: Thu, 19 Dec 2024 07:07:58 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b944da17175c77080cb8774711d10f0b88e7b131c7036b9ad130642f29955bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754b5f14591dc682613445f666f9460bab283af4d13ee4f7a9e3e47c27451707`

```dockerfile
```

-	Layers:
	-	`sha256:cc7c1950a5e5557483555eef92ae1c730a5df8239e11efd4015d579f2c48b149`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.4.1-dind-alpine3.21`

```console
$ docker pull docker@sha256:d33ffba5909705d375ef1a99bb69fe6e21d80482134283226b119acf18bb08b4
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

### `docker:27.4.1-dind-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:197a4c5f8ffb8e4940e2518b1863588839743d062576c9d144a91fc64400c25b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133448845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c9711c027ed5c0c1bc82bf858e1a428676cd76681a56c53068db5510594f55`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b98de49fe1ed993db53e09ac1d349e04edc68f3a669a0166fe861e63f21139`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 8.1 MB (8060708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af95ea946dd1ea6ddb09d4d16636c6dbdaf31f2a92f21fccf332f412f91978b`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313c9b4ec4148bbc92f321352088134bd5c79313a32b0346277392e67f81276a`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 18.7 MB (18669944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7c930da0eae6c203479c2208bc111980211a355e5ebe1d8b9d771bd3b3f5a2`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 18.8 MB (18798867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0028ab84266b23892e8257b849272b905514e4111ccc878a47fc9e050d94e`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf34514361d460f057db2b94643dcc0fa3771b2df3b514bcc118a203a10c95ba`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003372bc0a71b5fee80b7721b00c600392a2d1297a7bdc1382c4fe9b7a3c478`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654c3b9f6f86104ad7ac2a1861a8a6a3c9624bdb262e0024f0daee392ebdc1d`  
		Last Modified: Thu, 19 Dec 2024 06:27:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccacb1ec449ea2d8be4c5f1323c8f8f438ca6cbadb852569e5a1d30b2fccfb0`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 6.7 MB (6733442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db08b2b56d721154b01a601fafbf1388da92317b2a6fd84636403d145397cab`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 89.5 KB (89464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf58bc5c124acd8cd7867de0e5bfe811139bb7efbdfb4d3f384f5047368feadb`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed661c2bc3605af63c34b0e0e6b44c343cfaaeaeff5a9c5a1e90636c29b3c3`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 58.1 MB (58148385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd93031177fed6768ebac95908f7214e148aec625cde4db347278f785e7061f`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4580133da14d68ef765c552929a21bcefda14fd6f6d46ecd79ba394349848a`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:4d1ebca4fc352915e574abaa96ff6ed6588607144b48d49638664664171da1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785a52cc7646ffa85e15d5ffe60aac7f0f1a2d5253c2b101b6f346064092b53f`

```dockerfile
```

-	Layers:
	-	`sha256:57153e86db239ac28d0ccf1ea7c7b4f48b51df48813df21eab3ef9fec0624f79`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4.1-dind-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:8e53f8a2914c30d65228120667a050c54a74382d87f8e8205383be62560c9f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124579368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cc11a65e103a89e82e0f00f3eaea3ee929960b8b89fbf699a59f2bd46a109d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:148e72cbc3a4643c87b410580b6ae972ceafb99447e0d85bef2dd888ed7916d9`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 16.7 MB (16706481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfe37eaf11de403418a16f112ea736966145c615c0468af955274ca2d468276`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 17.4 MB (17448788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f071b9292f7441268ea76098e71b9dff0a1ec9f8311e4de77c6cd5af2c52a65`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 18.1 MB (18106565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a4fe84fb2fdef0c93d4c522edb4470e1d3558b04db73d6dc740cca4f2d3da6`  
		Last Modified: Thu, 19 Dec 2024 06:27:55 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa58f5b177c2d4b9d8d25bce148cba72f6b2db6ae71652dce2a49d1b4ecd88e`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755888e89afeff341e55361b436c6b35c8e67e7e05993e006c02d845c09320c3`  
		Last Modified: Thu, 19 Dec 2024 06:27:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ef02b0ebd56b76a25032f347f442a87fd532e2f07932b029c5a5ed2863ebdf`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 7.0 MB (7041137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa00a89210cf6cc619d32ecde33bcc417a048e4089420d3376e126502a34e868`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 89.1 KB (89114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314e6fc0bd408cd71d4f12dc2b30c175f02d576782580764a4d18dbe9397962a`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d2a39a9ca8dfcdf48360a081c2bacbd295c376b777d17ab83e02ace23e3d98`  
		Last Modified: Thu, 19 Dec 2024 07:08:09 GMT  
		Size: 53.8 MB (53837606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000fe248e69901663cba49cff877d5d4494f61261374eebd3e76654fdb4a9bb`  
		Last Modified: Thu, 19 Dec 2024 07:07:40 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e0a412273d2de4a63cf252e2955333edbb0387dab642897062720249f4180`  
		Last Modified: Thu, 19 Dec 2024 07:07:40 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:fbb76334b758da06115ce3db141b3a8d0384cf0fdfe0f1ae084cf566558cde04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05008ccd944add8210466657f1c49a19e043efce63da526e66de9aebb4b80ef`

```dockerfile
```

-	Layers:
	-	`sha256:d0c1d9bc2a056393fa0f5f33e177e88c39f2ff3b3ecab57b5172ba3064dfd763`  
		Last Modified: Thu, 19 Dec 2024 07:07:38 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4.1-dind-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:42fe1f55c44d24a6c3dabf704278f5beef25d390ca4c15966d714fb6e7908b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122921457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9248a004d8a619e67677191683cde42174b0b6a6f031c1bff04422a56ab7fafa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7384c11421040c34c2db4c9cbdff405dc1cb373620affa19cef0e6cd7889776b`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 16.7 MB (16694610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07bb9d6b4efc8e73c712cd756cad4ebdc7e4cd974f3b61319673b399cff7696`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 17.4 MB (17427589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e028074a72228d620c07c0306033af62a3bc33ecdbfdd182451a3940dbb3c47d`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 18.1 MB (18092645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b53f0105da3d54066118dde45e2db91fb53e54796d793199cb4d2ab602e9e2`  
		Last Modified: Thu, 19 Dec 2024 06:27:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6833631438bdcae5d6656508822939365cfd74de741e43abe8301361021b317`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b86ced47599bbfc27aa7dc389fb9cb257d493873490cc411bd8d27bdbf33bf`  
		Last Modified: Thu, 19 Dec 2024 06:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3cfec5adb0a4b5698f388de77eec77ddfae962de5b040d830dd95fded5c623`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 6.4 MB (6367338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f665ffa7443f60c8c9314082dba5723e72ede3f3451817173783b2ff36ffcb3`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 85.3 KB (85264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f8f3552eba49a36113015c2b82fecdb0cc6496614371b415212e14847dc60`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f31fefce9d3a0d0f1c7eb75b6cbde54e15ec723205ceea52b7da59ab4fb0dc`  
		Last Modified: Thu, 19 Dec 2024 07:07:45 GMT  
		Size: 53.8 MB (53837588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2522c47823d994b730d265c55af844c265eae9c9556e8e2200a9a35b9ac91a7`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06aa58a0bf71133cf40669589cd7fee930c7c0be06f93c2ff27147fd89bb1169`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:17996dd91287a758efee2344a070f6699509883f0d901af5ab238e9b387229bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b073ab412e1ae045cda1a9e0d874b37c17d7a32b94ca5af476daa61f0ae58438`

```dockerfile
```

-	Layers:
	-	`sha256:a559ea4afc9f0276e8285aa1e894d114568f8fc93aded28f64880c5b07631b25`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.4.1-dind-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c4618ee87c867fff3b390aab9eeb59d889e39a14fb3bfbf40560f7faf78f841b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125264161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a74c04d0ac72b0d4df5a0d63124bff4cce8b81fe2f6d669d6272b5c426ef00e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc8b2386f26a19ff7e378d0b71a659c1c6185ff0418ab0ba70f91c9d7564766`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 8.1 MB (8077202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb804615f812dd41590a2167ce26fcd2bc94e936ef063d6ad5d47716653c51e`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500337a2754d23cb29983332f91f13bafcc80a7c299b977b077090a0fdf6e5a9`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.6 MB (17619412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821da57d87be4b4be2263810265c5fdfbee2a0815f9ba40aab6a34d602dbf10f`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.1 MB (17106449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a3e8ce8d46be94b3c36743d7add34488c85986d7d67dc65e6b0024b4f9629`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 17.6 MB (17642746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9727d9b709f029f03a062308481e155e1e44a388f1c90336ea9e6e9c98f4bf02`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5132ed17107a2140233d234c98fe9ff02ed459ac10f5b4ed2256ac52caff0ba2`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c450deeac7bd4e43a7a23a0608a88019260374cee39dc6371807295ef79a48`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95254613e12389bf1f1f60f9b295f28cef95138ce1dbc50738110a66f798909e`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 7.0 MB (6982148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3b84891c5b5b5525368fd009a3faa7c2ce7964cb220ec38caec428b7a4e023`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 97.8 KB (97810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f85e673a5bfddb9b35bc2893ca0b6dce01582d542e954e1f8522a5dc5bb96fc`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e62d3dc2daa4a6f98b762917d7f0adea4d641834acf4f0f8a44e1d79d577ab7`  
		Last Modified: Thu, 19 Dec 2024 07:07:59 GMT  
		Size: 53.7 MB (53737262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a6c5cd3176c0cc42a77bceba546446aac5d823c9f2fe97ef71fa20cc12bea4`  
		Last Modified: Thu, 19 Dec 2024 07:07:58 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01edfa8f426bf8debb954258fd0e37e36488fa9ba98d3d941a5b763aec91984f`  
		Last Modified: Thu, 19 Dec 2024 07:07:58 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.4.1-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:b944da17175c77080cb8774711d10f0b88e7b131c7036b9ad130642f29955bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754b5f14591dc682613445f666f9460bab283af4d13ee4f7a9e3e47c27451707`

```dockerfile
```

-	Layers:
	-	`sha256:cc7c1950a5e5557483555eef92ae1c730a5df8239e11efd4015d579f2c48b149`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.4.1-dind-rootless`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:27.4.1-windowsservercore`

```console
$ docker pull docker@sha256:ce26a4b6892bb5fff408af70028fd1f7aadf1ba1817049f7c36d386b938f2a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `docker:27.4.1-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:b59b50eddc96fa024759736642b20d31e812c747839aa0e04e6b3cd306d9c08f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312956798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dac0ff62690131e5cbadefa8b3173ce78f2fedeb1bedfb9599c99488be059a9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Thu, 19 Dec 2024 06:27:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Dec 2024 06:28:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Dec 2024 06:28:35 GMT
ENV DOCKER_VERSION=27.4.1
# Thu, 19 Dec 2024 06:28:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.1.zip
# Thu, 19 Dec 2024 06:28:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:28:58 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 19 Dec 2024 06:28:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 19 Dec 2024 06:28:59 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 19 Dec 2024 06:29:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Thu, 19 Dec 2024 06:29:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-windows-x86_64.exe
# Thu, 19 Dec 2024 06:29:12 GMT
ENV DOCKER_COMPOSE_SHA256=5dc7ac86e8d3972c2c68066c6ac370daf0a42b7c8d3338336c9dbde34af06213
# Thu, 19 Dec 2024 06:29:24 GMT
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
	-	`sha256:c2d7502a1bbe13300d252a2f9df8e505261a1640bc1bd25b0948e9c00fcc5b01`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c5b28592218521960824b8276896946f244fbb3651810d08c43452a2582cb`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 357.3 KB (357322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6330b409518a6d4ccfc671760fb4c29c3aa61745511abc8406e7598afdeb72f4`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff2da6ec5d910a6c45c3b7bc2ada4de7ee595addaae450cfea2ba3fba3571f0`  
		Last Modified: Thu, 19 Dec 2024 06:29:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981fcf2dca12be8aa09825096e39af48ab18642d75e6e2791014b5511999719c`  
		Last Modified: Thu, 19 Dec 2024 06:29:30 GMT  
		Size: 19.0 MB (18965788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559ffe22c82820dbe4c523868249c3f6a55385142d2e0ead71e852d8a7251d56`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458e70a57b4ce24dfc2a913ab05c3222397fe2e8a5d93868622a5da7a9340e81`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dd3b199caac21501453ed73a1b07e07e8909c492da3b0c12264e12be24f8f7`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffced5034da239bcce196f61166f31fa32a1046a0b90925f73df0a56a4540555`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 19.6 MB (19615775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d1d24e414a381ae30c27fae03be0f84206adbad1d9b6b30407bfecceb5e1e5`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deeb14568d7a7f723c99e08a5b860258c0e121c9b475c7f14d316ac30cb06d68`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a34da183fbb7bde6f718a61627a8077978264175188a7e437d8f791c46033e`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdb77e5d84cc05ce04533280006424bb2742fe825cfe58eb5f5934b7a430dcf`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 20.1 MB (20132656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.4.1-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:c442ec204cc8c3af89a231557d7113d731304aa9004ecc2fd2b7fdea9a2a5ed5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073460288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd24b1732cd2a56ef18bd248405211562b17b3b25cc385edc36040b8cea00146`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Thu, 19 Dec 2024 06:27:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Dec 2024 06:28:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Dec 2024 06:28:36 GMT
ENV DOCKER_VERSION=27.4.1
# Thu, 19 Dec 2024 06:28:37 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.1.zip
# Thu, 19 Dec 2024 06:29:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:00 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 19 Dec 2024 06:29:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 19 Dec 2024 06:29:01 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 19 Dec 2024 06:29:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Thu, 19 Dec 2024 06:29:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-windows-x86_64.exe
# Thu, 19 Dec 2024 06:29:16 GMT
ENV DOCKER_COMPOSE_SHA256=5dc7ac86e8d3972c2c68066c6ac370daf0a42b7c8d3338336c9dbde34af06213
# Thu, 19 Dec 2024 06:29:30 GMT
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
	-	`sha256:e1cfd0430e259e32b94429bf581ea5f74b25080ea9e68899e17062c55bfdba4f`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089d2b012e4350683f7592078e0330072d47face607cfdcfa1b177015a1d055d`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 475.3 KB (475261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e54e6e8f743b8e62247f614caa153507aeea30e39ec7d133b120770472d150d`  
		Last Modified: Thu, 19 Dec 2024 06:29:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c46ebe5f7bc661958c2410ed2a60431be6d40269618a1223f8bc2c1f5392c26`  
		Last Modified: Thu, 19 Dec 2024 06:29:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac2d753848f2b9292c76be0e8c43f38d7c04ed25979be15179b781a3c2b47b9`  
		Last Modified: Thu, 19 Dec 2024 06:29:36 GMT  
		Size: 19.0 MB (18997863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4c651853f033dafb87a17fdd7690c1c3c3a0f4dfb6e083cf06ba8d91234d98`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1a3389962e8b333bfcead93ec3aad31713a4bafd7b7be628b737077da7d60b`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e030ce22f45d6c461af01d11e768dcd4638cd9b989e6dc8aa7e384b7ccb80129`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d987b1383b6b76eb88c20a38bac7e305fe1f8c311242b83bc819be0eee3eb3`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 19.6 MB (19648080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e0d2a17e8fa800de7106ca7d9cce51ab9562558d2d155ddfaaa0d979138750`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d9b36807cefb176cc3c814de379c2bf6a17663ed8e0372f69d2cb06a02cd4e`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f2c79cb8ac15f188f4afd8366afee1f46ec780fa70082a4c9e991ac09c8537`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f72ede2a361313c0a7e7b059df25505b175cc277540b12cb48ee012d5a4ba93`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 20.2 MB (20157227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.4.1-windowsservercore-1809`

```console
$ docker pull docker@sha256:5a5cd9f42944d54ac3da3dfda65c1d0342f266339ac3fde581f7021a2aa3c54c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `docker:27.4.1-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:c442ec204cc8c3af89a231557d7113d731304aa9004ecc2fd2b7fdea9a2a5ed5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073460288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd24b1732cd2a56ef18bd248405211562b17b3b25cc385edc36040b8cea00146`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Thu, 19 Dec 2024 06:27:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Dec 2024 06:28:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Dec 2024 06:28:36 GMT
ENV DOCKER_VERSION=27.4.1
# Thu, 19 Dec 2024 06:28:37 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.1.zip
# Thu, 19 Dec 2024 06:29:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:00 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 19 Dec 2024 06:29:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 19 Dec 2024 06:29:01 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 19 Dec 2024 06:29:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Thu, 19 Dec 2024 06:29:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-windows-x86_64.exe
# Thu, 19 Dec 2024 06:29:16 GMT
ENV DOCKER_COMPOSE_SHA256=5dc7ac86e8d3972c2c68066c6ac370daf0a42b7c8d3338336c9dbde34af06213
# Thu, 19 Dec 2024 06:29:30 GMT
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
	-	`sha256:e1cfd0430e259e32b94429bf581ea5f74b25080ea9e68899e17062c55bfdba4f`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089d2b012e4350683f7592078e0330072d47face607cfdcfa1b177015a1d055d`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 475.3 KB (475261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e54e6e8f743b8e62247f614caa153507aeea30e39ec7d133b120770472d150d`  
		Last Modified: Thu, 19 Dec 2024 06:29:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c46ebe5f7bc661958c2410ed2a60431be6d40269618a1223f8bc2c1f5392c26`  
		Last Modified: Thu, 19 Dec 2024 06:29:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac2d753848f2b9292c76be0e8c43f38d7c04ed25979be15179b781a3c2b47b9`  
		Last Modified: Thu, 19 Dec 2024 06:29:36 GMT  
		Size: 19.0 MB (18997863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4c651853f033dafb87a17fdd7690c1c3c3a0f4dfb6e083cf06ba8d91234d98`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1a3389962e8b333bfcead93ec3aad31713a4bafd7b7be628b737077da7d60b`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e030ce22f45d6c461af01d11e768dcd4638cd9b989e6dc8aa7e384b7ccb80129`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d987b1383b6b76eb88c20a38bac7e305fe1f8c311242b83bc819be0eee3eb3`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 19.6 MB (19648080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e0d2a17e8fa800de7106ca7d9cce51ab9562558d2d155ddfaaa0d979138750`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d9b36807cefb176cc3c814de379c2bf6a17663ed8e0372f69d2cb06a02cd4e`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f2c79cb8ac15f188f4afd8366afee1f46ec780fa70082a4c9e991ac09c8537`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f72ede2a361313c0a7e7b059df25505b175cc277540b12cb48ee012d5a4ba93`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 20.2 MB (20157227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.4.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:bbaca47510bc3b68824fca9b3d27ac84ec15755c88e1ac61a53c6f93ace9c225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `docker:27.4.1-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:b59b50eddc96fa024759736642b20d31e812c747839aa0e04e6b3cd306d9c08f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312956798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dac0ff62690131e5cbadefa8b3173ce78f2fedeb1bedfb9599c99488be059a9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Thu, 19 Dec 2024 06:27:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Dec 2024 06:28:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Dec 2024 06:28:35 GMT
ENV DOCKER_VERSION=27.4.1
# Thu, 19 Dec 2024 06:28:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.1.zip
# Thu, 19 Dec 2024 06:28:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:28:58 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 19 Dec 2024 06:28:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 19 Dec 2024 06:28:59 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 19 Dec 2024 06:29:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Thu, 19 Dec 2024 06:29:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-windows-x86_64.exe
# Thu, 19 Dec 2024 06:29:12 GMT
ENV DOCKER_COMPOSE_SHA256=5dc7ac86e8d3972c2c68066c6ac370daf0a42b7c8d3338336c9dbde34af06213
# Thu, 19 Dec 2024 06:29:24 GMT
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
	-	`sha256:c2d7502a1bbe13300d252a2f9df8e505261a1640bc1bd25b0948e9c00fcc5b01`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c5b28592218521960824b8276896946f244fbb3651810d08c43452a2582cb`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 357.3 KB (357322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6330b409518a6d4ccfc671760fb4c29c3aa61745511abc8406e7598afdeb72f4`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff2da6ec5d910a6c45c3b7bc2ada4de7ee595addaae450cfea2ba3fba3571f0`  
		Last Modified: Thu, 19 Dec 2024 06:29:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981fcf2dca12be8aa09825096e39af48ab18642d75e6e2791014b5511999719c`  
		Last Modified: Thu, 19 Dec 2024 06:29:30 GMT  
		Size: 19.0 MB (18965788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559ffe22c82820dbe4c523868249c3f6a55385142d2e0ead71e852d8a7251d56`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458e70a57b4ce24dfc2a913ab05c3222397fe2e8a5d93868622a5da7a9340e81`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dd3b199caac21501453ed73a1b07e07e8909c492da3b0c12264e12be24f8f7`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffced5034da239bcce196f61166f31fa32a1046a0b90925f73df0a56a4540555`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 19.6 MB (19615775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d1d24e414a381ae30c27fae03be0f84206adbad1d9b6b30407bfecceb5e1e5`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deeb14568d7a7f723c99e08a5b860258c0e121c9b475c7f14d316ac30cb06d68`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a34da183fbb7bde6f718a61627a8077978264175188a7e437d8f791c46033e`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdb77e5d84cc05ce04533280006424bb2742fe825cfe58eb5f5934b7a430dcf`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 20.1 MB (20132656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:2a9c1ba4816ddafdcf49a561201a9af2c451017e263a16a4fb1f878c454e1c44
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
$ docker pull docker@sha256:0d052bc5fcedc9b04935ffc5c1ca039c2c3f442c22dac9fab600f1e8348bc810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68471761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b387bcd9f4eb8854253fbd37d44ddd3a01ae6ed50d46fcf2371fbd0a72bf874e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b98de49fe1ed993db53e09ac1d349e04edc68f3a669a0166fe861e63f21139`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 8.1 MB (8060708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af95ea946dd1ea6ddb09d4d16636c6dbdaf31f2a92f21fccf332f412f91978b`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313c9b4ec4148bbc92f321352088134bd5c79313a32b0346277392e67f81276a`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 18.7 MB (18669944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7c930da0eae6c203479c2208bc111980211a355e5ebe1d8b9d771bd3b3f5a2`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 18.8 MB (18798867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0028ab84266b23892e8257b849272b905514e4111ccc878a47fc9e050d94e`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf34514361d460f057db2b94643dcc0fa3771b2df3b514bcc118a203a10c95ba`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003372bc0a71b5fee80b7721b00c600392a2d1297a7bdc1382c4fe9b7a3c478`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654c3b9f6f86104ad7ac2a1861a8a6a3c9624bdb262e0024f0daee392ebdc1d`  
		Last Modified: Thu, 19 Dec 2024 06:27:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:25b71b84216a6b6fa15b2e5d77e03b34e15d770a4e7bd0d5a12dc5a94e712a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32b3f66abca23fa334f7a356d599e2b285535319198c82ba778c5ae1d68c0d1`

```dockerfile
```

-	Layers:
	-	`sha256:e4b152243122d2a2b2ba6915e1be8a0003ac4d08efd17fcdf8208957caf3a8cb`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:2e6d722b4ad5fe9d873cddaf4f60fc20dcb740a401df852ba406b3068398b7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63605712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3487d4e2b40727fa327f1bc3ac2976f9c228483c0f71198a14759f48b37a693`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:148e72cbc3a4643c87b410580b6ae972ceafb99447e0d85bef2dd888ed7916d9`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 16.7 MB (16706481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfe37eaf11de403418a16f112ea736966145c615c0468af955274ca2d468276`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 17.4 MB (17448788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f071b9292f7441268ea76098e71b9dff0a1ec9f8311e4de77c6cd5af2c52a65`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 18.1 MB (18106565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a4fe84fb2fdef0c93d4c522edb4470e1d3558b04db73d6dc740cca4f2d3da6`  
		Last Modified: Thu, 19 Dec 2024 06:27:55 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa58f5b177c2d4b9d8d25bce148cba72f6b2db6ae71652dce2a49d1b4ecd88e`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755888e89afeff341e55361b436c6b35c8e67e7e05993e006c02d845c09320c3`  
		Last Modified: Thu, 19 Dec 2024 06:27:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:ff1cbb618b403ea74aa5eaef6d1ce343a27b799a14e73accc6d45186a8183c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ef782c195058519b295e8b5f7623848187120a6c037d0c852bc65400041fb6`

```dockerfile
```

-	Layers:
	-	`sha256:d4a3b6f2edb30ef6c175dc855c3cac8939a2acc6acf24bdba215d5e4bf9af607`  
		Last Modified: Thu, 19 Dec 2024 06:27:55 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:f89c36bd6f08a78078044ca2606b40abfd6e2bee5c34d5d0a227e545e70b31f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62625475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0973c3f1d70b0f02dd2301a26effa977c42a8930649cb0bb1dba2cad5abba685`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7384c11421040c34c2db4c9cbdff405dc1cb373620affa19cef0e6cd7889776b`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 16.7 MB (16694610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07bb9d6b4efc8e73c712cd756cad4ebdc7e4cd974f3b61319673b399cff7696`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 17.4 MB (17427589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e028074a72228d620c07c0306033af62a3bc33ecdbfdd182451a3940dbb3c47d`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 18.1 MB (18092645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b53f0105da3d54066118dde45e2db91fb53e54796d793199cb4d2ab602e9e2`  
		Last Modified: Thu, 19 Dec 2024 06:27:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6833631438bdcae5d6656508822939365cfd74de741e43abe8301361021b317`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b86ced47599bbfc27aa7dc389fb9cb257d493873490cc411bd8d27bdbf33bf`  
		Last Modified: Thu, 19 Dec 2024 06:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:82ae1c7b8fe94fdc49f39f3eec184d02572b400c4a225d2c5bc3a811850bbcb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394c76df731da9a4b7d8ffb5fc4820c5cabe9516f2202a945000d67de063966a`

```dockerfile
```

-	Layers:
	-	`sha256:4eac62d6a3079b4b3118e6b704cd97ad9ecd8ff718b1097e1cb02a713120697f`  
		Last Modified: Thu, 19 Dec 2024 06:27:30 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8e85a9901bc8d85c147f51091bc0a91ad62559db69480b088d838f5b52cdf542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64441149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b503fae5efdeebe409c4458ec85ccbe53f3abf5c2833f311ee7720d7a0b1bd60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc8b2386f26a19ff7e378d0b71a659c1c6185ff0418ab0ba70f91c9d7564766`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 8.1 MB (8077202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb804615f812dd41590a2167ce26fcd2bc94e936ef063d6ad5d47716653c51e`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500337a2754d23cb29983332f91f13bafcc80a7c299b977b077090a0fdf6e5a9`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.6 MB (17619412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821da57d87be4b4be2263810265c5fdfbee2a0815f9ba40aab6a34d602dbf10f`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.1 MB (17106449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a3e8ce8d46be94b3c36743d7add34488c85986d7d67dc65e6b0024b4f9629`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 17.6 MB (17642746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9727d9b709f029f03a062308481e155e1e44a388f1c90336ea9e6e9c98f4bf02`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5132ed17107a2140233d234c98fe9ff02ed459ac10f5b4ed2256ac52caff0ba2`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c450deeac7bd4e43a7a23a0608a88019260374cee39dc6371807295ef79a48`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:5a1c761171de4faf5bbd2753ce69aedb70bf0172682167323093305a9172bf8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d8489705c0a7ad5281a14fa0580dfe1e84ac35e8ed32f1e4746b551b3ec27d`

```dockerfile
```

-	Layers:
	-	`sha256:34348583b40c1f2b4ae040bdaa91a20e47adaa05541d9cafe8e43557dc582b3a`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:d33ffba5909705d375ef1a99bb69fe6e21d80482134283226b119acf18bb08b4
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
$ docker pull docker@sha256:197a4c5f8ffb8e4940e2518b1863588839743d062576c9d144a91fc64400c25b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133448845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c9711c027ed5c0c1bc82bf858e1a428676cd76681a56c53068db5510594f55`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b98de49fe1ed993db53e09ac1d349e04edc68f3a669a0166fe861e63f21139`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 8.1 MB (8060708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af95ea946dd1ea6ddb09d4d16636c6dbdaf31f2a92f21fccf332f412f91978b`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313c9b4ec4148bbc92f321352088134bd5c79313a32b0346277392e67f81276a`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 18.7 MB (18669944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7c930da0eae6c203479c2208bc111980211a355e5ebe1d8b9d771bd3b3f5a2`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 18.8 MB (18798867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0028ab84266b23892e8257b849272b905514e4111ccc878a47fc9e050d94e`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf34514361d460f057db2b94643dcc0fa3771b2df3b514bcc118a203a10c95ba`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003372bc0a71b5fee80b7721b00c600392a2d1297a7bdc1382c4fe9b7a3c478`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654c3b9f6f86104ad7ac2a1861a8a6a3c9624bdb262e0024f0daee392ebdc1d`  
		Last Modified: Thu, 19 Dec 2024 06:27:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccacb1ec449ea2d8be4c5f1323c8f8f438ca6cbadb852569e5a1d30b2fccfb0`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 6.7 MB (6733442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db08b2b56d721154b01a601fafbf1388da92317b2a6fd84636403d145397cab`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 89.5 KB (89464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf58bc5c124acd8cd7867de0e5bfe811139bb7efbdfb4d3f384f5047368feadb`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed661c2bc3605af63c34b0e0e6b44c343cfaaeaeff5a9c5a1e90636c29b3c3`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 58.1 MB (58148385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd93031177fed6768ebac95908f7214e148aec625cde4db347278f785e7061f`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4580133da14d68ef765c552929a21bcefda14fd6f6d46ecd79ba394349848a`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:4d1ebca4fc352915e574abaa96ff6ed6588607144b48d49638664664171da1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785a52cc7646ffa85e15d5ffe60aac7f0f1a2d5253c2b101b6f346064092b53f`

```dockerfile
```

-	Layers:
	-	`sha256:57153e86db239ac28d0ccf1ea7c7b4f48b51df48813df21eab3ef9fec0624f79`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:8e53f8a2914c30d65228120667a050c54a74382d87f8e8205383be62560c9f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124579368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cc11a65e103a89e82e0f00f3eaea3ee929960b8b89fbf699a59f2bd46a109d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:148e72cbc3a4643c87b410580b6ae972ceafb99447e0d85bef2dd888ed7916d9`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 16.7 MB (16706481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfe37eaf11de403418a16f112ea736966145c615c0468af955274ca2d468276`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 17.4 MB (17448788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f071b9292f7441268ea76098e71b9dff0a1ec9f8311e4de77c6cd5af2c52a65`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 18.1 MB (18106565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a4fe84fb2fdef0c93d4c522edb4470e1d3558b04db73d6dc740cca4f2d3da6`  
		Last Modified: Thu, 19 Dec 2024 06:27:55 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa58f5b177c2d4b9d8d25bce148cba72f6b2db6ae71652dce2a49d1b4ecd88e`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755888e89afeff341e55361b436c6b35c8e67e7e05993e006c02d845c09320c3`  
		Last Modified: Thu, 19 Dec 2024 06:27:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ef02b0ebd56b76a25032f347f442a87fd532e2f07932b029c5a5ed2863ebdf`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 7.0 MB (7041137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa00a89210cf6cc619d32ecde33bcc417a048e4089420d3376e126502a34e868`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 89.1 KB (89114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314e6fc0bd408cd71d4f12dc2b30c175f02d576782580764a4d18dbe9397962a`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d2a39a9ca8dfcdf48360a081c2bacbd295c376b777d17ab83e02ace23e3d98`  
		Last Modified: Thu, 19 Dec 2024 07:08:09 GMT  
		Size: 53.8 MB (53837606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000fe248e69901663cba49cff877d5d4494f61261374eebd3e76654fdb4a9bb`  
		Last Modified: Thu, 19 Dec 2024 07:07:40 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e0a412273d2de4a63cf252e2955333edbb0387dab642897062720249f4180`  
		Last Modified: Thu, 19 Dec 2024 07:07:40 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:fbb76334b758da06115ce3db141b3a8d0384cf0fdfe0f1ae084cf566558cde04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05008ccd944add8210466657f1c49a19e043efce63da526e66de9aebb4b80ef`

```dockerfile
```

-	Layers:
	-	`sha256:d0c1d9bc2a056393fa0f5f33e177e88c39f2ff3b3ecab57b5172ba3064dfd763`  
		Last Modified: Thu, 19 Dec 2024 07:07:38 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:42fe1f55c44d24a6c3dabf704278f5beef25d390ca4c15966d714fb6e7908b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122921457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9248a004d8a619e67677191683cde42174b0b6a6f031c1bff04422a56ab7fafa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7384c11421040c34c2db4c9cbdff405dc1cb373620affa19cef0e6cd7889776b`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 16.7 MB (16694610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07bb9d6b4efc8e73c712cd756cad4ebdc7e4cd974f3b61319673b399cff7696`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 17.4 MB (17427589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e028074a72228d620c07c0306033af62a3bc33ecdbfdd182451a3940dbb3c47d`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 18.1 MB (18092645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b53f0105da3d54066118dde45e2db91fb53e54796d793199cb4d2ab602e9e2`  
		Last Modified: Thu, 19 Dec 2024 06:27:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6833631438bdcae5d6656508822939365cfd74de741e43abe8301361021b317`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b86ced47599bbfc27aa7dc389fb9cb257d493873490cc411bd8d27bdbf33bf`  
		Last Modified: Thu, 19 Dec 2024 06:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3cfec5adb0a4b5698f388de77eec77ddfae962de5b040d830dd95fded5c623`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 6.4 MB (6367338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f665ffa7443f60c8c9314082dba5723e72ede3f3451817173783b2ff36ffcb3`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 85.3 KB (85264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f8f3552eba49a36113015c2b82fecdb0cc6496614371b415212e14847dc60`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f31fefce9d3a0d0f1c7eb75b6cbde54e15ec723205ceea52b7da59ab4fb0dc`  
		Last Modified: Thu, 19 Dec 2024 07:07:45 GMT  
		Size: 53.8 MB (53837588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2522c47823d994b730d265c55af844c265eae9c9556e8e2200a9a35b9ac91a7`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06aa58a0bf71133cf40669589cd7fee930c7c0be06f93c2ff27147fd89bb1169`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:17996dd91287a758efee2344a070f6699509883f0d901af5ab238e9b387229bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b073ab412e1ae045cda1a9e0d874b37c17d7a32b94ca5af476daa61f0ae58438`

```dockerfile
```

-	Layers:
	-	`sha256:a559ea4afc9f0276e8285aa1e894d114568f8fc93aded28f64880c5b07631b25`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c4618ee87c867fff3b390aab9eeb59d889e39a14fb3bfbf40560f7faf78f841b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125264161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a74c04d0ac72b0d4df5a0d63124bff4cce8b81fe2f6d669d6272b5c426ef00e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc8b2386f26a19ff7e378d0b71a659c1c6185ff0418ab0ba70f91c9d7564766`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 8.1 MB (8077202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb804615f812dd41590a2167ce26fcd2bc94e936ef063d6ad5d47716653c51e`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500337a2754d23cb29983332f91f13bafcc80a7c299b977b077090a0fdf6e5a9`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.6 MB (17619412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821da57d87be4b4be2263810265c5fdfbee2a0815f9ba40aab6a34d602dbf10f`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.1 MB (17106449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a3e8ce8d46be94b3c36743d7add34488c85986d7d67dc65e6b0024b4f9629`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 17.6 MB (17642746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9727d9b709f029f03a062308481e155e1e44a388f1c90336ea9e6e9c98f4bf02`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5132ed17107a2140233d234c98fe9ff02ed459ac10f5b4ed2256ac52caff0ba2`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c450deeac7bd4e43a7a23a0608a88019260374cee39dc6371807295ef79a48`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95254613e12389bf1f1f60f9b295f28cef95138ce1dbc50738110a66f798909e`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 7.0 MB (6982148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3b84891c5b5b5525368fd009a3faa7c2ce7964cb220ec38caec428b7a4e023`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 97.8 KB (97810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f85e673a5bfddb9b35bc2893ca0b6dce01582d542e954e1f8522a5dc5bb96fc`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e62d3dc2daa4a6f98b762917d7f0adea4d641834acf4f0f8a44e1d79d577ab7`  
		Last Modified: Thu, 19 Dec 2024 07:07:59 GMT  
		Size: 53.7 MB (53737262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a6c5cd3176c0cc42a77bceba546446aac5d823c9f2fe97ef71fa20cc12bea4`  
		Last Modified: Thu, 19 Dec 2024 07:07:58 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01edfa8f426bf8debb954258fd0e37e36488fa9ba98d3d941a5b763aec91984f`  
		Last Modified: Thu, 19 Dec 2024 07:07:58 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:b944da17175c77080cb8774711d10f0b88e7b131c7036b9ad130642f29955bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754b5f14591dc682613445f666f9460bab283af4d13ee4f7a9e3e47c27451707`

```dockerfile
```

-	Layers:
	-	`sha256:cc7c1950a5e5557483555eef92ae1c730a5df8239e11efd4015d579f2c48b149`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:5b6982daa87eac334c19156bfbcaa7931ac5758857d951b05be6136184534394
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:fc55380e4b93f80c1ed6d12d49cc548099c2cf4fc463a40d2e45a7441a15d625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155737519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8322a7c3c8154f09895c7509500e24519267dec8b762f4d2243bd47bfefd97`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
USER rootless
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977b7051d06b1d34b73deaa52f5754a4c978be3600910f7b3c2b0fd99f3804cf`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 8.1 MB (8060784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be87b6ab9de77ee2bb24607f32584efd4c8d288fb0ebd92f21da27c6fb0fe05`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32318e2f30f796ed4b7af8e3685d3687fc883573db4a149b52ea74788725ff21`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 18.7 MB (18670168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eade46c9571ec550a556f19f01811aa5ed2c8d6d66dbe5c6b879696d6652b1b`  
		Last Modified: Sat, 14 Dec 2024 01:28:57 GMT  
		Size: 18.8 MB (18799497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d7b24eacf786b52d80c07bc9d227f80f4b4ff879b36937506ba00283a87474`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 19.3 MB (19295662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a2d527e845f1b9d701a4f3acad785c3a2e23f0b660308cd25b755e606b275`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e2987b6254b27b8f98fd687e63ba6e98b22435e5b511b084f07928f607dd0`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f92ad0aa8787ef6e63b311833061f3d5251fb1a1f17dac1f8fe5a2a3c16dc`  
		Last Modified: Sat, 14 Dec 2024 01:28:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c5d3db468870faaa078287545ebd4ce0c97ee7272f3bdb295dc466bfa5f372`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 6.7 MB (6729883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df9d86b50821da8baad5d1beab4920cef028caa1db97dff5f7b8ff6dc5cf47d`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 89.4 KB (89379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5068e4b2be3e0e95ca33a3f2ec02acc8405790e4b354aaeadb98bb913222bbf9`  
		Last Modified: Sat, 14 Dec 2024 02:09:02 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9ce30e2857d84e08bbf13baf09599072c31f64a45cca98a5d2db5f034a63b`  
		Last Modified: Sat, 14 Dec 2024 02:09:04 GMT  
		Size: 58.1 MB (58147954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1484582dafdf336ddc9c0e4b9c157decc41f125fd5f9213a67fa254ed83765e8`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620491d45b64abb50f190afd835976134a08e3951aa9736fb39eee4acba99053`  
		Last Modified: Sat, 14 Dec 2024 02:09:03 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e959b26a34438101745b4a6b12e2158e837753abb318a703d6a997acee940b32`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 986.6 KB (986587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c29d0936b41295dfa648ee92b27ebca2e18c10700ce27472e57dfdbcec4c6a`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485d19b2a60bc8d264042588663e4e123d26cbedf4aa96bbcf6ca5483bc82ca2`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50381dd0e19aea2b08429ae4b5824848b0e9e42926ee71822ae02df5e2693d16`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 21.3 MB (21303866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653b8fb52f49b277b1595dfbe1e5b2c3689df958d2df014003ce5cba5b7aa0c7`  
		Last Modified: Sat, 14 Dec 2024 03:07:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f6e358577a60d964b0f1b11ecf89a63cb21351522e15f87d7dfc6ebcda5969ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28cc68cd831df9a34e164fc2ea5b3f364ee6b02cc1f49f036ca59a72bc72571`

```dockerfile
```

-	Layers:
	-	`sha256:644bc1fff97fcf26268d33246cca53014486994146f0e5d4b02de3f5a26c9bcc`  
		Last Modified: Sat, 14 Dec 2024 03:07:33 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:47cd9b46cc39d1ea39ce702f2b197f78006e12d471ac0d9143046b0805d3880c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149423499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486e46f1028dafc6440042fcd3a8a6bb5cefda114320b24a99730bc21b9f2484`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_VERSION=27.4.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_BUILDX_VERSION=0.19.2
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-amd64'; 			sha256='a5ff61c0b6d2c8ee20964a9d6dac7a7a6383c4a4a0ee8d354e983917578306ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v6'; 			sha256='1b94a6747c55098c1200a4544521d854720b621685d0078d43128e0911d17cf0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm-v7'; 			sha256='a446237ace8919415fcb8599c47f2bc786436b910450d0546d15936788aeb3a7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-arm64'; 			sha256='bd54f0e28c29789da1679bad2dd94c1923786ccd2cd80dd3a0a1d560a6baf10c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-ppc64le'; 			sha256='8312065303b9ff436d64e15b296951ce50b2e064b91d93befea19f09dc22115c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-riscv64'; 			sha256='9b226b369830eca078a6af7105aa7ee167e39f3a21e30d25f95eb433cdb3de92'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.2/buildx-v0.19.2.linux-s390x'; 			sha256='47572102e1888571da13804fcaed8294e1af33c576103b4dd9263288c0b6935d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.0
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-x86_64'; 			sha256='c204bc7058fb881b2a39175df5c3596f6b08ef9e358d7236df7cc781f74695bd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv6'; 			sha256='d72e2d4b8ab71fa4b0132b451f43267aaca980c4ee9cb670ae6f83fa101747e7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-armv7'; 			sha256='9e6b63bd2b863c4564fa61c18f2515f0130a8800f12a35c2836fdd6a044ff222'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-aarch64'; 			sha256='0bb65b36b32750a876cfdd5720e811ba1b70cb9eca72536fdf4ac7949fbc20e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-ppc64le'; 			sha256='5e05371a1b0f3bb4e9785aa9957c98bff625aab675a59e5ae6c75e7e7ec41027'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-riscv64'; 			sha256='726362c280a764de1249927857e51bb9f1321a0c4d5192dc0a5e2134ac29a999'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.0/docker-compose-linux-s390x'; 			sha256='d9c117c743131c3addc933d71d6ee5cbf70951ce34c43b765a7d57c80ef58429'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD ["sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Dec 2024 17:51:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Dec 2024 17:51:24 GMT
CMD []
# Mon, 09 Dec 2024 17:51:24 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Dec 2024 17:51:24 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Dec 2024 17:51:24 GMT
USER rootless
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f29899ccbbf1e741f60597ba30d60ac9c1b90e66805313b199804e42bb26b8`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 8.1 MB (8077216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf82dff70ae622662fa9a73a5223978930a18a6ae224cf22cb4cb544d20e54cb`  
		Last Modified: Sat, 14 Dec 2024 01:30:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4006eb8ef403cfad925fa266ee6c97b8e7437d82fada3b11ee40c73d1346fd29`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 17.6 MB (17619303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca033ddc28f236317e2717e08b0599bce7dc57f062d50e105789d951301709c1`  
		Last Modified: Sat, 14 Dec 2024 01:30:53 GMT  
		Size: 17.1 MB (17105676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac67c8631984a4a76018ae6dfcd431e33f8a842a5a41427c93622147b484e75`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 17.6 MB (17642698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca12aa3e41222dda17ff5dd783455ae9139e3b877645182502adeab17258e8`  
		Last Modified: Sat, 14 Dec 2024 01:30:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2a18af15ca954957a7847214082e4df2bce64335dedd3ff4fba98f76284eb5`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df37b79dff77ef37f0d3e37560e1338f542f623ef54cfe86bb41fa8d10608a7`  
		Last Modified: Sat, 14 Dec 2024 01:30:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa3443190ca0ce3c9348be68ac733b8e7eabb68fdf3494490329f5e4d077cf7`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 7.0 MB (6980417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df7beef76ff5ec34871261980d7ce36275d1e7863bacf11eb94ba868cdcb57d`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 97.8 KB (97751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2626027f39080c44a7fa749d2373483f2542a2948eb8ac4d5882687213fe6a0e`  
		Last Modified: Sat, 14 Dec 2024 02:11:26 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb24cb7fa88f82359854c9298528e58874dd980f2287c10cff566c0b9443a467`  
		Last Modified: Sat, 14 Dec 2024 02:11:28 GMT  
		Size: 53.7 MB (53728638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a2a3c134987087aa5476cad229889681f776f2e8be759adb1c64cbb7d11855`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabb2966a6d122e4ad14e5c38fec5c030edb1573f093739072db71a5fa52ec29`  
		Last Modified: Sat, 14 Dec 2024 02:11:27 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1095688739528f200fadd7670e4c7b354566e5b6a5663acc8690e24430f6e3`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 1.0 MB (1014153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecbf2c620964818ee2dcbc20a175aad27a6fb8b052fb19dd701cbbdb6f23e78`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac17c515dbd19f47019153943183a2995ace4060877f16ef7a715db68ae4181`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8818bf23aa3c08119351a436f05fc62b25a1fa448a59f02e05804a5ab92f00`  
		Last Modified: Sat, 14 Dec 2024 03:07:29 GMT  
		Size: 23.2 MB (23155158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056092e1c446a0219de668b0289797f8369a23417dd278d159af0606bf9b74c5`  
		Last Modified: Sat, 14 Dec 2024 03:07:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3f695216a693f4d4041900f72c45a3e39ab19ae5c1727df82414c0e158a605ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c5773897944ec73002da42dd7bafb32c8788aadf785e3ffbd20df78b3d7de2`

```dockerfile
```

-	Layers:
	-	`sha256:732f97201f7324ad6916ceab73e27ea9cf755fc3a41522c77793bdef203efd55`  
		Last Modified: Sat, 14 Dec 2024 03:07:27 GMT  
		Size: 30.8 KB (30787 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:d33ffba5909705d375ef1a99bb69fe6e21d80482134283226b119acf18bb08b4
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
$ docker pull docker@sha256:197a4c5f8ffb8e4940e2518b1863588839743d062576c9d144a91fc64400c25b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133448845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c9711c027ed5c0c1bc82bf858e1a428676cd76681a56c53068db5510594f55`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b98de49fe1ed993db53e09ac1d349e04edc68f3a669a0166fe861e63f21139`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 8.1 MB (8060708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af95ea946dd1ea6ddb09d4d16636c6dbdaf31f2a92f21fccf332f412f91978b`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313c9b4ec4148bbc92f321352088134bd5c79313a32b0346277392e67f81276a`  
		Last Modified: Thu, 19 Dec 2024 06:27:21 GMT  
		Size: 18.7 MB (18669944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7c930da0eae6c203479c2208bc111980211a355e5ebe1d8b9d771bd3b3f5a2`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 18.8 MB (18798867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0028ab84266b23892e8257b849272b905514e4111ccc878a47fc9e050d94e`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf34514361d460f057db2b94643dcc0fa3771b2df3b514bcc118a203a10c95ba`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003372bc0a71b5fee80b7721b00c600392a2d1297a7bdc1382c4fe9b7a3c478`  
		Last Modified: Thu, 19 Dec 2024 06:27:22 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654c3b9f6f86104ad7ac2a1861a8a6a3c9624bdb262e0024f0daee392ebdc1d`  
		Last Modified: Thu, 19 Dec 2024 06:27:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccacb1ec449ea2d8be4c5f1323c8f8f438ca6cbadb852569e5a1d30b2fccfb0`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 6.7 MB (6733442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db08b2b56d721154b01a601fafbf1388da92317b2a6fd84636403d145397cab`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 89.5 KB (89464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf58bc5c124acd8cd7867de0e5bfe811139bb7efbdfb4d3f384f5047368feadb`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed661c2bc3605af63c34b0e0e6b44c343cfaaeaeff5a9c5a1e90636c29b3c3`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 58.1 MB (58148385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd93031177fed6768ebac95908f7214e148aec625cde4db347278f785e7061f`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4580133da14d68ef765c552929a21bcefda14fd6f6d46ecd79ba394349848a`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:4d1ebca4fc352915e574abaa96ff6ed6588607144b48d49638664664171da1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785a52cc7646ffa85e15d5ffe60aac7f0f1a2d5253c2b101b6f346064092b53f`

```dockerfile
```

-	Layers:
	-	`sha256:57153e86db239ac28d0ccf1ea7c7b4f48b51df48813df21eab3ef9fec0624f79`  
		Last Modified: Thu, 19 Dec 2024 07:08:00 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:8e53f8a2914c30d65228120667a050c54a74382d87f8e8205383be62560c9f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124579368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cc11a65e103a89e82e0f00f3eaea3ee929960b8b89fbf699a59f2bd46a109d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:148e72cbc3a4643c87b410580b6ae972ceafb99447e0d85bef2dd888ed7916d9`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 16.7 MB (16706481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfe37eaf11de403418a16f112ea736966145c615c0468af955274ca2d468276`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 17.4 MB (17448788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f071b9292f7441268ea76098e71b9dff0a1ec9f8311e4de77c6cd5af2c52a65`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 18.1 MB (18106565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a4fe84fb2fdef0c93d4c522edb4470e1d3558b04db73d6dc740cca4f2d3da6`  
		Last Modified: Thu, 19 Dec 2024 06:27:55 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa58f5b177c2d4b9d8d25bce148cba72f6b2db6ae71652dce2a49d1b4ecd88e`  
		Last Modified: Thu, 19 Dec 2024 06:27:56 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755888e89afeff341e55361b436c6b35c8e67e7e05993e006c02d845c09320c3`  
		Last Modified: Thu, 19 Dec 2024 06:27:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ef02b0ebd56b76a25032f347f442a87fd532e2f07932b029c5a5ed2863ebdf`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 7.0 MB (7041137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa00a89210cf6cc619d32ecde33bcc417a048e4089420d3376e126502a34e868`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 89.1 KB (89114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314e6fc0bd408cd71d4f12dc2b30c175f02d576782580764a4d18dbe9397962a`  
		Last Modified: Thu, 19 Dec 2024 07:07:39 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d2a39a9ca8dfcdf48360a081c2bacbd295c376b777d17ab83e02ace23e3d98`  
		Last Modified: Thu, 19 Dec 2024 07:08:09 GMT  
		Size: 53.8 MB (53837606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000fe248e69901663cba49cff877d5d4494f61261374eebd3e76654fdb4a9bb`  
		Last Modified: Thu, 19 Dec 2024 07:07:40 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e0a412273d2de4a63cf252e2955333edbb0387dab642897062720249f4180`  
		Last Modified: Thu, 19 Dec 2024 07:07:40 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:fbb76334b758da06115ce3db141b3a8d0384cf0fdfe0f1ae084cf566558cde04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05008ccd944add8210466657f1c49a19e043efce63da526e66de9aebb4b80ef`

```dockerfile
```

-	Layers:
	-	`sha256:d0c1d9bc2a056393fa0f5f33e177e88c39f2ff3b3ecab57b5172ba3064dfd763`  
		Last Modified: Thu, 19 Dec 2024 07:07:38 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:42fe1f55c44d24a6c3dabf704278f5beef25d390ca4c15966d714fb6e7908b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122921457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9248a004d8a619e67677191683cde42174b0b6a6f031c1bff04422a56ab7fafa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6019fc938817b2078b7c4c37778a9be5003f940544f48327f305282887849`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 7.3 MB (7308430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ef18d0bcfddb1ddbdbba3d8987d58f2f15c6457f10ff245727c1f3ba49f50`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7384c11421040c34c2db4c9cbdff405dc1cb373620affa19cef0e6cd7889776b`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 16.7 MB (16694610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07bb9d6b4efc8e73c712cd756cad4ebdc7e4cd974f3b61319673b399cff7696`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 17.4 MB (17427589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e028074a72228d620c07c0306033af62a3bc33ecdbfdd182451a3940dbb3c47d`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 18.1 MB (18092645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b53f0105da3d54066118dde45e2db91fb53e54796d793199cb4d2ab602e9e2`  
		Last Modified: Thu, 19 Dec 2024 06:27:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6833631438bdcae5d6656508822939365cfd74de741e43abe8301361021b317`  
		Last Modified: Thu, 19 Dec 2024 06:27:31 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b86ced47599bbfc27aa7dc389fb9cb257d493873490cc411bd8d27bdbf33bf`  
		Last Modified: Thu, 19 Dec 2024 06:27:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3cfec5adb0a4b5698f388de77eec77ddfae962de5b040d830dd95fded5c623`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 6.4 MB (6367338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f665ffa7443f60c8c9314082dba5723e72ede3f3451817173783b2ff36ffcb3`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 85.3 KB (85264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f8f3552eba49a36113015c2b82fecdb0cc6496614371b415212e14847dc60`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f31fefce9d3a0d0f1c7eb75b6cbde54e15ec723205ceea52b7da59ab4fb0dc`  
		Last Modified: Thu, 19 Dec 2024 07:07:45 GMT  
		Size: 53.8 MB (53837588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2522c47823d994b730d265c55af844c265eae9c9556e8e2200a9a35b9ac91a7`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06aa58a0bf71133cf40669589cd7fee930c7c0be06f93c2ff27147fd89bb1169`  
		Last Modified: Thu, 19 Dec 2024 07:07:43 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:17996dd91287a758efee2344a070f6699509883f0d901af5ab238e9b387229bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b073ab412e1ae045cda1a9e0d874b37c17d7a32b94ca5af476daa61f0ae58438`

```dockerfile
```

-	Layers:
	-	`sha256:a559ea4afc9f0276e8285aa1e894d114568f8fc93aded28f64880c5b07631b25`  
		Last Modified: Thu, 19 Dec 2024 07:07:42 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c4618ee87c867fff3b390aab9eeb59d889e39a14fb3bfbf40560f7faf78f841b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125264161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a74c04d0ac72b0d4df5a0d63124bff4cce8b81fe2f6d669d6272b5c426ef00e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc8b2386f26a19ff7e378d0b71a659c1c6185ff0418ab0ba70f91c9d7564766`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 8.1 MB (8077202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb804615f812dd41590a2167ce26fcd2bc94e936ef063d6ad5d47716653c51e`  
		Last Modified: Thu, 19 Dec 2024 06:28:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500337a2754d23cb29983332f91f13bafcc80a7c299b977b077090a0fdf6e5a9`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.6 MB (17619412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821da57d87be4b4be2263810265c5fdfbee2a0815f9ba40aab6a34d602dbf10f`  
		Last Modified: Thu, 19 Dec 2024 06:28:07 GMT  
		Size: 17.1 MB (17106449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a3e8ce8d46be94b3c36743d7add34488c85986d7d67dc65e6b0024b4f9629`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 17.6 MB (17642746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9727d9b709f029f03a062308481e155e1e44a388f1c90336ea9e6e9c98f4bf02`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5132ed17107a2140233d234c98fe9ff02ed459ac10f5b4ed2256ac52caff0ba2`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c450deeac7bd4e43a7a23a0608a88019260374cee39dc6371807295ef79a48`  
		Last Modified: Thu, 19 Dec 2024 06:28:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95254613e12389bf1f1f60f9b295f28cef95138ce1dbc50738110a66f798909e`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 7.0 MB (6982148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3b84891c5b5b5525368fd009a3faa7c2ce7964cb220ec38caec428b7a4e023`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 97.8 KB (97810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f85e673a5bfddb9b35bc2893ca0b6dce01582d542e954e1f8522a5dc5bb96fc`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e62d3dc2daa4a6f98b762917d7f0adea4d641834acf4f0f8a44e1d79d577ab7`  
		Last Modified: Thu, 19 Dec 2024 07:07:59 GMT  
		Size: 53.7 MB (53737262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a6c5cd3176c0cc42a77bceba546446aac5d823c9f2fe97ef71fa20cc12bea4`  
		Last Modified: Thu, 19 Dec 2024 07:07:58 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01edfa8f426bf8debb954258fd0e37e36488fa9ba98d3d941a5b763aec91984f`  
		Last Modified: Thu, 19 Dec 2024 07:07:58 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:b944da17175c77080cb8774711d10f0b88e7b131c7036b9ad130642f29955bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754b5f14591dc682613445f666f9460bab283af4d13ee4f7a9e3e47c27451707`

```dockerfile
```

-	Layers:
	-	`sha256:cc7c1950a5e5557483555eef92ae1c730a5df8239e11efd4015d579f2c48b149`  
		Last Modified: Thu, 19 Dec 2024 07:07:57 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:ce26a4b6892bb5fff408af70028fd1f7aadf1ba1817049f7c36d386b938f2a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:b59b50eddc96fa024759736642b20d31e812c747839aa0e04e6b3cd306d9c08f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312956798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dac0ff62690131e5cbadefa8b3173ce78f2fedeb1bedfb9599c99488be059a9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Thu, 19 Dec 2024 06:27:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Dec 2024 06:28:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Dec 2024 06:28:35 GMT
ENV DOCKER_VERSION=27.4.1
# Thu, 19 Dec 2024 06:28:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.1.zip
# Thu, 19 Dec 2024 06:28:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:28:58 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 19 Dec 2024 06:28:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 19 Dec 2024 06:28:59 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 19 Dec 2024 06:29:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Thu, 19 Dec 2024 06:29:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-windows-x86_64.exe
# Thu, 19 Dec 2024 06:29:12 GMT
ENV DOCKER_COMPOSE_SHA256=5dc7ac86e8d3972c2c68066c6ac370daf0a42b7c8d3338336c9dbde34af06213
# Thu, 19 Dec 2024 06:29:24 GMT
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
	-	`sha256:c2d7502a1bbe13300d252a2f9df8e505261a1640bc1bd25b0948e9c00fcc5b01`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c5b28592218521960824b8276896946f244fbb3651810d08c43452a2582cb`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 357.3 KB (357322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6330b409518a6d4ccfc671760fb4c29c3aa61745511abc8406e7598afdeb72f4`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff2da6ec5d910a6c45c3b7bc2ada4de7ee595addaae450cfea2ba3fba3571f0`  
		Last Modified: Thu, 19 Dec 2024 06:29:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981fcf2dca12be8aa09825096e39af48ab18642d75e6e2791014b5511999719c`  
		Last Modified: Thu, 19 Dec 2024 06:29:30 GMT  
		Size: 19.0 MB (18965788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559ffe22c82820dbe4c523868249c3f6a55385142d2e0ead71e852d8a7251d56`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458e70a57b4ce24dfc2a913ab05c3222397fe2e8a5d93868622a5da7a9340e81`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dd3b199caac21501453ed73a1b07e07e8909c492da3b0c12264e12be24f8f7`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffced5034da239bcce196f61166f31fa32a1046a0b90925f73df0a56a4540555`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 19.6 MB (19615775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d1d24e414a381ae30c27fae03be0f84206adbad1d9b6b30407bfecceb5e1e5`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deeb14568d7a7f723c99e08a5b860258c0e121c9b475c7f14d316ac30cb06d68`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a34da183fbb7bde6f718a61627a8077978264175188a7e437d8f791c46033e`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdb77e5d84cc05ce04533280006424bb2742fe825cfe58eb5f5934b7a430dcf`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 20.1 MB (20132656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:c442ec204cc8c3af89a231557d7113d731304aa9004ecc2fd2b7fdea9a2a5ed5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073460288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd24b1732cd2a56ef18bd248405211562b17b3b25cc385edc36040b8cea00146`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Thu, 19 Dec 2024 06:27:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Dec 2024 06:28:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Dec 2024 06:28:36 GMT
ENV DOCKER_VERSION=27.4.1
# Thu, 19 Dec 2024 06:28:37 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.1.zip
# Thu, 19 Dec 2024 06:29:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:00 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 19 Dec 2024 06:29:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 19 Dec 2024 06:29:01 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 19 Dec 2024 06:29:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Thu, 19 Dec 2024 06:29:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-windows-x86_64.exe
# Thu, 19 Dec 2024 06:29:16 GMT
ENV DOCKER_COMPOSE_SHA256=5dc7ac86e8d3972c2c68066c6ac370daf0a42b7c8d3338336c9dbde34af06213
# Thu, 19 Dec 2024 06:29:30 GMT
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
	-	`sha256:e1cfd0430e259e32b94429bf581ea5f74b25080ea9e68899e17062c55bfdba4f`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089d2b012e4350683f7592078e0330072d47face607cfdcfa1b177015a1d055d`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 475.3 KB (475261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e54e6e8f743b8e62247f614caa153507aeea30e39ec7d133b120770472d150d`  
		Last Modified: Thu, 19 Dec 2024 06:29:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c46ebe5f7bc661958c2410ed2a60431be6d40269618a1223f8bc2c1f5392c26`  
		Last Modified: Thu, 19 Dec 2024 06:29:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac2d753848f2b9292c76be0e8c43f38d7c04ed25979be15179b781a3c2b47b9`  
		Last Modified: Thu, 19 Dec 2024 06:29:36 GMT  
		Size: 19.0 MB (18997863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4c651853f033dafb87a17fdd7690c1c3c3a0f4dfb6e083cf06ba8d91234d98`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1a3389962e8b333bfcead93ec3aad31713a4bafd7b7be628b737077da7d60b`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e030ce22f45d6c461af01d11e768dcd4638cd9b989e6dc8aa7e384b7ccb80129`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d987b1383b6b76eb88c20a38bac7e305fe1f8c311242b83bc819be0eee3eb3`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 19.6 MB (19648080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e0d2a17e8fa800de7106ca7d9cce51ab9562558d2d155ddfaaa0d979138750`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d9b36807cefb176cc3c814de379c2bf6a17663ed8e0372f69d2cb06a02cd4e`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f2c79cb8ac15f188f4afd8366afee1f46ec780fa70082a4c9e991ac09c8537`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f72ede2a361313c0a7e7b059df25505b175cc277540b12cb48ee012d5a4ba93`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 20.2 MB (20157227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:5a5cd9f42944d54ac3da3dfda65c1d0342f266339ac3fde581f7021a2aa3c54c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:c442ec204cc8c3af89a231557d7113d731304aa9004ecc2fd2b7fdea9a2a5ed5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073460288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd24b1732cd2a56ef18bd248405211562b17b3b25cc385edc36040b8cea00146`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Thu, 19 Dec 2024 06:27:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Dec 2024 06:28:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Dec 2024 06:28:36 GMT
ENV DOCKER_VERSION=27.4.1
# Thu, 19 Dec 2024 06:28:37 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.1.zip
# Thu, 19 Dec 2024 06:29:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:00 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 19 Dec 2024 06:29:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 19 Dec 2024 06:29:01 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 19 Dec 2024 06:29:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Thu, 19 Dec 2024 06:29:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-windows-x86_64.exe
# Thu, 19 Dec 2024 06:29:16 GMT
ENV DOCKER_COMPOSE_SHA256=5dc7ac86e8d3972c2c68066c6ac370daf0a42b7c8d3338336c9dbde34af06213
# Thu, 19 Dec 2024 06:29:30 GMT
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
	-	`sha256:e1cfd0430e259e32b94429bf581ea5f74b25080ea9e68899e17062c55bfdba4f`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089d2b012e4350683f7592078e0330072d47face607cfdcfa1b177015a1d055d`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 475.3 KB (475261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e54e6e8f743b8e62247f614caa153507aeea30e39ec7d133b120770472d150d`  
		Last Modified: Thu, 19 Dec 2024 06:29:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c46ebe5f7bc661958c2410ed2a60431be6d40269618a1223f8bc2c1f5392c26`  
		Last Modified: Thu, 19 Dec 2024 06:29:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac2d753848f2b9292c76be0e8c43f38d7c04ed25979be15179b781a3c2b47b9`  
		Last Modified: Thu, 19 Dec 2024 06:29:36 GMT  
		Size: 19.0 MB (18997863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4c651853f033dafb87a17fdd7690c1c3c3a0f4dfb6e083cf06ba8d91234d98`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1a3389962e8b333bfcead93ec3aad31713a4bafd7b7be628b737077da7d60b`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e030ce22f45d6c461af01d11e768dcd4638cd9b989e6dc8aa7e384b7ccb80129`  
		Last Modified: Thu, 19 Dec 2024 06:29:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d987b1383b6b76eb88c20a38bac7e305fe1f8c311242b83bc819be0eee3eb3`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 19.6 MB (19648080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e0d2a17e8fa800de7106ca7d9cce51ab9562558d2d155ddfaaa0d979138750`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d9b36807cefb176cc3c814de379c2bf6a17663ed8e0372f69d2cb06a02cd4e`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f2c79cb8ac15f188f4afd8366afee1f46ec780fa70082a4c9e991ac09c8537`  
		Last Modified: Thu, 19 Dec 2024 06:29:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f72ede2a361313c0a7e7b059df25505b175cc277540b12cb48ee012d5a4ba93`  
		Last Modified: Thu, 19 Dec 2024 06:29:35 GMT  
		Size: 20.2 MB (20157227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:bbaca47510bc3b68824fca9b3d27ac84ec15755c88e1ac61a53c6f93ace9c225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:b59b50eddc96fa024759736642b20d31e812c747839aa0e04e6b3cd306d9c08f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312956798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dac0ff62690131e5cbadefa8b3173ce78f2fedeb1bedfb9599c99488be059a9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Thu, 19 Dec 2024 06:27:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Dec 2024 06:28:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Dec 2024 06:28:35 GMT
ENV DOCKER_VERSION=27.4.1
# Thu, 19 Dec 2024 06:28:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.1.zip
# Thu, 19 Dec 2024 06:28:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:28:58 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 19 Dec 2024 06:28:59 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 19 Dec 2024 06:28:59 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 19 Dec 2024 06:29:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Dec 2024 06:29:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Thu, 19 Dec 2024 06:29:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-windows-x86_64.exe
# Thu, 19 Dec 2024 06:29:12 GMT
ENV DOCKER_COMPOSE_SHA256=5dc7ac86e8d3972c2c68066c6ac370daf0a42b7c8d3338336c9dbde34af06213
# Thu, 19 Dec 2024 06:29:24 GMT
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
	-	`sha256:c2d7502a1bbe13300d252a2f9df8e505261a1640bc1bd25b0948e9c00fcc5b01`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c5b28592218521960824b8276896946f244fbb3651810d08c43452a2582cb`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 357.3 KB (357322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6330b409518a6d4ccfc671760fb4c29c3aa61745511abc8406e7598afdeb72f4`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff2da6ec5d910a6c45c3b7bc2ada4de7ee595addaae450cfea2ba3fba3571f0`  
		Last Modified: Thu, 19 Dec 2024 06:29:28 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981fcf2dca12be8aa09825096e39af48ab18642d75e6e2791014b5511999719c`  
		Last Modified: Thu, 19 Dec 2024 06:29:30 GMT  
		Size: 19.0 MB (18965788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559ffe22c82820dbe4c523868249c3f6a55385142d2e0ead71e852d8a7251d56`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458e70a57b4ce24dfc2a913ab05c3222397fe2e8a5d93868622a5da7a9340e81`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dd3b199caac21501453ed73a1b07e07e8909c492da3b0c12264e12be24f8f7`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffced5034da239bcce196f61166f31fa32a1046a0b90925f73df0a56a4540555`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 19.6 MB (19615775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d1d24e414a381ae30c27fae03be0f84206adbad1d9b6b30407bfecceb5e1e5`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deeb14568d7a7f723c99e08a5b860258c0e121c9b475c7f14d316ac30cb06d68`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a34da183fbb7bde6f718a61627a8077978264175188a7e437d8f791c46033e`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdb77e5d84cc05ce04533280006424bb2742fe825cfe58eb5f5934b7a430dcf`  
		Last Modified: Thu, 19 Dec 2024 06:29:29 GMT  
		Size: 20.1 MB (20132656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
