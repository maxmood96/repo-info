## `docker:25-cli`

```console
$ docker pull docker@sha256:0dff342399b02ba94e03d367ba8117828b16bb4cf6fbef5692c89d6552ea5a6e
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

### `docker:25-cli` - linux; amd64

```console
$ docker pull docker@sha256:0b289662643c9aaa27690ae64dfd63da765907125fa460966196a52091cf7843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59510648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4402083d1ee69d2062efab3d8d1e77f1e26bf51e484df9a7cddcc15b97ff4f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Mon, 24 Jun 2024 17:06:04 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
ENV DOCKER_VERSION=25.0.5
# Mon, 24 Jun 2024 17:06:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Mon, 24 Jun 2024 17:06:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Mon, 24 Jun 2024 17:06:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 24 Jun 2024 17:06:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Jun 2024 17:06:04 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797dc925e2b04f6f1c1c85e86bce845d97af4cea7c311f1e26a91cf7214a13b1`  
		Last Modified: Mon, 24 Jun 2024 22:56:13 GMT  
		Size: 2.0 MB (2010476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ccce2bb2d348f207c785425f07ca7697cc0d991e78b017392f314f07d3f313`  
		Last Modified: Mon, 24 Jun 2024 22:56:13 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebc5ba2a434648dac665d8f542a3a4e63217c6f2c1b3488eac3afd5c7e37341`  
		Last Modified: Mon, 24 Jun 2024 22:56:14 GMT  
		Size: 16.9 MB (16902848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323f9f6e57fc6075e4d2dfd204c2bdb3d6dc21e05a63f6d2e24883317544fd17`  
		Last Modified: Mon, 24 Jun 2024 22:56:14 GMT  
		Size: 18.2 MB (18178854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529cf58ef749f7c4563ec1cbb798f122a22a4d6475ef1ea5c2fad7abca537312`  
		Last Modified: Mon, 24 Jun 2024 22:56:15 GMT  
		Size: 18.8 MB (18792455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f8256be983bae13590e73d425b50bd1660321867f3b39496af3c4294758193`  
		Last Modified: Mon, 24 Jun 2024 22:56:14 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed8512c563b108058c408c6aac71d7861f2f55373ca5da71a60fe8a226f23b`  
		Last Modified: Mon, 24 Jun 2024 22:56:15 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7259122cf82040508a4b81ec3ac3f5b0d63e7b362870e51e72b618b54faa2408`  
		Last Modified: Mon, 24 Jun 2024 22:56:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-cli` - unknown; unknown

```console
$ docker pull docker@sha256:161743c4e843ef23cdb4e42e3c2fd74176b7d35835a76b6de4b185794da393b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a54068a2095a0a43a1efa62f4dc50bc064d9f2a9d1fedc5173d1dc7450340d`

```dockerfile
```

-	Layers:
	-	`sha256:58f38c73f848a7ac28faa6dc388a6bc8e480cf1130abbc3af26a58ca9dd51a39`  
		Last Modified: Mon, 24 Jun 2024 22:56:13 GMT  
		Size: 37.4 KB (37418 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:514bb6a2377fb3984e7c9df1bf292023e2135db19043d1456e00b998878fede6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.4 MB (55399335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1365e7af85191ce41a75c190788389bfe72a48fef4c97705c387a44dd02226d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Mon, 24 Jun 2024 17:06:04 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
ENV DOCKER_VERSION=25.0.5
# Mon, 24 Jun 2024 17:06:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Mon, 24 Jun 2024 17:06:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Mon, 24 Jun 2024 17:06:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 24 Jun 2024 17:06:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Jun 2024 17:06:04 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d023b0d86d5f3c29ffac412805754ac7366e4ecc23c5177010d36847ad55a7`  
		Last Modified: Mon, 24 Jun 2024 16:53:24 GMT  
		Size: 2.0 MB (1993299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d6b44884f2fa15c4e561076223287af9c44c7cc4621122e79f252f814684c3`  
		Last Modified: Mon, 24 Jun 2024 16:53:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1cc16e187d7195f56a161fa75c6bee6aa17a40c38f75f3b762dacc1dc7b29d`  
		Last Modified: Mon, 24 Jun 2024 16:54:29 GMT  
		Size: 15.3 MB (15274084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bc25ced8857694962f1bfe92ceeb8bf55e069b7c8e326509b03deae4659cd1`  
		Last Modified: Mon, 24 Jun 2024 16:54:29 GMT  
		Size: 17.0 MB (17010826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba970c65d47cfb737276c240510f85995df732bb911628606f6d1893acf66c0c`  
		Last Modified: Mon, 24 Jun 2024 23:38:31 GMT  
		Size: 17.8 MB (17751794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866d3d2f5f4cdc23adb2e3a5543d14219bd82a158959e6a5edb1df459c06ee96`  
		Last Modified: Mon, 24 Jun 2024 23:38:30 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711bd8fb2f4b42bba5147d1364b3851449389b9a22e57853a07c56f3ea150c65`  
		Last Modified: Mon, 24 Jun 2024 23:38:30 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c41fd03b0db310dc3d9606e4a351ca80ed3443c1869d3fc3a8771595d6f3f78`  
		Last Modified: Mon, 24 Jun 2024 23:38:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-cli` - unknown; unknown

```console
$ docker pull docker@sha256:7bcc8c2ad197ad668f379e2a9cc5c33a5413fdb7858f133b486646a3f96e073c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa18d686500393dec6b7528df213f5791746431d4a4efd2fe8c93b60323baec`

```dockerfile
```

-	Layers:
	-	`sha256:803f419bd58f6a55c67a007845a4c22ab3a021ae0c9b20d74cbc05f570d2db6a`  
		Last Modified: Mon, 24 Jun 2024 23:38:30 GMT  
		Size: 37.6 KB (37567 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:d972fc0264ac96e7e7129dbc63e4556f7c132b70922e9d2d44cd4a66aebbf064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54947007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2d30641547cd77b86936ad9ae62b92baf39cd1633de45356dc2a14207c85e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 17:06:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 21 Jun 2024 17:06:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Jun 2024 17:06:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Jun 2024 17:06:26 GMT
ENV DOCKER_VERSION=25.0.5
# Fri, 21 Jun 2024 17:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Jun 2024 17:06:26 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Fri, 21 Jun 2024 17:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Jun 2024 17:06:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.0
# Fri, 21 Jun 2024 17:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-x86_64'; 			sha256='359043c2336e243662d7038c3edfeadcd5b9fc28dabe6973dbaecf48c0c1f967'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-armv6'; 			sha256='398d717e6cc9515ca0325035cfe626cbaaa1023754cfd22c13eab6b29ecc2d54'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-armv7'; 			sha256='604c00f22176ca8291f43d22f066cfcc89f4c09de2113d287f72c0bdcf611e46'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-aarch64'; 			sha256='296076f4d14d2a816ad750f6890355fc118692814e4b4542942794817f869d37'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-ppc64le'; 			sha256='c88c097fa475f07140c01e3ca370a503b927f377f200114fa17e0bee6e0cbc4d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-riscv64'; 			sha256='b563b99c5a1c03a1a83cb56ea1f7a492ef74e137afd0cbea485b828b6c61dbe5'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-s390x'; 			sha256='f701bd64dc5b204352c788931b43de9c778d47eed1be7caa81b57fc47a09164d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Jun 2024 17:06:26 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Jun 2024 17:06:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Jun 2024 17:06:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Jun 2024 17:06:26 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Jun 2024 17:06:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Jun 2024 17:06:26 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3be0ff3f8430a7c5e4c0602a3a190116b4a4d4d1d16b89c627d5436d8d3318a`  
		Last Modified: Mon, 24 Jun 2024 16:53:24 GMT  
		Size: 1.8 MB (1841225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e90c200cd38a52aed6f4457d4fb93031e32aab75a2c05019a3a2dda9db6b7f`  
		Last Modified: Mon, 24 Jun 2024 16:53:24 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f160e4936ad3ecdb18233c0d343680efbafb2be2a298e9a50761541c587d35c6`  
		Last Modified: Mon, 24 Jun 2024 16:54:21 GMT  
		Size: 15.3 MB (15273168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725ba4fdfc68afe8da9a814bfb6e5cc8cabf967f32b0c94c5f20ed32a0b82341`  
		Last Modified: Mon, 24 Jun 2024 16:54:22 GMT  
		Size: 17.0 MB (16998019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567072c17a1f8b7a9af012bdddbbce89a5f7e3da55003bc9f2f95625a5a693fb`  
		Last Modified: Mon, 24 Jun 2024 16:54:22 GMT  
		Size: 17.7 MB (17737570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b66ef505644842344b8b435433c338799753bcd556862f694751b6fb2b30cce`  
		Last Modified: Mon, 24 Jun 2024 16:54:21 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f8f62ea1c64eb969721f7d361012cda90026d9ddcbb78a4ace5f583fabd7c4`  
		Last Modified: Mon, 24 Jun 2024 16:54:22 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e16652ff15bdb11eac2070ba3f1e6b2113970d946aadf43f1427e153fc5613`  
		Last Modified: Mon, 24 Jun 2024 16:54:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a54af400f7422f860d5392a605c50239cf8ca6c9ccf8b4389ae2de26f5acf86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36d84683cb77a0bddd2d40a1d7a2fe31e9b1984fdff2fd2b771def6cae9228d`

```dockerfile
```

-	Layers:
	-	`sha256:73625fa3fda92edf1e86b9b024e7d148e71f307333d231bd45553294c9a1f5d3`  
		Last Modified: Mon, 24 Jun 2024 16:54:21 GMT  
		Size: 37.6 KB (37567 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:afb22bef16b20c0755f93978b0d4db8bbc05518a39c4ad4e0253572622d87c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55694837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077039290a5c510f7f9b00fe5cc3b4d330575428f41e602609509d2d0f2e7bcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Mon, 24 Jun 2024 17:06:04 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
ENV DOCKER_VERSION=25.0.5
# Mon, 24 Jun 2024 17:06:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Mon, 24 Jun 2024 17:06:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Mon, 24 Jun 2024 17:06:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 24 Jun 2024 17:06:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 24 Jun 2024 17:06:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Jun 2024 17:06:04 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8748a3ec57e134ccd57f5380286f503c468960d14815d75e49f8a7fa00bbddb9`  
		Last Modified: Mon, 24 Jun 2024 22:58:31 GMT  
		Size: 2.0 MB (2006605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d843f0fef030adf942f4bea037cda5f4755db1a7f6127261095313118908a3f2`  
		Last Modified: Mon, 24 Jun 2024 22:58:31 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16eb94ff4993726d1d33a2125f2011305038a429af92de6bb3075551079ea650`  
		Last Modified: Mon, 24 Jun 2024 22:58:31 GMT  
		Size: 15.9 MB (15907326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba572ce380e1c1294bb40b0b827b2f4e02206ed43411ae825ab5ca8997de5bd`  
		Last Modified: Mon, 24 Jun 2024 22:58:31 GMT  
		Size: 16.5 MB (16538037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7690ac483c401218c5746bb6c49b735924a12d695adcca7679bf7268c193780`  
		Last Modified: Mon, 24 Jun 2024 22:58:32 GMT  
		Size: 17.2 MB (17151898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f464fc5b9c92dd041c89d906d8a795531194374c908887d981a63c412f358c8d`  
		Last Modified: Mon, 24 Jun 2024 22:58:32 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fb5a78d7daad8990c548fdd674ec58a72a677b52a5376bf8d95a3ad0e1e300`  
		Last Modified: Mon, 24 Jun 2024 22:58:33 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459fb1ccfc39c5c0092404953e05fcba8fe12c6144dbc43dc92db48af88a67f0`  
		Last Modified: Mon, 24 Jun 2024 22:58:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4c0f56d3a6b6faf012b5f00bd3b3ab9af601a182545dac576e278a439d600920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1135c4feb573fa1c2d0e785b7992335f2d02dbe9a96cf1ca4a97c640f5ea440e`

```dockerfile
```

-	Layers:
	-	`sha256:7bcddbfead6b6c88e62c9572e31a0c9eeda0c32b099b4b49baceb7133a7554c0`  
		Last Modified: Mon, 24 Jun 2024 22:58:31 GMT  
		Size: 37.7 KB (37719 bytes)  
		MIME: application/vnd.in-toto+json
