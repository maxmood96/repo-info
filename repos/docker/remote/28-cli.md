## `docker:28-cli`

```console
$ docker pull docker@sha256:d2beec104c628e890985b76b9b59a1b9435c1217fdc5b7333cc16ab871460663
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
$ docker pull docker@sha256:a97610205a61aff9506ecb30df2164fe4d8d0d95634ec11c6a164f4946eb6662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73937547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec2f402cd078ba9ad4afc1ae116168750134b99702d5ddadfcb47c6483b69dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.1.1
# Mon, 19 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Mon, 19 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Mon, 19 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-x86_64'; 			sha256='8c410e789d3fa688201170a8efb52048ee0dcb0d4cde44ce92a1bb6949f49fcb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv6'; 			sha256='4726dc002180e66122087c4b48bc58c78a7cb97c92811ff2100296c73a426222'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv7'; 			sha256='583299ca517b1d32cd9739b58e747770ce0e8a38cf72818d023fa5d6fb973098'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-aarch64'; 			sha256='a1ad63fe3f1feffb096df472bcd793e9635907a51e5861a0e0bf78b0c4fefa18'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-ppc64le'; 			sha256='7c208fb561bd5a7f79d16774b0b8f5c9da12f6dbe71601a8a40e4664da9ab822'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-riscv64'; 			sha256='c6de2c0d930ec37a4465ecb786aa59153fac518acbec37b5f92c23760fcb20a9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-s390x'; 			sha256='c06364ce6bcd14c2b8c7c595789249d2c041f0b79ff50f59356471f7fd938611'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 17:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f5f64c726e2c31d560c8d9754340c9f1aeb301d60047e17b771570e92ee4de`  
		Last Modified: Mon, 19 May 2025 23:46:14 GMT  
		Size: 8.1 MB (8062931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1622324b9f32d2c28ed38601b18d9b823ae89f2e47af430b21692884ad1ab62e`  
		Last Modified: Mon, 19 May 2025 23:46:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8044a81615b9ecd78ed519e318c69de5cd2f77a95ff6f27f7376f005c40333`  
		Last Modified: Mon, 19 May 2025 23:46:18 GMT  
		Size: 19.6 MB (19565542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534946bec48bf3ce6f05f225e28d61d3e1c810174a98ff2fbe90c52d240132f9`  
		Last Modified: Mon, 19 May 2025 23:46:19 GMT  
		Size: 21.5 MB (21456661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d105ef29bbb02f078851b0019ed6241908d28d730a79b0896c39a8414e74ba77`  
		Last Modified: Mon, 19 May 2025 23:46:19 GMT  
		Size: 21.2 MB (21208008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bba9fb730a01da2b73429eb39827fcdbc65a19fe4af5d05db12698a1a6778fe`  
		Last Modified: Mon, 19 May 2025 23:46:15 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee246c8fb4e8702cdd4185e37c04495ff7c3f6857c21e1ec169eed0d1963c17`  
		Last Modified: Mon, 19 May 2025 23:46:15 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ab34ed322521e0a053c344589f8cfb12e95dd9b2cebe14be1c8a14272ab8e5`  
		Last Modified: Mon, 19 May 2025 23:46:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:521aa0a6fc7ce8c3e2402769ebf42400bffec359d32b0cc2777de0749d808cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb34c06ebdff0f240ae5eda4efd95f69796b2daa56a5cb34d71233d23aafe6f3`

```dockerfile
```

-	Layers:
	-	`sha256:8d9a4465994fe187ea2c2895828b73bc9650560629872d0e6c19a73ecbc5eac5`  
		Last Modified: Tue, 20 May 2025 02:07:43 GMT  
		Size: 38.1 KB (38115 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:087c738c779fa4e5378e8f660a76fc80268a01e16ef27d9326a0b699d2ac72f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68868791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421c09f87ab0d9adb2687ee6efdc4f3a4c0d383dd26bc1088759c4430bf03e1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.1.1
# Mon, 19 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Mon, 19 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Mon, 19 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-x86_64'; 			sha256='8c410e789d3fa688201170a8efb52048ee0dcb0d4cde44ce92a1bb6949f49fcb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv6'; 			sha256='4726dc002180e66122087c4b48bc58c78a7cb97c92811ff2100296c73a426222'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv7'; 			sha256='583299ca517b1d32cd9739b58e747770ce0e8a38cf72818d023fa5d6fb973098'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-aarch64'; 			sha256='a1ad63fe3f1feffb096df472bcd793e9635907a51e5861a0e0bf78b0c4fefa18'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-ppc64le'; 			sha256='7c208fb561bd5a7f79d16774b0b8f5c9da12f6dbe71601a8a40e4664da9ab822'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-riscv64'; 			sha256='c6de2c0d930ec37a4465ecb786aa59153fac518acbec37b5f92c23760fcb20a9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-s390x'; 			sha256='c06364ce6bcd14c2b8c7c595789249d2c041f0b79ff50f59356471f7fd938611'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 17:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 21:07:35 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 21:07:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabe4b1be1d57ade8a16d24392424cb161acf4950ab94290ffde72d3b5148f78`  
		Last Modified: Thu, 08 May 2025 17:23:12 GMT  
		Size: 17.5 MB (17512361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dff119413b0094e760b5ad418b937c9bd222be2caf464a545452a5d9e482883`  
		Last Modified: Thu, 08 May 2025 17:23:15 GMT  
		Size: 20.1 MB (20075449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648c43b0a312cc2760f195011db848a1e0d9b76c135ea351c7016df2ff32bd1f`  
		Last Modified: Mon, 19 May 2025 23:46:46 GMT  
		Size: 19.9 MB (19935940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932f6bb8cb0ffc7a0a8bc5f8146966de3bf136841c5a15f1dd1d245961864cbe`  
		Last Modified: Mon, 19 May 2025 23:46:42 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f565736812324ce1ddd7134d7c056ba03574880b3f68b392196b5314def096`  
		Last Modified: Mon, 19 May 2025 23:46:43 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27463e47c9a363d4fca5ee76f3fac35cf25f3871c0261aab9df41f56343195c0`  
		Last Modified: Mon, 19 May 2025 23:46:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6250c5488bec81073517e0a27ed3965fc468aee368d9ade0e3de4cf704ec7412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61852009337782a50671ee7b8813384b8b55937b0adf374c6787e05b2482f9d2`

```dockerfile
```

-	Layers:
	-	`sha256:72828e134e7df593530cb0d07606e0d54792ed8f9fe91492d70ed32f5c02caf6`  
		Last Modified: Tue, 20 May 2025 02:07:45 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:b7e621428249ea48ced0adadb573b68bf2a2aa2428b196d411f8871f9b675bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67880240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a8a6b477bcececd1ec22fdcd06b39e2de0986ec03651906790dd5b5ca1d0bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.1.1
# Mon, 19 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Mon, 19 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Mon, 19 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-x86_64'; 			sha256='8c410e789d3fa688201170a8efb52048ee0dcb0d4cde44ce92a1bb6949f49fcb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv6'; 			sha256='4726dc002180e66122087c4b48bc58c78a7cb97c92811ff2100296c73a426222'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv7'; 			sha256='583299ca517b1d32cd9739b58e747770ce0e8a38cf72818d023fa5d6fb973098'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-aarch64'; 			sha256='a1ad63fe3f1feffb096df472bcd793e9635907a51e5861a0e0bf78b0c4fefa18'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-ppc64le'; 			sha256='7c208fb561bd5a7f79d16774b0b8f5c9da12f6dbe71601a8a40e4664da9ab822'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-riscv64'; 			sha256='c6de2c0d930ec37a4465ecb786aa59153fac518acbec37b5f92c23760fcb20a9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-s390x'; 			sha256='c06364ce6bcd14c2b8c7c595789249d2c041f0b79ff50f59356471f7fd938611'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 17:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d088acd453a2810f068374be7c873ecdd373aa8cb73c7fa22edf9c6c6572532d`  
		Last Modified: Mon, 19 May 2025 23:46:39 GMT  
		Size: 7.3 MB (7301852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d61a4a1f1b93be982dd3087d4f4a07517959168fd4962c81f01e0f52003e46`  
		Last Modified: Mon, 19 May 2025 23:46:38 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7aa4924b4e7613873e5ecfb240c2ca81b132f23b2b650d4b063df465d18ee1b`  
		Last Modified: Mon, 19 May 2025 23:47:00 GMT  
		Size: 17.5 MB (17499373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda8952bdd051624a488c7a895abf2e7a67b87e2a3c896ed80b444fd6928bf65`  
		Last Modified: Mon, 19 May 2025 23:47:01 GMT  
		Size: 20.1 MB (20055850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6868652ba947b1ffa4e06dc845c102c887a72bf524b0332229b82270d79f047`  
		Last Modified: Mon, 19 May 2025 23:47:01 GMT  
		Size: 19.9 MB (19922888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6384ce11b66649114c5e22e454b4c1e3fc74431d27385a9a577b4123831f171e`  
		Last Modified: Mon, 19 May 2025 23:46:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3458ecb5240b928e0cde97bf12c3dcbd2f95ce30e810eceeac5a5cedf3fc26e5`  
		Last Modified: Mon, 19 May 2025 23:46:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efedcdf8e87a6f5bbbe600d2bf06fa6793f94caed993f7acdc7f5ddd05e81f53`  
		Last Modified: Mon, 19 May 2025 23:46:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f0accadc3c99d0086a5914de9418763017ebffc1f7b3d05630a1f2da83bf6640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e309e6d7be10672dc180061a0b973cee33003465510eea218db9306aa2fb03d5`

```dockerfile
```

-	Layers:
	-	`sha256:11079c6e3c9d2e532d36fcd8d2d70d1ff18172db54f2127d88e81d25fe97203b`  
		Last Modified: Tue, 20 May 2025 02:07:47 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7e0d49ac4c5b9528c681a757dfb11f8f8009ce40fa687358cb6689f95f3cf9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69684512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3014299580fe8b8e55e0222542460e80d79baa20108769f7a2cf7a3f96bdbfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.1.1
# Mon, 19 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Mon, 19 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Mon, 19 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-x86_64'; 			sha256='8c410e789d3fa688201170a8efb52048ee0dcb0d4cde44ce92a1bb6949f49fcb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv6'; 			sha256='4726dc002180e66122087c4b48bc58c78a7cb97c92811ff2100296c73a426222'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv7'; 			sha256='583299ca517b1d32cd9739b58e747770ce0e8a38cf72818d023fa5d6fb973098'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-aarch64'; 			sha256='a1ad63fe3f1feffb096df472bcd793e9635907a51e5861a0e0bf78b0c4fefa18'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-ppc64le'; 			sha256='7c208fb561bd5a7f79d16774b0b8f5c9da12f6dbe71601a8a40e4664da9ab822'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-riscv64'; 			sha256='c6de2c0d930ec37a4465ecb786aa59153fac518acbec37b5f92c23760fcb20a9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-s390x'; 			sha256='c06364ce6bcd14c2b8c7c595789249d2c041f0b79ff50f59356471f7fd938611'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 17:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fffdd893f2edce36ae9ef8552b4908e678780ed400d81510a7672b934b2c9b`  
		Last Modified: Mon, 19 May 2025 23:45:49 GMT  
		Size: 8.1 MB (8077199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d86e9e1048e11c509f223efe8388ce6b460fb5a34e23a02d017ec34b2c5bebd`  
		Last Modified: Mon, 19 May 2025 23:45:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8cfcc483cc0d3227380016efaba99a3dc92470f2827fa75dccc8ca8424a997`  
		Last Modified: Mon, 19 May 2025 23:46:33 GMT  
		Size: 18.5 MB (18485710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72096810dddbe61694cb28a92436375fdcdf8d04c0969f2e93abc8f5730dbd29`  
		Last Modified: Mon, 19 May 2025 23:46:33 GMT  
		Size: 19.7 MB (19692479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78d7b972c4bcf0f49e6b55911ae32a6ed70adbe9e1acbb9b8d6395d79f67655`  
		Last Modified: Mon, 19 May 2025 23:46:34 GMT  
		Size: 19.4 MB (19433940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc7f40ad492f29c1b857d995c206c26ea37323e4a5ee819db8b294f6bd1f34f`  
		Last Modified: Mon, 19 May 2025 23:46:34 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e435f7c0924da6a8d18ba41fd7360142b67e4fc934e5642b344c9c3c65e37e50`  
		Last Modified: Mon, 19 May 2025 23:46:35 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27463e47c9a363d4fca5ee76f3fac35cf25f3871c0261aab9df41f56343195c0`  
		Last Modified: Mon, 19 May 2025 23:46:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:89700de652e2b46cf445e148e5f386a3cdf03601a5f4e0bec654b4a95c4d3d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0cf1a4ccfce7642b04ffcadee6b80683539d07647886686ca757d7e38aebbe`

```dockerfile
```

-	Layers:
	-	`sha256:199488fd2d4a848ddd5b6d78e58c499fd1a53daca9ca55d187cfdde5dc71f4b0`  
		Last Modified: Tue, 20 May 2025 02:07:49 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json
