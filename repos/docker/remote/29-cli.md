## `docker:29-cli`

```console
$ docker pull docker@sha256:70303ed0d265aee7bf4be0ddffe20b0b6e4f69ffa125e2a20cbb3718b99688db
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

### `docker:29-cli` - linux; amd64

```console
$ docker pull docker@sha256:3459e4b0c6702acfdc23b2a48e4e8bdcfc51ef96bac2d0af3ea3edac4044192c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70660468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f34f75af30162c2d6b68fa089dac03a627ba7303e9758184d9d26dacb913ca7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:31:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:31:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:31:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:31:34 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:31:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:31:34 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:31:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:31:36 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:31:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:31:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:31:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:31:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f783f43bd0c479eca4a605cd057214fd4d32195579fd3858ea619042787418`  
		Last Modified: Wed, 25 Mar 2026 18:31:45 GMT  
		Size: 8.4 MB (8399805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dc00f58fe8675ce338442f1f3924e7575b889140324f529e6f7b7b552e6a8b`  
		Last Modified: Wed, 25 Mar 2026 18:31:44 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed7cc89d7e24509b5ecc2a876b68c336cc533fccd578553f96c40bd5977acaa`  
		Last Modified: Wed, 25 Mar 2026 18:31:45 GMT  
		Size: 18.9 MB (18925059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59f566876aae23a8d4ded9382841f58305b92c7453a48044734ac35241c5e5d`  
		Last Modified: Wed, 25 Mar 2026 18:31:46 GMT  
		Size: 28.5 MB (28516527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f27ff511c85a43e9a75a388dbd32088a24592f41c6987999fbcf0165672071d`  
		Last Modified: Wed, 25 Mar 2026 18:31:46 GMT  
		Size: 11.0 MB (10955101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac4601d8546b2a6477f79a9bff1a05ec9add30bf96dc48fcd27457170f39b07`  
		Last Modified: Wed, 25 Mar 2026 18:31:46 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b922537b6a3dd95fc487130c0ca4896eb541d70d4a9438dd39590ccb7b65943`  
		Last Modified: Wed, 25 Mar 2026 18:31:47 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62fa46a186b2dc7d1a25e70eb2c2653aa0431485adb908a7cf943d28c49cdf1`  
		Last Modified: Wed, 25 Mar 2026 18:31:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:827d9483e2a64b8c44523708ca54adaeec69e1ee40b1f275bb657e51828404f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587b7070e426c0932cb45f162874ea0917cc386aa52282a4e864f0aceeac21c5`

```dockerfile
```

-	Layers:
	-	`sha256:9c77ec231f2b5c72293c670da21cfc5dc7c509522268cc74c92f9098859cef6a`  
		Last Modified: Wed, 25 Mar 2026 18:31:44 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:ab088b3f5efe676c33f3339eeefbb2228b5e4b45cc6189a7ee8d717f98d47796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66741259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6299617540122589abca8da49bf316efc08ef3e0e4632b70f20e47121c8e7a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:20:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:20:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:20:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:20:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:20:55 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:20:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:20:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:20:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7327f5bd7b20a7c0c384c9bed111c54ed041e23650f2789ce160520bd54e7d64`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 8.3 MB (8300847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad441b201d110caa6bbae91773542ed3038e833916ab8fdbdee2efdd096951d`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a9b3570b577d5bd7b5702ea3b038bd6d6736da52c7e4cfa9204254b3ef6889`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 17.7 MB (17704832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687acedd268ebaa81d467b79f662cb296f999d5edc939573fc235718f10b3d5`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 26.8 MB (26774785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6738b4fa70496e709329c400187d16a1e6dcd9323aa0597219b36caeffbf73`  
		Last Modified: Wed, 25 Mar 2026 18:21:12 GMT  
		Size: 10.4 MB (10388825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0425cd14663ea2989a267ae635da01c39877aac17e1b4a26049c6e8584e9b7`  
		Last Modified: Wed, 25 Mar 2026 18:21:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7154483d9dd47aca8dda22548f6ac6381d6f297c1afcbda1c72dba31279d96f7`  
		Last Modified: Wed, 25 Mar 2026 18:21:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbfd7d41a6aa1e531936a17e36405a287262345307d1769bbf5e514f1f4955a`  
		Last Modified: Wed, 25 Mar 2026 18:21:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4a04a0fb0422d24efcd71966c2ec778971b5a49ba8fb1934681a3c061a4f7bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8881255256c5bafe467ec0dffa5cdafa965971effe17aab0e66a451dbac7b198`

```dockerfile
```

-	Layers:
	-	`sha256:e6eb00c7bd1756168105295aa8a9f0546960e7bf78727f47d669e70e1096cc65`  
		Last Modified: Wed, 25 Mar 2026 18:21:11 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:b4cf24daf2e960893a39d2f0a13a0b2b889e626725f5704295ff3c7a80e2ce56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65702900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e770b04316507e289fdbe463af8dd53873a490a5215e9664d3c38a2387b9b0bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:20:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:20:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:20:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:20:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:20:52 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:20:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:20:55 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:20:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:20:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:20:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9a25e5bfb326bc75a71b460d0544e0abe70b0c6c1498521b7fd245df901627`  
		Last Modified: Wed, 25 Mar 2026 18:21:05 GMT  
		Size: 7.6 MB (7597792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bd4d27cb3827cca3206705328c83ee80e164a78dc2aa97099d480bb1ded087`  
		Last Modified: Wed, 25 Mar 2026 18:21:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57192b9959272e69a74f1600a28d23141f96a9856eb275612e66d96aed4cb23`  
		Last Modified: Wed, 25 Mar 2026 18:21:05 GMT  
		Size: 17.7 MB (17694926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7afb84b0bb6525824e7b41a3eb6ca04fbd8a378336dace66c201e7f0a9fdfd`  
		Last Modified: Wed, 25 Mar 2026 18:21:06 GMT  
		Size: 26.8 MB (26754421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34cbd0d9bfc6a2fbae47c23f0d1c832eaf8aacf91c370cd7d44df319b6dcf32`  
		Last Modified: Wed, 25 Mar 2026 18:21:06 GMT  
		Size: 10.4 MB (10371888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92b6554d10f78775d85c869fd50243ef34c2f7fb06170e9bfd0f6cb1d8c722f`  
		Last Modified: Wed, 25 Mar 2026 18:21:06 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a550d751a72e95d6b192c5aa49bc54135cd12eaac778e2494033d746481e4e`  
		Last Modified: Wed, 25 Mar 2026 18:21:07 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbfd7d41a6aa1e531936a17e36405a287262345307d1769bbf5e514f1f4955a`  
		Last Modified: Wed, 25 Mar 2026 18:21:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:b36c22ea07bd32cf40c3233fe677b6cfd0b141b3c63f391124eed2843c5fe9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17c08feca64baed542d11807ef5bdc316ef9f6816d6d0e695109048771339bc`

```dockerfile
```

-	Layers:
	-	`sha256:d9a26fdeeceae1cd37f2b33208c330bcbaaa632331e7950fad92cdb05c62b6ea`  
		Last Modified: Wed, 25 Mar 2026 18:21:05 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:56cff04ad8dcf376a96423ddf5515c8bdcd171e683265335da57f17aa020ad1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65845112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee59cb9a3f85ae950ab85efdd43672abd503dbe5adcd1a55b95687f24e990ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 25 Mar 2026 18:28:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Mar 2026 18:28:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Mar 2026 18:28:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Mar 2026 18:28:13 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:28:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Mar 2026 18:28:13 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:28:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Mar 2026 18:28:14 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:28:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Mar 2026 18:28:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Mar 2026 18:28:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Mar 2026 18:28:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7edc56943efc5fd8ceeeec0973e7862a22eef8479f31e4506aaa7683706598`  
		Last Modified: Wed, 25 Mar 2026 18:28:21 GMT  
		Size: 8.5 MB (8453635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d7bdfa7dc871c3af6f5b34ef1ef53c930b2fde5801879b794f1849da1dc4d`  
		Last Modified: Wed, 25 Mar 2026 18:28:20 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c366b69bd090a1557acbb6f1ebdab176751b61ca7e1c82af675fd5dd30436a`  
		Last Modified: Wed, 25 Mar 2026 18:28:21 GMT  
		Size: 17.5 MB (17476961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b74c99f62156a67a1a2f1edfa046c0c13825a6cdef351e68e41cbbffd8badb`  
		Last Modified: Wed, 25 Mar 2026 18:28:22 GMT  
		Size: 25.7 MB (25732670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fed48b65e655b617bf78f3b0c6df9994322561de4c1c4a706e621ec83f8fb84`  
		Last Modified: Wed, 25 Mar 2026 18:28:22 GMT  
		Size: 10.0 MB (9982606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318a3b2c176f6893caa80c95a652634492e38503c58e091a916b6d9c341a0648`  
		Last Modified: Wed, 25 Mar 2026 18:28:23 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c910ec30db0949d800f54bb9c1b3c4e2af20695bf5b14f43f4f9be42a0ecb2c`  
		Last Modified: Wed, 25 Mar 2026 18:28:23 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd0d057ad753e2ef837845dd9504265e602e0802dceee1b0083e05f00291b8c`  
		Last Modified: Wed, 25 Mar 2026 18:28:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a3331dd737a9d4ad382fff64040bbad2660884a99286e44af8338a00851aec68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ed74d502ab8399d1e1a43c9de66bf070e1741c40c8a187c876aa031385bd08`

```dockerfile
```

-	Layers:
	-	`sha256:5de0f8302079e7f4909158e85e3fcabf6c532e1b84c2c25003b4bf3343ea0e94`  
		Last Modified: Wed, 25 Mar 2026 18:28:21 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json
