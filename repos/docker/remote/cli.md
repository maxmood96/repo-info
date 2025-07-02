## `docker:cli`

```console
$ docker pull docker@sha256:402f150151fd6e68c8f9a0cb7c50d35ee3bf64268d920716b4f6dc93bf093830
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

### `docker:cli` - linux; amd64

```console
$ docker pull docker@sha256:80ae90b9a3bdc4068da7d8df8e55aaec90d4f7ce69ebabbd8284e295dc2feada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75408303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9495e14f29e58f2427eac8352bc4f61421eee3af468784882361290d7c08165`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
ENV DOCKER_VERSION=28.3.0
# Mon, 30 Jun 2025 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Mon, 30 Jun 2025 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Mon, 30 Jun 2025 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 30 Jun 2025 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 23:04:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd44dfd9ed005c75b2cb9a6c317864eb4368c58ae4b63c38b49fcef96744bb3d`  
		Last Modified: Tue, 01 Jul 2025 22:15:59 GMT  
		Size: 8.2 MB (8207456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af87fb31fb204b986a2ce24d6a6290a769e24244e9db397c1bbb1f5e25ea1f62`  
		Last Modified: Tue, 01 Jul 2025 22:15:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ba0d1476fc03a1254882d18ff825a820613a2f00f046c3f019e29eed558d77`  
		Last Modified: Tue, 01 Jul 2025 22:16:00 GMT  
		Size: 20.5 MB (20460129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6554ec0ba85c0894e2b7ceefee577e11d3196b43f4ac00d19601f4ebf8e056b1`  
		Last Modified: Tue, 01 Jul 2025 22:16:00 GMT  
		Size: 21.7 MB (21664158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb2482a56648c057e733df5ad11a730bf635646cfe2dbbbacc26b9e4e5f6750`  
		Last Modified: Tue, 01 Jul 2025 22:16:00 GMT  
		Size: 21.3 MB (21277560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8f41e8fb760475e415f7e10d472bcf110b277816449c514abd3d5768f3bcbf`  
		Last Modified: Tue, 01 Jul 2025 22:15:58 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c78189052135631fbdad76724fa4c1a058ea6a8e3e2acb40e64ee7007e6b7cb`  
		Last Modified: Tue, 01 Jul 2025 22:15:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661366313eb25141f764ddced9e982fdd56adec7e328a83a55879e9570f78fa5`  
		Last Modified: Tue, 01 Jul 2025 22:15:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:75782cd3045e6837e7bf0eb42ba89b4ab7cd62ca70b58b67dca1b0129ffa29e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036ffe134dcd1c2281defd257186b0013203869fd3fa113f2ebc9f829bf23daf`

```dockerfile
```

-	Layers:
	-	`sha256:e603f47308a6268cabf1bac03e6ceded0eeb0603ea5e274b36fc5cf2753ce8b9`  
		Last Modified: Tue, 01 Jul 2025 23:07:22 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:aeb0c62b036219755d5585858f38337e4191f2ff8fcc43d47eda625d49399d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70375572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a55f20771ba0c09f9e1f3f112b2dd1defb479c75ee1b22093aad22cb828ed5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
ENV DOCKER_VERSION=28.3.0
# Mon, 30 Jun 2025 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Mon, 30 Jun 2025 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Mon, 30 Jun 2025 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 30 Jun 2025 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 23:04:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42e53f526b8a259bd0a40a1e4bd0b2260cff84e1e8b971b67710b00aa26bf23`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 18.5 MB (18450874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3e045309567bd3067c3cf10a1fb430ad752a41f119321624784597490af9db`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.3 MB (20295398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30748a721bdde8b7e9865c9e87bc80d25a591904008c1b5b5cffd8f111d2be8`  
		Last Modified: Tue, 01 Jul 2025 22:18:05 GMT  
		Size: 20.0 MB (20011536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621f4f1ab61f47da9035c9b6c9090999ef7aaef958c3397ef23615873901c988`  
		Last Modified: Tue, 01 Jul 2025 22:18:01 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddfadd26517807ba13fef711559d3d49293d92e6a62a2a81697d3debd12fedd`  
		Last Modified: Tue, 01 Jul 2025 22:18:01 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7704dd5f7f13252be46dd437a387cd1d23c9ed98f85dc18a5de516dd359bcd6d`  
		Last Modified: Tue, 01 Jul 2025 22:18:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:57d3de170c3b0afdd04a183e10f34fd2114b8e0413c587c43ecfa2958c1234d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f04baec39c6d0a83bb66289a2e6bf064bf7df8f0e836058db07e00759571c4`

```dockerfile
```

-	Layers:
	-	`sha256:825894b3fcfd87c68de258d997beb95f728da180970ec4b9ffd3a048a5ae4fcd`  
		Last Modified: Tue, 01 Jul 2025 23:07:25 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:1e410b1a1489db7264c57d85e45eb63153fc6516d12bd3661ffb3feec86ef314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69376200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bda4a4c36c2f2d97282657d1bea4c1bd0058b0bf12d516ee6d075c85a31324b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
ENV DOCKER_VERSION=28.3.0
# Mon, 30 Jun 2025 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Mon, 30 Jun 2025 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Mon, 30 Jun 2025 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 30 Jun 2025 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 23:04:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36118c75c096abacc33cc7ff9c915c1b08741b58f40b1df1f2253602c110c0d9`  
		Last Modified: Tue, 01 Jul 2025 22:39:32 GMT  
		Size: 18.4 MB (18435302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd64d1a02256e0c7542f1bc10502b3f04bf16329b08a39bf61100799f738145`  
		Last Modified: Tue, 01 Jul 2025 22:39:32 GMT  
		Size: 20.3 MB (20282783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3babb6f7c4cd959e097c5cf3caf6f0c1db2fa92269de7f80620107c3788e4bc`  
		Last Modified: Tue, 01 Jul 2025 22:39:32 GMT  
		Size: 20.0 MB (19996159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba058723ca5c3d95da762f7068d6aa56245ba5111d164dc78aa3c64ba45ca74`  
		Last Modified: Tue, 01 Jul 2025 22:39:29 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0545b505b86e624c197c47e25540d0883baea3a00f1bc6d38afaae537c30ac`  
		Last Modified: Tue, 01 Jul 2025 22:39:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df978e43260eef70b2c2162b4089223c204d665a0d4483252bf90de953b9393f`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:d72e4f551c881d3e5c1af2f1389cdde1266f55b6ff8ce8f85507abef30907223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714307eecf0af367fba796bc13de05cad278399d791c47df4079cd808ec6339a`

```dockerfile
```

-	Layers:
	-	`sha256:9611899962483b6d63670d7c55fee918db4ff84b027b56a1d0ade7a578337007`  
		Last Modified: Wed, 02 Jul 2025 02:07:26 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5e4f578fbee0c884a4ba1b42a2025251c1e5946279a212d39d3cb23913c86c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70967237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a75b2c9e75095f0cf747d8ea0cc132b9517f6990f6ed5db3b3613d798dceed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
ENV DOCKER_VERSION=28.3.0
# Mon, 30 Jun 2025 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Mon, 30 Jun 2025 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Mon, 30 Jun 2025 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 30 Jun 2025 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 30 Jun 2025 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 23:04:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae849b9084d460522cebb3818fc98e6d28d805f368cf9d2c893acb8579ca0652`  
		Last Modified: Wed, 02 Jul 2025 02:34:29 GMT  
		Size: 8.2 MB (8229011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8f8af99f3b057c596e68842ff5ff7876f90748260dd417464665c066213a81`  
		Last Modified: Wed, 02 Jul 2025 02:34:26 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2437ed2f5b7920ce2e061e9fec3d55d952be4ede0a8f02e80199bfe2d75eb9e4`  
		Last Modified: Wed, 02 Jul 2025 02:34:29 GMT  
		Size: 19.3 MB (19267883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f880bb5cdac82cea0898b67e16953c9d485ee871f903f69f7c6a444d44fb504`  
		Last Modified: Wed, 02 Jul 2025 02:34:29 GMT  
		Size: 19.8 MB (19819436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b78d8c4b8b0c2b40344d1bf304461206a66f23c9cc2bab0334f151fcbae6ac3`  
		Last Modified: Wed, 02 Jul 2025 02:34:29 GMT  
		Size: 19.5 MB (19512814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2bd7635d7c7ed610f14cfdc0d09beff4af2ddd079d6a5208037c06f2c8ca51`  
		Last Modified: Wed, 02 Jul 2025 02:34:27 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3841942abe2f8e5b1d5ba33241dad8cc861c3599a1ee5b7436f3ea192daec4e6`  
		Last Modified: Wed, 02 Jul 2025 02:34:27 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de132f2f5e2995a5c5287a9918aa165fd1f2fea3ac16c72800758e187a3e56f4`  
		Last Modified: Wed, 02 Jul 2025 02:34:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:fb765c8748e420baf0f3576ea05ea86e340927bb558c005657cab7ed47441a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e132700ac9a5a70f915922cc873b1ea2d60b9507de9875994a1f0ede652dc1`

```dockerfile
```

-	Layers:
	-	`sha256:7e0478a290e4bded590c09f50adb5686361e42c86cf5f49c51a47a7da8ce904c`  
		Last Modified: Wed, 02 Jul 2025 05:07:26 GMT  
		Size: 38.3 KB (38321 bytes)  
		MIME: application/vnd.in-toto+json
