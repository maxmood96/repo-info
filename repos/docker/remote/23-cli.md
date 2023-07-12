## `docker:23-cli`

```console
$ docker pull docker@sha256:0a2f759eac9befb5b44bf6a918d5b53944f1f14e869ef9564fddaa2a5e330a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23-cli` - linux; amd64

```console
$ docker pull docker@sha256:6138f085aa8ca0d8e6f4d9e06cf9248595522dc756baf5ed3a3adaa8c86756a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57107804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af261a0809a5e00bd197f841f9172950efa954ccc5db953d718b995c9e85232`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Tue, 11 Jul 2023 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 11 Jul 2023 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Jul 2023 17:04:15 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 11 Jul 2023 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Jul 2023 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Tue, 11 Jul 2023 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Jul 2023 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.20.0
# Tue, 11 Jul 2023 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.20.0/docker-compose-linux-x86_64'; 			sha256='b49e358d11c198fa228fb7eca2a177affd8e1e33e06d29940668668482f797cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.20.0/docker-compose-linux-armv6'; 			sha256='72a0362081a268eb2410a4e57ec0df466ff2eb34e38ffb5552f9a6e58213758d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.20.0/docker-compose-linux-armv7'; 			sha256='a5f181e83a78f5ab8c202f99713bc745712acbf387d9d2ce687c76e1ccdb36e2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.20.0/docker-compose-linux-aarch64'; 			sha256='f82c5bc86cb0937628ae616087224aa7d02372d50e638eca646d5834c6766ee7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.20.0/docker-compose-linux-ppc64le'; 			sha256='2a8e638362cd3dc1f739b49066cf9f4d0d21e6e46f082d359c82c7d0c8081eee'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.20.0/docker-compose-linux-riscv64'; 			sha256='5e5c89c6ce73d0f4aa1d01542fc287c97880d0ecb1766162c34b3a7b2852a50f'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.20.0/docker-compose-linux-s390x'; 			sha256='d58d6545d9d88f24a495199e4a438cf10351416b7655acda334e0e9e8448177c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Jul 2023 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Jul 2023 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jul 2023 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Jul 2023 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Jul 2023 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 17:04:15 GMT
CMD ["sh"]
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
	-	`sha256:8cbbfe9c78c82698902d2f699f3a866996d040be1686dd10f629e37d89ea33ee`  
		Last Modified: Thu, 15 Jun 2023 05:28:31 GMT  
		Size: 16.3 MB (16250874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5708dec9aea531c023a63cb6d674e4e42d94d8d84f51fcb66e9ced1c260f9e8e`  
		Last Modified: Thu, 06 Jul 2023 20:22:30 GMT  
		Size: 17.5 MB (17453587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf554b0341340bba9ca8f40a34b996d1189987b02e6459e40af91689923c2b2`  
		Last Modified: Tue, 11 Jul 2023 22:24:23 GMT  
		Size: 18.0 MB (17989258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c819f276701a37a6450afbb3cfadae11de1f95d3743651206aa3c7ddb5345876`  
		Last Modified: Tue, 11 Jul 2023 22:24:21 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375415ef3e5823e8ee70740b214761ad1cb48f2a4047d20507efedf2d54026ab`  
		Last Modified: Tue, 11 Jul 2023 22:24:21 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e140755a240b025a4d883b157975a1462401a6f3f494280321dd57f89f6c551a`  
		Last Modified: Tue, 11 Jul 2023 22:24:20 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:52097a1dd7c3d7d3e38d783dda0b7de8eeacc884f1417c4efa4506dd9c6ab58c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52767477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadb22f966b496f505956206aef220f706f218fcc7ebf0254559d169042fa335`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Tue, 11 Jul 2023 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 11 Jul 2023 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 11 Jul 2023 17:04:15 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 11 Jul 2023 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 11 Jul 2023 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Tue, 11 Jul 2023 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-amd64'; 			sha256='34927047282ef9052f57809fe94783b2dc0ab556fdd60c2c0b7f4e6e5f05a53b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v6'; 			sha256='ec7b60a4946c7c0fdaa3a44590adc08a0ead0ecca860358c57ca62d3e9a3a0be'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm-v7'; 			sha256='d122ec20622a744419fea021fd4850edc56d816b5cbc746d1f90184dbc227fec'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-arm64'; 			sha256='1649de43c6477eb8bf615f0817932e69e500ce530422bed47c9f3a689baeb788'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-ppc64le'; 			sha256='78cfc6cdb3982770ce4e922e62c42ee0750b4b2837349661d20834356f004d16'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-riscv64'; 			sha256='1d932a0925e9aee66c85cb7a351e9dbd210294ccb8d01208bf953108ad321f4d'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.linux-s390x'; 			sha256='89466f278264f597d3c81e5230ab5795b2578ad62d2c7e8f8be398546e02c3d7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 11 Jul 2023 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.20.0
# Tue, 11 Jul 2023 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.20.0/docker-compose-linux-x86_64'; 			sha256='b49e358d11c198fa228fb7eca2a177affd8e1e33e06d29940668668482f797cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.20.0/docker-compose-linux-armv6'; 			sha256='72a0362081a268eb2410a4e57ec0df466ff2eb34e38ffb5552f9a6e58213758d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.20.0/docker-compose-linux-armv7'; 			sha256='a5f181e83a78f5ab8c202f99713bc745712acbf387d9d2ce687c76e1ccdb36e2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.20.0/docker-compose-linux-aarch64'; 			sha256='f82c5bc86cb0937628ae616087224aa7d02372d50e638eca646d5834c6766ee7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.20.0/docker-compose-linux-ppc64le'; 			sha256='2a8e638362cd3dc1f739b49066cf9f4d0d21e6e46f082d359c82c7d0c8081eee'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.20.0/docker-compose-linux-riscv64'; 			sha256='5e5c89c6ce73d0f4aa1d01542fc287c97880d0ecb1766162c34b3a7b2852a50f'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.20.0/docker-compose-linux-s390x'; 			sha256='d58d6545d9d88f24a495199e4a438cf10351416b7655acda334e0e9e8448177c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 11 Jul 2023 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 11 Jul 2023 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jul 2023 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 11 Jul 2023 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 11 Jul 2023 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 17:04:15 GMT
CMD ["sh"]
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
	-	`sha256:c51d2d067e69a1f5a948d2d1133441f75a192e5bcc4154ca7be51943ff4a24d5`  
		Last Modified: Wed, 14 Jun 2023 22:42:12 GMT  
		Size: 15.3 MB (15325099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f28a2d02144ee951238b5623115d8fe18645df105f9e258b004975a591788`  
		Last Modified: Thu, 06 Jul 2023 19:43:51 GMT  
		Size: 15.8 MB (15759517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b4a7f989c8217386aa58f71d589edacb6aa6014387c5908eae8724bf379785`  
		Last Modified: Tue, 11 Jul 2023 22:43:38 GMT  
		Size: 16.3 MB (16327244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f57b97e16b187448099301ce7953db3cde58d921b473ee6646cf9d1305d8e9`  
		Last Modified: Tue, 11 Jul 2023 22:43:36 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6098d7778cc15523ef58d47763ae6e0946ddfc046aef50b29aa7198b1aab34f2`  
		Last Modified: Tue, 11 Jul 2023 22:43:36 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2b192e859e1fad96743f49770a460093570575b868edd1ef1daf53e759cf1c`  
		Last Modified: Tue, 11 Jul 2023 22:43:36 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
