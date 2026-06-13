## `docker:rc-cli`

```console
$ docker pull docker@sha256:15d52e787177e0a00f17dbcb517c9a59b1779e64d2f8727e028e7d003ad330b6
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

### `docker:rc-cli` - linux; amd64

```console
$ docker pull docker@sha256:21075e9d0ad14b8249d8433df0723dfa77bd11352e58026fd931c90990770a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65222989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b481938becc5a3e0398b773ed1dbbea9906aff9435e7504920fde763b9c085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:45:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:45:32 GMT
ENV DOCKER_VERSION=29.4.0-rc.1
# Fri, 03 Apr 2026 16:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.4.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.4.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.4.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.4.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:45:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:45:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:45:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:45:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:45:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:45:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:45:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:45:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:45:34 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a862c5b641d191a8570b6c771850c7bf6d69ff018998c8c6e8ab0af85d7e722`  
		Last Modified: Fri, 03 Apr 2026 16:45:40 GMT  
		Size: 8.4 MB (8399871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d988359739f9cda1af49479a5068fde3176673df0b32676010ba2074daa37c94`  
		Last Modified: Fri, 03 Apr 2026 16:45:39 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899f440d05310ab33e00c2a4c25cf5d022bd2dcab7974f3682b5afaadecd82e8`  
		Last Modified: Fri, 03 Apr 2026 16:45:40 GMT  
		Size: 19.5 MB (19464828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf1e951f79378a4c6cb10215f618a0e3df38aab53e63f90097474c46c542032`  
		Last Modified: Fri, 03 Apr 2026 16:45:41 GMT  
		Size: 22.5 MB (22539232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fed5ea151389c2b1c28faf0c1acbb944554888b3a2f4f52fd325d9dbc8b5b6`  
		Last Modified: Fri, 03 Apr 2026 16:45:41 GMT  
		Size: 11.0 MB (10955095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f247a2dab9364495324a6db86f72130933e2a2ebda1064270dec0cdc76df996f`  
		Last Modified: Fri, 03 Apr 2026 16:45:41 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871ef8eae2ec4aed037056cf6a97343dfcd041b96373234238b75409278b6dd1`  
		Last Modified: Fri, 03 Apr 2026 16:45:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c439f1cf026b0aa47c9165eb355e02ce6d0ced2b939c0b61059a74a88da882d7`  
		Last Modified: Fri, 03 Apr 2026 16:45:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2363eac4a63bc4a10f455341308ae07ded67b29b606259a2c37c6258abc7af65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39a5abeeff78868cf317504efed2794435a6ae5463516764d7177ab91d23af1`

```dockerfile
```

-	Layers:
	-	`sha256:27d0fa480c310b979b185347bf68032d589ea2fdf84a5376c85af6fa6328bbfc`  
		Last Modified: Fri, 03 Apr 2026 16:45:39 GMT  
		Size: 37.8 KB (37847 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:007be4602f1052149aa7e29025849568c6e949e5107910e49e7b6023f72a3068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61523257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af04f60be058d8f407764a80ca9ed666ae4314c0e0730a9521bec68bab0ee346`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:42:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:42:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:42:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:42:28 GMT
ENV DOCKER_VERSION=29.4.0-rc.1
# Fri, 03 Apr 2026 16:42:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.4.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.4.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.4.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.4.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:42:28 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:42:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:42:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:42:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:42:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:42:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:42:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:42:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:42:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:42:33 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740b77d615bd7056fdfa10ac45a84e645f200a1dd058906d2f7c5a35bcc02e0e`  
		Last Modified: Fri, 03 Apr 2026 16:42:40 GMT  
		Size: 8.3 MB (8300856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db9e15d099697e3e0f63334517990f0d02a61abec8f671ec78dada6c111aeb8`  
		Last Modified: Fri, 03 Apr 2026 16:42:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c28b1955542958382dc080ec6055df3c73c260a20b8530ff91d446782675fa3`  
		Last Modified: Fri, 03 Apr 2026 16:42:40 GMT  
		Size: 18.1 MB (18109738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d607dc6571f8f41c5fd0ef403f2bb6863b58d364a66443f9da8ca7f9cde4f3`  
		Last Modified: Fri, 03 Apr 2026 16:42:40 GMT  
		Size: 21.2 MB (21151868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c19d41d111a7e7675fbe26893a7f5ea7f2cf803ede26347e86e8e37a298210`  
		Last Modified: Fri, 03 Apr 2026 16:42:41 GMT  
		Size: 10.4 MB (10388825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbb061e40326dcdf5834050fe1c1afe0410137446275b196003f5f67d5a256c`  
		Last Modified: Fri, 03 Apr 2026 16:42:42 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14ba039043cee9b399c84ca71dfebbe89a11dd6cb153d242ff1aff26c849b92`  
		Last Modified: Fri, 03 Apr 2026 16:42:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47ca6b6bd80ba8b3cccf5857e45c7d6268ea2d8aee37db059fa433b2f5e1a40`  
		Last Modified: Fri, 03 Apr 2026 16:42:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6f2b7578584e1fcabe2a89e2cef8cfb0cc20b8b1808ae6d1610823a4ffd6ab37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7577ddb8303c01b9d61dec3929b3bb38572e4ebe8bca975300c2ce61e1706ea9`

```dockerfile
```

-	Layers:
	-	`sha256:af8b9f3106287ee004f3dd99cba87bff0534e294e27d0f0baf916dd09e1aba55`  
		Last Modified: Fri, 03 Apr 2026 16:42:39 GMT  
		Size: 38.0 KB (38005 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:af225d12726523cc588e601c132e670c3bcab35e267f5c946adb6cf5ac102ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60480048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f8b26093ee1d950230fbc1486bed81518232fd34283a16cabcaf5fead0509a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:45:27 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:45:27 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:45:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:45:30 GMT
ENV DOCKER_VERSION=29.4.0-rc.1
# Fri, 03 Apr 2026 16:45:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.4.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.4.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.4.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.4.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:45:30 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:45:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:45:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:45:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:45:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:45:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:45:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:45:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:45:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:45:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160cf480df4223e9c093a6b03d8f0cd776adbef0fbdc1971883c906a5ae77b80`  
		Last Modified: Fri, 03 Apr 2026 16:45:41 GMT  
		Size: 7.6 MB (7597819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf534ca20b632b12018f8e8dfdfa51940fe217db89e43a8997881d6b495e92f`  
		Last Modified: Fri, 03 Apr 2026 16:45:40 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bff7fce72b212b15e3e8402f591077ed586e9f115fa28fb845348ca78a873a9`  
		Last Modified: Fri, 03 Apr 2026 16:45:41 GMT  
		Size: 18.1 MB (18096731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0356f5841a728cad51a1481993e784e7f4a8b779016d2ca39a0d38c26e3c4e6f`  
		Last Modified: Fri, 03 Apr 2026 16:45:41 GMT  
		Size: 21.1 MB (21129737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76071f6eb91825d431e60e3c47685988fbad4ffd90171974bdb4ba738139d649`  
		Last Modified: Fri, 03 Apr 2026 16:45:42 GMT  
		Size: 10.4 MB (10371886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f46a410c1050397824cbce037710d306a9c8fcd7770269f17306ec04458266`  
		Last Modified: Fri, 03 Apr 2026 16:45:42 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364b86d679f89998946eb197c7fbb57dba59afadadb2c77475eaef68b241c843`  
		Last Modified: Fri, 03 Apr 2026 16:45:43 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c8f8ce62b35bbd451cdb86b3ad27fe1a62812d9212c5927f710fe0100dc881`  
		Last Modified: Fri, 03 Apr 2026 16:45:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9d9d32e5898408a4f9c06f4089950e195a9722c92e533eae2300cfa528605e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f35c0fda133823ba4ffd0280606ef9247e4364c0fc1d88d211a48a7eb138e1`

```dockerfile
```

-	Layers:
	-	`sha256:3934cb3b324c0e28ed74a743b766830a6a86745edefba7de068b0ab3d63640e4`  
		Last Modified: Fri, 03 Apr 2026 16:45:40 GMT  
		Size: 38.0 KB (38005 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a1e9a83db2b69a86793ee8877e18094faad1f5ebf39128c7f5b328229bbb9e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61009769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d4211de73926468823981f9cf5cc5a92213821abf3448253dd2eed4b3becfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:46:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 03 Apr 2026 16:46:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 03 Apr 2026 16:46:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 03 Apr 2026 16:46:26 GMT
ENV DOCKER_VERSION=29.4.0-rc.1
# Fri, 03 Apr 2026 16:46:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.4.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.4.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.4.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.4.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 03 Apr 2026 16:46:26 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:46:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:46:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 03 Apr 2026 16:46:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Apr 2026 16:46:30 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cf3b22a72236bcd96d49d3c387816a361250229f3968f19201054c93d84e02`  
		Last Modified: Fri, 03 Apr 2026 16:46:37 GMT  
		Size: 8.5 MB (8453703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17755aac57a17b26d227e90cda5640c7c481dc4fcaf611bf324f1daada29915d`  
		Last Modified: Fri, 03 Apr 2026 16:46:36 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682f2d485bf31736dee0191ef557ffac1677d2ca7616b68bd897c00dac88a0d6`  
		Last Modified: Fri, 03 Apr 2026 16:46:38 GMT  
		Size: 17.9 MB (17921106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574c5303b6bc47aa320f517b4685fc9c6f6200164d88576103e67819138f8cf5`  
		Last Modified: Fri, 03 Apr 2026 16:46:37 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0716bf65cfc3f79e5669633d4f1d4e319e9559b9e2c3d046355baeb5fb2411ed`  
		Last Modified: Fri, 03 Apr 2026 16:46:38 GMT  
		Size: 10.0 MB (9982606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e85224845d30b48450ae005b18d574486b616f2b39423e3c1e27e01dde92124`  
		Last Modified: Fri, 03 Apr 2026 16:46:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e893ec30a6e80f38e4580c01a95e766a4e139bfaf6b4c3005a3575a8e9be8f4`  
		Last Modified: Fri, 03 Apr 2026 16:46:38 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d12a8770b81efe9be207a2014600874c93611c8eac5b8980ccbc1717fa2531c`  
		Last Modified: Fri, 03 Apr 2026 16:46:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:60a045c08fb03d62afce2fc84d32dde2cc9d895a20fdc7c1ec319ecf0992fb1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a903ad87cad1f4a6d10f1d3f5b4a6149b412d008590def3cd23f3c005eb96b89`

```dockerfile
```

-	Layers:
	-	`sha256:d24f0e0c352aa2d762d2f52f95d6a195c526ee1de480f5e481de23c619174275`  
		Last Modified: Fri, 03 Apr 2026 16:46:36 GMT  
		Size: 38.0 KB (38037 bytes)  
		MIME: application/vnd.in-toto+json
