## `docker:dind-rootless`

```console
$ docker pull docker@sha256:c47e057971e54262ed442dfc9c77fbc8cf0084cf37f6b73e5fd62976114cd07f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:b89b1f543bc68cefccc0ade704f41904052426ba503666c6434f12505deebde5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155711452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63cfa671fa7986aa185a6c156417d81f266c629c1c534a447f29fb329829333`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735b20db87539c7463591fa766b2629a58ab3aef544540d52804dfdc5a6ecb5b`  
		Last Modified: Wed, 08 Jan 2025 05:51:55 GMT  
		Size: 8.0 MB (8040072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4478f0e85bc542c00947578413ad67f79b687aced7cbf4c9ba0dfedbedd3fd`  
		Last Modified: Tue, 07 Jan 2025 03:14:08 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e7418271751ce7ce091188e84d9ae36f237290650c3b3d8de6a92f427e3652`  
		Last Modified: Tue, 07 Jan 2025 03:14:09 GMT  
		Size: 18.7 MB (18669947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58846b2ad37606232e7deae90371872fd4246c809d37763223fcdca3c2e50958`  
		Last Modified: Tue, 07 Jan 2025 03:14:09 GMT  
		Size: 18.8 MB (18798861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b9895271a3c8c25426eace05dedbb6c0de2bbdb39194b264ab7ee93891fa52`  
		Last Modified: Tue, 07 Jan 2025 03:14:09 GMT  
		Size: 19.3 MB (19295667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de94683a173a31bade986c7cc662189db5c9a6cbb76cac50607f05fed6060e7f`  
		Last Modified: Tue, 07 Jan 2025 03:14:09 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa0dac476916b4b92f039adba29496d16c5046f88489a7aa26e0f66092ffdca`  
		Last Modified: Tue, 07 Jan 2025 03:14:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4c9b11fbc08c77ca7a69c29bf95d710bfa0a63cc59a7d9610c45898f958ed`  
		Last Modified: Wed, 08 Jan 2025 05:53:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532bf802cdbaf6126b4deda51d3b4eca4d51c2dc4ddab0cdbf094c2c1207614d`  
		Last Modified: Wed, 08 Jan 2025 05:49:52 GMT  
		Size: 6.7 MB (6733375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3d093ba670a344b46c22f33e14af265d013225ec1f6ea9fd94240a244d20d3`  
		Last Modified: Tue, 07 Jan 2025 04:17:57 GMT  
		Size: 89.2 KB (89153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdd580e29986944d11d5c6ebf396fecf1a57671a38ce3e195c0736b80b7d404`  
		Last Modified: Tue, 07 Jan 2025 04:17:57 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea104b5e241789c0848b43764b7ac58455739a8c7daf5282457a1abef48130b8`  
		Last Modified: Tue, 07 Jan 2025 04:17:59 GMT  
		Size: 58.1 MB (58148426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69fde5d45d660ed944e404d2295dc89602c47c12082ecd2da27292846587d63`  
		Last Modified: Tue, 07 Jan 2025 04:17:58 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5e8aef9433447441b9c59a5084a6d7245b165c046409ba9e26a701eb6dd3fa`  
		Last Modified: Tue, 07 Jan 2025 04:17:58 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60588895f0fa8896811cb06228dfa63d6cfe2b0cc84137c6490451f3d0bf4eb2`  
		Last Modified: Tue, 07 Jan 2025 05:13:42 GMT  
		Size: 986.6 KB (986571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea47ef985a7bb96da23fe62290856821a33fb310945952492d69431b42a5335`  
		Last Modified: Tue, 07 Jan 2025 05:13:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1ff33756d3f7c7a8dc639f9845682c32a2857fe05f77a94526cec8eecb64b1`  
		Last Modified: Tue, 07 Jan 2025 05:13:42 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0949d3bc2e13d5053596a53ef5730d0247b8b3f261e66125bd6b1e8d146c486c`  
		Last Modified: Tue, 07 Jan 2025 05:13:43 GMT  
		Size: 21.3 MB (21303866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f141ec4e6fdec744a8bdafcb69667c12f28fd9c3a1d4254f3505e04961022933`  
		Last Modified: Tue, 07 Jan 2025 05:13:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:e6c175ee8f274d67b370b67fe422f46eafcd63f89faf013486ba4ebe3a0cabe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c55038a6f4c881b633eeb6867cce6c4704cf5770c0a071ee340a48e2bb4a4d9`

```dockerfile
```

-	Layers:
	-	`sha256:780e0f2fa68c323c95868f392b377227c85a443b3af82dae734336c6d9738459`  
		Last Modified: Tue, 07 Jan 2025 05:13:42 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0cf9901aa66898ac7048e4bba73fc829856bad351ea999620278692964796d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149408622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d576d7d73bbbc5f88bc8928a03bf85bc9cbe31a89c583c6f3aeeb527764d59b7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
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
	-	`sha256:ce1ead7d0d6b13bd89d8ced3a7da7f9bfaf320b108f1f136679e234b241f9435`  
		Last Modified: Tue, 07 Jan 2025 03:58:38 GMT  
		Size: 17.6 MB (17619412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b599e3959a030d724cc0a0b5e722a0b8a64e41fecc9b83f85c3cb80db7b4850`  
		Last Modified: Tue, 07 Jan 2025 03:58:38 GMT  
		Size: 17.1 MB (17106454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d7723d0215c2c397185101a17ccb36904378cbf882494743481733c8964e1f`  
		Last Modified: Tue, 07 Jan 2025 03:58:38 GMT  
		Size: 17.6 MB (17642747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01483a5ff9b9a7cdb913e5a359e2ef10d87372a278c6764a1d2efbe1433f0e2`  
		Last Modified: Tue, 07 Jan 2025 03:58:37 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89e2d6fe159cc7ab343c7c063d0a74b49b25bfb881e0c7e0e88c73d28220b45`  
		Last Modified: Tue, 07 Jan 2025 03:58:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429b7872ce7d9009794e11d712031dc4f383d9c06a9d4dc60248d010c21f772f`  
		Last Modified: Tue, 07 Jan 2025 03:58:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca15ed9409d21366ce7d395eb277ca97997eaf6dea1533547e948aa4b3b6f11f`  
		Last Modified: Tue, 07 Jan 2025 15:51:45 GMT  
		Size: 7.0 MB (6982181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a4e43557df78f397d010ef9e0431c8c39454e3bc8f7e6df07fd208b2285cb5`  
		Last Modified: Tue, 07 Jan 2025 15:51:44 GMT  
		Size: 97.5 KB (97550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931e577592694205abc1b5b1bcf896a697df31d4b7c18c00f3df67e58e5745dc`  
		Last Modified: Wed, 08 Jan 2025 04:48:24 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c57029471c9c034c62dd27528d629698643f74be66658f12ba389f319f32111`  
		Last Modified: Tue, 07 Jan 2025 15:51:46 GMT  
		Size: 53.7 MB (53737264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623a412e62b91e30e6bcc47250ed6b8165d16f5730404b0566189fb39daa029e`  
		Last Modified: Tue, 07 Jan 2025 15:51:45 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a872f64241cca3cf1b28edb4b345fea22d6054770fdfa79a13c468e0c51e63`  
		Last Modified: Tue, 07 Jan 2025 15:51:45 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300d7feee66474d435a24f71baae440e3e91656751fe8ba277bc18e79bf14f9a`  
		Last Modified: Tue, 07 Jan 2025 18:37:43 GMT  
		Size: 1.0 MB (1013836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9021f43e977d173fef6db42a182a57875458076153af0b9c502ca24a47c1a48`  
		Last Modified: Tue, 07 Jan 2025 18:37:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdd042c421e6be5c85e78552a08e04550cb71e433c0ef32edce5a90b2a6eccb`  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a9668d4a4e9392d58401be836000f704e9e3fa5c0abd2e3828029a3166c7a7`  
		Last Modified: Tue, 07 Jan 2025 18:37:44 GMT  
		Size: 23.2 MB (23155143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf7226469d06f67e01934d4978d8246a818ebd2ced8a0cfdb65f8df4b88db7a`  
		Last Modified: Tue, 07 Jan 2025 18:37:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:20816fa65515cf6be180c0a14fa3ab47d08cc5b13b103d4995fb01071ea2e4ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b0ce5ca006cbeb9bf153dbcc6581aa09f88c0ce368785397d6bf17b7c323f94`

```dockerfile
```

-	Layers:
	-	`sha256:f59af1d228c921c2a853dcac5261bd1459f6affd4f8ab3b1ad113eadb78204ad`  
		Last Modified: Tue, 07 Jan 2025 18:37:43 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json
