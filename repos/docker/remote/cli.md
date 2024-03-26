## `docker:cli`

```console
$ docker pull docker@sha256:16840df28f715a7c32ec81eec277adc1c441c6d9abd4885cead3e31e723c7869
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
$ docker pull docker@sha256:a073f182e82f021a1839e0a8fc6a14f06a4804d5cbe1704cf524cc607d7258fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59062616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8cf2387ac909941bde86f283d8a38c2536fa3691dcfdbc435ac12988022c7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 22 Mar 2024 23:07:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
ENV DOCKER_VERSION=26.0.0
# Fri, 22 Mar 2024 23:07:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Fri, 22 Mar 2024 23:07:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.0
# Fri, 22 Mar 2024 23:07:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-x86_64'; 			sha256='59c6b262bedc4a02f46c8400e830e660935684899c770c3f5e804a2b7079fc16'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv6'; 			sha256='97dac0aa10961ea30a79f6fe2c4a13bfe4da562926365a63042fcceb88d9d125'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv7'; 			sha256='d607ed69f5fe92ee1fd831cf764f977174c86192957a4de678c01db671c3dc52'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-aarch64'; 			sha256='6f00ed24a846046b441c0f0a0f8c1e00194f4b0e33f2433fac0d2dd0e486fc80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-ppc64le'; 			sha256='e3afa6956f6cd4fdbaa8fe19781ae07a1bb8fb2f4d54a1aac857090d6fe1710d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-riscv64'; 			sha256='1d080f5bc04b4b97c61ce3f57ff4a7bd11299f486bc287833f162360be201a7d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-s390x'; 			sha256='5f302fb8e7d973b53f1f9dc808d2b1af08f94687cb14b3f26cc7b358854184b5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 22 Mar 2024 23:07:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Mar 2024 23:07:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd7fda0220e224941f21b2a7c0993e99ebfd3b7ece6fe3d55d12291fe82e96`  
		Last Modified: Mon, 25 Mar 2024 19:12:02 GMT  
		Size: 2.0 MB (2026148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cdfe127e634247a6b098e079b029836ad519669d1738f1065a83327cd4c32a`  
		Last Modified: Mon, 25 Mar 2024 19:12:02 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2b6d6f61c1d4a2f362fec9bbb807462097ca361a5c8b682a79a0393cabf8db`  
		Last Modified: Mon, 25 Mar 2024 19:12:03 GMT  
		Size: 17.0 MB (16973499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ef9d78a4502641bb254d13fd73fe032461ac8bb8d901f0edb697a8404e0535`  
		Last Modified: Mon, 25 Mar 2024 19:12:03 GMT  
		Size: 18.0 MB (17982275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa022d7f0c8dad5f0844192dffb0604a107bdb65f345e6611c9e093d621940db`  
		Last Modified: Mon, 25 Mar 2024 19:12:04 GMT  
		Size: 18.7 MB (18669703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ef7eb639b9fca58d031d4a3137cb480f90f97f12ee87f55b1467926198501c`  
		Last Modified: Mon, 25 Mar 2024 19:12:03 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee617bc1d245ce26f81569d2445e31019a417656d59cc1025ab571544187c79`  
		Last Modified: Mon, 25 Mar 2024 19:12:04 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd4613e45a427c1de727da2af56d945a4bfac3faedeca3f315397df751b233b`  
		Last Modified: Mon, 25 Mar 2024 19:12:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:0fa22915e08ed2515d87468235714ae563fa866df088938f78d925f2d9cbb217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.5 KB (425499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee725485415cf306333c27e68846bfe23e319275c54cfb22a91febde6a4ee570`

```dockerfile
```

-	Layers:
	-	`sha256:43b20ce871b197c430eeb27a9063097f9f09c9f8dde63a29bab2a455e98d4aaf`  
		Last Modified: Mon, 25 Mar 2024 19:12:03 GMT  
		Size: 387.5 KB (387456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c5228ae8ff3e17ce68a82e0c5f4a5a4caf2f9cd305df8a333066dc463376b3a`  
		Last Modified: Mon, 25 Mar 2024 19:12:02 GMT  
		Size: 38.0 KB (38043 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:67df5cf1e5662603b272000e5153b0a8ff522c495dcdee023a998f5efef0b92a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55087490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f6e2bfb83ce6feeb670506d7fe47208c52c21efcbd0617994498aa41fb15f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 22 Mar 2024 23:07:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
ENV DOCKER_VERSION=26.0.0
# Fri, 22 Mar 2024 23:07:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Fri, 22 Mar 2024 23:07:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.0
# Fri, 22 Mar 2024 23:07:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-x86_64'; 			sha256='59c6b262bedc4a02f46c8400e830e660935684899c770c3f5e804a2b7079fc16'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv6'; 			sha256='97dac0aa10961ea30a79f6fe2c4a13bfe4da562926365a63042fcceb88d9d125'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv7'; 			sha256='d607ed69f5fe92ee1fd831cf764f977174c86192957a4de678c01db671c3dc52'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-aarch64'; 			sha256='6f00ed24a846046b441c0f0a0f8c1e00194f4b0e33f2433fac0d2dd0e486fc80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-ppc64le'; 			sha256='e3afa6956f6cd4fdbaa8fe19781ae07a1bb8fb2f4d54a1aac857090d6fe1710d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-riscv64'; 			sha256='1d080f5bc04b4b97c61ce3f57ff4a7bd11299f486bc287833f162360be201a7d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-s390x'; 			sha256='5f302fb8e7d973b53f1f9dc808d2b1af08f94687cb14b3f26cc7b358854184b5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 22 Mar 2024 23:07:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Mar 2024 23:07:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b118eac215e4599e4010c9e5f0a1e8d36da6b557f5f7ff6cac0b485c2f1aeb3`  
		Last Modified: Mon, 25 Mar 2024 19:52:24 GMT  
		Size: 2.1 MB (2116777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487abfe1cd292c85e2f7bff0176655656a8cfb029d981b200971d5a138a7f45`  
		Last Modified: Mon, 25 Mar 2024 19:52:23 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688fbf3ecfa8784947b23b3298fe206f7a7bb53fb1b05d1e8880adea3de8157e`  
		Last Modified: Mon, 25 Mar 2024 19:52:24 GMT  
		Size: 15.4 MB (15353242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7756736cd19c64f654ab89c07d134444ad5423c72488ca38e29408b991fc83`  
		Last Modified: Mon, 25 Mar 2024 19:52:24 GMT  
		Size: 16.8 MB (16818355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669aee440bca76bf54399909d0bea654c534a2ca99b1ebe1ae681e3a6382900d`  
		Last Modified: Mon, 25 Mar 2024 19:52:25 GMT  
		Size: 17.6 MB (17631455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44414516d8a4ca6e41f21b8f2416774184c3f1fdc0688c4b3585235647a87f79`  
		Last Modified: Mon, 25 Mar 2024 19:52:25 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6099c94c0b9f1a21c4014574b4f4ffd2b74ebbfc479ef602628d61c509d6cf`  
		Last Modified: Mon, 25 Mar 2024 19:52:25 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad1dbfc423a9278fb9906ee2db5624260ba29f735f9a64fe2387f5b4c49f37e`  
		Last Modified: Mon, 25 Mar 2024 19:52:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:fb4529df1172f3e4fb194aec529c95e5ed919c892b0a6662db779eca02c7ee54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c32296fad097e5a588dd8e3351f3e74cc57cfe0191b0e1b32adad6b20198049`

```dockerfile
```

-	Layers:
	-	`sha256:4acf0435f59e8c6621ad3e63f0d3fa532868eadd1125db6a84d174f27b607c35`  
		Last Modified: Mon, 25 Mar 2024 19:52:23 GMT  
		Size: 38.0 KB (37983 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:1908cc6d015e5ec0128be62e8957b21a71812260c64f626f5d7c2b4ae9f70782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54585989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99c3399383a369239e62f304aabd7de0037823d2add2886fe985122b0addb46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 22 Mar 2024 23:07:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
ENV DOCKER_VERSION=26.0.0
# Fri, 22 Mar 2024 23:07:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Fri, 22 Mar 2024 23:07:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.0
# Fri, 22 Mar 2024 23:07:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-x86_64'; 			sha256='59c6b262bedc4a02f46c8400e830e660935684899c770c3f5e804a2b7079fc16'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv6'; 			sha256='97dac0aa10961ea30a79f6fe2c4a13bfe4da562926365a63042fcceb88d9d125'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv7'; 			sha256='d607ed69f5fe92ee1fd831cf764f977174c86192957a4de678c01db671c3dc52'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-aarch64'; 			sha256='6f00ed24a846046b441c0f0a0f8c1e00194f4b0e33f2433fac0d2dd0e486fc80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-ppc64le'; 			sha256='e3afa6956f6cd4fdbaa8fe19781ae07a1bb8fb2f4d54a1aac857090d6fe1710d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-riscv64'; 			sha256='1d080f5bc04b4b97c61ce3f57ff4a7bd11299f486bc287833f162360be201a7d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-s390x'; 			sha256='5f302fb8e7d973b53f1f9dc808d2b1af08f94687cb14b3f26cc7b358854184b5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 22 Mar 2024 23:07:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Mar 2024 23:07:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62203ebc003cf77a4ff92a3c67a89cd14dcf1adf84fb125d2f3329ad08ad9a61`  
		Last Modified: Sat, 16 Mar 2024 15:21:10 GMT  
		Size: 1.9 MB (1896160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8418dd6a88f431ade9efd4277500a4c6483d9ac98459ff95a86dbfde7d02e2a`  
		Last Modified: Sat, 16 Mar 2024 15:21:10 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379a08f7972893d46b71e7b905cdc61d943b0d710bae6cd5d41985a5bb36f184`  
		Last Modified: Wed, 20 Mar 2024 23:55:51 GMT  
		Size: 15.3 MB (15347101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709298659c489dcbb4eb40106515d6d66d8044bcf98e5880042f03dcfec5c8fb`  
		Last Modified: Wed, 20 Mar 2024 23:55:51 GMT  
		Size: 16.8 MB (16804622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdb6745728d3376b271f87ec7407e421bb5fe9146065356997b524d1952501e`  
		Last Modified: Mon, 25 Mar 2024 21:49:14 GMT  
		Size: 17.6 MB (17616935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df466f330d545024cf2a68d8a747fcb1c34fbb95325c42aecaea60e465f9d89a`  
		Last Modified: Mon, 25 Mar 2024 21:49:13 GMT  
		Size: 551.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276671d6138b33d9e49b88cc4355f74b3698b87466a472e938443ed838fa42a7`  
		Last Modified: Mon, 25 Mar 2024 21:49:13 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedefcafbace661350c2ef729e1bac592cee27965882e48d7a6612ee4c0ea9da`  
		Last Modified: Mon, 25 Mar 2024 21:49:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:9a2e23bbb6f0dd48b16c225b045064810267ec36bb9d1317f18be8cd2c0ce026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.1 KB (420063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342603f1404f578808b1d9bf7dda2af1238a0004fa37f750f7d4b2fab38319a9`

```dockerfile
```

-	Layers:
	-	`sha256:4da145b5b42ce5d4ca6986c7ef269a9cecebf7a75271167a888870ef821145f1`  
		Last Modified: Mon, 25 Mar 2024 21:49:13 GMT  
		Size: 382.0 KB (382031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e2fbcefa37e675177b4a8667654ae525caaac308e5e85dc4eb3e41aa895a59`  
		Last Modified: Mon, 25 Mar 2024 21:49:13 GMT  
		Size: 38.0 KB (38032 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c36f4256c4efe0e64fa07d02de3c4c691bd48cc5c2fe15a859e6d435f0dfc0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54749099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5474636564e9ceb53d2f934c18a48d3489d222a72cb83b427b3a064e1e7706db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 22 Mar 2024 23:07:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
ENV DOCKER_VERSION=26.0.0
# Fri, 22 Mar 2024 23:07:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Fri, 22 Mar 2024 23:07:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.0
# Fri, 22 Mar 2024 23:07:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-x86_64'; 			sha256='59c6b262bedc4a02f46c8400e830e660935684899c770c3f5e804a2b7079fc16'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv6'; 			sha256='97dac0aa10961ea30a79f6fe2c4a13bfe4da562926365a63042fcceb88d9d125'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv7'; 			sha256='d607ed69f5fe92ee1fd831cf764f977174c86192957a4de678c01db671c3dc52'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-aarch64'; 			sha256='6f00ed24a846046b441c0f0a0f8c1e00194f4b0e33f2433fac0d2dd0e486fc80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-ppc64le'; 			sha256='e3afa6956f6cd4fdbaa8fe19781ae07a1bb8fb2f4d54a1aac857090d6fe1710d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-riscv64'; 			sha256='1d080f5bc04b4b97c61ce3f57ff4a7bd11299f486bc287833f162360be201a7d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-s390x'; 			sha256='5f302fb8e7d973b53f1f9dc808d2b1af08f94687cb14b3f26cc7b358854184b5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 22 Mar 2024 23:07:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 22 Mar 2024 23:07:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Mar 2024 23:07:24 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b275a3377f65492f727dc46aa2b70be6ec8ff96583fcd9a7b699692b5170bc`  
		Last Modified: Sat, 16 Mar 2024 04:06:09 GMT  
		Size: 2.0 MB (2019704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c53acdebd8fb391eae546ed72149f049f8ab4d594f12c74c49be04cc3b9708`  
		Last Modified: Sat, 16 Mar 2024 04:06:08 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11eaffe3eb71643155936daeaa1598d665bd3ce7e4cd7ce7540eda599ce5e7fe`  
		Last Modified: Thu, 21 Mar 2024 00:17:46 GMT  
		Size: 16.0 MB (15983712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee06d9bd87570975d69f1b498d43c5d73ee2272dc95ec1a0ef1cf417a2b4e81`  
		Last Modified: Thu, 21 Mar 2024 00:17:45 GMT  
		Size: 16.3 MB (16349527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1172287503895a29f7a27066f3d541d4edb368754c3a6aa3555f6f5e783bd893`  
		Last Modified: Mon, 25 Mar 2024 19:11:37 GMT  
		Size: 17.0 MB (17046172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28cda27aeb58e151f6347653aaa6582fef35c655140f6d2a6cddc9fafec2cba`  
		Last Modified: Mon, 25 Mar 2024 19:11:36 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff57bb0e39d9ba044b2015dd11c7b4972b2e49e12e5969181f6da81f8c0402e1`  
		Last Modified: Mon, 25 Mar 2024 19:11:37 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cde276bbe4ee1509df387ac8a92f4b6aeb60b25f76f8db835e917d494790ce`  
		Last Modified: Mon, 25 Mar 2024 19:11:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:e1633b1503d4cf6708c9bf35c400cb17a38742bd6f5c0f8a31f46afc7ea375fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.4 KB (420389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1491b8f50749a23bf53286c06d31cb9233e6fbd5ae875e24e888de88eca616`

```dockerfile
```

-	Layers:
	-	`sha256:694aac811bc2ec6463a58c3e6bb9891cc8b0e5916de629ccb5fc16a8372d7c2a`  
		Last Modified: Mon, 25 Mar 2024 19:11:37 GMT  
		Size: 382.5 KB (382500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9df3335cc36fdcabf7edc758a6e1e147c7b231bd0f9e6c8a86be0b1cc6d21cf`  
		Last Modified: Mon, 25 Mar 2024 19:11:36 GMT  
		Size: 37.9 KB (37889 bytes)  
		MIME: application/vnd.in-toto+json
