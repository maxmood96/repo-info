## `docker:cli`

```console
$ docker pull docker@sha256:067c301efe497cd5d174d468b7b3422a485ae4aca8f7ec1ffd4655c9fa383af2
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
$ docker pull docker@sha256:f82fc0e21aa488c72a9e02e320d92ad2ef16e8a3cbb3a964cd2fe818c03fd397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70653487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdace0db4b905ddbe62dc946839491a54e946fe35459eb8376ee7afbe273d777`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:46:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:46:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:46:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:46:28 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:46:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:46:28 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:46:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:46:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:46:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:46:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:46:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:46:30 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f1c7a58cda4399b7be2fb8427c3b756917df1abb433e17a98888259aa70c83`  
		Last Modified: Thu, 05 Mar 2026 18:46:37 GMT  
		Size: 8.4 MB (8399691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba58ca1e42e5eeec21273f066c06e25afee78a5211c7d6deb38ba545b7d6240`  
		Last Modified: Thu, 05 Mar 2026 18:46:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f8c3243c30359f68ee8e1f96a24d246ca1357a82d8b30de9a33e9d282d93e1`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 18.9 MB (18919365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e9c4ffbcbf205284b573f955de57155f10b92234b491b2127720a57c90c1ce`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 28.5 MB (28516523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34962ed90623b311790e104f78a280cdc54a1ce559635328476148c6fc522888`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 11.0 MB (10953934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a9731c772a36b5ae18988bc0c1c69aff62cb86d597f2de367c5b330fb8d459`  
		Last Modified: Thu, 05 Mar 2026 18:46:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a294ee3d24d1214f1944e57dadb6ef9c4b434a1a170e348838dafb16d31127`  
		Last Modified: Thu, 05 Mar 2026 18:46:39 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df03e33ed496925038509c0abcd9f087ab5ec4e4b917ed51730d71d63a87c91`  
		Last Modified: Thu, 05 Mar 2026 18:46:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:7732b83c24c090579194233e599c16514cecd4ecd47cfb2120e78fed9a151b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e946aaf10695166ffe2821bd79a384e866142f664252f7c17cfef0c52d5049`

```dockerfile
```

-	Layers:
	-	`sha256:f77befaf6d46144afdc0da5842fd778e6bebc9284b1d5cd47fb3ee26aa56ea38`  
		Last Modified: Thu, 05 Mar 2026 18:46:36 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:0a3764432b5f28f668904b0d061dda199f9cb056eea537ec9847684faf017499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66732000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d50761708975b53ca35b9d4cdc7f748c341a8c7653e9653bee918d00d70e6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:45:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:45:36 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:45:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:45:39 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:45:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:45:39 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:45:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:45:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:45:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:45:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:45:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:45:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0593a5009b5f1611e29afa031add0caa8e17436567b91fa0cd2b29e51d22c89`  
		Last Modified: Thu, 05 Mar 2026 18:45:50 GMT  
		Size: 8.3 MB (8300931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aae9fbc3eb9720394677e4ecd6aab19d036b3e73b352fb74b67d6b3a2fc9fa6`  
		Last Modified: Thu, 05 Mar 2026 18:45:50 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d66dff73ca29a47e9b6b4c6c761a4d7aa8867dca97bc28872f55bf9f47e2c6`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 17.7 MB (17698879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2808c066fd3febfd5f5674816180176477b47da3158ad376e658eb6d8136fab1`  
		Last Modified: Thu, 05 Mar 2026 18:45:51 GMT  
		Size: 26.8 MB (26774787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663b0b4076c27408b2184d77a831c36817e8a8d8d4897cb92fce9cdd0165335a`  
		Last Modified: Thu, 05 Mar 2026 18:45:51 GMT  
		Size: 10.4 MB (10385429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3615b056b4ef975abfd3ae24796393abcb6cd5c819f1c8a6e68c1488f641f1a`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32f9cb2f283cf611fe753cefc9ac89c970b2a82e793b029047ec9a74dd88da4`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5dc68331a182d6047cc64dc01811876321654c40481e65df941bf21d1129ff`  
		Last Modified: Thu, 05 Mar 2026 18:45:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:ddb748c94db7b691af9ae9a1262a3474fcfd1d257112ec1a80f72e7c2f3f0b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267d7647afcf5b970633ca4d8d596bf4a5871b705334f1b4f604ee3ac43c10f3`

```dockerfile
```

-	Layers:
	-	`sha256:852fd13688d41f0fe187746f1f381dba22d39520d78d58393a485d802e04ac3c`  
		Last Modified: Thu, 05 Mar 2026 18:45:50 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:c5196756e72be8ddb97e1d3e30db112e016d8026e1dddec89447ab5f233b8c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65697201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2370139bb3be53322ba100956e0f625461f029dad648d3351b08e3c6cd886912`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:46:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:46:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:46:32 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:46:36 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:46:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:46:36 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:46:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:46:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:46:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:46:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:46:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:46:40 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95152b95c4ccfeb5059ced14a96c4f1c17872baa3e875c18056cb5bed1b56676`  
		Last Modified: Thu, 05 Mar 2026 18:46:46 GMT  
		Size: 7.6 MB (7597774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d532e57eb4774540148a1cccd311fc10645e4dc68e8512d6b4f5a07d77498e82`  
		Last Modified: Thu, 05 Mar 2026 18:46:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64983bc952c232855d431fc0da6e3080f4c4c64fc0dce721c1086cc916d3037`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 17.7 MB (17691333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0552f021a975b88c2f33fc3057737b716d29921dcf12fff1a7bd017272ee52bf`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 26.8 MB (26754433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe274cdce52e0d95eda23b7407fdd0cd8a861a2014d8a240bda6be387b22c74`  
		Last Modified: Thu, 05 Mar 2026 18:46:47 GMT  
		Size: 10.4 MB (10369783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28feee09383ef1673e7a0cec5e45cf0ad41f8b64208682ad535da48f8de7e08e`  
		Last Modified: Thu, 05 Mar 2026 18:46:48 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c266b2e92e5c06c3362ac89279eac9742220da712ded40590f3312de938eb16a`  
		Last Modified: Thu, 05 Mar 2026 18:46:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b204129a9de694faa70c2c825548fbe88d190e24ecc2d949a3ea099c0ac40d3`  
		Last Modified: Thu, 05 Mar 2026 18:46:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:e2b136948486c88e4802c318ed319a2700e102e96e1fb47dcc2aa42a057c1dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c847e7727300290e168d4c987094fa88104501c1a10efad2632180d4862a1307`

```dockerfile
```

-	Layers:
	-	`sha256:4e56569c6a1d563f36af4ef3f4e56d9adb1d18e59380468844cd3cb22919e740`  
		Last Modified: Thu, 05 Mar 2026 18:46:46 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:25563ce4f95a232d02403181d2f22e211a839b27df0570c597fba9570e0cd799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65832267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a3ca73ed3e97db8ad3ee399f6f9b3af94ea994351e1e5517b0e0697594e55b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Mar 2026 18:44:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Mar 2026 18:44:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Mar 2026 18:44:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Mar 2026 18:44:32 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:44:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Mar 2026 18:44:32 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:44:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-amd64'; 			sha256='2bbc1b8ebc9a05287b01bc2fe6633ec5e2f53d58ee955ae69756d668e7098e5e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v6'; 			sha256='545d2b678e9a494e0891526ee4977699132c16659c8b3c25a4be8484cf19f691'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm-v7'; 			sha256='c3abd2992c0cbef5d307ec59d490f65c563008798a6b01a85a82069ad9945aad'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-arm64'; 			sha256='f03767cb0149759d409cd600b915bce764175ffda6eb3e86e14cc84a5637176a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-ppc64le'; 			sha256='7d6428c784d5665e846d533c8ae2309942cbc5ef2fa82c5d2c20a9cdd2aa9609'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-riscv64'; 			sha256='ff29d3ad8756d11c2fdfddf068d794615d52a2b052b0e2e50edbdbeaf11cbe42'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.linux-s390x'; 			sha256='f3e5e960ce35f16c592354e9d6a704f206550d92292c850f193c1af5289b60e5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:44:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-x86_64'; 			sha256='5633cb21e06a7c88c7ca48a9334d3d0f7f892e9605ae9e9a45f9a095d4ffceb8'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv6'; 			sha256='14159a5fde026633a7d436d6f61979351296a6c24921c009900ff6fb289dd097'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-armv7'; 			sha256='364a8f6d32daa9c4343c5335451af9b7f9531d9079f9621d6800c6c60eb438a1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-aarch64'; 			sha256='da671ae15b4d7c68c38b572a2e9ceba89f09657d2682c2d2e34ad6db828e7442'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-ppc64le'; 			sha256='074fe8a082415c84d37a11c325808c2f4aa35e1ed3b15e3fd676feb85480ee59'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-riscv64'; 			sha256='f09c0fe479a22563ab70a87ff09611a0da66a02b29bc97926bbc926e6ea27cea'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-linux-s390x'; 			sha256='6a5c638f7c3b2cacd87eda50af1b98474950d38ea094308a370c7fa3db10c47c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Mar 2026 18:44:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Mar 2026 18:44:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Mar 2026 18:44:34 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74f52f7948b98f731cc47a7da43a1a028f38396d447d93fa458cc7b1ee9ade0`  
		Last Modified: Thu, 05 Mar 2026 18:44:41 GMT  
		Size: 8.5 MB (8453572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50de1b9f6ee9b0bb47a9cb5e7877595782f60dc2d6c014088cfb72c4dca02106`  
		Last Modified: Thu, 05 Mar 2026 18:44:40 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8cd16e98d03b1081e8606a566c45e24d404e6738ce672011e2f5e3fe3b637b`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 17.5 MB (17472694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a548a65df6cf925e933ead68a3677913c3c9586d7115d161b6afd378cd8b1836`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 25.7 MB (25732665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09bdc4530b81e1aa74fe3d0322209932119b3cb64a72447d5442bd9c50cd4ed`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 10.0 MB (9974089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b96e65028eacc3700698877e774e4bfbca321b41420638481e753d07449225c`  
		Last Modified: Thu, 05 Mar 2026 18:44:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faab51bb66faa3b0c0d737ebc09cfb486e94acbcdc20e883d8022102e4fc2fd`  
		Last Modified: Thu, 05 Mar 2026 18:44:43 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd02735b351188e3d18abc71b56816ddc7406e1d55c433166d34e8fd46aa5692`  
		Last Modified: Thu, 05 Mar 2026 18:44:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:dd5bbcccfedb5ab4a2a04e113c8a6139f18bb538933b7da4cfd0e9578691d56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5da68ad52d2648b8d5b58e92c5f84e04f1b92e9fcb5d96f933dc61cd41d3a4e`

```dockerfile
```

-	Layers:
	-	`sha256:6f18ccc7ae4a65a1c710dde53d9e317d7f0f4bf8cf0db0aa37b96c25cd1b07b3`  
		Last Modified: Thu, 05 Mar 2026 18:44:40 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json
