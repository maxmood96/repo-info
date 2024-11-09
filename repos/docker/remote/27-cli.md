## `docker:27-cli`

```console
$ docker pull docker@sha256:af743bf68f5f30f37573c8c34717361ea6d737c80c8f4d3af73485eca7a4549d
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
$ docker pull docker@sha256:d50b5e6aa8abae52866c43a7b2e986874fe8a14db796a8f242d027cf350c3bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67763141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0eb8a55fb3cfd08c0a145c7fec2638a24ec79e8ab0d0a419996c541753ec2b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 18:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
ENV DOCKER_VERSION=27.3.1
# Thu, 07 Nov 2024 18:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Thu, 07 Nov 2024 18:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.3
# Thu, 07 Nov 2024 18:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-x86_64'; 			sha256='fbb4853d3f2148b0f2f0916f8971c9e500784e4e4949324934fc0b7dc2ed5016'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-armv6'; 			sha256='7116c73bd22504ff61e5e25f3ea6638a7b2a5d126764fccdec4fd7623cf17963'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-armv7'; 			sha256='944402b85b5eb8492ebbe2e4dcbf962adcaaa16b0ed66b51abaf2ac3e3809b1b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-aarch64'; 			sha256='8fed7b79b8bd1cb0624142f7d723c3cc67ba747c77ed69abbdefdc77a6d416d1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-ppc64le'; 			sha256='9a5d9fd85e852a9c3c9137ea8ea80d66f0fe349d34b3e329255d98cd960c331e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-riscv64'; 			sha256='eda617db72d24fe79be98e2273e1fb433943a18479cedc86601963f75666304f'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-s390x'; 			sha256='9476a64e9605df956e3e33b09acfdaed2d4a2c71da5b4a09899a9b7d428263a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 07 Nov 2024 18:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Nov 2024 18:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d54a3aade6eff1cdd9e78b1df495a4f08ba7c73c29cb42cd4fecd9edef9505`  
		Last Modified: Sat, 09 Nov 2024 02:00:20 GMT  
		Size: 7.9 MB (7889966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75c42edf92c01017a85b0a5bf6c7e49d064bcdca350a7764fa1b46bb824727f`  
		Last Modified: Sat, 09 Nov 2024 02:00:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3728d9cc2aff530ad7f9c758c88f82e05264b8b1a1bfa7dd474e330474b5af`  
		Last Modified: Sat, 09 Nov 2024 02:00:20 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9116f7ee1dc0303eeb4e7c6fda422d38643498a9c419fd0373ed67478e9e8c`  
		Last Modified: Sat, 09 Nov 2024 02:00:20 GMT  
		Size: 18.6 MB (18566632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e123e80dfb98e5bd393dc8d0c0489f62d2c98ceb4df73bb4c6b8eeada815d51c`  
		Last Modified: Sat, 09 Nov 2024 02:00:21 GMT  
		Size: 19.1 MB (19117166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d75d0d064b19490ccd80d55683d5de424ebb3b45702111383769d5b38d8c5d2`  
		Last Modified: Sat, 09 Nov 2024 02:00:21 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65f629885e432ecda7562cd694b7a224d5c5d7a8c8fae3da7f2785b5bee1736`  
		Last Modified: Sat, 09 Nov 2024 02:00:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afdf08f2c92e8a5bdeb90a92412311559f73b841ea1d4f5517ce23a45800f03b`  
		Last Modified: Sat, 09 Nov 2024 02:00:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:df1284141a61cc3d45dbf3db678088d3ba54a7702a8980f5cf64466be083daa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba676160e0ca25aa0028cd7af93d6e21228727db27b169463fffe901bdfb6f2`

```dockerfile
```

-	Layers:
	-	`sha256:4f2f52fd21b516cc624cb78acffe89e93a50dbcb1c21328b5c18ac1daeb132cf`  
		Last Modified: Sat, 09 Nov 2024 02:00:20 GMT  
		Size: 38.0 KB (37953 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:2645bfce7b117dfb854177a264751cf5d70e226c176a2f80becf294c88d3779f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62985112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef37a6f67c51423eb15e8990b3044a9f90a5df86e1503c322cd9b34a9b589188`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 18:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
ENV DOCKER_VERSION=27.3.1
# Thu, 07 Nov 2024 18:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Thu, 07 Nov 2024 18:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.3
# Thu, 07 Nov 2024 18:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-x86_64'; 			sha256='fbb4853d3f2148b0f2f0916f8971c9e500784e4e4949324934fc0b7dc2ed5016'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-armv6'; 			sha256='7116c73bd22504ff61e5e25f3ea6638a7b2a5d126764fccdec4fd7623cf17963'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-armv7'; 			sha256='944402b85b5eb8492ebbe2e4dcbf962adcaaa16b0ed66b51abaf2ac3e3809b1b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-aarch64'; 			sha256='8fed7b79b8bd1cb0624142f7d723c3cc67ba747c77ed69abbdefdc77a6d416d1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-ppc64le'; 			sha256='9a5d9fd85e852a9c3c9137ea8ea80d66f0fe349d34b3e329255d98cd960c331e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-riscv64'; 			sha256='eda617db72d24fe79be98e2273e1fb433943a18479cedc86601963f75666304f'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-s390x'; 			sha256='9476a64e9605df956e3e33b09acfdaed2d4a2c71da5b4a09899a9b7d428263a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 07 Nov 2024 18:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Nov 2024 18:04:14 GMT
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
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f324dbcf74fa1d94fe2a8e47fde042fed09a46196e848a7e9e5bde25dd43e52c`  
		Last Modified: Sat, 09 Nov 2024 01:59:58 GMT  
		Size: 18.0 MB (17961838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8a01c1fea32f0cef572d5588bb2174d1f73fe558ad6b03d9f82c49ae5c27e3`  
		Last Modified: Sat, 09 Nov 2024 01:59:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019930564620592e71a4f1f4f025de6df8d2fd2ade4ed1eecb3355293e1d247c`  
		Last Modified: Sat, 09 Nov 2024 01:59:57 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5374b3e7271feabba5026e0f9ede24ece64973228f4efc6a432600cb79928d9`  
		Last Modified: Sat, 09 Nov 2024 01:59:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:ee09420296ed1691d6b4276e50ed62e45a6aa48f480dfd9ca6a23a800655122f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401303f70c4c0e0098071e69f9311d69835f6e93dd9a002cc3862da12a8c9cb3`

```dockerfile
```

-	Layers:
	-	`sha256:96b30a6ce03a79937077bce7a2250f0dc84a0602922acd93fbee5f96d3057687`  
		Last Modified: Sat, 09 Nov 2024 01:59:57 GMT  
		Size: 38.1 KB (38108 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:020222ddda813bb84e70c9be7f35a6561af1b8a7cd04ae2a00acb1a68ab45de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62009855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadca07ba086b70770ab3acf2d04d902c8851463b7036cf4c4f8b7137321dc34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 18:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
ENV DOCKER_VERSION=27.3.1
# Thu, 07 Nov 2024 18:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Thu, 07 Nov 2024 18:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.3
# Thu, 07 Nov 2024 18:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-x86_64'; 			sha256='fbb4853d3f2148b0f2f0916f8971c9e500784e4e4949324934fc0b7dc2ed5016'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-armv6'; 			sha256='7116c73bd22504ff61e5e25f3ea6638a7b2a5d126764fccdec4fd7623cf17963'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-armv7'; 			sha256='944402b85b5eb8492ebbe2e4dcbf962adcaaa16b0ed66b51abaf2ac3e3809b1b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-aarch64'; 			sha256='8fed7b79b8bd1cb0624142f7d723c3cc67ba747c77ed69abbdefdc77a6d416d1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-ppc64le'; 			sha256='9a5d9fd85e852a9c3c9137ea8ea80d66f0fe349d34b3e329255d98cd960c331e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-riscv64'; 			sha256='eda617db72d24fe79be98e2273e1fb433943a18479cedc86601963f75666304f'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-s390x'; 			sha256='9476a64e9605df956e3e33b09acfdaed2d4a2c71da5b4a09899a9b7d428263a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 07 Nov 2024 18:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Nov 2024 18:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f03c7b4dee5d1571b9860b776e1c755e4c8957b7e816f1000e540ee80be8a6e`  
		Last Modified: Sat, 09 Nov 2024 01:59:47 GMT  
		Size: 17.9 MB (17940702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad982b6de6e36953158ed3f715663100e17a66d876b977a4bbb4e5dfe3b7bce`  
		Last Modified: Sat, 09 Nov 2024 01:59:46 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753c8cd320c430777e9b334f684ebcb3edf2a242c1ce3ec99e96138038bcb47a`  
		Last Modified: Sat, 09 Nov 2024 01:59:46 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fc03bb39f6a100c70f5aefb3ea9c96e11d5b4f9d6dadc746e5ec7e0ef131b9`  
		Last Modified: Sat, 09 Nov 2024 01:59:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:cba65b4b1ed6d30147580cf06d3d881f689b87abfcfb41307fefe7bccc729257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadc30463806e01960ae0da93b1973de59bcf9348fad984898e6ad29f642680f`

```dockerfile
```

-	Layers:
	-	`sha256:be30b6cc5ffd08d00b2296eebf00eea1e2784a076f272dda4277197ed603f813`  
		Last Modified: Sat, 09 Nov 2024 01:59:46 GMT  
		Size: 38.1 KB (38108 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:894631eeedec26bfc54a5f018261445f66b9a3ef5b36cec7b1a52bea2e639c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63997155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1ec1b106f9553a240c90ed5d2c93995eee7d8f597ec85865dbb56302d10fe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 18:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
ENV DOCKER_VERSION=27.3.1
# Thu, 07 Nov 2024 18:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Thu, 07 Nov 2024 18:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.3
# Thu, 07 Nov 2024 18:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-x86_64'; 			sha256='fbb4853d3f2148b0f2f0916f8971c9e500784e4e4949324934fc0b7dc2ed5016'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-armv6'; 			sha256='7116c73bd22504ff61e5e25f3ea6638a7b2a5d126764fccdec4fd7623cf17963'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-armv7'; 			sha256='944402b85b5eb8492ebbe2e4dcbf962adcaaa16b0ed66b51abaf2ac3e3809b1b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-aarch64'; 			sha256='8fed7b79b8bd1cb0624142f7d723c3cc67ba747c77ed69abbdefdc77a6d416d1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-ppc64le'; 			sha256='9a5d9fd85e852a9c3c9137ea8ea80d66f0fe349d34b3e329255d98cd960c331e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-riscv64'; 			sha256='eda617db72d24fe79be98e2273e1fb433943a18479cedc86601963f75666304f'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-s390x'; 			sha256='9476a64e9605df956e3e33b09acfdaed2d4a2c71da5b4a09899a9b7d428263a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 07 Nov 2024 18:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 07 Nov 2024 18:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Nov 2024 18:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e43f55707db6d948d30e0d585d75deb844410c4ab9d911079c1fdd3bc5e2043`  
		Last Modified: Sat, 09 Nov 2024 01:59:52 GMT  
		Size: 8.0 MB (7998266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce647b7b927d1e8fb13b3dbd553a34caa93df673f299b9e27b5155f4c44de8d4`  
		Last Modified: Sat, 09 Nov 2024 01:59:51 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8144e9cffd285a08fbee301d54ccec077394f4a0e4ff9caded199bd8397a5c`  
		Last Modified: Sat, 09 Nov 2024 01:59:52 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784d375a63dcc3acaa9893367896e10e252d06c9d7a4443e809b1d1e1d4179d9`  
		Last Modified: Sat, 09 Nov 2024 01:59:52 GMT  
		Size: 16.9 MB (16905178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8660c51903dc1a4bf8e7cec04902681fc2a5ae2c7a0b2770d0bb5099e588697a`  
		Last Modified: Sat, 09 Nov 2024 01:59:53 GMT  
		Size: 17.5 MB (17489935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817c43677c078c9ce894bb2663ad325458d8967bcc649a40217b3c061a65f6a1`  
		Last Modified: Sat, 09 Nov 2024 01:59:53 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b19dc88f6cbce170991bb878ec0d3e1220da8dfeb04a4b657b386873314a8b`  
		Last Modified: Sat, 09 Nov 2024 01:59:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20526f3a9818e0d14055f6ca7cd816c99c89157ffe5d434664e09486a604c9e4`  
		Last Modified: Sat, 09 Nov 2024 01:59:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3b2949feb446bab7334cec3a66638ff6fc9d51d6ee7030a486e637260bf78fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de1e7ad1ff5b7d1b4de579313df89cbfa6ec577352b73f9eb16a81c68a1ca5b`

```dockerfile
```

-	Layers:
	-	`sha256:4d0968f85fcb5c224d8edc6d621ede5dfa70e547cbe7e76dba38d498e0c7dfc4`  
		Last Modified: Sat, 09 Nov 2024 01:59:51 GMT  
		Size: 38.2 KB (38153 bytes)  
		MIME: application/vnd.in-toto+json
