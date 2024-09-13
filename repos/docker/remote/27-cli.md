## `docker:27-cli`

```console
$ docker pull docker@sha256:6c9f1da3862b1ca5be1bf70d7ed12cc532ad022c0739e841dd46922c1d45b81c
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
$ docker pull docker@sha256:89b3e683bc443089a334ce5bd04ae81f5a061e8dfa2db38e24774dbbc91fb398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67579350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9fe1c2db032c493e657a13c3e0dee1e17e3037e33097bf53c1511a86773221`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 12 Sep 2024 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
ENV DOCKER_VERSION=27.2.1
# Thu, 12 Sep 2024 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Thu, 12 Sep 2024 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.3
# Thu, 12 Sep 2024 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-x86_64'; 			sha256='241b75fe0f8194a48d01f99d683aa1100579b21caa60d2d78c9c824855c57937'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-armv6'; 			sha256='4abff57472ce971e84ccd6d09287da02515e99e1a2208e867c5d03123a1c406d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-armv7'; 			sha256='37fabd59e170943e12b4945a1a85c853e7db4759091f16036787fa02f6e2ec0a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-aarch64'; 			sha256='10ded2b3b02b15957b1650b99d1e5ff216d882c5203a563d0aa7a87580a0d8ca'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-ppc64le'; 			sha256='f8c63bcc8e8dca6703893c6fe909a10aef288bc347ee37922afc0099abf87946'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-riscv64'; 			sha256='9e51a8531b0db7f96b1ef8c9c27f104b4847c867af72056d3f7625b065cf9861'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-s390x'; 			sha256='3929a9d8a6a7a2521de7c2b148337f04dd360e30a2114a8200b123b398e97c35'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Sep 2024 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Sep 2024 17:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b73c950e7f3a32fd7ceb93726963d969961fd167a6d65b87d92b85f23d5894`  
		Last Modified: Thu, 12 Sep 2024 23:02:46 GMT  
		Size: 7.9 MB (7880485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc674fca04480f360447f23f5b6226a0136c2004211e1fdd5383f268a52857ca`  
		Last Modified: Thu, 12 Sep 2024 23:02:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4df0710d38a30fe74446b6fc15a9824de3ed1449a8a3ef483f369c97be57d1`  
		Last Modified: Thu, 12 Sep 2024 23:02:45 GMT  
		Size: 18.6 MB (18601178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6556e2ee6eafda8125d4630170735634cfb38a3381185bc72ad00672264841`  
		Last Modified: Thu, 12 Sep 2024 23:02:45 GMT  
		Size: 18.4 MB (18432738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5c00fb7e3c0a0d0743eda2b24f7b87c37b93b8cf425f56a6a09ad40b4ea476`  
		Last Modified: Thu, 12 Sep 2024 23:02:46 GMT  
		Size: 19.0 MB (19038987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee252a06ce3640f6b208505c2737471f84c115fcaa5965d11d9eeab7b15a107e`  
		Last Modified: Thu, 12 Sep 2024 23:02:46 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e82320323feca9f265f14ab1f1b237bf949f34fb4665705f2f841753e566b56`  
		Last Modified: Thu, 12 Sep 2024 23:02:46 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac89f463e2f9cb2edc81d58f0037df59c4182200cca3be345b2c42a88ecbe49`  
		Last Modified: Thu, 12 Sep 2024 23:02:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:cdb6d78065fddddb768081dc88b24bda6c6cdb0fa84f1f04385b3fee417f8b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3d9e01de0f42f3f3d69c1b31d91d0991db4e727f599ec742dbec8c4983be9d`

```dockerfile
```

-	Layers:
	-	`sha256:86eb8e3260a765e2c4cbee2231e7854726bb7913dbb684a3223fc6ea7ad0cfd1`  
		Last Modified: Thu, 12 Sep 2024 23:02:45 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:71b3a48f3b6f55b500a6c65f72be98315c3962d0135be169d09244f1e28d1f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62855178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7361c0e11037596420a011b72b78dd06e372d4cb4c21c22449e2c295b052be70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 12 Sep 2024 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
ENV DOCKER_VERSION=27.2.1
# Thu, 12 Sep 2024 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Thu, 12 Sep 2024 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.3
# Thu, 12 Sep 2024 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-x86_64'; 			sha256='241b75fe0f8194a48d01f99d683aa1100579b21caa60d2d78c9c824855c57937'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-armv6'; 			sha256='4abff57472ce971e84ccd6d09287da02515e99e1a2208e867c5d03123a1c406d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-armv7'; 			sha256='37fabd59e170943e12b4945a1a85c853e7db4759091f16036787fa02f6e2ec0a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-aarch64'; 			sha256='10ded2b3b02b15957b1650b99d1e5ff216d882c5203a563d0aa7a87580a0d8ca'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-ppc64le'; 			sha256='f8c63bcc8e8dca6703893c6fe909a10aef288bc347ee37922afc0099abf87946'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-riscv64'; 			sha256='9e51a8531b0db7f96b1ef8c9c27f104b4847c867af72056d3f7625b065cf9861'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-s390x'; 			sha256='3929a9d8a6a7a2521de7c2b148337f04dd360e30a2114a8200b123b398e97c35'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Sep 2024 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Sep 2024 17:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1aa033c3dd6f9dcabf3e5db8b0d23e75bacc18083a9fc5fc3bf8dd32b531c9`  
		Last Modified: Wed, 11 Sep 2024 02:01:30 GMT  
		Size: 17.1 MB (17141620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb697e41a6cf989909a1ffd4bdc4e0568f8b77fdff1bcdfa5e73a93153b74af`  
		Last Modified: Thu, 12 Sep 2024 23:19:17 GMT  
		Size: 17.9 MB (17891123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258123d90a2142af3caa748dbbdb8d8bae3759288f77abcd838b4d779ff4f54c`  
		Last Modified: Thu, 12 Sep 2024 23:19:16 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac1a5ac2c4218893716024623e9ac2090aa96186597eedbbe4894c00061d10b`  
		Last Modified: Thu, 12 Sep 2024 23:19:17 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04933fb9b3e0fe8e1a58d06ea518fa9b731e8343c509c6e1c1b21711e01cbcf2`  
		Last Modified: Thu, 12 Sep 2024 23:19:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a7714f34f9298f4b8f61430d1b9c33090e5d0007ba737a19869e930671652e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b8568a5c2583564de32d950b6beab5661a7938038ff5e32ccbfe89075d8310`

```dockerfile
```

-	Layers:
	-	`sha256:c056efab7d1d68069b4a2a9e4ab527d047821d9f1dc7db5c6d0a8a18b7d0fa17`  
		Last Modified: Thu, 12 Sep 2024 23:19:16 GMT  
		Size: 38.1 KB (38070 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:827b20386b50d2962129587b4157d190fa18d4ef3b4b71b06eb9d7ed04b2d427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61877695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b707075faa4ad333f878cf8cd45034ccbb7165d768ca103b971fb2402dda03f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 12 Sep 2024 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
ENV DOCKER_VERSION=27.2.1
# Thu, 12 Sep 2024 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Thu, 12 Sep 2024 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.3
# Thu, 12 Sep 2024 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-x86_64'; 			sha256='241b75fe0f8194a48d01f99d683aa1100579b21caa60d2d78c9c824855c57937'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-armv6'; 			sha256='4abff57472ce971e84ccd6d09287da02515e99e1a2208e867c5d03123a1c406d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-armv7'; 			sha256='37fabd59e170943e12b4945a1a85c853e7db4759091f16036787fa02f6e2ec0a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-aarch64'; 			sha256='10ded2b3b02b15957b1650b99d1e5ff216d882c5203a563d0aa7a87580a0d8ca'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-ppc64le'; 			sha256='f8c63bcc8e8dca6703893c6fe909a10aef288bc347ee37922afc0099abf87946'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-riscv64'; 			sha256='9e51a8531b0db7f96b1ef8c9c27f104b4847c867af72056d3f7625b065cf9861'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-s390x'; 			sha256='3929a9d8a6a7a2521de7c2b148337f04dd360e30a2114a8200b123b398e97c35'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Sep 2024 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Sep 2024 17:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cf2b1859f16ea4a3efc3ebdcff929c005fc44c05d7202ce69bbd5258d6989a`  
		Last Modified: Wed, 11 Sep 2024 02:01:58 GMT  
		Size: 17.1 MB (17129209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c141c6e33210dfb2c6b052e8a54a9902272d20cca356ac70681658d985fca1`  
		Last Modified: Fri, 13 Sep 2024 03:51:28 GMT  
		Size: 17.9 MB (17873150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956f54e00ee505b794adf0581e0f3090f285ecbf7bc6ccb3218f3c95755b752f`  
		Last Modified: Fri, 13 Sep 2024 03:51:28 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626127f8564a5ed1e725bf0d9efe271ea397cdefc51160c22630dbb7b31a4b60`  
		Last Modified: Fri, 13 Sep 2024 03:51:28 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868eee0786e8e53ff53835ebbac487ad62251eaa3ae0bb30050a012715521c3f`  
		Last Modified: Fri, 13 Sep 2024 03:51:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:48fdacc26fe3f85724861bc1ca9e24bab121dcc1e30b9e1c171dcda3d57041f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc32657d9cb964588b33f4b465fa696f900cff328de7601e17d1d501d8087e62`

```dockerfile
```

-	Layers:
	-	`sha256:0b6c0390d5e2a3d24c973348fa1a7d04e34f03bfc7996b5cc013851b35232dbb`  
		Last Modified: Fri, 13 Sep 2024 03:51:27 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5f993021a73353832d6c14947d64058abb9f4ab90d17e7fea27b6c7ab5ff1ed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63837168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80af79c68369557ec55041dc65ac41e089d981d789d5d2e5b9de21668b13ecd3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 12 Sep 2024 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
ENV DOCKER_VERSION=27.2.1
# Thu, 12 Sep 2024 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Thu, 12 Sep 2024 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.3
# Thu, 12 Sep 2024 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-x86_64'; 			sha256='241b75fe0f8194a48d01f99d683aa1100579b21caa60d2d78c9c824855c57937'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-armv6'; 			sha256='4abff57472ce971e84ccd6d09287da02515e99e1a2208e867c5d03123a1c406d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-armv7'; 			sha256='37fabd59e170943e12b4945a1a85c853e7db4759091f16036787fa02f6e2ec0a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-aarch64'; 			sha256='10ded2b3b02b15957b1650b99d1e5ff216d882c5203a563d0aa7a87580a0d8ca'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-ppc64le'; 			sha256='f8c63bcc8e8dca6703893c6fe909a10aef288bc347ee37922afc0099abf87946'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-riscv64'; 			sha256='9e51a8531b0db7f96b1ef8c9c27f104b4847c867af72056d3f7625b065cf9861'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-s390x'; 			sha256='3929a9d8a6a7a2521de7c2b148337f04dd360e30a2114a8200b123b398e97c35'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Sep 2024 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Sep 2024 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Sep 2024 17:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbb813c4053e6c015d7f5fcb6793b026b26b1df3c62961c091a3a6d14d557f6`  
		Last Modified: Fri, 13 Sep 2024 01:52:16 GMT  
		Size: 17.4 MB (17409484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2480d419e95acd54ba45b7f4041b382bfd61cb82d6ff75519e474d137363268c`  
		Last Modified: Fri, 13 Sep 2024 01:52:15 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af427d473f0363101e2e26495d126b44bbbf6dc1fe133afcc289aa523eb7471d`  
		Last Modified: Fri, 13 Sep 2024 01:52:15 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d178fe3d6363af31c38f932fddf70aa61fb48e578ece2a361c102eca033cc51`  
		Last Modified: Fri, 13 Sep 2024 01:52:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6d631c8a9de655a4029d2795e5f14260e2ba2eeacf9764daf8c5fd7107c83c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70b0c9d1012e93d1b4d023699c52a27e65cb25ea3d15154cb71ec7a935e9de7`

```dockerfile
```

-	Layers:
	-	`sha256:a8d560ae7ea38809061995673f252cb9d7b09eb60bb9f0e3bd6ef8c68b76e008`  
		Last Modified: Fri, 13 Sep 2024 01:52:15 GMT  
		Size: 38.2 KB (38227 bytes)  
		MIME: application/vnd.in-toto+json
