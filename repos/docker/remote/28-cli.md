## `docker:28-cli`

```console
$ docker pull docker@sha256:79bf825c5bed0d579820cc19f6857738abc424a680b619171591e969114f2015
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

### `docker:28-cli` - linux; amd64

```console
$ docker pull docker@sha256:407b05f8635f0c78530a074e5ac3d7ca547e494f41d0b8279eb378c957d59eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73996743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7ace64e87a3531934d9d783dd55b09fba672037fb47361e760477742f81dbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795da19ece39a2f3e799e489d3386b647d821a7e85ce5b46158fda8385c90ae`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661467c513c0068cd667d83c057ef762773b5ccf6aad8dca72be7b0e9e58e9e`  
		Last Modified: Tue, 04 Mar 2025 00:29:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec760ee5d6f28773e7cbf44a8a2b6b34fb4aa0d6fa6d0b614fc080d333c7676`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 19.5 MB (19500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c635aaeace6c21c4023ef00aa52d94d6562588edaa3aad82866677d7cd6a5ff`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 21.8 MB (21830052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14474db62f6d4f2619294ffb73aa5732222ebff4ce811b4a7b46a392f84987`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998be54fa1411f0ee896dc23f34ff26d9187f809346db77c1a808fb03dbcb953`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb44047f2a37f86a5f6b5e48070a7d913119ce8f1b209cb835655226264209`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edd909f3e7692f076d353fc1fe5c12f1c94db3cde6d2c554c3c65f97cdba45`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e83e577007c54ec761b3cc9df69167cff393d56c84b9982c5aeaff3dc875c360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb394d129acd56043f7f5fb7f10a740ff52c5b301d50e34652f30fc3f4968535`

```dockerfile
```

-	Layers:
	-	`sha256:4e8c6e0b6ddceec47cfd0a4b2d23a912d8a9825b3412c2492d4162b91835a3ee`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:eeb4ad44bd101ca297d84a0a0c3d0a65e9c0b45a038e0311f029cf84ea075f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68966316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9dc49b493ad218febee37e481279ef5472fa3bb9a9c005a77ea867233c0fda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f7bc764352ec86fba70db21ddeab29e555fe6bffb436bc5d212212d378f99`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 20.4 MB (20432360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7978e71e4b0a8ba81baf022cb3a734d0d6b005a7a3babd6414b3300e4458c62e`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 19.7 MB (19725898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9de33aa6df2b53c82eae086878b3e34c1c6cb5d0259e4369bc57a422f4be523`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccec5dd4325c3a0e62da84a7230a9f3d459d05ba0c2f3e9854f4319563e396e5`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82378aeb3d1e2aab7b8f2c4cff9675ec966ea134e12518f7ce032edad9c5f4a4`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:dc9b040b7560289fbd5081459c6b6ddecaaf4363ef2436ae6c2b925e0382e3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d631428cc9605f46e62098c617996c4c90c97ed9efb14436c836857db508b29`

```dockerfile
```

-	Layers:
	-	`sha256:1fcd6fd391dd1a77f96dadcb8f3583ac995b301d90af68b3d9e3b9937c3213d9`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:da6f62e7a4822d683c95524b9c38b7e39d43633a4d518865fc88807116650172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67972911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1523a85a50b40de6aa255336254486bbf1dc534c39a0f2dcb7a5f69afffde5d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117311ad7167b9553281abaa7235fd5f3832a7b012cfb6b899a8b4349598da64`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 7.3 MB (7299499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b971d99e53aeff617c5aaca904195a15aeb770e375b8cfc9a61a40c532f2c869`  
		Last Modified: Thu, 27 Feb 2025 01:59:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76c5d192a5373a5dfcf506e6f8e42c9a769bd40c46e970d7af316afbc14457`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 17.5 MB (17453605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aad7a6acb154ca593060d3e37bab904fc643be425607a808faf28baf102e3e0`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.4 MB (20410959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cbe930c38e298b5d215172a43649b69d4ec822e6f2dd9c9653d3e10c6fef7c`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 19.7 MB (19708563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ab58dff7537f1f21940512a5873857c7bfcd83b70ea566c0d893b0ed4bbe`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c58f32e0a401949f3015339b40763f13997ec258f8de853a296c690175b9a`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb034e3b9968792379e5445118d7e948eae0509b74bbe0222c32450ce369231`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1c453d9c45321fd866c5830abe9036744fd50ea31aef24f0fd5b441f600d0d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310b7edd1a05f5a6b1de9c12d0a3fd30be28798ce7d656f5b306158eb590c45c`

```dockerfile
```

-	Layers:
	-	`sha256:da87a8f3030a2c4d7a3e171d90c90259cecb58ab16f1f9570b999f97d340a6c6`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0e8384ace3dbca30fdface67dd29a8510a7285efdd842c51949e027ec0276891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69760973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a211b50f388cffbcec654f2c7e6951b74377f9657875d06fad2bc3915cad32c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:89c7bb5547d975cc3d11e0ae1a8ccc0351bf5fbc5335d2f5ddd2f35f6660c361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34de87369c83245725f8ef817f4b9e791ffcc508b41d1739e66e78f37aa131d9`

```dockerfile
```

-	Layers:
	-	`sha256:c32e99100ba19083df91a0159b4677528fb0e7aa00801be5cf350ba9ffa4b16e`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json
