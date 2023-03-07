## `docker:git`

```console
$ docker pull docker@sha256:f95b2b2d168363f77fb2498bc5dc168ea3075c96ec66dc87f54767113019c71f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:bcd59702ddd31d877e824ec1beb699c4b8a285cbd22a29df1fb53c767f5d17bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57159058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25197288371c3dd3627a486fcc2eaf177813cf1a4427b7a94346bfd95caa9481`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Tue, 07 Mar 2023 19:39:58 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 07 Mar 2023 19:40:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Tue, 07 Mar 2023 19:40:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Tue, 07 Mar 2023 19:40:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 07 Mar 2023 19:40:03 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 07 Mar 2023 19:40:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 07 Mar 2023 19:40:03 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Mar 2023 19:40:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 07 Mar 2023 19:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Mar 2023 19:40:04 GMT
CMD ["sh"]
# Tue, 07 Mar 2023 19:40:28 GMT
RUN apk add --no-cache git
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
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dc96e583396dc04a040a8ac1b599776195684683c8b400026f510df27eb5d1`  
		Last Modified: Tue, 07 Mar 2023 19:41:40 GMT  
		Size: 16.0 MB (16001693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c007c9e333b949ea9a70201ea5255ec5a3a88081ede8ea3ac5966585ee46a24`  
		Last Modified: Tue, 07 Mar 2023 19:41:43 GMT  
		Size: 15.3 MB (15343457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31b9f3137a18505841188b20a2a078ec13cfec0c012eb3ac6564b9f36ad10e7`  
		Last Modified: Tue, 07 Mar 2023 19:41:37 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782206789a08d4a0b5f7277a3960323085a14418b343394a39d0fcd8655b1fb1`  
		Last Modified: Tue, 07 Mar 2023 19:41:37 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e415889ffe259edce6eb2b4e5f73e100ec218ce333cad23232877d2da5ec5efa`  
		Last Modified: Tue, 07 Mar 2023 19:41:37 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a428b38d9be63538e594bcd66d761a70b9162729da0b7b682179fad053409c2`  
		Last Modified: Tue, 07 Mar 2023 19:42:53 GMT  
		Size: 4.2 MB (4152975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:596851f20d1b9b4087943a6499f94e329cfd85faa9e090471f297753a5229270
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53051021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd37181691b86ecbccf7b7ee8f88c57465861306ac9db53eb1153f39ffc9635`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Tue, 07 Mar 2023 19:41:52 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 07 Mar 2023 19:41:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Tue, 07 Mar 2023 19:41:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Tue, 07 Mar 2023 19:41:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 07 Mar 2023 19:41:59 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 07 Mar 2023 19:41:59 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 07 Mar 2023 19:41:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Mar 2023 19:41:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 07 Mar 2023 19:41:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Mar 2023 19:41:59 GMT
CMD ["sh"]
# Tue, 07 Mar 2023 19:42:22 GMT
RUN apk add --no-cache git
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
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ea4c438d18e17f6888a7baf3c2b2267cd0618bad0814132c1cccc6a5c67aea`  
		Last Modified: Tue, 07 Mar 2023 19:43:37 GMT  
		Size: 14.4 MB (14441450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74682fc31891ec2a65f71caf0d75552ecc7156f12a475e0dbc03985fdbc5a36b`  
		Last Modified: Tue, 07 Mar 2023 19:43:39 GMT  
		Size: 13.8 MB (13819067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f0314218eab9fd98058d0a13e3e5b50fc5b62a61c810a85c45d70c14ec6749`  
		Last Modified: Tue, 07 Mar 2023 19:43:35 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e58ca3baf0b96f6dec880163a8f2d8032ccf2a470433dcc693ab049164c08a5`  
		Last Modified: Tue, 07 Mar 2023 19:43:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8e21532cc6211c8d464a9e3f46c62ed3384d3b146ec5df74ee00c50c0cd5df`  
		Last Modified: Tue, 07 Mar 2023 19:43:35 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c354ac7eaa35e21f30f835ec237368bfdb2100d75f0300ad72c91060504b90`  
		Last Modified: Tue, 07 Mar 2023 19:44:47 GMT  
		Size: 4.2 MB (4195186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
