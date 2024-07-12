## `docker:26-cli`

```console
$ docker pull docker@sha256:13906073c64a581d3cd8e4471892e157d60348860d626f477df1be198c5eac11
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

### `docker:26-cli` - linux; amd64

```console
$ docker pull docker@sha256:ef929fa60d48484ca8776900c94ca052cc33c91c3b86213a35c175fba92f268a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66746429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f25ecd99c1f978d630b319441f7a92c2c102137389280ec1fd160d4ec3cbc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 23:08:36 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
ENV DOCKER_VERSION=26.1.4
# Thu, 11 Jul 2024 23:08:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Thu, 11 Jul 2024 23:08:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-amd64'; 			sha256='9a9a6ca0b929a57db01020fb226b1a2ea2bc57eba63d4adec46c43d0009506e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v6'; 			sha256='902f1240a6071c721f9746f0ff0859ef7b7368b683e322c08a1daa92d61d698a'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v7'; 			sha256='81d53f05d1d02306844f5a364cae6d7ad24451497c171ee29e1c000a78f30c5c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm64'; 			sha256='1aa8f0438866c706654a6dd96e211e509d42b16b1a0e66c1777c95edb2f14f49'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-ppc64le'; 			sha256='569f4a47bca797385eccac18e14e1d4bb681e35eeff6304c432de5bcd543120d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-riscv64'; 			sha256='e0cfc5072a792088115560e77a8540c9bf8299716984d42adc0735161472f076'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-s390x'; 			sha256='80ff8dcddbc3d0306e5cb819eddf89ce970ea1dbf806eb0adf7b6cd616d1da63'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Thu, 11 Jul 2024 23:08:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 11 Jul 2024 23:08:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 23:08:36 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cac8e32ef6911c4215304717991c4c32c8833cb9aef4603c90a48c5bc7ab98`  
		Last Modified: Fri, 12 Jul 2024 00:55:47 GMT  
		Size: 7.9 MB (7869241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d3d9fae81ec1a34c94578fbff235a752e44289f425f70aa9fd6d777cdc357d`  
		Last Modified: Fri, 12 Jul 2024 00:55:47 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfbb42c60225563f802bde2b987402be6548744d04db97c952d442fcce27dc4`  
		Last Modified: Fri, 12 Jul 2024 00:55:47 GMT  
		Size: 18.1 MB (18054139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3205a43f799392fcb04011df83ea05d24f58151693596f3990b3e5233b91e3`  
		Last Modified: Fri, 12 Jul 2024 00:55:47 GMT  
		Size: 18.4 MB (18404604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d7089eb11bedd0389efe77a0967fc782c75e7fb44c61cd023fe3bfb7d8c534`  
		Last Modified: Fri, 12 Jul 2024 00:55:48 GMT  
		Size: 18.8 MB (18792449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e60ea0bace50fdc4b3cd083304b19a6d60f1a1069e7418a4b00d9a71dd91222`  
		Last Modified: Fri, 12 Jul 2024 00:55:48 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c194e79e5136f3628975fb579549e4f1ccd13253a8592968ba2d1a659df798bb`  
		Last Modified: Fri, 12 Jul 2024 00:55:48 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc9d3b62c9f6598f528f60eb9f97a92e7dec53f0cd0f0b8463991d8f16ee164`  
		Last Modified: Fri, 12 Jul 2024 00:55:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-cli` - unknown; unknown

```console
$ docker pull docker@sha256:736cc36dbbe2f21aecfb29f8e57d4a7f4890f3c7e83d7f35a669a367573389ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce17420d6ed72ed13a64e3ab68fa7d0bac598b9b8129febd60aca5380fcf2e8`

```dockerfile
```

-	Layers:
	-	`sha256:1e4ab7b4b20a4778793402f56e9a5733211168366aa05f75d297f845ad7a4b16`  
		Last Modified: Fri, 12 Jul 2024 00:55:47 GMT  
		Size: 37.6 KB (37623 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:00296728e2be401bbcf5c90e8a4ec73bc222a51714a1c075cdd3282907e607a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62367268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96e762395eec2b7e792998473a0ff6e37390fcd6dfc2c29b67701780579fe15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 23:08:36 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
ENV DOCKER_VERSION=26.1.4
# Thu, 11 Jul 2024 23:08:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Thu, 11 Jul 2024 23:08:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-amd64'; 			sha256='9a9a6ca0b929a57db01020fb226b1a2ea2bc57eba63d4adec46c43d0009506e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v6'; 			sha256='902f1240a6071c721f9746f0ff0859ef7b7368b683e322c08a1daa92d61d698a'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v7'; 			sha256='81d53f05d1d02306844f5a364cae6d7ad24451497c171ee29e1c000a78f30c5c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm64'; 			sha256='1aa8f0438866c706654a6dd96e211e509d42b16b1a0e66c1777c95edb2f14f49'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-ppc64le'; 			sha256='569f4a47bca797385eccac18e14e1d4bb681e35eeff6304c432de5bcd543120d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-riscv64'; 			sha256='e0cfc5072a792088115560e77a8540c9bf8299716984d42adc0735161472f076'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-s390x'; 			sha256='80ff8dcddbc3d0306e5cb819eddf89ce970ea1dbf806eb0adf7b6cd616d1da63'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Thu, 11 Jul 2024 23:08:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 11 Jul 2024 23:08:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 23:08:36 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59052305dc7a728f2251e66eac45b2767b6973b8141d2aae6c8715001fa6d6b`  
		Last Modified: Fri, 12 Jul 2024 00:55:34 GMT  
		Size: 7.8 MB (7799513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3348f69f01290c149c5073ba7b49da64e1a4c954fe5f8d3648308da3b260d57b`  
		Last Modified: Fri, 12 Jul 2024 00:55:33 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7b0f2c45443d602152c372915cd82cf130729aea1c4ae9031c4cf0daa9589b`  
		Last Modified: Fri, 12 Jul 2024 00:56:07 GMT  
		Size: 16.3 MB (16329527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bfe82b207e147ad825b5f12e36f07151a05bd6c55e9180aac1d5235a9ba7fa`  
		Last Modified: Fri, 12 Jul 2024 00:56:08 GMT  
		Size: 17.1 MB (17117105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6432a4e86bf119743bbd56bf503707957418d0f005b773ffd7bc819c19b36c4`  
		Last Modified: Fri, 12 Jul 2024 00:56:08 GMT  
		Size: 17.8 MB (17751814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150fd3d217801b41d4397751afdf9b033f8e05352cbc34bd67160a58ae8ca780`  
		Last Modified: Fri, 12 Jul 2024 00:56:07 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b559323a956fb37d5fff0e88389b9465381a1fe2673dc65f6d67a8f022a0262f`  
		Last Modified: Fri, 12 Jul 2024 00:56:08 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b930b20600a8948df103740903f1117a0339ed3f73a50e4a7c6aca8ca24548d`  
		Last Modified: Fri, 12 Jul 2024 00:56:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-cli` - unknown; unknown

```console
$ docker pull docker@sha256:74def123e01d046a6b679c7060169f2e2e7ba4f48b0f7469a2f8160510fb625b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46c32b91678e51fc49ced523a8bb980a3e58165dfe5b576108ad9325ecd5380`

```dockerfile
```

-	Layers:
	-	`sha256:35552a2698aa2d51c832009980c7aaadd3a551644857df021917c83fce611ab9`  
		Last Modified: Fri, 12 Jul 2024 00:56:06 GMT  
		Size: 37.7 KB (37711 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:e1ab2cc90d66b3abffd1b60074cf9e995e75036e3e1ac373d5dcb840d3a3ed3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61395596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066b4081625f120a44dfead4ca73c664c922b62aa6ba96132797554852260d0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 23:08:36 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
ENV DOCKER_VERSION=26.1.4
# Thu, 11 Jul 2024 23:08:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
ENV DOCKER_BUILDX_VERSION=0.16.0
# Thu, 11 Jul 2024 23:08:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-amd64'; 			sha256='9a9a6ca0b929a57db01020fb226b1a2ea2bc57eba63d4adec46c43d0009506e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v6'; 			sha256='902f1240a6071c721f9746f0ff0859ef7b7368b683e322c08a1daa92d61d698a'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v7'; 			sha256='81d53f05d1d02306844f5a364cae6d7ad24451497c171ee29e1c000a78f30c5c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm64'; 			sha256='1aa8f0438866c706654a6dd96e211e509d42b16b1a0e66c1777c95edb2f14f49'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-ppc64le'; 			sha256='569f4a47bca797385eccac18e14e1d4bb681e35eeff6304c432de5bcd543120d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-riscv64'; 			sha256='e0cfc5072a792088115560e77a8540c9bf8299716984d42adc0735161472f076'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-s390x'; 			sha256='80ff8dcddbc3d0306e5cb819eddf89ce970ea1dbf806eb0adf7b6cd616d1da63'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Thu, 11 Jul 2024 23:08:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 11 Jul 2024 23:08:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 11 Jul 2024 23:08:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 23:08:36 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f8f43a5e9dffdca5dd025bbd85398b3ab11be727ceb38b46694cf6e545adac`  
		Last Modified: Fri, 12 Jul 2024 00:55:31 GMT  
		Size: 7.1 MB (7138083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f9bc370fd50d38ec8b5e504a743060eee5295761d82f66e58e6447947bf0a3`  
		Last Modified: Fri, 12 Jul 2024 00:55:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc209020341b7c303bd18e035d6daca531694fd25b26d3c8424157252a5168b0`  
		Last Modified: Fri, 12 Jul 2024 00:56:06 GMT  
		Size: 16.3 MB (16319702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f771928f86b594c3cf62ff939e94dde8e116f0b19b90caf8ab7f37a4cb132d98`  
		Last Modified: Fri, 12 Jul 2024 00:56:06 GMT  
		Size: 17.1 MB (17104557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb51ee171390650cc1c7f27472a34bce0845953359b68c0b15650b878ebaf885`  
		Last Modified: Fri, 12 Jul 2024 00:56:06 GMT  
		Size: 17.7 MB (17736243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05c1dcefffb2dfef8547d8e2407b2a29cb0f6d5f1ddc69767e892cd62b09233`  
		Last Modified: Fri, 12 Jul 2024 00:56:05 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b02c708392dcb9cda9289df3313c8bb41f2e2bb53608d73868c6c5908d526d`  
		Last Modified: Fri, 12 Jul 2024 00:56:06 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a32acf5749946f390201e05ed43a589b72b84f83e556b75d50e0f306ee580ab`  
		Last Modified: Fri, 12 Jul 2024 00:56:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f67960184b2747160c3dd32eee711dbdf81105ca94b72ddea9598c0c96e79ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc446e3b90e2291ba1f2e4d25bbd64d2e2bf5603a925437b0fc80e4ef8eb84c`

```dockerfile
```

-	Layers:
	-	`sha256:2977ebbb3fd371cdce5d940430339371c05a6f4778f8bc5905a8fe7deea101bf`  
		Last Modified: Fri, 12 Jul 2024 00:56:05 GMT  
		Size: 37.8 KB (37771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ffa38a0dff5d3e6c6feaaf21b39600b4c16fc4fb84f01d3f6bf33b76256665e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62769359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5dcbb89471748739059133fbe8a7c3cbe156899cb5cdc4c457d0e37ddbe3a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 21:37:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENV DOCKER_VERSION=26.1.4
# Mon, 01 Jul 2024 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Mon, 01 Jul 2024 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Mon, 01 Jul 2024 21:37:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 01 Jul 2024 21:37:08 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 01 Jul 2024 21:37:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jul 2024 21:37:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d0a0e3728c638822326d4bd5741e292d7e5ff128e1ca81be05bf3dd691c8ed`  
		Last Modified: Wed, 03 Jul 2024 19:22:52 GMT  
		Size: 8.0 MB (7976917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4644cf50cadd0e57adc9327b67f3ff25a810337384ce8eda69b6fd36e3b76e`  
		Last Modified: Wed, 03 Jul 2024 19:22:51 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24081d04446f8d9ff97699a4f37f37a21ddbddfe88c812e808e310e152bf0b8`  
		Last Modified: Wed, 03 Jul 2024 19:23:17 GMT  
		Size: 17.0 MB (17011548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2e3b573120f0ddf6875f40bb74649d87aa07b702a88f62aca5783454b61e87`  
		Last Modified: Wed, 03 Jul 2024 19:23:16 GMT  
		Size: 16.5 MB (16538045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3666bef369e3716dfc09da937230b4847f336be1d0958040e0bef93d5fdc6d9`  
		Last Modified: Wed, 03 Jul 2024 19:23:17 GMT  
		Size: 17.2 MB (17151898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11d453d9525e3e1610776edf9affade4e4e8ba667ad32c2205f3581417d7d36`  
		Last Modified: Wed, 03 Jul 2024 19:23:16 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e5be2989251d64c32e022b6932080878a6067ec2efaa54c539d527fac981e6`  
		Last Modified: Wed, 03 Jul 2024 19:23:17 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d80a792505f6ae3a8d40ac709e1bf04590ff6be8a03591f8a6adbbda46bafd`  
		Last Modified: Wed, 03 Jul 2024 19:23:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-cli` - unknown; unknown

```console
$ docker pull docker@sha256:89a7cdcc751405f7e2b167cdcaecfa7d4016113633d8394566524a0ab1ff447f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3062c9b6d6fe8de27f9e484ed30d3bd29e6cc639487e83dd583a76d0431c6137`

```dockerfile
```

-	Layers:
	-	`sha256:ceb32ccd36c949f4f5cb1b4c720ce10c827f4d1f1ab24f0164221cbb05f3df69`  
		Last Modified: Wed, 03 Jul 2024 19:23:16 GMT  
		Size: 37.9 KB (37923 bytes)  
		MIME: application/vnd.in-toto+json
