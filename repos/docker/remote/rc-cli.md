## `docker:rc-cli`

```console
$ docker pull docker@sha256:e3fe1d0362e7006b8beb6a57140e5022010154fb87267317badbf5635ccf71ef
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

### `docker:rc-cli` - linux; amd64

```console
$ docker pull docker@sha256:cb14864ac2beab8400a4b48929ee09b3199d26cda118df150f8b9323254b1aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60655286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070aeaccb451dcb71b349e6947e5b151b245e22399ae5db20ba80f11c62b9807`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 11:10:40 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 11:10:40 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 11:10:40 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
ENV DOCKER_VERSION=27.0.0-rc.2
# Thu, 20 Jun 2024 11:10:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Thu, 20 Jun 2024 11:10:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.2
# Thu, 20 Jun 2024 11:10:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-x86_64'; 			sha256='6fbaf6e93ccc43078a71a12db1d38224725cb5a9675391c38510355073f24066'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv6'; 			sha256='10b465c1771c262d372e24b09ed30fdc63687e35ae61c2365089e3998372a776'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv7'; 			sha256='b5bd40dfadf089617fe9cacb7a08d6fd5fae28e2a465191be1f25f22ffead344'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-aarch64'; 			sha256='de8c48203f4876fe3ae8bf27081a9aa69dc87de67a705f9d76c3a3ad776ed0c2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-ppc64le'; 			sha256='5810b3e6184032edbd21f12ed165ddecc823b8222ff5e4f6c55112af6f617c6d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-riscv64'; 			sha256='2c138daa9eaa909434c808018c4ab748a5f25caee16e3a7810fbeb3897b40878'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-s390x'; 			sha256='4084bdab8782e98c57a5f7aa7384699490048ce117dc7e70cad183702cc1645b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Jun 2024 11:10:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 11:10:40 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8b33ee29814bcd7e403ef1b8929a89b75decadf5c00c697f4b40e26a34bd18`  
		Last Modified: Thu, 20 Jun 2024 23:59:10 GMT  
		Size: 2.0 MB (2010479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69091f1b731d79c0c3ffa23a3ea2185244670eb2c361167c5b930b69086f65cd`  
		Last Modified: Thu, 20 Jun 2024 23:59:10 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec03a51f222338ae6fb4931b24b2b34f2c0a66421bba6ae7cdef246d1475e9e`  
		Last Modified: Thu, 20 Jun 2024 23:59:10 GMT  
		Size: 18.1 MB (18069006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724707ec6497f2c777ca139e84343c4d624c0a10aa956d6074ef24c25fb00b82`  
		Last Modified: Thu, 20 Jun 2024 23:59:10 GMT  
		Size: 18.2 MB (18178854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d96ba145e08bd218ab4539e6ada14c7b315d4d7a009f845853e56c91370a989`  
		Last Modified: Thu, 20 Jun 2024 23:59:11 GMT  
		Size: 18.8 MB (18770936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a0379d05541021105172cf5be25aa00d4871aa675a01bdc597a28392bf522f`  
		Last Modified: Thu, 20 Jun 2024 23:59:11 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c8ed5df351b89acedf744ba4efdd19ea5bce58e281b153beb28b2485c35226`  
		Last Modified: Thu, 20 Jun 2024 23:59:11 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80df29db38b76fd8f3e9f3239568a5b8a9e5e38d1853a8c3f092095004489189`  
		Last Modified: Thu, 20 Jun 2024 23:59:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:81c088364d2edbbad296e5ddeabf1be58819ebda46a2df3d90b857b10665bcb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e5dc635f68359d34f383c606433ef92d0d14bb028b6bd639bc194ac928e7b9`

```dockerfile
```

-	Layers:
	-	`sha256:8b0ea9d5e6573ea2d949e20dec18a4a304245657fb76438cc50cf5b2776ced30`  
		Last Modified: Thu, 20 Jun 2024 23:59:10 GMT  
		Size: 37.5 KB (37501 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:fd8760afbb49ec785f8fb4d01404c0f1a36000b9230379017609b1ac6e4e739d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56448797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f37372fb7f5e78202ac6051a1b5461447f684c8c99e672c2c844eaaeed4fedc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 11:10:40 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 11:10:40 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 11:10:40 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
ENV DOCKER_VERSION=27.0.0-rc.2
# Thu, 20 Jun 2024 11:10:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Thu, 20 Jun 2024 11:10:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.2
# Thu, 20 Jun 2024 11:10:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-x86_64'; 			sha256='6fbaf6e93ccc43078a71a12db1d38224725cb5a9675391c38510355073f24066'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv6'; 			sha256='10b465c1771c262d372e24b09ed30fdc63687e35ae61c2365089e3998372a776'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv7'; 			sha256='b5bd40dfadf089617fe9cacb7a08d6fd5fae28e2a465191be1f25f22ffead344'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-aarch64'; 			sha256='de8c48203f4876fe3ae8bf27081a9aa69dc87de67a705f9d76c3a3ad776ed0c2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-ppc64le'; 			sha256='5810b3e6184032edbd21f12ed165ddecc823b8222ff5e4f6c55112af6f617c6d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-riscv64'; 			sha256='2c138daa9eaa909434c808018c4ab748a5f25caee16e3a7810fbeb3897b40878'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-s390x'; 			sha256='4084bdab8782e98c57a5f7aa7384699490048ce117dc7e70cad183702cc1645b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Jun 2024 11:10:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 11:10:40 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123240d8ede45552263d1fd6df1ca89a6ca0284db54f1ac9556095375871831e`  
		Last Modified: Fri, 21 Jun 2024 05:27:43 GMT  
		Size: 2.0 MB (1993297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642d942c643ad6cf3229d2340a51718a3fca432b5a6df2cc6a2ca106cd72b85`  
		Last Modified: Fri, 21 Jun 2024 05:27:42 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4022369eca2e684860e8e8cd296e6294c9d49ed02886d44383354e92a55228db`  
		Last Modified: Fri, 21 Jun 2024 05:27:43 GMT  
		Size: 16.3 MB (16340362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f302c1fc18b6feb4b79d4a0f080f9fa5b84c0d0f3c962162d0aa18199a1508e9`  
		Last Modified: Fri, 21 Jun 2024 05:27:43 GMT  
		Size: 17.0 MB (17010836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b037aad28574df580b1831560d96b324bd0eb9e9b38bbfc1ac4833d6af3e91`  
		Last Modified: Fri, 21 Jun 2024 05:27:44 GMT  
		Size: 17.7 MB (17734977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec4d365a56b2c0eb0c49d7d4019f7f977b551b00c63a03969ddb4d4f14a3bbd`  
		Last Modified: Fri, 21 Jun 2024 05:27:44 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750aa34d39eb13db52a5029457e10edbbb849ed707c9801b0dbab8b4c12a88b5`  
		Last Modified: Fri, 21 Jun 2024 05:27:45 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c435a43062ef9eb1d64879b0cd61a23950def350e15d287f05131b18934228`  
		Last Modified: Fri, 21 Jun 2024 05:27:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:ff0b893349b0bb75db7f4784eef7f20193cdaf0e6d37797c6b9eb59f6225fc01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410d44f96febaaa0c8a5a711a2fcde7b3d13923c684d2fdc555edd762818be0a`

```dockerfile
```

-	Layers:
	-	`sha256:51a59284fa2caa8dd6611e2c531e0b117300123161567d4737e6020a182bbaca`  
		Last Modified: Fri, 21 Jun 2024 05:27:42 GMT  
		Size: 37.6 KB (37650 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:1a81201dd6fd1291dec42e48011f7ca2ab74b2ff77b735b8825f5a6a41bd248f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (55984466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7a1b866fcc671aef3cb5b5d948c4e6a3da30c02a274ff55a984479ee85fdfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 11:10:40 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 11:10:40 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 11:10:40 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
ENV DOCKER_VERSION=27.0.0-rc.2
# Thu, 20 Jun 2024 11:10:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Thu, 20 Jun 2024 11:10:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.2
# Thu, 20 Jun 2024 11:10:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-x86_64'; 			sha256='6fbaf6e93ccc43078a71a12db1d38224725cb5a9675391c38510355073f24066'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv6'; 			sha256='10b465c1771c262d372e24b09ed30fdc63687e35ae61c2365089e3998372a776'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv7'; 			sha256='b5bd40dfadf089617fe9cacb7a08d6fd5fae28e2a465191be1f25f22ffead344'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-aarch64'; 			sha256='de8c48203f4876fe3ae8bf27081a9aa69dc87de67a705f9d76c3a3ad776ed0c2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-ppc64le'; 			sha256='5810b3e6184032edbd21f12ed165ddecc823b8222ff5e4f6c55112af6f617c6d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-riscv64'; 			sha256='2c138daa9eaa909434c808018c4ab748a5f25caee16e3a7810fbeb3897b40878'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-s390x'; 			sha256='4084bdab8782e98c57a5f7aa7384699490048ce117dc7e70cad183702cc1645b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Jun 2024 11:10:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 11:10:40 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bab6db990bd0b9b920bfc503079bfb8464b2351005282fca8a6acb8ea03b71c`  
		Last Modified: Fri, 21 Jun 2024 05:18:04 GMT  
		Size: 1.8 MB (1841227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed62b2888fbe346a599db258694fb0ea9d289f961feae65b434defb298c52cf`  
		Last Modified: Fri, 21 Jun 2024 05:18:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bb3e6e0c06131b5806b446e36f55bc64eca6d3c91f96400d743208ad5d5057`  
		Last Modified: Fri, 21 Jun 2024 05:18:05 GMT  
		Size: 16.3 MB (16332794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35b9870267f9734ce21b800e8bbace39152fe1e4cb7a3bb75b41afe403a583a`  
		Last Modified: Fri, 21 Jun 2024 05:18:05 GMT  
		Size: 17.0 MB (16998041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2f718a6a49f4b731d9979c386125db3c2736d8ea6fa7e843c84f5621e4402a`  
		Last Modified: Fri, 21 Jun 2024 05:18:06 GMT  
		Size: 17.7 MB (17715379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665856066e1e7d250191e7400b3d0889243b0d4171689f1005c1713511075848`  
		Last Modified: Fri, 21 Jun 2024 05:18:05 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f034ea9013fe9037216bc92cfb9227baebc6b5a92cb4c98100deb34c0a919b`  
		Last Modified: Fri, 21 Jun 2024 05:18:06 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b3d8e4828efe0b655d7785a5de2fc8176e54226df0907563fe7c2a6301b6f1`  
		Last Modified: Fri, 21 Jun 2024 05:18:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:de68c883a259f83ea4e115b7ac15cb1d81d26bc68a011043a6822a5f2f78ebfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c5112275955949b982a2829a84b1fb2d4fe5c76b5dbc922f5a8b06f51aa4f5`

```dockerfile
```

-	Layers:
	-	`sha256:f1039e5e971e79ab277f148f0814f774bde8aa993439b1f0273f2d9c8a25084d`  
		Last Modified: Fri, 21 Jun 2024 05:18:04 GMT  
		Size: 37.6 KB (37650 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:16275d4dc46a8200664acc1811458ac001f4d539bae1deca0a25f8bf418b371c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56802649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0207b088e464244d60a2a0564031d0c4f0d8c0329cd96a8b5abf84218fcb6726`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 20 Jun 2024 11:10:40 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 11:10:40 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 11:10:40 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
ENV DOCKER_VERSION=27.0.0-rc.2
# Thu, 20 Jun 2024 11:10:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Thu, 20 Jun 2024 11:10:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.2
# Thu, 20 Jun 2024 11:10:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-x86_64'; 			sha256='6fbaf6e93ccc43078a71a12db1d38224725cb5a9675391c38510355073f24066'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv6'; 			sha256='10b465c1771c262d372e24b09ed30fdc63687e35ae61c2365089e3998372a776'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv7'; 			sha256='b5bd40dfadf089617fe9cacb7a08d6fd5fae28e2a465191be1f25f22ffead344'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-aarch64'; 			sha256='de8c48203f4876fe3ae8bf27081a9aa69dc87de67a705f9d76c3a3ad776ed0c2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-ppc64le'; 			sha256='5810b3e6184032edbd21f12ed165ddecc823b8222ff5e4f6c55112af6f617c6d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-riscv64'; 			sha256='2c138daa9eaa909434c808018c4ab748a5f25caee16e3a7810fbeb3897b40878'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-s390x'; 			sha256='4084bdab8782e98c57a5f7aa7384699490048ce117dc7e70cad183702cc1645b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Jun 2024 11:10:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Jun 2024 11:10:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 11:10:40 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe01b594f40bdec3ca33c28b35f6c07fdcab95fbd6b3dde4e5a726487139f99`  
		Last Modified: Fri, 21 Jun 2024 07:16:21 GMT  
		Size: 2.0 MB (2006605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c80050ca831a092bdc48b735d815a7ea2c5282900d0ae45b061524c464cf1d9`  
		Last Modified: Fri, 21 Jun 2024 07:16:21 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6858cc868e201cf93e949fc5920c6c6e04704cd92e089f9b77eeaa95ccac15`  
		Last Modified: Fri, 21 Jun 2024 07:16:21 GMT  
		Size: 17.0 MB (17029158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af27568734f42c2ac0ea4f13c611238c102360c443c8c4c221bcbd1f7a861350`  
		Last Modified: Fri, 21 Jun 2024 07:16:22 GMT  
		Size: 16.5 MB (16538007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3b88164869014d66e282b9a285ab9ca07bec8fc74d1c808ce646cf82b5ab0a`  
		Last Modified: Fri, 21 Jun 2024 07:16:23 GMT  
		Size: 17.1 MB (17137910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07bbd3e2c7fbf8ea030a24c1975cef088975c5de7b2cc5b219047d0b7ef764d`  
		Last Modified: Fri, 21 Jun 2024 07:16:22 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b725b8573291a96ac8c860a0dfd3b5175eebe9ebd3973b248441b5eac3e5f64`  
		Last Modified: Fri, 21 Jun 2024 07:16:23 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e886fccfd74bfd1df911faf3d086eef2e84e764538f90cb38525417383808a46`  
		Last Modified: Fri, 21 Jun 2024 07:16:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:b691a6053be1bada5523f9b95e4eb7c95535ea7115f518a0bc55d103dac3ce5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb113556e638858a5e36aa20890d1e6de86160347afdba15aa9a2f5b8f8e8e6f`

```dockerfile
```

-	Layers:
	-	`sha256:3e6bb3e263ee153286179cb532fde48094b1a5df1bed91c5bed2cd520df2cb7f`  
		Last Modified: Fri, 21 Jun 2024 07:16:20 GMT  
		Size: 37.8 KB (37802 bytes)  
		MIME: application/vnd.in-toto+json
