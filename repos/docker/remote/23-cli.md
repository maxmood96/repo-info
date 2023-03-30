## `docker:23-cli`

```console
$ docker pull docker@sha256:a3a5b560b6b4c4005eba5ebbd3311830826402adbd9cb93e33252999375358eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23-cli` - linux; amd64

```console
$ docker pull docker@sha256:bc0d012483a9663eca61f690456be9857b221a8439d943ae65be46ae6d86d263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54050317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d5a38ff53d15ec9c1955d1ece6ab27f35a5cd69a5c16d90a42c26591b03cff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 18:19:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 29 Mar 2023 18:19:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 29 Mar 2023 18:19:24 GMT
ENV DOCKER_VERSION=23.0.2
# Wed, 29 Mar 2023 18:19:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 29 Mar 2023 18:19:24 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 29 Mar 2023 18:19:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 29 Mar 2023 18:19:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.2
# Wed, 29 Mar 2023 18:19:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-x86_64'; 			sha256='895e20812231543eae9f6b98ef9395327f4f21f1f31fa51fc252d21415802dda'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-armv6'; 			sha256='16a2ce7e9bc45cb864020fb61a4da7425162cb5215ee7c81c48f98b6a7c945c4'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-armv7'; 			sha256='4c8948696831fde2992e82dfcb505c5d6e4a56df9d759cd39a1dee6b6cded1c0'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-aarch64'; 			sha256='fcc2a21588907a7e6d9aa83538f134d2916f7a756cf391e5ce11b9d67bc4aad0'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-ppc64le'; 			sha256='546e0421cda6f0bbedd82efc2d95daf9775ec736ae0c82bcdc051c952eee09cd'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-riscv64'; 			sha256='65824b6aad564debb5ae9f70423f94bf5bbf20062fa4d9d47d2d2bcaf6a822b7'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-s390x'; 			sha256='4fcf6d847203162eb0a698657b98007542047c167188df3c65cca047b4b656c0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 29 Mar 2023 18:19:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 29 Mar 2023 18:19:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Mar 2023 18:19:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 29 Mar 2023 18:19:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 29 Mar 2023 18:19:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["sh"]
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
	-	`sha256:634492f0d979fcfa35bf8dbef20f736e2c0f66dda48876a863e37ac3873fe32c`  
		Last Modified: Wed, 29 Mar 2023 18:45:23 GMT  
		Size: 16.2 MB (16233120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0374339fff0d35f7f529605c944ae273974d4d3aae91de301335767acf0205d6`  
		Last Modified: Wed, 29 Mar 2023 18:45:22 GMT  
		Size: 16.0 MB (16001790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140b66e8d8603c7fd0bb99e8a856d4c33d059234fbc00040d82c07d9917d6fb5`  
		Last Modified: Wed, 29 Mar 2023 18:45:22 GMT  
		Size: 16.4 MB (16375110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e994128f0f06c3e1548e880464a633e31eea3ef12bfc537db379c58bae7a56`  
		Last Modified: Wed, 29 Mar 2023 18:45:19 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a555f71dffd819a5fd451dc9e99a4ef4e444f6362c49c35c51b9b741403339`  
		Last Modified: Wed, 29 Mar 2023 18:45:19 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11783ff70e21df88aed96d968fa3480259ea787c8cec99e6000d787959add5cc`  
		Last Modified: Wed, 29 Mar 2023 18:45:19 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5ebd1ab266c1e907c3a9125ca280676fbfac41e2fc52034bef7b43f50351e18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49879157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced2f7f6bc26aebd3703be20a4b7aae094c4558eb73f376a32d5cdea939d39a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:18 GMT
ADD file:e51d4089e73ad6dee52b31f0c8059a00c17df6e23f6741fe11b43bd84cc99008 in / 
# Wed, 29 Mar 2023 17:39:18 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 17:39:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 29 Mar 2023 17:39:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 29 Mar 2023 17:39:18 GMT
ENV DOCKER_VERSION=23.0.2
# Wed, 29 Mar 2023 17:39:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 29 Mar 2023 17:39:18 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 29 Mar 2023 17:39:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 29 Mar 2023 17:39:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.2
# Wed, 29 Mar 2023 17:39:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-x86_64'; 			sha256='895e20812231543eae9f6b98ef9395327f4f21f1f31fa51fc252d21415802dda'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-armv6'; 			sha256='16a2ce7e9bc45cb864020fb61a4da7425162cb5215ee7c81c48f98b6a7c945c4'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-armv7'; 			sha256='4c8948696831fde2992e82dfcb505c5d6e4a56df9d759cd39a1dee6b6cded1c0'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-aarch64'; 			sha256='fcc2a21588907a7e6d9aa83538f134d2916f7a756cf391e5ce11b9d67bc4aad0'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-ppc64le'; 			sha256='546e0421cda6f0bbedd82efc2d95daf9775ec736ae0c82bcdc051c952eee09cd'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-riscv64'; 			sha256='65824b6aad564debb5ae9f70423f94bf5bbf20062fa4d9d47d2d2bcaf6a822b7'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-s390x'; 			sha256='4fcf6d847203162eb0a698657b98007542047c167188df3c65cca047b4b656c0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 29 Mar 2023 17:39:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 29 Mar 2023 17:39:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Mar 2023 17:39:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 29 Mar 2023 17:39:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 29 Mar 2023 17:39:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 17:39:18 GMT
CMD ["sh"]
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
	-	`sha256:f7bec6e2df285849c47f49df6602301832eb8b4378cbcc8c199978a564c9eaa1`  
		Last Modified: Thu, 30 Mar 2023 05:48:10 GMT  
		Size: 15.3 MB (15307065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5b666dfe6d5587ec27c8e4b5c91a3c2e78854e77c589335c0e03804683bb64`  
		Last Modified: Thu, 30 Mar 2023 05:48:08 GMT  
		Size: 14.4 MB (14441458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8d43fea4f0b07c65009787fb7283d7a8a0095c13e4e6c2ba42012cf6423bea`  
		Last Modified: Thu, 30 Mar 2023 05:48:08 GMT  
		Size: 14.8 MB (14830416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f66b40b57a1d23d3e17592e6e560415d18fdd76bcd11e7c088499ff1a34073f`  
		Last Modified: Thu, 30 Mar 2023 05:48:06 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5489bd927b8bc23d3bbbb5fb1a8b1e68dd0be3458855dbcfb9bb0975d8cb6806`  
		Last Modified: Thu, 30 Mar 2023 05:48:07 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff23b781bb55cba28399d68c3e947d4dd7d50eca0e9f05c92f828721ebf57a5a`  
		Last Modified: Thu, 30 Mar 2023 05:48:07 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
