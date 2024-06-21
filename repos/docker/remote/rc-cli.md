## `docker:rc-cli`

```console
$ docker pull docker@sha256:09ab13d7a15c208a3fbc940f5022cf0999a6e4c9ebfd120e1625aa66d91e0698
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
$ docker pull docker@sha256:9ed0e67fc531c4986ba5f069de85698f072e582702101c25b4c53f5a30e30a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56450339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce27afd92d4a8a09c1f1d09b8db43e3e3fcce1f960319721524ba36c72aedf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_VERSION=27.0.0-rc.2
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Jun 2024 22:51:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2542faface5bae0b5d14b82d3e6183d4e5563bff6f3affda3a98565f63409958`  
		Last Modified: Mon, 17 Jun 2024 23:52:50 GMT  
		Size: 2.0 MB (1993292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8317922e3f3dd871674dcf604aab6d64e8e68db0fdc188c4007c4ef7c0c58826`  
		Last Modified: Mon, 17 Jun 2024 23:52:50 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8db86e1ae797994751670ce22b40adb2c0e32090c3cae95ceec315b4afeeb32`  
		Last Modified: Mon, 17 Jun 2024 23:52:51 GMT  
		Size: 16.3 MB (16340363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05e7843fbb803dd95114e7556198894a1320f751825883b5485cd9345b7ebd7`  
		Last Modified: Mon, 17 Jun 2024 23:52:51 GMT  
		Size: 17.0 MB (17010707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5884cfbc0a91ce10e86f69efe5b545a13f31ef1a89acf54b7d0b18f27a22fcd0`  
		Last Modified: Mon, 17 Jun 2024 23:52:52 GMT  
		Size: 17.7 MB (17738752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d205caeb2c3a802dacc8fd2c3c728799211b19e912c58501045eea76213e1fad`  
		Last Modified: Mon, 17 Jun 2024 23:52:51 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf97c9c651389a1c3349117b72dbe3f271306c7a29a0206bcd5576303d5c597`  
		Last Modified: Mon, 17 Jun 2024 23:52:55 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176e30315448c5d8f87b330b2dd05d9a825448ce9365130ecaa41309d9ebf415`  
		Last Modified: Mon, 17 Jun 2024 23:52:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:626976cfdad19f2760c5eff3700de60314e58c4495c05d87799b2eb31cfb5896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d0c5a19a42d00f3ed86ed0ce6351414763d23d89f7f49f1c6d930b1cbecdc6`

```dockerfile
```

-	Layers:
	-	`sha256:77133fede01aa99145219c5a96aa801ff94d274c78308df15b37aa5c8c5390eb`  
		Last Modified: Mon, 17 Jun 2024 23:52:50 GMT  
		Size: 37.6 KB (37649 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:82f9dd0269618be7516130507b913c38e05f57a0401437242b1e54ae1bb82e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (55986996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c26651c1b6045194bfb0a15496baeb899ac4bd96ab1e91dfd13787a5a3872f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_VERSION=27.0.0-rc.2
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Jun 2024 22:51:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07ef1c681cdd754917fb053121aa9ad399e9aad1e0d15e555a72d27bf50b3a0`  
		Last Modified: Mon, 17 Jun 2024 23:52:41 GMT  
		Size: 1.8 MB (1841229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361fa6970836ee5a0b385559ba3f81b64c4593fbce0f7dd5bf3ffd6f524d36a6`  
		Last Modified: Mon, 17 Jun 2024 23:52:41 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967823ba350c586bbcfc4c4d81e2646415628208a81aa0ba3207c53a30007484`  
		Last Modified: Mon, 17 Jun 2024 23:52:42 GMT  
		Size: 16.3 MB (16332795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c65c95f27be9d92a52051261b903d140c8390adeec74cba156a66e49bbf2cec`  
		Last Modified: Mon, 17 Jun 2024 23:52:42 GMT  
		Size: 17.0 MB (16995849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12396a85c8c4e6177979e2f214d3013d50c540935e5c5f14ef7d5d8f41d52a50`  
		Last Modified: Mon, 17 Jun 2024 23:52:43 GMT  
		Size: 17.7 MB (17720916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c599c739bd1eb86148c439563fae116b8893519d9a57834be5fd80dfb23daa`  
		Last Modified: Mon, 17 Jun 2024 23:52:42 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7de0e03cf51bc7633975ce9f510beed8495b8b6d4b60d2a0d58072d4ec2523`  
		Last Modified: Mon, 17 Jun 2024 23:52:43 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9c13cbe575ca98a38eb354f705440ba1d03f03169f2a6220a0ed61ed9466da`  
		Last Modified: Mon, 17 Jun 2024 23:52:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e98f3235986beca95b819a906500d63e1bc5ed5a822ed6ce39c530163b3e71f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d10386c9ee6aafd887e15c3060f154d0c7b7ce3e4f31d2e46f57479d73b7de4`

```dockerfile
```

-	Layers:
	-	`sha256:bcddf83a0eed2ed7f4a01ba3df23f698b1b0060a3003caa80bd7bc29e5615aa6`  
		Last Modified: Mon, 17 Jun 2024 23:52:41 GMT  
		Size: 37.6 KB (37650 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:84ba78f17c6620fffd0663432008bf57b465e1946c97cc75e6fa2dd80c1a492e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56808260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f793a92a52c508d10411f75f4e8182f3e5a6c3bffab502a6b88def2e11b90a41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_VERSION=27.0.0-rc.2
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Jun 2024 22:51:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a37c6920cf419f019cc2ece413c620d2c2c0c024b4f0c6e947adf6f650c0d32`  
		Last Modified: Tue, 18 Jun 2024 00:10:11 GMT  
		Size: 2.0 MB (2006612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226cbf91e38cd25c76a4cf8d25355d629193815e2234ac234d08474c3f47d241`  
		Last Modified: Tue, 18 Jun 2024 00:10:10 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebe42042517502c0a4214ec067e5e805812571248eb59007767634d4626c284`  
		Last Modified: Tue, 18 Jun 2024 00:10:11 GMT  
		Size: 17.0 MB (17029163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb7eeeea5f866d8f13beb04dcd0031ccd9fd374689779d555f0746a8fd0a7fe`  
		Last Modified: Tue, 18 Jun 2024 00:10:12 GMT  
		Size: 16.5 MB (16538686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca9f866f2e1c6ed3778e7a5e207db02ba4ef4dfe8a6482d489f68539d0418a0`  
		Last Modified: Tue, 18 Jun 2024 00:10:12 GMT  
		Size: 17.1 MB (17144849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527ee42643cc834ef80264a74abff8cb77379bede35cda028db368b8ce5558b2`  
		Last Modified: Tue, 18 Jun 2024 00:10:12 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0628e85c34c1cbad0cd6daef18eee405426305a16569c2fad2eee104c3432`  
		Last Modified: Tue, 18 Jun 2024 00:10:13 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82aa64d3a7abb094e57b17ffec25482c5d47d599a88fb847a1b788e9afda51bd`  
		Last Modified: Tue, 18 Jun 2024 00:10:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:80e00f7f81464eb7bc0cb7cbb10603a68b295bbfcb687a064c329b98363bfd13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147f1992eed04bcafb04993c3c847c098bcda256a67ead14d13bc647646711b8`

```dockerfile
```

-	Layers:
	-	`sha256:914bd7670ca3633772b85ce5c098a9cc84063dedb82d78c22b397bf057909aed`  
		Last Modified: Tue, 18 Jun 2024 00:10:11 GMT  
		Size: 37.8 KB (37800 bytes)  
		MIME: application/vnd.in-toto+json
