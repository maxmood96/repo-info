## `docker:rc-cli`

```console
$ docker pull docker@sha256:13546a5b7395ba1d4b1f9e3e14908a11e0f917ad857eceffdb7468642dfaae13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:rc-cli` - linux; amd64

```console
$ docker pull docker@sha256:b6c4ae7415f27df598e3ee8c611e1197187afb14887bfb3163499db3276aed11
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51323710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc51e8759c19a2cf7a404965a0a806bd4f06e8f2d572e83acb94f82fdcd12c2`
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
# Wed, 07 Dec 2022 01:27:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.14.0
# Wed, 07 Dec 2022 01:27:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-x86_64'; 			sha256='fdf634ab2b01aca33372bef2bf866699ef2e1f2dab19972e37967b1fc2a11402'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-armv6'; 			sha256='63e0826ddebc1ae776f38ab872b41f68b48fca246cdf67c709e07eef543cdf88'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-armv7'; 			sha256='c1664c4dcefc2a56a4f16f4dbd76e531f237bfbf713b90d3acea50df42a1aada'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-aarch64'; 			sha256='0265f45b30f4f0e1d53c1968c590181f64c546129d967460de382c6de38af191'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-ppc64le'; 			sha256='dbee58426af567787e5c1d14e925cca0d0a958edc55203c4b29c10dda8e27355'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-riscv64'; 			sha256='d447a75ff4d900b19d40e0c69811b335518f8a5fbc6377e0aff25a3b999a8c49'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-s390x'; 			sha256='2c5bbb6513d7377919bd4189f25d8bf5d8706a5345f10609d8c49d5cf4d8ab88'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 07 Dec 2022 01:27:03 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 07 Dec 2022 01:27:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 07 Dec 2022 01:27:03 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 07 Dec 2022 01:27:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 07 Dec 2022 01:27:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Dec 2022 01:27:04 GMT
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
	-	`sha256:9df75e9aba34de86c9cdcd9928b67989d0ade13db6399386714fd94287141081`  
		Last Modified: Wed, 07 Dec 2022 01:28:22 GMT  
		Size: 14.5 MB (14476603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f2b48fbf9066876cd6cc4ca3ab23e7e2387b2e2ee37a18d07613aa3d9d45d7`  
		Last Modified: Wed, 07 Dec 2022 01:28:19 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0693f4182015442b90c16b83f4baa76ac6314ec2a44fa241fea53b60d5dcf5a2`  
		Last Modified: Wed, 07 Dec 2022 01:28:19 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eba7cae798ea82ceb5893939ea46cb423213fc26623b44553968bee070c4ed6`  
		Last Modified: Wed, 07 Dec 2022 01:28:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9fc2d4a8ea0c1e4213d49ddb75771833308549c7d6b8d27412fc020e0b3b301e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47412782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35b8cb546fa4ba2da06469b518836caddf1e0458d87b5826cdb403693c55b8b`
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
# Wed, 07 Dec 2022 01:45:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.14.0
# Wed, 07 Dec 2022 01:45:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-x86_64'; 			sha256='fdf634ab2b01aca33372bef2bf866699ef2e1f2dab19972e37967b1fc2a11402'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-armv6'; 			sha256='63e0826ddebc1ae776f38ab872b41f68b48fca246cdf67c709e07eef543cdf88'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-armv7'; 			sha256='c1664c4dcefc2a56a4f16f4dbd76e531f237bfbf713b90d3acea50df42a1aada'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-aarch64'; 			sha256='0265f45b30f4f0e1d53c1968c590181f64c546129d967460de382c6de38af191'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-ppc64le'; 			sha256='dbee58426af567787e5c1d14e925cca0d0a958edc55203c4b29c10dda8e27355'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-riscv64'; 			sha256='d447a75ff4d900b19d40e0c69811b335518f8a5fbc6377e0aff25a3b999a8c49'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-s390x'; 			sha256='2c5bbb6513d7377919bd4189f25d8bf5d8706a5345f10609d8c49d5cf4d8ab88'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 07 Dec 2022 01:45:25 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 07 Dec 2022 01:45:25 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 07 Dec 2022 01:45:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 07 Dec 2022 01:45:26 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 07 Dec 2022 01:45:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Dec 2022 01:45:26 GMT
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
	-	`sha256:8ee55b5cd54757773ba95fd918b41c355db0ce037d53dcbdb9799611971c6543`  
		Last Modified: Wed, 07 Dec 2022 01:46:40 GMT  
		Size: 13.1 MB (13066766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acad96fc3f56c3deb438194641810c08807ed2486f99777bfb2f886bb28d756`  
		Last Modified: Wed, 07 Dec 2022 01:46:39 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a310d812dcde2c1054badbc4005a728b4edee2d27254e11d8d3efb57dea339b`  
		Last Modified: Wed, 07 Dec 2022 01:46:39 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3f5f4fa84b20ef4f6ef3117833fb439ea72bfd078828f1618d7659ee861f5f`  
		Last Modified: Wed, 07 Dec 2022 01:46:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
