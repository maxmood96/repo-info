## `docker:rc-cli`

```console
$ docker pull docker@sha256:df1f394cb8e62040be13fb4f69fdfc3bf95cb1e8bd56f5867d31bc98cefdceb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:rc-cli` - linux; amd64

```console
$ docker pull docker@sha256:b1bb3b17bc191fd023024d016b987f977aae6070dc4cf36c588a21111908d43b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51322089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d5313900aa634ec393a9114ea08b843d259800fe8c4782c93e3288ffb630f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Tue, 29 Nov 2022 01:27:01 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Nov 2022 01:27:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Wed, 07 Dec 2022 01:26:54 GMT
ENV DOCKER_VERSION=23.0.0-beta.1
# Wed, 07 Dec 2022 01:26:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-23.0.0-beta.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-23.0.0-beta.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-23.0.0-beta.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-23.0.0-beta.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Wed, 07 Dec 2022 01:26:58 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Wed, 07 Dec 2022 01:27:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Thu, 22 Dec 2022 01:56:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.14.2
# Thu, 22 Dec 2022 01:56:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-x86_64'; 			sha256='d056a8330a01f22c249b9fa03ad0d5be889b79b648cad43c8549eb4c3f8ff0ba'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-armv6'; 			sha256='164b04d5970f340eb6cb4da171b2dc0d12c345a6092c8ac2409b5fb4fc8af5e6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-armv7'; 			sha256='6e01028d97bc48bfd3894d9161586e74c0f37cf7d67a67ab7eafb351c2003cb3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-aarch64'; 			sha256='48ef22ecea70b4b197def1c1bfd2e797f7117db5257f6e505e64f03fdc329a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-ppc64le'; 			sha256='8cbceb45fc656ec9f9e24b8e61fda54d233ecc8f46cee8ef5ae5acfdcc7940d4'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-riscv64'; 			sha256='e9d612ff8d198911f93706f4eec2bb58abb24c0f869cff7d69f6a8e24ce05420'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-s390x'; 			sha256='9fec4a8628729766f4600ec0f8fb5aa760b6a20673e1abfb3d78f3b2eb02696a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 22 Dec 2022 01:56:10 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 22 Dec 2022 01:56:10 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 22 Dec 2022 01:56:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 22 Dec 2022 01:56:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 22 Dec 2022 01:56:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Dec 2022 01:56:11 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93eea1d5d8e5eb7f3c01c44eb6652605d4b5ad66cf819d1e3b6053733f2f13cf`  
		Last Modified: Tue, 29 Nov 2022 01:28:59 GMT  
		Size: 2.1 MB (2064254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef02f9f1efc27efc29707880482dfa2ad75f9438dc67f8e6874b36848775c12`  
		Last Modified: Wed, 07 Dec 2022 01:28:23 GMT  
		Size: 16.2 MB (16206327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8080842079f84ea37ca12e0c88883b94e02511f6a628f2880960051186d33fd`  
		Last Modified: Wed, 07 Dec 2022 01:28:22 GMT  
		Size: 15.2 MB (15204105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78c390e44ed3c841d8304c497cddf76949652139467d7d9b73c9ed1d5140aa5`  
		Last Modified: Thu, 22 Dec 2022 01:57:49 GMT  
		Size: 14.5 MB (14474968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26a621e3198ed3892e012e4ac73fc8a9eca4fee161180e6abf56dae6fa662ac`  
		Last Modified: Thu, 22 Dec 2022 01:57:47 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29d1acff9d1ce643c2f03e933fc9095e1c3d591f03703e67029cf3307816c0d`  
		Last Modified: Thu, 22 Dec 2022 01:57:47 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41098c0f132c31a0dc4ff2212550f1a14716a58358b55350c52516c6079e5ff9`  
		Last Modified: Thu, 22 Dec 2022 01:57:47 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a58931b5374845d2ff4d7a285287abcf65e791449fdbddd9a9e815a306ca66e5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47409348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e292403173f858be326baebba14e1a7591e46eb5545f99552c77f4217ff3c8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 22 Nov 2022 22:39:21 GMT
ADD file:685b5edadf1d5bf0aeb2aec35f810d83876e6d2ea0903b213f75a9c5f0dc5901 in / 
# Tue, 22 Nov 2022 22:39:21 GMT
CMD ["/bin/sh"]
# Tue, 29 Nov 2022 01:42:08 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Nov 2022 01:42:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Wed, 07 Dec 2022 01:45:17 GMT
ENV DOCKER_VERSION=23.0.0-beta.1
# Wed, 07 Dec 2022 01:45:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-23.0.0-beta.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-23.0.0-beta.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-23.0.0-beta.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-23.0.0-beta.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Wed, 07 Dec 2022 01:45:20 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Wed, 07 Dec 2022 01:45:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Thu, 22 Dec 2022 00:41:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.14.2
# Thu, 22 Dec 2022 00:41:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-x86_64'; 			sha256='d056a8330a01f22c249b9fa03ad0d5be889b79b648cad43c8549eb4c3f8ff0ba'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-armv6'; 			sha256='164b04d5970f340eb6cb4da171b2dc0d12c345a6092c8ac2409b5fb4fc8af5e6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-armv7'; 			sha256='6e01028d97bc48bfd3894d9161586e74c0f37cf7d67a67ab7eafb351c2003cb3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-aarch64'; 			sha256='48ef22ecea70b4b197def1c1bfd2e797f7117db5257f6e505e64f03fdc329a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-ppc64le'; 			sha256='8cbceb45fc656ec9f9e24b8e61fda54d233ecc8f46cee8ef5ae5acfdcc7940d4'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-riscv64'; 			sha256='e9d612ff8d198911f93706f4eec2bb58abb24c0f869cff7d69f6a8e24ce05420'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.14.2/docker-compose-linux-s390x'; 			sha256='9fec4a8628729766f4600ec0f8fb5aa760b6a20673e1abfb3d78f3b2eb02696a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 22 Dec 2022 00:41:57 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 22 Dec 2022 00:41:57 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 22 Dec 2022 00:41:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 22 Dec 2022 00:41:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 22 Dec 2022 00:41:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Dec 2022 00:41:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:261da4162673b93e5c0e7700a3718d40bcc086dbf24b1ec9b54bca0b82300626`  
		Last Modified: Tue, 22 Nov 2022 22:39:45 GMT  
		Size: 3.3 MB (3259190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb5dec0c1f562bd55dc773ccc0c77fbfd42b92083262478523c19bcc0f397af`  
		Last Modified: Tue, 29 Nov 2022 01:44:14 GMT  
		Size: 2.0 MB (2036851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c931478a7d4262453158b142ce84704388d7a888881237bb0fe62210b5de51e`  
		Last Modified: Wed, 07 Dec 2022 01:46:42 GMT  
		Size: 15.3 MB (15283665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e624c6a935d00e78b1ab5eba821e18b39a5cb5e34e6f3542e06d74ac0800514`  
		Last Modified: Wed, 07 Dec 2022 01:46:41 GMT  
		Size: 13.8 MB (13764593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc8b08dab25383e004e9355a00a68f322e13af2cc97adcef9108584f88aee43`  
		Last Modified: Thu, 22 Dec 2022 00:43:29 GMT  
		Size: 13.1 MB (13063319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b5867a2a4e5f07e9655480ddc5eb507ea7346aa293ea9770a5b4861857216f`  
		Last Modified: Thu, 22 Dec 2022 00:43:27 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8a4c31f0268c3290a8fbe409067b25d3fd4ffa67d9cfdeb9d7c1a20d2886e5`  
		Last Modified: Thu, 22 Dec 2022 00:43:27 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1385f96e38037a51fe02f6d588447d706be7fd0b9a567fd45592d3c770694c1`  
		Last Modified: Thu, 22 Dec 2022 00:43:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
