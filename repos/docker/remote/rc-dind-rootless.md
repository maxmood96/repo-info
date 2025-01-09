## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:2eefce22722a77bafb780c2beabacc18282884abd0571d36e9daa6fda3648a9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e47dcbe07662b7bc1074eb3e41d226683fd2db114d2f98b54bd2219cebc76058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156090797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16456bc7bb0893269b8ee7bbdb07034e42698ecfea4d82d9eef634dd3507bbc5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 23 Dec 2024 12:04:24 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
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
# Mon, 23 Dec 2024 12:04:24 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.5.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.5.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 23 Dec 2024 12:04:24 GMT
USER rootless
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d185366bdae3ff1be746691465de29a0e0b2f3e04f28b39180d9375234c91e73`  
		Last Modified: Wed, 08 Jan 2025 17:58:05 GMT  
		Size: 8.1 MB (8058731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84093b170643807426ca3245685f647e26fe436e1ef1abba0ef4cf9534f507c3`  
		Last Modified: Wed, 08 Jan 2025 17:58:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa172934c35105c4a18182bd9b857ade0907d0d1764f9ad891155264506fe4c6`  
		Last Modified: Wed, 08 Jan 2025 17:58:07 GMT  
		Size: 18.8 MB (18849783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728c7914f544bf3f45e01d7a92f1ec9bd4d0f74f8279cf05e3fec45d6e3330d7`  
		Last Modified: Wed, 08 Jan 2025 17:58:07 GMT  
		Size: 18.8 MB (18798856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7588327f44f74c8cfb1df740b4b112bb9f349bea682699af57bce24c05cc282`  
		Last Modified: Wed, 08 Jan 2025 17:58:07 GMT  
		Size: 19.3 MB (19295660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212466ce3060eb51a55ca7cf64d97bf0e233dddf9601a6dc91616bda989f5492`  
		Last Modified: Wed, 08 Jan 2025 17:58:07 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804b79a204afdb2c58388b282b8ed120b0dc158fa22a5c2d2923a3bf5db3c694`  
		Last Modified: Wed, 08 Jan 2025 17:58:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7fc56b24e6aa15361bc928b8d0f71e680d193590e02cd51997ae117cff498a`  
		Last Modified: Wed, 08 Jan 2025 17:58:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ce56b066b7f1a2e1cb04c0ed90445bad38b8c414a9c27006b3ca3098425bd4`  
		Last Modified: Wed, 08 Jan 2025 18:22:38 GMT  
		Size: 6.7 MB (6733426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2551a79e473f82b2cb73722fa4d175a9725291d437bea02e2dde16d078dfbbd4`  
		Last Modified: Wed, 08 Jan 2025 18:22:38 GMT  
		Size: 89.4 KB (89424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422eaf51f4a3d2557c721bb2fbf4aa5c6da8a6192e02775a6b75bcb7180c6303`  
		Last Modified: Wed, 08 Jan 2025 18:22:38 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c27f02717d15f06e8cd063d7ec087252029a32b52779b32237536e0ee0f87d`  
		Last Modified: Wed, 08 Jan 2025 18:22:39 GMT  
		Size: 58.3 MB (58323493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b0fe9078f68b5f22dd608a929bf185a70bc1542b81dd94568b3a4fe38b96eb`  
		Last Modified: Wed, 08 Jan 2025 18:22:38 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c71dab6b9c4bb76b0a2ea08f1a1bbd61984f942774c226e982c3df443a6f25`  
		Last Modified: Wed, 08 Jan 2025 18:22:39 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7785a798c937c018cdd3af2bc144cde3d83fc6e2d4561d43e729aa4ce2ba0bd6`  
		Last Modified: Wed, 08 Jan 2025 19:14:13 GMT  
		Size: 986.6 KB (986568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f3c57dde844bb8f32338ac28634833e1b0ecf9c68038f1e5fba34c99448319`  
		Last Modified: Wed, 08 Jan 2025 19:14:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e08e8dc62e5d70a45ee064e0d7099f277f734f228fca074e25aa3c272875be4`  
		Last Modified: Wed, 08 Jan 2025 19:14:14 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9db7c4c5c7db7b21c74bb66c42c0386efd80d9bbce8f72b4c0fd1260456b564`  
		Last Modified: Wed, 08 Jan 2025 19:14:14 GMT  
		Size: 21.3 MB (21303853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db86b7a4cedf0254eb848cb16f4e777de211523c2a434ed700c1702531363d4`  
		Last Modified: Wed, 08 Jan 2025 19:14:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:05f6c80ec8c0eeb899b85e0e3a28d5adda70a06d1cbda0d91a79c02ae96a432f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b897f0fbff33981fd884379ac6c6905c99102fc368d0e53155461b9430ee389`

```dockerfile
```

-	Layers:
	-	`sha256:7e91067358821cab24d7139af9408a02b8db780469933c9d0305a3cab6846d84`  
		Last Modified: Wed, 08 Jan 2025 19:14:13 GMT  
		Size: 30.4 KB (30370 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:68e187d8bd9277144d6aeae67b72fbcd979f00b44a267509921988c3bf70d9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149760488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aaadf33d10cb82e7efa4e7f7ce90fc0776195db51ef0bf0c4184d988e8443f4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 23 Dec 2024 12:04:24 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
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
# Mon, 23 Dec 2024 12:04:24 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.5.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.5.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 23 Dec 2024 12:04:24 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 23 Dec 2024 12:04:24 GMT
USER rootless
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd118a02a977501603a666f0534bd4e65d18527588ad5cf400f8c10d29b641a2`  
		Last Modified: Wed, 08 Jan 2025 18:21:52 GMT  
		Size: 8.1 MB (8073087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7344f9e39163b0db1d8cc353b60bb1b0f4a1f5bce6103ce319dc4b80767896`  
		Last Modified: Wed, 08 Jan 2025 18:21:51 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9d0501c659e9996506457c271e935b286b1a36410eeba8026d42730c469bde`  
		Last Modified: Wed, 08 Jan 2025 18:21:52 GMT  
		Size: 17.8 MB (17795775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c13fd75e9ccda9d1d254561f4bbbb148870f59ca6f4b024cd65844a98cb71cb`  
		Last Modified: Wed, 08 Jan 2025 18:21:52 GMT  
		Size: 17.1 MB (17106460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85bcd21765cb8c05d3739bcd1fb5482cbb351da6b1ad78fe38f3b9951dad85d`  
		Last Modified: Wed, 08 Jan 2025 18:21:54 GMT  
		Size: 17.6 MB (17642749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bb73011f2d3c9afe5ebd89ba6f896b42afb86f59c361549393c69cabc91720`  
		Last Modified: Wed, 08 Jan 2025 18:21:53 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3943034a025077136d95699e23a430ae80a733bcf578ba514dba74b0a1e1cd0`  
		Last Modified: Wed, 08 Jan 2025 18:21:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5550cda41ef4efe67333dba99c08cf7b06cf3f4b175838e8c086f1040d4b3b`  
		Last Modified: Wed, 08 Jan 2025 18:21:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3a896f7a68e0f48326a593f2cce10ad547a4322b9970818e57174e93f34aaa`  
		Last Modified: Thu, 09 Jan 2025 06:32:13 GMT  
		Size: 7.0 MB (6981996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e612b84bc88030d8f8d806c83dc0506c270c4893d4d83de133c47e7af48ef713`  
		Last Modified: Thu, 09 Jan 2025 06:32:13 GMT  
		Size: 97.8 KB (97784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598dddec7f951f177c12864ccb158ed3a942f6d37e301f65d09cf0d00e63483a`  
		Last Modified: Thu, 09 Jan 2025 06:32:13 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a11a51928abd5966a87eb055d8e90c81a1f22da87471d109da2c96872fb1e4`  
		Last Modified: Thu, 09 Jan 2025 06:32:15 GMT  
		Size: 53.9 MB (53891628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55843b928240fd4a75cda0f4ef221b7e844651046fc1d5f5c84b41e056a52e21`  
		Last Modified: Thu, 09 Jan 2025 06:32:14 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e97719df89f4c6ff945aa2a3a70cbb56806b9a2d1fbe0e358b66f0af472a801`  
		Last Modified: Thu, 09 Jan 2025 06:32:14 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83f9c9486195a50ce8ea03cddcd0ffe6dcb5ee7a9cf08dfd9bc9cfe60c0a6f2`  
		Last Modified: Thu, 09 Jan 2025 08:49:20 GMT  
		Size: 1.0 MB (1014209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306a67d42f29d78c0c17832f0bc86256f738c87d306d41b23af19167ab9a0150`  
		Last Modified: Thu, 09 Jan 2025 08:49:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80115f085bd5ab957bfccee71e23c181bd1796d7bd61d1ee8f4dba4de6f3261e`  
		Last Modified: Thu, 09 Jan 2025 08:49:22 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9352c64859a849db86df8ca2713f799715dcd3601c56af245178e68e714089f9`  
		Last Modified: Thu, 09 Jan 2025 08:49:24 GMT  
		Size: 23.2 MB (23155142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490851dfb2f53f71f5cbdd41bce16fcb77942621bb3468c6ae20caf52c6e176f`  
		Last Modified: Thu, 09 Jan 2025 08:49:24 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6298f08c1eb8c457ff8970d23d672ad684e6fa48777fc12955d65a69818bf456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f1578cb007eb4d89c4c990bdbdfcfabe9bb03d6d0fe0791f27af4e75375a0e`

```dockerfile
```

-	Layers:
	-	`sha256:d639be882db8921eda84e4d1ee9a3c878011462e54346edf38f592004b48778b`  
		Last Modified: Thu, 09 Jan 2025 08:49:23 GMT  
		Size: 30.5 KB (30527 bytes)  
		MIME: application/vnd.in-toto+json
