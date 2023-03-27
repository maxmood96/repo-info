## `docker:git`

```console
$ docker pull docker@sha256:cb2aae290d6b41faf9e26f3913d11d969e4860e664a747cea3013eb20d75cc3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:ef1160cd232534af54294ce3bc584b9a2ca3fdd553ac1cb4d9ff0a6508fbd0e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58190220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d245a1dfff410787603a516c33e856cc74c73e25610972ec3c8310a3cc5c54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Tue, 14 Mar 2023 00:19:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Tue, 14 Mar 2023 00:19:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Tue, 14 Mar 2023 00:19:39 GMT
ENV DOCKER_VERSION=23.0.1
# Tue, 14 Mar 2023 00:19:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Tue, 14 Mar 2023 00:19:43 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 14 Mar 2023 00:19:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Mon, 27 Mar 2023 22:23:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.2
# Mon, 27 Mar 2023 22:23:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-x86_64'; 			sha256='895e20812231543eae9f6b98ef9395327f4f21f1f31fa51fc252d21415802dda'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-armv6'; 			sha256='16a2ce7e9bc45cb864020fb61a4da7425162cb5215ee7c81c48f98b6a7c945c4'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-armv7'; 			sha256='4c8948696831fde2992e82dfcb505c5d6e4a56df9d759cd39a1dee6b6cded1c0'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-aarch64'; 			sha256='fcc2a21588907a7e6d9aa83538f134d2916f7a756cf391e5ce11b9d67bc4aad0'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-ppc64le'; 			sha256='546e0421cda6f0bbedd82efc2d95daf9775ec736ae0c82bcdc051c952eee09cd'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-riscv64'; 			sha256='65824b6aad564debb5ae9f70423f94bf5bbf20062fa4d9d47d2d2bcaf6a822b7'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-s390x'; 			sha256='4fcf6d847203162eb0a698657b98007542047c167188df3c65cca047b4b656c0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Mar 2023 22:23:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Mar 2023 22:23:06 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Mar 2023 22:23:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Mar 2023 22:23:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Mar 2023 22:23:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Mar 2023 22:23:07 GMT
CMD ["sh"]
# Mon, 27 Mar 2023 22:23:30 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79632185ca8edd2f81e00df639abe673c41d8eccdaf5645018f84176515ec993`  
		Last Modified: Tue, 14 Mar 2023 00:21:02 GMT  
		Size: 2.1 MB (2063925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96acd0207079f4bb502230e442b915f42f6fdf9a5a529df671e43170af4921a3`  
		Last Modified: Tue, 14 Mar 2023 00:21:03 GMT  
		Size: 16.2 MB (16220359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9b23e3d65924a9a6c0966e8b8f5c404bdf7309d3dbe1272de7d17c4aad5f0a`  
		Last Modified: Tue, 14 Mar 2023 00:21:02 GMT  
		Size: 16.0 MB (16001693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2860b8252eee309d93b431d781779ac8a28f0cebd16597b7eeb5f24bfaa43df8`  
		Last Modified: Mon, 27 Mar 2023 22:24:22 GMT  
		Size: 16.4 MB (16375123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc699d02dda65a83714d8de11f782e82627fac5f66b16c206ba1e08428b55a0`  
		Last Modified: Mon, 27 Mar 2023 22:24:19 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa39c007c49b4597875b385a6a26ab1fd72ec83c53ba13a51aa01ce6a873d397`  
		Last Modified: Mon, 27 Mar 2023 22:24:19 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794e3b1c8fe98c2ced50f8fcd9a3922080139355560407e5df75873572515eb6`  
		Last Modified: Mon, 27 Mar 2023 22:24:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c52886848357daee157cbb6a5742e460c370299028ae33688b845f6ed8c2ab`  
		Last Modified: Mon, 27 Mar 2023 22:25:28 GMT  
		Size: 4.2 MB (4152944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5f3f2c9d38d0d8c16eb9d81c85764bb700353905adb2825ecde0d9b806002dce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54062007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c9b99da752573e6b22fed72b5f5d5291bd15269cadb19b7cfe2005d09adf16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Tue, 14 Mar 2023 00:39:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Tue, 14 Mar 2023 00:39:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Tue, 14 Mar 2023 00:39:26 GMT
ENV DOCKER_VERSION=23.0.1
# Tue, 14 Mar 2023 00:39:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Tue, 14 Mar 2023 00:39:31 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 14 Mar 2023 00:39:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Mon, 27 Mar 2023 22:41:45 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.2
# Mon, 27 Mar 2023 22:41:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-x86_64'; 			sha256='895e20812231543eae9f6b98ef9395327f4f21f1f31fa51fc252d21415802dda'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-armv6'; 			sha256='16a2ce7e9bc45cb864020fb61a4da7425162cb5215ee7c81c48f98b6a7c945c4'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-armv7'; 			sha256='4c8948696831fde2992e82dfcb505c5d6e4a56df9d759cd39a1dee6b6cded1c0'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-aarch64'; 			sha256='fcc2a21588907a7e6d9aa83538f134d2916f7a756cf391e5ce11b9d67bc4aad0'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-ppc64le'; 			sha256='546e0421cda6f0bbedd82efc2d95daf9775ec736ae0c82bcdc051c952eee09cd'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-riscv64'; 			sha256='65824b6aad564debb5ae9f70423f94bf5bbf20062fa4d9d47d2d2bcaf6a822b7'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-s390x'; 			sha256='4fcf6d847203162eb0a698657b98007542047c167188df3c65cca047b4b656c0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Mar 2023 22:41:48 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Mar 2023 22:41:48 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Mar 2023 22:41:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Mar 2023 22:41:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Mar 2023 22:41:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Mar 2023 22:41:49 GMT
CMD ["sh"]
# Mon, 27 Mar 2023 22:42:09 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1173461b5ecef3415b4ac3667e3fa411fde1f1de59ebd55382468436e35659d6`  
		Last Modified: Tue, 14 Mar 2023 00:40:51 GMT  
		Size: 2.0 MB (2036661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c470f9a84de1191669030a6b3e5ff5eae92cc3634bdc4369f5886691cd1493`  
		Last Modified: Tue, 14 Mar 2023 00:40:52 GMT  
		Size: 15.3 MB (15294711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ac63e805444d1ba480b909046597a8d37e29428b4f57b028527d8fdf76c49f`  
		Last Modified: Tue, 14 Mar 2023 00:40:50 GMT  
		Size: 14.4 MB (14441446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7098a89c12364441074dad63b13de6e8cd1acf46af17b559d9ff92efe2dd7235`  
		Last Modified: Mon, 27 Mar 2023 22:42:58 GMT  
		Size: 14.8 MB (14830344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0568d7ff50394129bc850746679c67c381f006e6276277aba35a95178f94e157`  
		Last Modified: Mon, 27 Mar 2023 22:42:56 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a92f53666b01432ceae66a55a0e3e7f2be5ba16aabc165ef5d0b53f8395054`  
		Last Modified: Mon, 27 Mar 2023 22:42:56 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e943fe71769daa78a8378e808e2de6d6af25bc5166c23f3e328052a4529ae08`  
		Last Modified: Mon, 27 Mar 2023 22:42:56 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37e6aec8655758f4d2c78b5c8adb39dc021972d9c938de4b87d9e1272073bfc`  
		Last Modified: Mon, 27 Mar 2023 22:43:59 GMT  
		Size: 4.2 MB (4195160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
